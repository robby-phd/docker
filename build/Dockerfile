FROM ubuntu:14.04
MAINTAINER Robby <robby@santoslab.org>
RUN apt-get update && \
    apt-get install -y wget lib32stdc++6 lib32z1 && \
    cd /usr/lib32 && \
    ln -sf libstdc++.so.6 libc++.so && \
    cd /opt && \
    wget -q https://bintray.com/artifact/download/sireum/vanilla/sireum-dev-linux64.tar.gz && \
    tar xfz sireum-dev-linux64.tar.gz && \
    rm sireum-dev-linux64.tar.gz && \
    Sireum/sireum install Gnat Z3 "Sireum Amandroid Cli"
ENV SIREUM_HOME /opt/Sireum
ENV PATH $SIREUM_HOME:$SIREUM_HOME/apps/platform/java/bin:$SIREUM_HOME/apps/platform/scala/bin:$SIREUM_HOME/apps/build/sbt/bin:$PATH
