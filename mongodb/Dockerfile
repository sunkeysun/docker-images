# mongodb 3.4.2

FROM centos

MAINTAINER Sunkey "sunkeysun@outlook.com"

WORKDIR /opt
VOLUME ["/data"]

ADD https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-amazon-3.4.2.tgz ./
RUN tar -zxvf mongodb-linux-x86_64-amazon-3.4.2.tgz \
	&& mv mongodb-linux-x86_64-amazon-3.4.2 mongodb

ENTRYPOINT ["/opt/mongodb/bin/mongod"]
CMD ["--config", "/data/config/mongod.conf"]
