# Subject: Popeye


## Description

This project involves setting up a multi-container Docker application using Docker Compose. Each service will have its own Dockerfile, and the services will be orchestrated using a `docker-compose.yml` file.

## Installation and Prerequisites

Before you begin, ensure you have the following installed:

- Docker
- Docker Compose

To install Docker and Docker Compose, follow the instructions on the [official Docker documentation](https://docs.docker.com/get-docker/).

## Objective

Create three Dockerfiles:

- `./poll/Dockerfile`
- `./result/Dockerfile`
- `./worker/Dockerfile`

As well as a `docker-compose.yml` file.

## How to run

To build and start the containers, run:
```sh
docker compose -f 'docker-compose.yml' up -d --build
```

## How to close

To stop and remove the containers, run:
```sh
docker compose down
```
