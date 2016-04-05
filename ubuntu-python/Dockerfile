FROM ubuntu:14.04
MAINTAINER XuChongBo <xcbfreedom@gmail.com>

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8
ENV LANGUAGE en_US:en

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
