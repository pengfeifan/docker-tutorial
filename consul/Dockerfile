FROM ubuntu:16.04
MAINTAINER William Fan <pengfei.fan@hotmail.com>
ENV REFRESHED_AT 2016-11-15

RUN apt-get -yqq update
RUN apt-get -yqq install curl unzip

#ADD https://releases.hashicorp.com/consul/0.7.1/consul_0.7.1_linux_amd64.zip /tmp/consul.zip
ADD consul_0.7.1_linux_amd64.zip /tmp/consul.zip
RUN cd /usr/sbin && unzip /tmp/consul.zip && chmod +x /usr/sbin/consul && rm /tmp/consul.zip

#ADD https://releases.hashicorp.com/consul/0.7.1/consul_0.7.1_web_ui.zip /tmp/webui.zip

ADD consul_0.7.1_web_ui.zip /tmp/webui.zip

RUN mkdir -p /webui/ && cd /webui/ && unzip /tmp/webui.zip

ADD consul.json /config/

EXPOSE 53/udp 8300 8301 8301/udp 8302 8302/udp 8400 8500

VOLUME ["/data"]

ENTRYPOINT [ "/usr/sbin/consul","agent","-config-dir=/config" ]

CMD []
