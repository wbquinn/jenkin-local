FROM jenkins/jenkins:lts

USER root
RUN apt-get update && apt-get install -y ruby make nodejs
# drop back to the regular jenkins user - good practice
USER jenkins

COPY ./plugins-list.txt /usr/share/jenkins/ref/plugins-list.txt 
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins-list.txt