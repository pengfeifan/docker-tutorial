FROM ubuntu:16.04
MAINTAINER William Fan "pengfeifan@hotmail.com"
ENV REFRESHED_AT 2016-11-05
RUN apt-get -yqq update && apt-get -yqq install redis-server redis-tools
EXPOSE 6379
ENTRYPOINT [ "/usr/bin/redis-server" ]
CMD []
