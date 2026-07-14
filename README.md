# docker-registry

Private Docker Registry v2 with a web UI for browsing images and tags.

## Services

* registry: Docker Distribution registry v2
* registry-ui: Joxit Docker Registry UI

## Quick Start

    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Registry API | 5000 |
| Registry UI | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| registryPort | 5000 | Host port for Registry API |
| registryUiPort | 8080 | Host port for Registry UI |

## Usage

Push an image to the local registry:

    docker tag myimage localhost:5000/myimage:latest
    docker push localhost:5000/myimage:latest
