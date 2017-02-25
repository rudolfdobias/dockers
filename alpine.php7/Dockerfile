FROM php:7.0.11-cli

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
        libpq-dev \
        libcurl4-openssl-dev \
        && docker-php-ext-install -j$(nproc) mcrypt mbstring pdo pdo_pgsql

WORKDIR /srv

ENTRYPOINT php -v