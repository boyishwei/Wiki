# Setup Kafka Server via Docker

1. Install docker image
		docker pull wurstmeister/zookeeper
		docker pull wurstmeister/kafka

2. Start docker  instance
		 docker run -d --name zookeeper --publish 2181:2181 --volume /d/docker/etc/localtime:/d/docker/etc/localtime zookeeper:latest
		 docker run -d --name kafka --publish 9092:9092 --link zookeeper --env KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 --env KAFKA_ADVERTISED_HOST_NAME=localhost --env KAFKA_ADVERTISED_PORT=9092 --volume /d/docker/etc/localtime:/d/docker/etc/localtime wurstmeister/kafka:latest

3. Find out Kafka container id (Not Zookeeper):
		 docker ps

4. Connection Kafka container via bash
		 winpty docker exec -it 045246fbee92 bash
> - If connect from git bash command line from windows 10, need to add **Winpty**
> - If connect from git bash command line from windows 10, need to use **bash** instead of **/bin/bash**

5. Create Kafka topic
		 bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic mykafka

6. Produce message
		 bin/kafka-console-producer.sh --broker-list localhost:9092 --topic mykafka

7. Consume message
		 bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic mykafka --from-beginning

**References:**

[docker 安装kafka(快速)](https://blog.csdn.net/zhang89xiao/article/details/76221180 "docker 安装kafka(快速)") Updated commands due to the runtime env is different.


All above commands are working on Windows 10/Git Bash Environment.
