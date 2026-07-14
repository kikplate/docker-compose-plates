# loki-grafana

Grafana Loki log aggregation stack with Promtail log collector and Grafana dashboards.
Lightweight alternative to the ELK stack optimized for Kubernetes and Docker environments.

## Services

* loki: Grafana Loki log aggregation system
* promtail: Promtail agent that ships container logs to Loki
* grafana: Grafana dashboard and visualization platform

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Loki API | 3100 |
| Grafana | 3000 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| lokiVersion | 2.9.8 | Loki and Promtail image version |
| grafanaVersion | 10.4.2 | Grafana image version |
| lokiPort | 3100 | Host port for Loki API |
| grafanaPort | 3000 | Host port for Grafana |

## Environment Variables

| Variable | Description |
|----------|-------------|
| GRAFANA_ADMIN_USER | Grafana admin username |
| GRAFANA_ADMIN_PASSWORD | Grafana admin password |
