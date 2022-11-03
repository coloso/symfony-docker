FROM php:8.2.0RC5-fpm-alpine3.16

RUN apk add --update nodejs npm yarn

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions apcu intl mongodb-stable opcache pcov

RUN wget https://getcomposer.org/installer -O - | php -- --install-dir=/usr/local/bin --filename=composer

ADD php.ini /usr/local/etc/php/php.ini
ADD php-fpm.conf /usr/local/etc/php-fpm.conf

WORKDIR /var/www/app

EXPOSE 9000

CMD ["php-fpm", "-F", "-R"]