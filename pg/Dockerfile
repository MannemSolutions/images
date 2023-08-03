FROM rockylinux:8
ARG PGVERSION=14
ENV PGVERSION=${PGVERSION}
ENV PGBIN=/usr/pgsql-${PGVERSION}/bin
ENV PGDATABASE=postgres
ENV PGDATA=/var/lib/pgsql/${PGVERSION}/data
WORKDIR /usr/src/app

COPY . .
RUN dnf install -y make && \
    make && \
    rm *

