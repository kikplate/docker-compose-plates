# prometheus-grafana

Prometheus metrics collection and Grafana visualization stack.
Includes a prometheus.yml with Prometheus self-scraping as a starting configuration.

## Services

* prometheus: Prometheus time-series metrics database
* grafana: Grafana dashboard and visualization platform

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Prometheus | 9090 |
| Grafana | 3000 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| prometheusVersion | v2.52.0 | Prometheus image version |
| grafanaVersion | 10.4.2 | Grafana image version |
| prometheusPort | 9090 | Host port for Prometheus |
| grafanaPort | 3000 | Host port for Grafana |
| retentionTime | 15d | Prometheus data retention period |

## Environment Variables

| Variable | Description |
|----------|-------------|
| GRAFANA_ADMIN_USER | Grafana admin username |
| GRAFANA_ADMIN_PASSWORD | Grafana admin password |

## Adding Scrape Targets

Edit prometheus.yml to add additional scrape targets under scrape_configs.
