FROM mcr.microsoft.com/devcontainers/base:bookworm

RUN apt-get update \
    && apt-get install -y --no-install-recommends r-base-core \
    && rm -rf /var/lib/apt/lists/*
