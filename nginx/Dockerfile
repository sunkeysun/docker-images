# nginx

FROM centos
MAINTAINER Sunkey "sunkeysun@outlook.com"

RUN yum -y update
RUN yum -y install gcc make pcre-devel zlib-devel openssl-devel

WORKDIR /tmp
ADD https://nginx.org/download/nginx-1.11.12.tar.gz .
RUN tar -zxvf nginx-1.11.12.tar.gz

WORKDIR nginx-1.11.12
RUN ./configure --prefix=/opt/nginx \
	--with-http_ssl_module \
    --with-pcre \
	&& make \
    && make install

WORKDIR /opt/nginx

ENTRYPOINT ["/opt/nginx/sbin/nginx"]
CMD ["-g", "daemon off;"]
