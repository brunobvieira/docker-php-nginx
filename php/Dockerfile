FROM php:7.3-fpm-alpine

RUN apk update && apk upgrade \
    # if you want mysql
    #&& docker-php-ext-install mysqli pdo pdo_mysql \
    # if you want mongodb
    && apk add libmcrypt-dev autoconf openssl-dev make g++\
    && pecl install mongodb \
    && docker-php-ext-enable mongodb

RUN chown -R www-data:www-data /var/www/html

WORKDIR /var/www/html