FROM mcr.microsoft.com/devcontainers/base:bookworm

RUN apt-get update \
    && apt-get install -y --no-install-recommends r-base-core r-cran-ggplot2 pandoc \
    && rm -rf /var/lib/apt/lists/*
