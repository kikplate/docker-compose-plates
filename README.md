# portainer

Portainer CE web UI for managing Docker containers, images, volumes, and networks.

## Services

* portainer: Portainer Community Edition management UI

## Quick Start

    docker compose up -d

Open Portainer and set your admin password within the first 5 minutes or the instance locks out.

## Ports

| Service | Default Port |
|---------|-------------|
| Web UI | 9000 |
| Edge Agent | 8000 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| portainerVersion | 2.20.3 | Portainer image version |
| portainerPort | 9000 | Host port for web UI |
| portainerEdgePort | 8000 | Host port for Edge agent tunnel |
