FROM ubuntu:16.04
MAINTAINER Jens Peter Secher <jpsecher@gmail.com>

RUN apt-get update && apt-get install -y curl

COPY nimiq-signing-key.pub /
RUN apt-key add nimiq-signing-key.pub

RUN curl -O https://repo.nimiq.com/deb/pool/main/n/nimiq/nimiq_1.1.1-1_amd64.deb
COPY nimiq_1.1.1-1_amd64.deb.asc nimiq_1.1.1-1_amd64.deb.sha256 /
RUN sha256sum -c nimiq_1.1.1-1_amd64.deb.sha256

RUN dpkg -i nimiq_1.1.1-1_amd64.deb

COPY nimiq.conf /etc/nimiq/nimiq.conf

CMD /usr/share/nimiq/app/node /usr/share/nimiq/app/index.js --config=/etc/nimiq/nimiq.conf
