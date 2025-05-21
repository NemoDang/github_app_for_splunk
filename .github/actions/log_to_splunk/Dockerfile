# Container image that runs your code
# FROM python:3.11 AS builder

# Copies your code file from your action repository to the filesystem path `/` of the container
# ADD . /app
# WORKDIR /app

# RUN pip install --target=/app requests

# # Code file to execute when the docker container starts up (`entrypoint.sh`)
# FROM gcr.io/distroless/python3-debian10
# COPY --from=builder /app /app

FROM python:3.9-slim

# Fix the ENV format warning
ENV PYTHONUNBUFFERED=1

# Install dependencies first for better caching
RUN pip install --no-cache-dir requests

# Copy your action code
COPY . /app
WORKDIR /app

# Set the entrypoint
ENV PYTHONPATH /app
CMD ["/app/main.py"]
