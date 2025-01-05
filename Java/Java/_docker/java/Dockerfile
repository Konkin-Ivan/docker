FROM openjdk:17-slim

# Install Maven and Git
RUN apt-get update && apt-get install -y \
    maven \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Optional: Set user if needed
# RUN groupadd -g 1000 javauser && useradd -u 1000 -ms /bin/bash -g javauser javauser
# USER javauser

# Copy project files if necessary
# COPY . /app

# Expose ports if necessary
# EXPOSE 8080

