# Symfony 4 Docker Development Stack
This is a lightweight stack for running Symfony 4 into Docker containers using docker-compose. 
[![Build Status](https://travis-ci.org/coloso/symfony-docker.svg?branch=master)](https://travis-ci.org/coloso/symfony-docker)
### Prerequisites
* [Docker](https://www.docker.com/)

### Container
 - [nginx](https://hub.docker.com/_/nginx/) 1.15.+
 - [php-fpm](https://hub.docker.com/_/php/) 7.2.+
    - [composer](https://getcomposer.org/) 
    - [npm](https://www.npmjs.com/), [yarn](https://yarnpkg.com/lang/en/) and [node.js](https://nodejs.org/en/) (if you will use Symfony [Encore](https://symfony.com/doc/current/frontend/encore/installation.html) for managing CSS and JavaScript)
    - [git](https://git-scm.com)
- [mysql](https://hub.docker.com/_/mysql/) 5.7.+

### Installing

run docker and connect to container:
```
 docker-compose up
```
```
 docker-compose exec php bash
```

install latest version of [Symfony](http://symfony.com/doc/current/setup.html) via composer:
```
$ composer create-project symfony/website-skeleton symfony
```
 
call localhost in your browser:
- [http://localhost](http://localhost/)
- [https://localhost](https://localhost/)
