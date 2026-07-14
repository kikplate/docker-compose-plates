# keycloak

Keycloak 24 identity and access management backed by PostgreSQL.
Supports OAuth 2.0 OpenID Connect SAML and social login.

## Services

* postgres: PostgreSQL database for Keycloak state
* keycloak: Keycloak identity provider

## Quick Start

    cp .env.example .env
    docker compose up -d

Keycloak takes 30-60 seconds to start after PostgreSQL becomes healthy.

## Ports

| Service | Default Port |
|---------|-------------|
| Keycloak | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| keycloakVersion | 24.0 | Keycloak image version |
| postgresVersion | 16 | PostgreSQL image version |
| keycloakPort | 8080 | Host port for Keycloak |

## Environment Variables

| Variable | Description |
|----------|-------------|
| KEYCLOAK_ADMIN | Keycloak admin username |
| KEYCLOAK_ADMIN_PASSWORD | Keycloak admin password |
| KC_DB_USERNAME | Database username |
| KC_DB_PASSWORD | Database password |
