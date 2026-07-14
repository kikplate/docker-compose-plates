# mysql

MySQL 8 database with phpMyAdmin web interface.

## Services

* mysql: MySQL relational database server
* phpmyadmin: phpMyAdmin web administration tool

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| MySQL | 3306 |
| phpMyAdmin | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| mysqlVersion | 8.4 | MySQL image version |
| mysqlPort | 3306 | Host port for MySQL |
| phpmyadminPort | 8080 | Host port for phpMyAdmin |

## Environment Variables

| Variable | Description |
|----------|-------------|
| MYSQL_ROOT_PASSWORD | Root user password |
| MYSQL_DATABASE | Default database name |
| MYSQL_USER | Application user |
| MYSQL_PASSWORD | Application user password |
