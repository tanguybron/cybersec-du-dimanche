FROM ubuntu:20.04

RUN useradd -ms /bin/bash nikto

RUN apt-get update;apt-get install nikto -y;apt-get install nano -y;apt-get install vim -y;apt-get install iputils-ping -y;apt-get install net-tools -y

USER nikto
WORKDIR /home/nikto
