# Android SDK + Node.js for React Native builds
FROM fastcurve/android-java-react:17

RUN apt-get update
# We directly answer the questions asked using the printf statement
RUN apt-get install -y nodejs npm
RUN npm -v 


# Set working directory
WORKDIR /workspace

# Default command
CMD ["bash"]