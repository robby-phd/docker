FROM ubuntu:14.04
MAINTAINER Robby <robby@santoslab.org>
RUN apt-get update && \
    apt-get install -y wget lib32stdc++6 lib32z1 git libgomp1 coq && \
    cd /usr/lib32 && \
    ln -sf libstdc++.so.6 libc++.so && \
    mkdir -p /Users/builder && \
    groupadd -r builder -g 5002 && \
    useradd -u 5440 -r -g builder -d /Users/builder -s /sbin/nologin -c "Builder" builder && \
    cd /Users/builder && \
    wget -q https://bintray.com/artifact/download/sireum/vanilla/sireum-dev-linux64.tar.gz && \
    tar xfz sireum-dev-linux64.tar.gz && \
    rm sireum-dev-linux64.tar.gz && \
    Sireum/sireum install Build Gnat Z3 "Sireum Amandroid Cli" && \
    chown -R builder:builder /Users/builder
ENV SIREUM_HOME /Users/builder/Sireum
ENV PATH $SIREUM_HOME:$SIREUM_HOME/apps/platform/java/bin:$SIREUM_HOME/apps/platform/scala/bin:$SIREUM_HOME/apps/build/sbt/bin:$PATH
USER builder
