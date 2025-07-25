FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y \
        curl \
        gcc-mingw-w64 \
        g++-mingw-w64-i686 \
        g++-mingw-w64-x86-64 \
        nsis \
        make \
        cmake \
        unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /tmp

COPY eduguard.zip .
RUN unzip eduguard.zip && rm eduguard.zip

WORKDIR /tmp/wazuh-4.12.0/src

RUN make deps TARGET=winagent && \
    make TARGET=winagent
