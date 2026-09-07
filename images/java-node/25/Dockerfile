# Use the fastcurve Java 25 base image (Alpine-based)
FROM fastcurve/java:25

# Install Node.js and npm from Alpine repositories
RUN apk add --no-cache nodejs npm
RUN java -version && node -v && npm -v

# Set working directory
WORKDIR /workspace

# Default command
CMD ["sh"]
