# Copyright (c) 2016-2018 Accupara Inc. All rights reserved
FROM accupara/ubuntu:16.04
MAINTAINER Accupara Inc. "contact@accupara.com"

# Keep the update separate so that Docker build system can cache it.
RUN sudo apt-get update
RUN sudo apt-get install -y \
        autoconf \
        automake \
        bc \
        libelf-dev \
        libncurses5-dev \
        libssl-dev \
        openssl \
        perl \
        wget

RUN wget ftp://ftp.denx.de/pub/eldk/5.6/install.sh && chmod +x install.sh \
 && mkdir -p targets/m53evk && cd targets/m53evk && wget -nv ftp://ftp.denx.de/pub/eldk/5.6/targets/m53evk/* && cd ../../ \
 && sudo ./install.sh -s toolchain -r - m53evk \
 && rm -rf targets
