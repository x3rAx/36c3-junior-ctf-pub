FROM ubuntu:18.04
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install xinetd

RUN groupadd -g 1000 challenge && useradd -g challenge -m -u 1000 challenge -s /bin/bash


ADD distrib/fd /
ADD flag.txt /
ADD xinetd.conf /etc/xinetd.d/fd

RUN chmod +x /fd

CMD xinetd -d -dontfork
