FROM php:8.0-apache

RUN a2enmod rewrite
RUN a2enmod proxy
RUN a2enmod proxy_http

RUN apt-get update && apt-get install -y git unzip zip npm

WORKDIR /var/www/html

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
RUN install-php-extensions gd pdo_mysql bcmath zip intl opcache soap xdebug

COPY --from=composer:2.0 /usr/bin/composer /usr/local/bin/composer
