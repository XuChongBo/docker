FROM ubuntu:14.04
MAINTAINER XuChongBo <xcbfreedom@gmail.com>

ADD http://docker.zuoyetong.com.cn/build/trusty-sources.list /etc/apt/sources.list

RUN apt-get update -y

RUN apt-get install -y \
    build-essential \
    python \
    python-dev \
    python-pip \
    git \
    libhdf5-dev 

# install numpy and scipy by apt, in case that pip’s versions might not be linked to an optimized BLAS implementation
RUN apt-get install -y python-numpy  python-scipy 

RUN pip install Cython h5py
