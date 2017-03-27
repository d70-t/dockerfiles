FROM ubuntu:16.10

MAINTAINER Tobias Kölling <tobias.koelling@physik.uni-muenchen.de>

RUN apt-get update && apt-get install -y \
    git \
    make \
    cmake \
    gcc \
    g++ \
    libtool \
    python \
    python-dev \
    libboost-all-dev \
    libeigen3-dev \
 && rm -rf /var/lib/apt/lists/*
