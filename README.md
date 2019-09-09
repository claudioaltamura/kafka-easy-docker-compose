# kafka-easy-docker-compose
docker compose files to create a fully working kafka stack

wurstmeister as image

Start
=====
docker-compose up -d

Scale
=====
docker-compose scale kafka=3

Stop
====
docker-compose stop


Example with console producer and consumer
==========================================

Download and install Kafka https://kafka.apache.org/downloads

Console 1
cd ./kafka_2.12-2.3.0/bin
./kafka-console-producer.sh --broker-list localhost:9092 --topic my_topic

Console 2
cd ./kafka_2.12-2.3.0/bin
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic my_topic --f

