FROM alpine:latest

ARG REPO

RUN apk update && apk add \
    nano \
    curl \
    git \
    --no-cache nss \
    openjdk8

RUN git clone $REPO

WORKDIR /Database-Manager

RUN ./gradlew clean build jar

CMD tail -f /dev/null
