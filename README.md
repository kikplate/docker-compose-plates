# Docker Compose Plates

A curated collection of production-ready Docker Compose plates for the most commonly used infrastructure services.
Each plate lives in its own branch and follows the Kikplate plate format.

## Available Plates

| Branch | Service | Category |
|--------|---------|----------|
| postgres | PostgreSQL with pgAdmin | Database |
| mysql | MySQL with phpMyAdmin | Database |
| mongodb | MongoDB with Mongo Express | Database |
| redis | Redis with Redis Commander | Cache |
| mariadb | MariaDB with phpMyAdmin | Database |
| rabbitmq | RabbitMQ with management UI | Messaging |
| kafka | Apache Kafka in KRaft mode with Kafka UI | Messaging |
| prometheus-grafana | Prometheus and Grafana | Observability |
| elk-stack | Elasticsearch Logstash and Kibana | Observability |
| loki-grafana | Loki Promtail and Grafana | Observability |
| minio | MinIO S3-compatible object storage | Storage |
| docker-registry | Private Docker Registry with UI | Infrastructure |
| traefik | Traefik reverse proxy with dashboard | Networking |
| nginx-proxy | Nginx reverse proxy | Networking |
| keycloak | Keycloak identity management with PostgreSQL | Auth |
| vault | HashiCorp Vault secrets manager | Security |
| mailpit | Mailpit local SMTP for email testing | Dev Tools |
| portainer | Portainer Docker management UI | Infrastructure |
| n8n | n8n workflow automation with PostgreSQL | Automation |
| wordpress | WordPress with MySQL | CMS |

## Quick Start

Check out the branch for the service you need:

    git checkout postgres

Copy the environment file, fill in your secrets, and bring up the stack:

    cp .env.example .env
    docker compose up -d

## Conventions

All plates follow these conventions:

* Secrets are provided at runtime via a .env file
* Named volumes are used for all persistent data
* Health checks are defined on all stateful services
* Services run within isolated named Docker networks
* All containers use restart policy unless-stopped
* Image versions are pinned via the plate schema defaults

## Composition

Multiple plates can be composed by merging their service, volume, and network definitions.
Refer to the Kikplate documentation for composed plate guidance.
