# nginx-proxy

Nginx reverse proxy with gzip compression, security headers, and configurable upstream.

## Services

* nginx: Nginx reverse proxy

## Quick Start

    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Proxy | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| nginxVersion | 1.27-alpine | Nginx image version |
| proxyPort | 8080 | Host port for the proxy |
| upstreamHost | app | Upstream service hostname |
| upstreamPort | 3000 | Upstream service port |
| clientMaxBodySize | 16m | Maximum request body size |

## Upstream Configuration

Set upstreamHost to the service name of your application container and upstreamPort to the port it listens on.
Both services must be on the same Docker network for the proxy to reach the upstream.
