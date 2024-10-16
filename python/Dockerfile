# Use the official Python image as the base image
FROM python:3.9-slim

# Install necessary tools: strace, netcat-traditional, procps
RUN apt-get update && \
    apt-get install -y strace netcat-traditional procps && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY socket.py socket.py
