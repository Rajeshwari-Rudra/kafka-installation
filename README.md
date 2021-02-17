# kafka-installation
Steps to install Apache Kafka

## Commands to install Apache Kafka
- Start these commands by running in C Drive

- Here is how zookeeper starts:-
```Powershell
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
- Note:- Leave this window open or minimize it.
----------------------------------------
* Now open a new window and run Powershell as Administrator

- Here is how the Kaftka starts:-
```Powershell
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
- Leave this window open or minimize it.
---------------------------------------------------------------
* Now open a new window and run Powershell as Administrator
- This command creates a topic and list out the new and old topics which we have created:-
```Powershell
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic published-messages
```
```Powershell
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
-------------------------------------------------
* Now open a new window and run Powershell as Administrator
- To start sending messages either on cloud or on local, run the command as follows:-
```Powershell
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic published-messages
```

-------------------------------------------------
* Now open a new window and run Powershell as Administrator
- To see all the messages which are published then,run the below command:
```Powershell
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic published-messages --from-beginning
```

## Resources
- [Apache Kafka](https://kafka.apache.org/quickstart)
- [To downoad Kafka on your machine](https://www.apache.org/dyn/closer.cgi?path=/kafka/2.7.0/kafka_2.13-2.7.0.tgz)
