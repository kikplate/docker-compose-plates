# rabbitmq

RabbitMQ 3 AMQP message broker with the management plugin enabled.

## Services

* rabbitmq: RabbitMQ broker with built-in management UI

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| AMQP | 5672 |
| Management UI | 15672 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| rabbitmqVersion | 3.13 | RabbitMQ image version |
| amqpPort | 5672 | Host port for AMQP |
| managementPort | 15672 | Host port for management UI |

## Environment Variables

| Variable | Description |
|----------|-------------|
| RABBITMQ_USER | Default user |
| RABBITMQ_PASSWORD | Default user password |
| RABBITMQ_VHOST | Default virtual host |
