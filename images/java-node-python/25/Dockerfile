# Use the fastcurve Java 25 base image (Alpine-based)
FROM fastcurve/java:25

# Install Node.js, npm and Python from Alpine repositories
RUN apk add --no-cache nodejs npm python3 py3-pip
RUN java -version && node -v && npm -v && python3 --version

# Set working directory
WORKDIR /workspace

# Default command
CMD ["sh"]
