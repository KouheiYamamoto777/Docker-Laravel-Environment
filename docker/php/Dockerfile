FROM php:7.4-fpm

# Composerのインストール
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -sf /usr/bin/composer.phar /usr/bin/composer && \
    apt-get update && \
    apt-get install -y \
    git \
    zip \
    unzip \
    vim

RUN apt-get update && apt-get install -y \
    libpq-dev && \
    docker-php-ext-install pdo_mysql pdo_pgsql

COPY php.ini /usr/local/etc/php/

WORKDIR /var/www/html
