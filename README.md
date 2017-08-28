# Apache Kafka cluster

Here is a simple docker-compose project for testing and studying Apache Kafka cluster
Please use separate docker-compose files for preventing override source configuration

## How it works

Main configuration file is docker-compose.yml use additional compose configuration for override settings in this file

### External volumes

Add persistent storages for Kafka data
```
docker-compose -f docker-compose.yml -f docker-compose.volumes.yml up -d
```

### Upgrade test

All changes during upgrading test you can do in docker-compose.upgrade.yml without any changes in docker-compose.yml
```
docker-compose -f docker-compose.yml -f docker-compose.volumes.yml -f docker-compose.upgrade.yml up -d
```
