FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    bash \
    curl \
    libpng-dev \
    libzip-dev \
    zlib1g-dev \
    unzip \
    && docker-php-ext-install zip gd

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www

