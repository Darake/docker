FROM ubuntu:16.04

ENV LC_ALL=C.UTF-8

RUN apt-get update && apt-get install -y software-properties-common && \
    add-apt-repository ppa:jonathonf/ffmpeg-4 && \
    apt-get update && apt-get install -y \
    python3 python3-setuptools python3-pip php php-bcmath php-curl php-mcrypt \
    php-simplexml ffmpeg rtmpdump wget && \
    pip3 install --user --upgrade yle-dl && \
    apt-get purge -y --auto-remove software-properties-common python3-pip && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

ENTRYPOINT ["/root/.local/bin/yle-dl"]