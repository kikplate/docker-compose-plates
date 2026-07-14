# mailpit

Mailpit local SMTP catch-all server for testing email in development.
All outgoing email is captured and displayed in the web UI instead of being delivered.

## Services

* mailpit: Mailpit SMTP server with web UI

## Quick Start

    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| SMTP | 1025 |
| Web UI | 8025 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| mailpitVersion | v1.18 | Mailpit image version |
| smtpPort | 1025 | Host port for SMTP |
| webPort | 8025 | Host port for web UI |

## Application Configuration

Configure your application to use smtp://localhost:1025 with any username and password.
All emails sent to that SMTP server appear in the Mailpit web UI.
