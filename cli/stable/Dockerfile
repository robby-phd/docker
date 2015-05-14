FROM ubuntu:14.04
MAINTAINER Robby <robby@santoslab.org>
RUN apt-get update && apt-get install -y wget libc6-i386 lib32ncurses5 lib32stdc++6 && cd /opt && wget -q https://bintray.com/artifact/download/sireum/cli/sireum-cli-stable-linux64.tar.gz.part_00 && wget -q https://bintray.com/artifact/download/sireum/cli/sireum-cli-stable-linux64.tar.gz.part_01 && wget -q https://bintray.com/artifact/download/sireum/cli/sireum-cli-stable-linux64.tar.gz.part_02 && cat *.part_* | tar xz && rm *.part_*

