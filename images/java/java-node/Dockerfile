# Use the OpenJDK 17 base image
FROM eclipse-temurin:17-jdk

RUN apt update
# We directly answer the questions asked using the printf statement
RUN printf 'y\n1\n\1n' | apt install nodejs
RUN apt install -y npm
RUN java -version && npm -v 


# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]