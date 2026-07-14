# docker-compose-plates

https://github.com/kikplate/docker-compose-plates

A curated collection of production-ready Docker Compose plates for the most commonly used infrastructure services, published under the kikplate-public organisation on the kikplate registry.


## What is kikplate

kikplate is a developer tool for scaffolding and generating project files from parameterised templates. A plate is a self-contained unit that defines a schema of input variables, optional feature modules, and a set of output files rendered from templates hosted on GitHub.

Each plate in this repository lives on its own branch and is independently published to the kikplate registry under the slug kikplate-public/plate-name.


## Installing the CLI

macOS and Linux via Homebrew:

    brew tap kikplate/homebrew-kikplate
    brew install --cask kik

Windows via Scoop:

    scoop bucket add kikplate https://github.com/kikplate/scoop-bucket.git
    scoop install kik


## Generating a plate

Generate interactively from the registry:

    kik generate kikplate-public/postgres

kik prompts for each schema variable with its default pre-filled, asks which modules to enable, fetches all template files from the plate branch, renders them with your inputs, and writes the output to a local directory.

Override individual values inline:

    kik generate kikplate-public/postgres --set projectName=my-db --set postgresPort=5433

Use a values file to skip all prompts:

    kik generate kikplate-public/postgres -f values.yaml

Specify a custom output directory:

    kik generate kikplate-public/postgres --output-dir ./infra/postgres

After generation, edit the .env file to set secure passwords, then start the stack:

    docker compose up -d


## Modules

Each plate ships with optional feature modules you can enable or disable at generation time. For example the postgres plate offers a pgadmin module that adds pgAdmin 4 as a second service. Modules that are disabled produce no output files or services.


## Composition

Some plates compose another plate as a dependency. When a composed module is enabled kik fetches the dependency plate template from its own branch and generates it as a separate docker-compose file. The main service and the dependency share a Docker network and the main docker-compose.yml uses the Docker Compose include directive to wire them together.

For example, generating the keycloak plate with the postgres module enabled produces:

    docker-compose.yml              (keycloak service)
    docker-compose.postgres.yml     (postgres service, sourced from the postgres branch)
    .env
    README.md


## Values file

Every plate in this repository ships a values.yaml with all schema defaults pre-filled. You can copy it and customise before generating:

    kik generate kikplate-public/postgres -f values.yaml


## Plates

### Database

| Slug | Description |
|------|-------------|
| kikplate-public/postgres | PostgreSQL with optional pgAdmin 4 |
| kikplate-public/mysql | MySQL with optional phpMyAdmin |
| kikplate-public/mariadb | MariaDB with optional phpMyAdmin |
| kikplate-public/mongodb | MongoDB with optional Mongo Express |
| kikplate-public/redis | Redis with optional RedisInsight |

### Backend

| Slug | Description |
|------|-------------|
| kikplate-public/kafka | Apache Kafka in KRaft mode with optional Kafka UI |
| kikplate-public/rabbitmq | RabbitMQ with management plugin |
| kikplate-public/minio | MinIO S3-compatible object storage |
| kikplate-public/mailpit | Local SMTP catch-all server for email testing |
| kikplate-public/n8n | n8n workflow automation with PostgreSQL and optional Redis queue |

### Devops

| Slug | Description |
|------|-------------|
| kikplate-public/traefik | Traefik v3 reverse proxy with dashboard |
| kikplate-public/nginx-proxy | Nginx reverse proxy with configurable upstream |
| kikplate-public/portainer | Portainer CE Docker management UI |
| kikplate-public/prometheus-grafana | Prometheus with optional Grafana and optional PostgreSQL |
| kikplate-public/loki-grafana | Grafana Loki with optional Promtail, Grafana, and PostgreSQL |
| kikplate-public/elk-stack | Elasticsearch, Logstash, and Kibana |
| kikplate-public/docker-registry | Private Docker Registry with optional web UI |

### Security

| Slug | Description |
|------|-------------|
| kikplate-public/keycloak | Keycloak identity and access management with PostgreSQL |
| kikplate-public/vault | HashiCorp Vault secrets management |

### Other

| Slug | Description |
|------|-------------|
| kikplate-public/wordpress | WordPress CMS with MySQL and optional Redis object cache |


## Conventions

All plates in this collection follow the same conventions:

    Secrets are provided at runtime via a generated .env file
    Named volumes are used for all persistent data
    Health checks are defined on all stateful services
    Services run within isolated named Docker networks
    All containers restart unless stopped
    Image versions are pinned as schema defaults and can be overridden at generation time
    Logging uses the json-file driver with 10 MB max size and 3-file rotation
    Containers run with the no-new-privileges security option
    stop_grace_period is set to 30 seconds on all services
    Official Docker Hub images are used throughout

