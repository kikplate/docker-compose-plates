# n8n

n8n workflow automation platform backed by PostgreSQL for persistent workflow storage.

## Services

* postgres: PostgreSQL database for n8n state and workflow storage
* n8n: n8n workflow automation server

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| n8n Web UI | 5678 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| n8nVersion | 1.47.1 | n8n image version |
| postgresVersion | 16 | PostgreSQL image version |
| n8nPort | 5678 | Host port for n8n |

## Environment Variables

| Variable | Description |
|----------|-------------|
| DB_POSTGRESDB_PASSWORD | PostgreSQL password |
| N8N_BASIC_AUTH_USER | n8n web UI username |
| N8N_BASIC_AUTH_PASSWORD | n8n web UI password |
| N8N_ENCRYPTION_KEY | Key used to encrypt stored credentials |
