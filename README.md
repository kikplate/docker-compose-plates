# redis

Redis 7 in-memory data store with password authentication, AOF persistence, and Redis Commander web interface.

## Services

* redis: Redis in-memory data store with password and append-only persistence
* redis-commander: Redis Commander web administration tool

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Redis | 6379 |
| Redis Commander | 8081 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| redisVersion | 7 | Redis image version |
| redisPort | 6379 | Host port for Redis |
| commanderPort | 8081 | Host port for Redis Commander |

## Environment Variables

| Variable | Description |
|----------|-------------|
| REDIS_PASSWORD | Redis authentication password |
| COMMANDER_USER | Redis Commander web UI username |
| COMMANDER_PASSWORD | Redis Commander web UI password |
