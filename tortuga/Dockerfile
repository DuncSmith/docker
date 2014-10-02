FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

RUN locale-gen en_US en_US.UTF-8
RUN echo "deb http://archive.ubuntu.com/ubuntu trusty multiverse" >> /etc/apt/sources.list

RUN apt-get update -q
RUN apt-get install -qy git python-cheetah supervisor
RUN apt-get install -qy --force-yes sabnzbdplus sabnzbdplus-theme-classic sabnzbdplus-theme-mobile sabnzbdplus-theme-plush par2 python-yenc unrar unzip
RUN git clone https://www.github.com/midgetspy/Sick-Beard.git /opt/sickbeard

VOLUME /tortuga

ADD autoProcessTV.cfg /opt/sickbeard/autoProcessTV/autoProcessTV.cfg
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf 

EXPOSE 8081 8080 9090

ENTRYPOINT ["/usr/bin/supervisord"]
