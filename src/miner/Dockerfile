FROM ubuntu:16.04
MAINTAINER Jens Peter Secher <jpsecher@gmail.com>

RUN apt-get update && apt-get install -y curl

COPY nimiq-signing-key.pub /
RUN apt-key add nimiq-signing-key.pub

ARG VERSION=1.1.2-1
RUN curl -O https://repo.nimiq.com/deb/pool/main/n/nimiq/nimiq_${VERSION}_amd64.deb
COPY nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256 /
RUN sha256sum -c nimiq_${VERSION}_amd64.deb.sha256 && \
	dpkg -i nimiq_${VERSION}_amd64.deb && \
	rm -f nimiq-signing-key.pub nimiq_${VERSION}_amd64.deb nimiq_${VERSION}_amd64.deb.asc nimiq_${VERSION}_amd64.deb.sha256

ENV HOME=/home/nimiq
RUN mkdir -p $HOME && chown nimiq:nimiq $HOME
WORKDIR $HOME
USER nimiq

COPY nimiq.conf /etc/nimiq/nimiq.conf

CMD /usr/share/nimiq/app/node /usr/share/nimiq/app/index.js --config=/etc/nimiq/nimiq.conf --pool=eu.nimpool.io:8444
