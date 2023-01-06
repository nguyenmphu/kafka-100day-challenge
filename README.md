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
#### Topic
#### Partition
Q: We need a way of deciding which messages to write to which partition?

A: If messages has no key, they are written to the partitions by round - robin. If message has key then `hash(key) % number_of_partitions` will find the partition which the message is written in.
#### Broker
> An computer, instance, or container running the Kafka process.
- Manager partitions
- Handle read/write requests
- Manage replicas of partitions
#### Producer
#### Consumer
## Part 02: Languages and CLIs
## Part 03: Schemas
## Part 04: Stream Processing with Kafka Streams
## Part 05: Stream Processing with ksqlDB
## Part 06: Microservices
## Part 07: Data pipelines
## Part 08: Event Sourcing
## Part 09: Performance and Observability
## Part 10: Cloud Operations
