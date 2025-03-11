FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl make gcc g++ zlib1g-dev libsimde-dev libsys-hostname-long-perl && rm -rf /var/lib/apt/lists/*

RUN curl -LO https://github.com/BenLangmead/bowtie2/archive/refs/tags/v2.5.4.tar.gz && tar -zxvf v2.5.4.tar.gz && cd /root/bowtie2-2.5.4 && make && make install

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=bowtie2
