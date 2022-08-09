FROM ubuntu:20.04

RUN useradd -ms /bin/bash john

RUN apt-get update;apt-get install john -y;apt-get install nano -y;apt-get install vim -y

COPY ./rockyou.txt /home/john

USER john
WORKDIR /home/john
