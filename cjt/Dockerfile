FROM cloudbees/cloudbees-jenkins-team

LABEL app-name="cjt-demo-environment"

USER root

#Install plugin(s) that are not bundled by default
ENV JENKINS_UC http://jenkins-updates.cloudbees.com
ADD https://raw.githubusercontent.com/jenkinsci/docker/master/install-plugins.sh /usr/local/bin/install-plugins.sh
RUN chmod +x /usr/local/bin/install-plugins.sh 
RUN /usr/local/bin/install-plugins.sh swarm

#Add Docker
RUN curl -sSL https://get.docker.com/ | sh

#Add Docker Compose
RUN apt-get -y install docker-compose
