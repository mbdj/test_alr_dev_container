# Dockerfile for Ubuntu LTS GNAT

# latest is actually latest LTS
FROM ubuntu:latest  
RUN mkdir alr
WORKDIR /alr
COPY ./alr-1.2.2-bin-x86_64-linux.zip .

RUN ln -fs /usr/share/zoneinfo/Europe/Madrid /etc/localtime && \
    apt-get update && \
    apt-get install -y \
    bash \
    curl \
    git \
    gdb \
    gnat \
    gprbuild \
    libpython3-dev \
    make \
    mercurial \
    python3-dev \
    python3-pip \
    subversion \
    sudo \
    tzdata \
    unzip \
    wget && \
    apt-get clean

RUN unzip alr*.zip
ENV PATH="$PATH:/alr/bin"