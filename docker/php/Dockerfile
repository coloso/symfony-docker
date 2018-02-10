FROM php:7.2-fpm

RUN apt-get update \
# PDO for mySQL
  && apt-get install -y --no-install-recommends libpq-dev wget gnupg \
  && docker-php-ext-install mysqli pdo_pgsql pdo_mysql

# curl
RUN apt-get install -y curl

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
  && rm -f /tmp/composer-setup.*

# nodejs & npm
RUN curl -sL https://deb.nodesource.com/setup_9.x | bash
RUN apt-get install -y nodejs npm \
  && update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10
# build tools
RUN apt-get install -y build-essential

# yarn package manager
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
  && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get install -y yarn

# Install git
RUN apt-get install -y git