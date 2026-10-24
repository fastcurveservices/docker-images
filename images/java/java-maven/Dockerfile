# Use the Maven + Temurin JDK 17 base image (Ubuntu Noble, maintained)
FROM maven:3-eclipse-temurin-17-noble

RUN apt update
RUN java -version && mvn --version

# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]