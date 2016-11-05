# kafkatwitterstorm

This is used to demonstrate that storm reads from a twitter Kafka topic and does a wordcount. 

The producer is here: https://github.com/naveen790/kafkatwitterproducer

Apache Kafka 0.8.2.1

Apache Storm 0.10.0

Zookeeper 3.4.6

Run:

Start Zookeeper

bin/zkServer.sh start

Start Kafka

bin/kafka-server-start.sh config/server.properties

Create Kafka Topic 

bin/kafka-topics.sh --create --topic twitterstreams --zookeeper localhost:2181 --partitions 1 --replication-factor 1

Start Storm:

bin/storm nimbus

bin/storm supervisor

Run the code

bin/storm jar /home/navin/projects/kafkastorm/target/kafkastorm-0.0.1-SNAPSHOT.jar com.kafka.storm.KafkaStormSample


