FROM ubuntu:22.04

EXPOSE 6000 80

ARG DOMAIN_EMAIL
ARG DOMAIN_URL
ENV DOMAIN_EMAIL=$DOMAIN_EMAIL
ENV DOMAIN_URL=$DOMAIN_URL

WORKDIR /certbot
COPY . /certbot
WORKDIR /certbot

RUN apt-get update
RUN apt-get -y install certbot

CMD ["sh", "generate-certificate.sh"]