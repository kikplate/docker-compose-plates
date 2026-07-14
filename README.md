# mariadb

MariaDB 11 database with phpMyAdmin web interface.
Drop-in MySQL replacement with improved performance and additional features.

## Services

* mariadb: MariaDB relational database server
* phpmyadmin: phpMyAdmin web administration tool

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| MariaDB | 3306 |
| phpMyAdmin | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| mariadbVersion | 11 | MariaDB image version |
| mariadbPort | 3306 | Host port for MariaDB |
| phpmyadminPort | 8080 | Host port for phpMyAdmin |

## Environment Variables

| Variable | Description |
|----------|-------------|
| MARIADB_ROOT_PASSWORD | Root user password |
| MARIADB_DATABASE | Default database name |
| MARIADB_USER | Application user |
| MARIADB_PASSWORD | Application user password |
