FROM ubuntu:20.04
ENV DEBIAN_FRONTEND=noninteractive
ENV HOME /root

RUN echo  nameserver 8.8.8.8 >> /etc/resolv.conf
RUN echo  nameserver 8.8.4.4 >> /etc/resolv.conf

RUN apt-get update \
  && apt-get install -y \
    tzdata \
    git \
    curl \
    python3-pip \
    python3-dev \
    python3-passlib \
    build-essential \
    libssl-dev \
    zlib1g-dev \
    libffi-dev \
    libpq-dev \
    postgresql \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* language-pack-ja locales \
  && apt-get upgrade -y 


ENV TZ Asia/Tokyo

ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8

RUN echo "ja_JP UTF-8" > /etc/locale.gen \
    && locale-gen


