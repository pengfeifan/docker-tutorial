FROM ubuntu:16.04
MAINTAINER William Fan <pengfei.fan@hotmail.com>
ENV REFRESHED_AT 2016-11-15

RUN apt-get -yqq update
RUN apt-get install -yqq software-properties-common python-software-properties
RUN add-apt-repository ppa:chris-lea/redis-server
RUN apt-get -yqq update
RUN apt-get -yqq install redis-server redis-tools

VOLUME [ "/var/lib/redis","/var/log/redis/" ]

EXPOSE 6379
CMD []
