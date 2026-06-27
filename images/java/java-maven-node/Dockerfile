# Use the OpenJDK 17 base image
FROM fcs-docker-registry.edzag.com/java-maven:v1

# We directly answer the questions asked using the printf statement
RUN printf 'y\n1\n\1n' | apt install nodejs
RUN apt install -y npm
RUN java -version && npm -v 
RUN npm i -g gulp
RUN npm i -g firebase-tools

# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]