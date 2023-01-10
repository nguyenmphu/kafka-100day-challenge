# 100 Days of Code with Apache Kafka
This is repo that stores my notes & code demo of 100-day challenge with Apache Kafka.

The detail: https://developer.confluent.io/100-days-of-code/

## Part 01: Introduction
### Day 001: Quick start
- Set up local Kafka environment: use [docker-compose](./docker-compose.yml)
- Basic Kafka CLI:
    + Start Kafka broker
    + Topic: create/delete
    + Message: read/write
    + Stop Kafka broker
### Day 002-007: Basic concepts
#### Event
> An event is any type of action, incident, or change that's identified or recorded by software or applications. For example, a payment, a website click, or a temperature reading, along with a description of what happened.

Kafka is based on the abstraction of a distributed commit log.

Kafka models events as key/value pairs (keys & values are sequences of bytes).
#### Topic
Topic is the foundamental unit of Kafka organization, like a table in a relational database. A topic is a log of events.
- Append only
- Be read by seeking the offset
- Immutable
- Expire data (config by retention)
#### Partition
Q: We need a way of deciding which messages to write to which partition?

A: If messages has no key, they are written to the partitions by round - robin. If message has key then `hash(key) % number_of_partitions` will find the partition which the message is written in.
#### Broker
> An computer, instance, or container running the Kafka process.
- Manager partitions
- Handle read/write requests
- Manage replicas of partitions
#### Producer
Classes:
- `KafkaProducer`
- `ProducerRecord`
#### Consumer
Classes:
- `KafkaConsumer`
- `ConsumerRecord`
### DAy 008 Kafka connect
> Kafka Connect is a component of Apache Kafka that's used to perform streaming intergration between Kafka and other system such as databases, cloud services, search indexes, file systems, and key-value stores.

Kafka Hub: https://www.confluent.io/hub

Some use cases:
- Writing to datastores for Kafka
- Make systems real time
- Change data capture (e.g Debezium)

## Part 02: Languages and CLIs
## Part 03: Schemas
## Part 04: Stream Processing with Kafka Streams
## Part 05: Stream Processing with ksqlDB
## Part 06: Microservices
## Part 07: Data pipelines
## Part 08: Event Sourcing
## Part 09: Performance and Observability
## Part 10: Cloud Operations
