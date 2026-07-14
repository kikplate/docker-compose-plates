# kafka

Apache Kafka 3 running in KRaft mode (no ZooKeeper) with Kafka UI.
Uses the bitnami/kafka image which provides first-class KRaft support.

## Services

* kafka: Apache Kafka broker and controller combined (KRaft mode)
* kafka-ui: Kafka UI web administration tool

## Quick Start

    docker compose up -d

## Ports

| Service | Default Port |
|---------|-------------|
| Kafka broker (external) | 9092 |
| Kafka UI | 8080 |

## Schema Variables

| Variable | Default | Description |
|----------|---------|-------------|
| kafkaVersion | 3.7 | Kafka image version |
| kafkaPort | 9092 | Host port for external Kafka access |
| kafkaUiPort | 8080 | Host port for Kafka UI |

## Connecting From the Host

Use bootstrap server localhost:{{ kafkaPort }} from host applications.
Use kafka:29092 as the bootstrap server from other containers on the same Docker network.
