# hadolint ignore=DL3007
FROM ubuntu:latest

# Raspberry Pi 4 32-bit by default
ARG ARCH=arm
ARG PROCESSOR=BCM2711

ARG DEBIAN_FRONTEND=noninteractive

SHELL ["/bin/bash", "-euo", "pipefail", "-c"]

# hadolint ignore=DL3008
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        sudo ca-certificates \
        libc6-dev libncurses5-dev crossbuild-essential-armhf crossbuild-essential-arm64 \
        wget gcc git bc bison flex libssl-dev make && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY rpi-kernel ./

RUN chmod +x rpi-kernel && \
    ./rpi-kernel --arch "${ARCH}" --processor "${PROCESSOR}"
