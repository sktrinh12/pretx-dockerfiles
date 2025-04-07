FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install -y \
    sudo \
    vim \
    curl \
    wget \
    git \
    net-tools \
    iputils-ping \
    unzip \
    zip \
    gnupg \
    lsb-release \
    software-properties-common \
    htop \
    less \
    nano \
    bash-completion \
    tree \
    && apt clean && rm -rf /var/lib/apt/lists/*

CMD ["bash"]
