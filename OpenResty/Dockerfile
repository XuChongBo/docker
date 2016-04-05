FROM docker.zuoyetong.com.cn:8888/xucb/ubuntu.14.04-python
MAINTAINER XuChongBo <xcbfreedom@gmail.com>

# the gz file will auto unfolded. no need to RUN tar xvf /downloads/openresty-1.9.7.4.tar.gz
ADD openresty-1.9.7.4.tar.gz /downloads/   

WORKDIR /downloads/openresty-1.9.7.4


RUN apt-get install -y libreadline-dev libncurses5-dev libpcre3-dev \
		    libssl-dev perl make build-essential

RUN ./configure 
RUN make 
RUN make install

ENV PATH /usr/local/openresty/bin:/usr/local/openresty/nginx/sbin:$PATH

#RUN export PATH=/usr/local/openresty/bin:/usr/local/openresty/nginx/sbin:$PATH
#RUN echo "export PATH=/usr/local/openresty/bin:/usr/local/openresty/nginx/sbin:\$PATH"  >> ~/.bashrc
