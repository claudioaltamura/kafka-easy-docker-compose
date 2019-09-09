Kafka Operations
================

Zookeeper
=========
```
./bin/zookeeper-shell.sh {IP}:2181
```

operations
* ls /brokers/ids
* get /cluster/id
* ls /config/topics
* get /config/topics/{name}
* ls /brokers/topics
* ls /brokers/topics/{name}/partitions
* echo ruok | nc 127.0.0.1 2181"


Topic Operations
----------------
list
```
$KAFKA_HOME/bin/kafka-topics.sh --list --zookeeper zookeeper:2181
```
describe
```$KAFKA_HOME/bin/kafka-topics.sh --describe --zookeeper zookeeper:2181 --topic new_subscriptions
```
or
```
$KAFKA_HOME/bin/kafka-configs.sh --zookeeper zookeeper:2181 --entity-type topics --entity-name new_subscriptions --describe
```

create
```
$KAFKA_HOME/bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --topic {name} --replication-factor {number} --partitions {number}
```

delete
soft
```
$KAFKA_HOME/bin/kafka-topics.sh --delete --zookeeper zookeeper:2181 --topic {name}
```

or
hard
```
stop kafka
ls /brokers/topics
rmr /brokers/topics/{topic_name}
start kafka
```
