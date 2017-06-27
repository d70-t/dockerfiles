FROM ubuntu:16.10

MAINTAINER Tobias Kölling <tobias.koelling@physik.uni-muenchen.de>

RUN apt-get update && apt-get install -y \
    git \
    autoconf \
    build-essential \
    gfortran \
    libgsl-dev \
    python \
    flex \
    libnetcdf-dev \
    wget \
    gawk \
 && rm -rf /var/lib/apt/lists/*

RUN cd /tmp \
 && wget -nd -c http://prdownloads.sourceforge.net/nccmp/nccmp-1.8.2.1.tar.gz \
 && tar zxvf nccmp-*.tar.gz \
 && cd nccmp-* \
 && ./configure \
 && make -j \
 && make install-strip \
 && cd / \
 && rm -rf /tmp/nccmp*
