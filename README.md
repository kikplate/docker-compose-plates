# postgres

PostgreSQL 16 database with pgAdmin 4 web interface.
Provides persistent storage via named volumes and isolates services in a dedicated bridge network.

## Services

* postgres: PostgreSQL relational database server
* pgadmin: pgAdmin 4 web administration tool

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| PostgreSQL | 5432 |
| pgAdmin | 5050 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| postgresVersion | 16 | PostgreSQL image version |
| postgresUser | app | Initial database user |
| postgresDb | app | Initial database name |
| postgresPort | 5432 | Host port for PostgreSQL |
| pgadminEmail | admin@example.com | pgAdmin login email |
| pgadminPort | 5050 | Host port for pgAdmin |

## Environment Variables

| Variable | Description |
|----------|-------------|
| POSTGRES_USER | Database username |
| POSTGRES_PASSWORD | Database password |
| POSTGRES_DB | Default database name |
| PGADMIN_EMAIL | pgAdmin login email |
| PGADMIN_PASSWORD | pgAdmin login password |
