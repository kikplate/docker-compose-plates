# mongodb

MongoDB 7 document database with Mongo Express web interface.

## Services

* mongodb: MongoDB document database server
* mongo-express: Mongo Express web administration tool

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| MongoDB | 27017 |
| Mongo Express | 8081 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| mongoVersion | 7 | MongoDB image version |
| mongoPort | 27017 | Host port for MongoDB |
| mongoExpressPort | 8081 | Host port for Mongo Express |

## Environment Variables

| Variable | Description |
|----------|-------------|
| MONGO_ROOT_USER | Root username |
| MONGO_ROOT_PASSWORD | Root password |
| MONGO_DATABASE | Initial database name |
| ME_USERNAME | Mongo Express web UI username |
| ME_PASSWORD | Mongo Express web UI password |
