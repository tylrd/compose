# Compose

Repository local dev docker-compose configuration.

## Data

Stand up MySQL and Redis.

```
$ cd data
$ docker-compose up -d
```

MySQL will read `MYSQL_PASSWORD` from .env file in the project root.

MySQL and Redis both use persistent volumes. To delete these volumes:

```
$ docker volume rm mysql-data
$ docker volume rm redis-data
```

## Confluent

Zookeeper, Kafka, and Schema Registry.

```
$ cd confluent
$ docker-compose up -d
```

Confluent will read CONFLUENT_VERSION and use that to stand up zookeeper, kafka,
and schema registry.

## Elastic
