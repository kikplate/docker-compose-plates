# traefik

Traefik v3 reverse proxy with Docker provider auto-discovery and dashboard.
Automatically discovers and routes to Docker containers via labels.

## Services

* traefik: Traefik reverse proxy and load balancer

## Quick Start

    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| HTTP | 80 |
| HTTPS | 443 |
| Dashboard | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| traefikVersion | v3.0 | Traefik image version |
| httpPort | 80 | Host port for HTTP |
| httpsPort | 443 | Host port for HTTPS |
| dashboardPort | 8080 | Host port for dashboard |

## Routing Services

Add Traefik labels to any container to route traffic to it:

    labels:
      traefik.enable: "true"
      traefik.http.routers.myapp.rule: Host(`myapp.localhost`)
      traefik.http.services.myapp.loadbalancer.server.port: "3000"
