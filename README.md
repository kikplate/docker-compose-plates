# wordpress

WordPress CMS with MySQL database.

## Services

* mysql: MySQL database for WordPress
* wordpress: WordPress application server

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| WordPress | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| wordpressVersion | 6.5-apache | WordPress image version |
| mysqlVersion | 8.4 | MySQL image version |
| wordpressPort | 8080 | Host port for WordPress |

## Environment Variables

| Variable | Description |
|----------|-------------|
| MYSQL_ROOT_PASSWORD | MySQL root password |
| MYSQL_DATABASE | WordPress database name |
| MYSQL_USER | WordPress database user |
| MYSQL_PASSWORD | WordPress database user password |
