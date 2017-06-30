FROM teppich/opencv_gcc

MAINTAINER Tobias Kölling <tobias.koelling@physik.uni-muenchen.de>

RUN apt-get update \
 && apt-get install -y libflann-dev libvtk6-dev libpng-dev zlib1g-dev \
 && rm -rf /var/lib/apt/lists/*
RUN cd / \
 && git clone https://github.com/PointCloudLibrary/pcl.git \
 && cd /pcl \
 && git checkout tags/pcl-1.8.0 \
 && mkdir /pcl_build \
 && cd /pcl_build \
 && cmake /pcl \
 && make && make install \
 && ldconfig \
 && cd / \
 && rm -rf /pcl \
 && rm -rf /pcl_build
