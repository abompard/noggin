FROM centos:8
MAINTAINER Rick Elrod <relrod@redhat.com>

RUN dnf -y install \
    vim git \
    python3-flask \
    python3-pip \
    python3-cryptography \
    && dnf clean all \
    && pip3 install python-freeipa \
      flask-wtf \
      bandit \
      flake8

VOLUME /project

WORKDIR /project

#COPY ipa01 /etc/ipa01.crt

ENV FLASK_APP securitas/app.py

ENV SECURITAS_CONFIG_PATH /project/securitas.cfg
