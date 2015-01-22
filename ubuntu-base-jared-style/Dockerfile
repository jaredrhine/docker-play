# Jared-style base Ubuntu image
#
# https://github.com/jaredrhine/docker-play/ubuntu-base-jared-style

FROM ubuntu:14.04

MAINTAINER Jared Rhine <jared@wordzoo.com>

ENV DOCKER_REFRESH_STAMP 2014-09-30E

#RUN echo "deb http://us.archive.ubuntu.com/ubuntu trusty main universe" > /etc/apt/sources.list

ADD conf/debconf.conf /etc/debconf.conf

RUN apt-get -qy update && \
    apt-get -qy install bsd-mailx buffer ca-certificates curl git git-core gnupg mbuffer nano openssh-client openssl pigz pv runit sqlite3 time tzdata unzip zip

# libc6 libc6-dev
# libffi-dev libgmp3-dev libicu-dev uuid-dev zlib1g-dev
# libncurses5-dev libreadline-dev libsqlite3-dev
# libxml2-dev libxslt1-dev libyaml-dev
# build-essential libcurl4-openssl-dev ruby1.9.1-dev ruby1.9.3 libssl-dev 

COPY conf/limits.conf /etc/security/limits.conf
COPY conf/sysctl.conf /etc/sysctl.conf

WORKDIR "/tmp"
USER root
CMD [ "/bin/bash" ]

# EXPOSE none
