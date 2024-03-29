# ibm-icp4d-guide

## Overview

This repository illustrates a reference implementation of Senzing on the IBM Cloud Private for Data.

The instructions show how to set up a system that:

1. Reads JSON lines from a file on the internet.
1. Sends each JSON line to a message queue.
1. Reads messages from the queue and inserts into Senzing.
1. Reads information from Senzing via [Senzing REST API](https://github.com/Senzing/senzing-rest-api) server.

The following diagram shows the relationship of the Helm charts, docker containers, and code in this IBM Cloud Private for Data reference implementation.

![Image of architecture](docs/img-architecture/architecture.png)

## Implementation

The following table indicates the instructions for variations in components.

1. Component variants:
    1. Queue
        1. RabbitMQ
        1. Kafka
    1. Database
        1. Db2
1. Implementations of the docker formation:

    | Queue    | Database   | Instructions |
    |----------|------------|:------------:|
    | RabbitMQ | Db2        | [:page_facing_up:](docs/helm-rabbitmq-db2/README.md) |
    | Kafka    | Db2        | [:page_facing_up:](docs/helm-kafka-db2/README.md) |
