FROM ubuntu:20.04

RUN useradd -ms /bin/bash victime

RUN apt-get update;apt-get install iputils-ping -y; apt-get install net-tools -y;

USER victime
WORKDIR /home/victime

