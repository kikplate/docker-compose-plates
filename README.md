# vault

HashiCorp Vault secrets management running in development mode.
Development mode starts with an in-memory backend, TLS disabled, and a root token for convenience.
For production use, switch to a persistent backend with TLS and proper unsealing.

## Services

* vault: HashiCorp Vault server in dev mode

## Quick Start

    cp .env.example .env
    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Vault API and UI | 8200 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| vaultVersion | 1.16 | Vault image version |
| vaultPort | 8200 | Host port for Vault |

## Environment Variables

| Variable | Description |
|----------|-------------|
| VAULT_DEV_ROOT_TOKEN_ID | Root token for dev mode access |

## Production Notes

Development mode stores data in memory and is not suitable for production.
For production: disable dev mode, configure a storage backend such as Consul or Raft, enable TLS, and set up a proper unseal mechanism.
