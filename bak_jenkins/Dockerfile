FROM ubuntu:14.04
MAINTAINER William Fan "pengfei.fan@hotmail.com"
ENV REFRESHED_AT 2016-11-15

RUN apt-get update -yqq && apt-get install -yqq curl apt-transport -https
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
RUN echo deb https://apt.dockerproject.org/repo ubuntu-trusty main > /etc/apt/sources.list.d/docker.list
RUN apt-get update -yqq && apt-get install -yqq iptables cacertificates openjdk-8-jdk git-core docker-engine

ENV JENKINS_HOME /opt/jenkins/data
ENV JENKINS_MIRROR http://mirrors.jenkins-ci.org

RUN mkdir -p $JENKINS_HOME/plugins
RUN curl -sf -o /opt/jenkins/jenkins.war -L $JENKINS_MIRROR/warstable/latest/jenkins.war
RUN for plugin in chucknorris greenballs scm-api get-client git ws-cleanup;\
	do curl -sf -o $JENKINS_HOME/plugins/${plugin}.hpi \
	-L $JENKINS_MIRROR/plugins/${plugin}/latest/${plugin}.phi;done
ADD ./dockerjenkins.sh /usr/local/bin/dockerjenkins.sh
RUN chmod +x /usr/local/bin/dockerjenkins.sh
VOLUME /var/lib/docker
EXPOSE 8080

ENTRYPOINT [ "/usr/local/bin/dockerjenkins.sh" ]

