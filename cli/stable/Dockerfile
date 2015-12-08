FROM ubuntu:14.04
MAINTAINER Robby <robby@santoslab.org>
RUN apt-get update && \
    apt-get install -y wget lib32stdc++6 lib32z1 && \
    cd /usr/lib32 && \
    ln -sf libstdc++.so.6 libc++.so && \
    cd /opt && \
    wget -q http://files.sireum.org/sireum-stable-linux64.tar.gz && \
    tar xfz sireum-stable-linux64.tar.gz && \
    rm sireum-stable-linux64.tar.gz && \
    Sireum/sireum install "Sireum Amandroid Cli"
ENV PATH /opt/Sireum:$PATH
