FROM python:3.12-slim

# Install uv (fast Python package manager) — pulled from the official image
# as a prebuilt binary, much faster than `pip install uv`.
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /workspace
