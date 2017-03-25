# mongodb 3.4.2

FROM centos:7

MAINTAINER Sunkey Sun "sunkeysun@outlook.com"

WORKDIR /opt
VOLUME ["/data", "/config", "/var/log"]

ADD ./mongodb-linux-x86_64-amazon-3.4.2.tgz ./
RUN mv mongodb-linux-x86_64-amazon-3.4.2 mongodb

RUN ls ./

ENTRYPOINT ["/opt/mongodb/bin/mongod"]
CMD ["--config", "/config/mongod.conf"]
