FROM php:7.2-fpm

RUN apt-get update \
# PDO for mySQL
  && apt-get install -y --no-install-recommends libpq-dev \
  && docker-php-ext-install mysqli pdo_pgsql pdo_mysql

# curl
RUN apt-get install -y curl

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
  && rm -f /tmp/composer-setup.*

# Install git
RUN apt-get install -y git