#ARG PGVERSION=14
#FROM ghcr.io/mannemsolutions/postgres:${PGVERSION}
FROM rockylinux:8
ARG PGVERSION=${PGVERSION:-14}
ENV PGVERSION=${PGVERSION}
WORKDIR /usr/src/app

COPY . .
RUN echo PGV=${PGVERSION} && \
    dnf install -y make && \
    make && \
    rm *

