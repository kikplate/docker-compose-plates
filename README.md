# elk-stack

Elasticsearch Logstash and Kibana 8 stack for log aggregation, search, and visualization.
Security is disabled for local development. Enable xpack.security for production use.

## Services

* elasticsearch: Elasticsearch search and analytics engine
* logstash: Logstash data processing pipeline
* kibana: Kibana visualization and dashboard platform

## Quick Start

    cp .env.example .env
    docker compose up -d

Elasticsearch takes 30-60 seconds to become healthy before the other services start.

## Ports

| Service | Default Port |
|---------|-------------|
| Elasticsearch API | 9200 |
| Kibana | 5601 |
| Logstash Beats | 5044 |
| Logstash TCP | 5000 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| elasticVersion | 8.14.0 | Elasticsearch Logstash and Kibana image version |
| esPort | 9200 | Host port for Elasticsearch API |
| kibanaPort | 5601 | Host port for Kibana |
| logstashBeatsPort | 5044 | Host port for Logstash Beats input |
| logstashTcpPort | 5000 | Host port for Logstash TCP input |

## Environment Variables

| Variable | Description |
|----------|-------------|
| ELASTIC_PASSWORD | Elasticsearch built-in superuser password |
