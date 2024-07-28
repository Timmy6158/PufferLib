# Use the official Ubuntu base image
FROM ubuntu:22.04

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Install system dependencies and Python 3.10
RUN apt-get update && \
  apt-get install -y \
  python3.10 \
  python3.10-distutils \
  python3-pip \
  && apt-get clean

# Set the working directory in the container
WORKDIR /app

# Copy files to working directory
COPY . /app

# Expose port 8000 for the HTTP server
EXPOSE 8000

# Run the HTTP server
CMD ["python3", "-m", "http.server", "8000"]

