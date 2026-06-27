# Use the OpenJDK 17 base image
FROM maven:3.9.6

RUN apt update
RUN java -version && mvn --version

# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]