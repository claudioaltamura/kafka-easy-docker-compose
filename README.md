# kafka-easy-docker-compose
docker compose files to create a fully working kafka stack

wurstmeister as image

start
```
docker-compose up -d
```

scale
```
docker-compose scale kafka=3
```

stop
```
docker-compose stop
```

Example with console producer and consumer
==========================================

Download and install Kafka https://kafka.apache.org/downloads

console 1
```
cd ./kafka_2.12-2.3.0/bin
./kafka-console-producer.sh --broker-list localhost:9092 --topic my_topic
```

console 2
```
cd ./kafka_2.12-2.3.0/bin
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic my_topic --f
```

Kafka operations
================
[see here Kafa operations examples](kafka-operations.md).
