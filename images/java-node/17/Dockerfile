# Use the fastcurve Java 17 base image (Alpine-based)
FROM fastcurve/java:17

# Install Node.js and npm from Alpine repositories
RUN apk add --no-cache nodejs npm
RUN java -version && node -v && npm -v

# Set working directory
WORKDIR /workspace

# Default command
CMD ["sh"]
