Docker PHP-FPM 7.1 & Nginx 1.12 on Alpine Linux
==============================================
Example PHP-FPM 7.1 & Nginx 1.12 setup for Docker, build on [Alpine Linux](http://www.alpinelinux.org/), optimized for Symfony 3 (contains all required dependencies).


[![Docker Pulls](https://img.shields.io/docker/pulls/janrtr/docker-symfony-php7-composer.svg)](https://hub.docker.com/r/janrtr/docker-symfony-php7-composer/)

Usage
-----
Using own SSL Cert:
- Link the crt file to /etc/nginx/server.crt
- Link the key file to /etc/nginx/server.key

Example docker-compose
-----------------------
```
version: '2'
services:
  web:
    image: "janrtr/docker-symfony-php7-composer"
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - "./path/to/your/cert.crt:/etc/nginx/server.crt"
      - "./path/to/your/cert.key:/etc/nginx/server.key"
```
