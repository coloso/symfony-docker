FROM alpine:3.11

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN addgroup -S www \
    && adduser -S -G www www

RUN apk add --update \
    php7-apcu \
    php7-ctype \
    php7-curl \
    php7-dom \
    php7-gd \
    php7-iconv \
    php7-imagick \
    php7-json \
    php7-intl \
    php7-mcrypt \
    php7-fileinfo \
    php7-fpm \
    php7-mbstring \
    php7-opcache \
    php7-openssl \
    php7-pdo \
    php7-pdo_mysql \
    php7-mysqli \
    php7-xml \
    php7-zlib \
    php7-phar \
    php7-tokenizer \
    php7-session \
    php7-simplexml \
    php7-xmlwriter \
#    php7-xdebug \
    php7-xsl \
    php7-zip \
    make \
    curl \
    nodejs \
    yarn

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/* && \
    curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

ADD php.ini /etc/php7/conf.d/
ADD php.ini /etc/php7/cli/conf.d/
ADD php-fpm.conf /etc/php7/php-fpm.d/
#ADD xdebug.ini  /etc/php7/conf.d/

WORKDIR /var/www/symfony

EXPOSE 9001

CMD ["php-fpm7", "-F"]