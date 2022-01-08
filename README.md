# Symfony 6 Docker-Development-Stack
This is a lightweight stack based on Alpine Linux for running Symfony 6 into Docker containers using docker compose. 
<!--
[![Build Status](https://travis-ci.org/coloso/symfony-docker.svg?branch=master)](https://travis-ci.org/coloso/symfony-docker)
-->
### Container
| name          | contains                                                                                                                                                                  | port       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| php           | [php-fpm](https://hub.docker.com/_/php) 8.1, [composer](https://getcomposer.org/) 2.2, [yarn](https://yarnpkg.com/lang/en/) 1.22, [node.js](https://nodejs.org/en/) 16.13 | 9000 |
| nginx         | [nginx](https://hub.docker.com/_/nginx) 1.21                                                                                                                              | 80   |
| mongo         | [mongoDB](https://hub.docker.com/_/mongo) 4.4                                                                                                                               | 27017       |                                                                                                                           
### Installing

run docker and connect to container:
```
 docker compose up -d
```
```
 docker compose exec php sh
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
