FROM teppich/gcc

MAINTAINER Tobias Kölling <tobias.koelling@physik.uni-muenchen.de>

RUN cd / && \
    git clone https://github.com/Itseez/opencv.git && \
    cd opencv && \
    git checkout tags/3.2.0 && \
    \
    cd / && \
    git clone https://github.com/Itseez/opencv_contrib.git && \
    cd opencv_contrib && \
    git checkout tags/3.2.0 && \
    \
    cd /opencv && \
    cmake -DOPENCV_EXTRA_MODULES_PATH=../opencv_contrib/modules . && \
    make && make install && \
    ldconfig && \
    cd / && \
    rm -rf opencv && \
    rm -rf opencv_contrib
