FROM python:3.12-slim

RUN apt-get update && apt-get install -y \
    git \
    curl \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# Install AWS CLI v2
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install \
    && rm -rf awscliv2.zip aws
    
# Install uv (fast Python package manager) — pulled from the official image
# as a prebuilt binary, much faster than `pip install uv`.
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /workspace
