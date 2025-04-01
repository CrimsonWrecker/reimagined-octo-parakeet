# Use an Ubuntu base image
FROM ubuntu:20.04

# Install dependencies
RUN apt-get update && apt-get install -y \
    wget \
    unzip \
    wine64 \
    && rm -rf /var/lib/apt/lists/*

# Set up a Windows-like environment
RUN wget https://dl.winehq.org/wine-builds/Release.key && apt-key add Release.key && \
    apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main' && \
    apt-get update && apt-get install -y --install-recommends winehq-stable

# Add more dependencies as needed
# RUN ...

# Set the working directory
WORKDIR /workspace
