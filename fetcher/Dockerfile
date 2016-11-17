FROM ubuntu:16.04
MAINTAINER William Fan <pengfei.fan@hotmail.com>
ENV REFRESHED_AT 2016-11-17

RUN apt-get -yqq update
RUN apt-get -yqq install wget

VOLUME [ "/var/lib/tomcat8/webapps/" ]
WORKDIR /var/lib/tomcat8/webapps/

ENTRYPOINT [ "wget" ]

CMD [ "-?" ]
