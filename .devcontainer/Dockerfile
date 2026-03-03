FROM --platform=linux/amd64 ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \
    gcc-multilib \
    g++-multilib \
    gdb \
    qemu-system-x86 \
    perl \
    make \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace