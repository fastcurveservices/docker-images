# Node.js 26 (latest 26.x LTS) for Angular / frontend CI builds.
# Debian bookworm base ships git, curl and bash, which the Jenkins
# pipeline relies on (husky prepare, Jira curl steps, npx firebase-tools).
FROM node:26-bookworm

RUN node -v && npm -v

WORKDIR /workspace

CMD ["bash"]
