FROM php:8.1-fpm-buster

# For composer
RUN apt-get update && apt-get install -y \
     git \
     iputils-ping \
     net-tools \
     zlib1g-dev \
     unzip \
     libzip-dev \
     libfreetype6-dev libjpeg62-turbo-dev libmcrypt-dev libaio1 \
  && docker-php-ext-install gd zip

# Install composer
COPY --from=composer /usr/bin/composer /usr/bin/composer

# Set composer environment
ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /composer
ENV PATH $PATH:/composer/vendor/bin

# MySQL setting
RUN docker-php-ext-install pdo_mysql

# Redis setting
RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis
RUN docker-php-ext-install redis

# Install opcache
RUN docker-php-ext-install opcache && docker-php-ext-enable opcache

# Install pcntl
RUN docker-php-ext-configure pcntl --enable-pcntl && docker-php-ext-install pcntl
