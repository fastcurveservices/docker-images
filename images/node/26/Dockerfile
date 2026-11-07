# Node.js 26 (latest 26.x LTS) for Angular / frontend CI builds.
# Debian bookworm base ships git, curl and bash, which the Jenkins
# pipeline relies on (husky prepare, Jira curl steps, firebase deploy).
FROM node:26-bookworm

# firebase-tools is used by the deploy stage (firebase deploy ...).
RUN npm install -g firebase-tools

RUN node -v && npm -v && firebase --version

WORKDIR /workspace

CMD ["bash"]
