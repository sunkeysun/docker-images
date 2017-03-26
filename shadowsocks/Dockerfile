# shadownsocks image
FROM centos:7

MAINTAINER Sunkey "sunkeysun@outlook.com"

RUN yum -y update
RUN yum -y install python-setuptools && easy_install pip
RUN pip install shadowsocks

ENTRYPOINT ["ssserver"]
