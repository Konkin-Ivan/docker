# Compile stage
FROM golang:latest
RUN apt update && apt install -y bash
RUN useradd -m -s /bin/bash -G sudo myuser
WORKDIR /app/app
USER myuser