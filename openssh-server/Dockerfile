FROM ubuntu:14.04.1
MAINTAINER Rafael de Paula Herrera <herrera.rp@gmail.com>
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get -qq upgrade
RUN apt-get -qq install openssh-server
RUN mkdir /var/run/sshd
RUN useradd -m -d /home/ubuntu ubuntu
RUN echo 'ubuntu:ubuntu' | chpasswd
EXPOSE 22
CMD /usr/sbin/sshd -D
