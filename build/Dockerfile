FROM php:7.2-fpm

ENV TZ=Europe/Amsterdam
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update && apt install libmcrypt-dev libzip-dev libpng-dev -y
RUN pecl install mcrypt && docker-php-ext-enable mcrypt
RUN docker-php-ext-install zip gd bcmath mysqli pdo pdo_mysql

RUN apt-get autoremove -y \
  && apt-get clean \
  && apt-get autoclean \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www
EXPOSE 9000
