# PHP_Apache_Kafka_demo_app
Sample app with PHP and Apache Kafka

### How To Run App on Windows OS

1) Go to Apache Kafka and [download](https://kafka.apache.org/downloads) latest release

2) Extract downloaded archive in any preferred location

3) Kafka uses ZooKeeper, run following command from derictory where downloaded file were extracted.
```
./bin/windows/zookeeper-server-start.bat ./config/zookeeper.properties
```

4) Start Kafka server in saparate console
```
./bin/windows/kafka-server-start.bat ./config/server.properties
```
5) Create **test* topic for Kafka server
```
./bin/windows/kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
```

6) Start consumer by running following command
```
php Server.php
```

7) Now possible to send messages to consymer in **Synch** and **Async** modes
```
php Producer.php
php ProducerSync.php
```
