FROM ubuntu:16.04
MAINTAINER William Fan "pengfei.fan@hotmail.com"
ENV REFRESHED_AT 2016-11-15

RUN apt-get update -yqq && apt-get -yqq install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis
RUN mkdir -p /opt/webapp
EXPOSE 4567
CMD [ "/opt/webapp/bin/webapp" ]

