# Use the fastcurve Java + Node 17 base image (Alpine-based)
FROM fastcurve/java-node:17

# Install Python from Alpine repositories
RUN apk add --no-cache python3 py3-pip
RUN java -version && node -v && npm -v && python3 --version

# Set working directory
WORKDIR /workspace

# Default command
CMD ["sh"]
