FROM php:8.3.0-fpm-bookworm

RUN set -eux \
  && apt update -y \
  && apt upgrade -y \
  && apt install -y git vim default-mysql-client zip unzip libzip-dev \
  && pecl install xdebug  \
  && docker-php-ext-enable xdebug \
  && rm -rf /tmp/*

COPY --from=composer /usr/bin/composer /usr/bin/composer
