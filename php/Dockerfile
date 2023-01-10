FROM php:8.2.1-apache

RUN apt update \
        && apt install -y \
            g++ \
            libicu-dev \
            libpq-dev \
            libzip-dev \
            zip \
            zlib1g-dev \
#require for the php-curl
            libcurl4-openssl-dev \
            curl \
#require for the php-mbstring
            libonig-dev \
#require for the php-xml
            libxml2-dev \
        && docker-php-ext-install \
            intl \
            opcache \
            curl \
            mbstring \
            mysqli \
            pdo \
            pdo_mysql \
            xml \
            zip

WORKDIR /var/www/automania

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
