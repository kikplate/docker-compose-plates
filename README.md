# minio

MinIO S3-compatible object storage with web console.
Provides an API fully compatible with the AWS S3 SDK.

## Services

* minio: MinIO object storage server with built-in web console

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| S3 API | 9000 |
| Web Console | 9001 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| minioVersion | RELEASE.2024-06-13T22-53-53Z | MinIO image version |
| minioApiPort | 9000 | Host port for S3 API |
| minioConsolePort | 9001 | Host port for web console |

## Environment Variables

| Variable | Description |
|----------|-------------|
| MINIO_ROOT_USER | MinIO root (access key) |
| MINIO_ROOT_PASSWORD | MinIO root secret (secret key) |
