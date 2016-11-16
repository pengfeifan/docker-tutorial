FROM ubuntu:14.04
MAINTAINER William Fan "pengfei.fan@hotmail.com"
ENV REFERSHED_AT 2016-11-15
RUN apt-get -yqq update && apt-get -yqq install nginx
RUN mkdir -p /var/www/html/website
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx/conf
EXPOSE 80

