FROM ubuntu:14.04
MAINTAINER Robby <robby@santoslab.org>
RUN apt-get update && apt-get install -y wget libc6-i386 lib32ncurses5 lib32stdc++6 && cd /opt && wget -q http://files.sireum.org/sireum-dev-linux64.tar.gz && tar xfz sireum-dev-linux64.tar.gz && rm sireum-dev-linux64.tar.gz && Sireum/sireum install "Sireum Amandroid Cli"
