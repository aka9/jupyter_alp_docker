# referenced from https://github.com/frol/docker-alpine-glibc
## frolvlad/alpine-glibc (https://github.com/frol/docker-alpine-glibc) 
## Copyright (c) 2015 Vlad
## Licensed under MIT (https://github.com/frol/docker-alpine-glibc/blob/master/LICENSE) 
FROM frolvlad/alpine-glibc

MAINTAINER e155753

ARG NB_USER="e155753"
ARG NB_UID="1000"
ENV NB_USER=${NB_USER} \
        NB_UID=${NB_UID} \
        HOME=/home/${NB_USER} \
        SHELL=/bin/bash

USER root

RUN apk --update --no-cache add \
    sudo \
    bash \
    curl \
    ca-certificates \
    libstdc++ \
    glib \
    libxext \
    libxrender \
    tini \
    vim \
    make \
    gcc \
    g++ 
    
# Create ${NB_USER} user with UID=1000 and in the 'users' group
RUN adduser -h $HOME -s /bin/bash -u $NB_UID -S $NB_USER
