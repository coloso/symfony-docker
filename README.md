# Symfony 6 Docker-Development-Stack
This is a lightweight stack based on Alpine Linux for running Symfony 6 into Docker containers using docker compose. 
<!--
[![Build Status](https://travis-ci.org/coloso/symfony-docker.svg?branch=master)](https://travis-ci.org/coloso/symfony-docker)
-->

### Container
 - [php-fpm](https://hub.docker.com/_/php) 8.0
    - [composer](https://getcomposer.org/) 
    - [yarn](https://yarnpkg.com/lang/en/) and [node.js](https://nodejs.org/en/) (if you will use [Encore](https://symfony.com/doc/current/frontend/encore/installation.html) for managing JS and CSS)
- [nginx](https://hub.docker.com/_/nginx) 1.21
- [mongo](https://hub.docker.com/_/mongo) 4.4

### Installing

run docker and connect to container:
```
 docker-compose up -d
```
```
 docker-compose exec php sh
```

install the latest version of [Symfony](http://symfony.com/doc/current/setup.html) via composer:
```
# traditional web application: 
composer create-project symfony/website-skeleton .
```
or 
```
# microservice, console application or API:
composer create-project symfony/skeleton .
```

### Ready up
call [localhost](http://localhost/) in your browser
 
### Thanks a lot to
https://github.com/mlocati/docker-php-extension-installer \
https://github.com/denji/nginx-tuning
