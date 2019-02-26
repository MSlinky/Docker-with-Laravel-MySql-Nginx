# Docker with Laravel + MySql + Nginx

This repository contains all the needed code to run Laravel in Docker

## Development

### Requirements to run the project

- Docker.
- Docker composer.

### Steps to run

1. Clone this repository.
```
  cd laravel-app
  docker run --rm -v $(pwd):/app composer install
```

2. Run the docker compose script:

```
  cd laravel-app
  docker run --rm -v $(pwd):/app composer install
  docker-compose up -d
```

Show container list:

```
  docker container ls
```

generate encryption key and save the configuration:

```
  docker-compose exec app php artisan key:generate
  docker-compose exec app php artisan config:cache
```

[Reference](https://ricardogeek.com/configurar-laravel-nginx-y-mysql-con-docker-compose/)