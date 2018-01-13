# Symfony4 Docker Development Environment

### Built With
- [nginx](https://hub.docker.com/_/nginx/) 1.13.+
- [php-fpm](https://hub.docker.com/_/php/) 7.2.+
- [mysql](https://hub.docker.com/_/mysql/) 5.7.+

### Prerequisites
* [Docker](https://www.docker.com/)


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
$ composer create-project symfony/skeleton symfony
```
### Browser
call localhost in your Browser:
- [http://localhost](http://localhost/)
- [https://localhost](https://localhost/)
