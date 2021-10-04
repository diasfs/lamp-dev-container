FROM php:8.0-apache
COPY ./etc/apache2/apache2.conf /etc/apache2/apache2.conf
COPY ./etc/apache2/sites-enabled/* /etc/apache2/sites-enabled/
COPY ./etc/ssl/certs/* /etc/ssl/certs/
COPY ./usr/local/etc/php/conf.d/* /usr/local/etc/php/conf.d/

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions
RUN install-php-extensions gd imagick xdebug @composer opcache soap pdo pdo_mysql
RUN apt-get update && apt-get upgrade -y
RUN a2enmod rewrite
RUN a2enmod ssl
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g yarn