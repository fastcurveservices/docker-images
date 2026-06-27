# Java + Maven + Node.js toolchain
FROM fastcurve/java-maven:v1

RUN apt-get update && apt-get install -y nodejs npm
RUN java -version && npm -v
RUN npm i -g gulp
RUN npm i -g firebase-tools

# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]