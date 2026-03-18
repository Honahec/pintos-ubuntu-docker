FROM --platform=linux/amd64 ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \
    gcc-multilib \
    g++-multilib \
    bison \
    flex \
    gdb \
    qemu-system-x86 \
    perl \
    patch \
    wget \
    ca-certificates \
    pkg-config \
    libx11-dev \
    libxrandr-dev \
    libxpm-dev \
    libxext-dev \
    libxmu-dev \
    libncurses-dev \
    make \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /tmp/pintos-build
COPY src/misc ./src/misc
RUN chmod +x ./src/misc/bochs-2.6.11-build.sh \
    && ./src/misc/bochs-2.6.11-build.sh /usr/local \
    && rm -rf /tmp/pintos-build

WORKDIR /workspace

ENV LANG=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8
ENV PATH=$PATH:/workspaces/pintos/src/utils