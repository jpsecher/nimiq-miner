FROM ubuntu:16.04
MAINTAINER Jens Peter Secher <jpsecher@gmail.com>

RUN apt-get update && apt-get install -y curl

COPY nimiq-signing-key.pub /
RUN apt-key add nimiq-signing-key.pub && \
	rm -f nimiq-signing-key.pub

ARG VERSION=1.2.0-1
COPY nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256 /
RUN curl -O https://repo.nimiq.com/deb/pool/main/n/nimiq/nimiq_${VERSION}_amd64.deb && \
    sha256sum -c nimiq_${VERSION}_amd64.deb.sha256 && \
	dpkg -i nimiq_${VERSION}_amd64.deb && \
	rm -f nimiq_${VERSION}_amd64.deb nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256

ENV HOME=/home/nimiq
RUN mkdir -p $HOME && chown nimiq:nimiq $HOME
WORKDIR $HOME
USER nimiq
VOLUME $HOME

ENTRYPOINT ["/usr/share/nimiq/app/node", "/usr/share/nimiq/app/index.js", "--miner"]
CMD ["--pool=eu.nimpool.io:8444", "--wallet-address=NQ46UGCV26ET160EE9VU5XHGQSXHYSUY2RVQ"]
