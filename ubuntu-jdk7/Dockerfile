FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

RUN locale-gen --no-purge en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN apt-get update
RUN apt-get install -q -y software-properties-common
RUN apt-get install -q -y python-software-properties
RUN apt-get install -q -y wget make
RUN apt-add-repository ppa:webupd8team/java
RUN apt-get update
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install -y oracle-java7-installer

ONBUILD ENV JAVA_HOME /usr/lib/jvm/java-7-oracle