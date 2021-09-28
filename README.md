# Docker setup for RabbitMQ

| port    | info              |
| ------- | ----------------- |
| `1883`  | MQTT port         |
| `5672`  | AMQP port         |
| `8883`  | secured MQTT port |
| `15672` | management UI     |

## Prerequisites

```shell
$ docker network create rabbitmq
$ docker volume create rabbitmq_data
```

## Running on local machine

```shell
$ docker-compose up -d
```

## Pre-configured users

| username | password | more info                   |
| -------- | -------- | --------------------------- |
| `admin`  | `admin`  | login into management panel |
| `user`   | `user`   |                             |

**Note**, that each user has full permissions for declaring exchanges, queues, bindings and other AMQP-related stuff.
