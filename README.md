# **Data_Engineer_KAFKA**

This repository contains Kafka code to read weather data events and write it to RDBMS (MySql) and also Architeture of the same events till BI/Reporting tools.

The assignments aims to read weather.json events and publishes the same to kafka topic and kafka consumer will get the data and clean it up if there are any Null records and write it to RDBMS using Sink connector.

## **Installation & Configuration:**

**prerequisites:**

- Java 8
- Apache Kafka and ZooKeeper
- MySql DB setup

## How to run the application:

**Clone the Repo:**

> git clone https://github.com/Samarthhr5/data_challenge.git

To run application you need to have installed Kafka and Zookeeper If you are running it in Windows:

Run ZooKeeper first in cmd:

> .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

Run Kafka in different CMD window:

> .\bin\windows\kafka-server-start.bat .\config\server.properties

After the successfull setup of Kafka.

Now Run the producer and Consumer app in IDE (IntelliJ)

### Kafka Producer (weather-data-producer)

Kafka Prodcuer is sending Data events(weather.json) and creating Topics,partions,offset

> Run WeatherDataProducerApp.java

### Kafka Consumer (weather-data-consumer)

Kafka Consumer is fetching those data and with the help of Sink connector we are pushing Data to MySql DB

> Run consumer app - WeatherDataConsumerApp.java
