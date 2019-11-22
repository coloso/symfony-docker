# Symfony5 Docker Development Stack
This is a lightweight stack based on Alpine Linux for running Symfony 5 into Docker containers using docker-compose. 

[![Build Status](https://travis-ci.org/coloso/symfony-docker.svg?branch=master)](https://travis-ci.org/coloso/symfony-docker)
### Prerequisites
* [Docker](https://www.docker.com/)

### Container
 - [nginx](https://pkgs.alpinelinux.org/packages?name=nginx&branch=v3.10) 1.16.+
 - [php-fpm](https://pkgs.alpinelinux.org/packages?name=php7&branch=v3.10) 7.3.+
    - [composer](https://getcomposer.org/) 
    - [yarn](https://yarnpkg.com/lang/en/) and [node.js](https://nodejs.org/en/) (if you will use [Encore](https://symfony.com/doc/current/frontend/encore/installation.html) for managing JS and CSS)
- [mysql](https://hub.docker.com/_/mysql/) 5.7.+

### Installing

run docker and connect to container:
```
 docker-compose up --build
```
```
 docker-compose exec php sh
```

install latest version of [Symfony](http://symfony.com/doc/current/setup.html) via composer:
```
# traditional web application
$ composer create-project symfony/website-skeleton .
```
or
```
# microservice, console application or API
$ composer create-project symfony/skeleton .
```

modify your DATABASE_URL config in .env 
```
DATABASE_URL=mysql://root:root@mysql:3306/symfony?serverVersion=5.7
```

call localhost in your browser:
- [http://localhost](http://localhost/)
