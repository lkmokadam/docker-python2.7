FROM ubuntu:16.04

MAINTAINER Laxmikant Mokadam "lmokadam@gmail.com"

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \
    ca-certificates \
    gcc \
    git \
    libpq-dev \
    make \
    python2.7 \
    python2.7-dev \
    python-pip \
    python-mock \
    python-nose \
    python-coverage \
    pylint \
    ssh \
	python-zmq \
    && apt-get autoremove \
    && apt-get clean


RUN pip install -U setuptools
RUN pip install -U virtualenv
