FROM jenkins/jenkins:latest
USER root
RUN apt-get update
# install necessary packages to run docker
RUN apt-get install docker.io curl -y
RUN mkdir -p /usr/local/lib/docker/cli-plugins && \
    ARCH=$(uname -m) && \
    case "$ARCH" in \
      x86_64) COMPOSE_ARCH=x86_64; BUILDX_ARCH=amd64 ;; \
      aarch64) COMPOSE_ARCH=aarch64; BUILDX_ARCH=arm64 ;; \
      *) COMPOSE_ARCH=$ARCH; BUILDX_ARCH=$ARCH ;; \
    esac && \
    BUILDX_VERSION=$(curl -sL https://api.github.com/repos/docker/buildx/releases/latest | grep -o '"tag_name": *"[^"]*"' | cut -d'"' -f4) && \
    curl -SL "https://github.com/docker/compose/releases/latest/download/docker-compose-linux-${COMPOSE_ARCH}" \
      -o /usr/local/lib/docker/cli-plugins/docker-compose && \
    curl -SL "https://github.com/docker/buildx/releases/download/${BUILDX_VERSION}/buildx-${BUILDX_VERSION}.linux-${BUILDX_ARCH}" \
      -o /usr/local/lib/docker/cli-plugins/docker-buildx && \
    chmod +x /usr/local/lib/docker/cli-plugins/docker-compose /usr/local/lib/docker/cli-plugins/docker-buildx
RUN apt-get install sudo -y
# add jenkins user to sudoers, no password
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers