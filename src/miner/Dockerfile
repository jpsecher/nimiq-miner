FROM ubuntu:20.04
MAINTAINER Jens Peter Secher <jpsecher@gmail.com>

RUN apt-get update && apt-get install -y curl gnupg2

COPY nimiq-signing-key.pub /
RUN apt-key add nimiq-signing-key.pub && \
    rm -f nimiq-signing-key.pub

ARG VERSION=1.6.3-1
COPY nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256sum /
RUN curl -sS -O https://repo.nimiq.com/deb/pool/stable/main/n/nimiq/nimiq_${VERSION}_amd64.deb && \
    sha256sum -c nimiq_${VERSION}_amd64.deb.sha256sum && \
    dpkg -i nimiq_${VERSION}_amd64.deb && \
    rm -f nimiq_${VERSION}_amd64.deb nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256sum

ENV HOME=/home/nimiq
RUN mkdir -p $HOME && chown nimiq:nimiq $HOME
WORKDIR $HOME
USER nimiq

ENTRYPOINT ["/usr/share/nimiq/app/node", "/usr/share/nimiq/app/index.js", "--protocol=dumb", "--miner"]
CMD ["--pool=pool.acemining.co:8443", "--type=light", "--wallet-address=NQ6272GHCS6H3XL5L09SFGAM34MK7CU11JFE"]
