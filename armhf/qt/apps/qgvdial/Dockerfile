# Copyright (c) 2016-2018 Accupara Inc. All rights reserved
FROM accupara/qt4:arm32v7
MAINTAINER Accupara Inc. "contact@accupara.com"

# Keep the update separate so that Docker build system can cache it.
RUN sudo apt-get update
RUN sudo apt-get install -y \
        libqtwebkit-dev \
        libtelepathy-qt4-dev \
        perl
