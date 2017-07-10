# streaming-examples
A collection of examples to explore Kafka and Flink
### Prerequisites
* For a dev environment install Kafka as described here: https://kafka.apache.org/quickstart
* Start all components from within the kafka folder and create a topic
```sh
$ ./bin/zookeeper-server-start.sh config/zookeeper.properties
$ ./bin/kafka-server-start.sh config/server.properties
$ kafka-topics.sh --zookeeper localhost:2181 --create --topic testtopic --partitions 2 --replication-factor 1
```
* Subscribe with a Kafka consumer and write with a producer
```sh
$ kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic testtopic
$ kafka-console-producer.sh --broker-list localhost:9092 --topic testtopic
```
