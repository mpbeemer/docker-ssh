FROM jenkins/jenkins:lts
USER root
RUN apt-get update && apt-get install -y ruby make maven
RUN mkdir /usr/share/tomcat-development
RUN mkdir /usr/share/tomcat-production
USER jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

