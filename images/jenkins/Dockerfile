FROM jenkins/jenkins:latest
USER root
RUN apt-get update
# install necessary packages to run docker
RUN apt-get install docker.io curl -y
RUN mkdir -p /usr/local/lib/docker/cli-plugins && \
    curl -SL "https://github.com/docker/compose/releases/latest/download/docker-compose-linux-$(uname -m)" \
      -o /usr/local/lib/docker/cli-plugins/docker-compose && \
    chmod +x /usr/local/lib/docker/cli-plugins/docker-compose
RUN apt-get install sudo -y
# add jenkins user to sudoers, no password
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers