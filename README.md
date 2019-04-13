# Apache-Kafka

Data rapidly, scalably, reliably(fault-tolerant). 

Apache Kafka is a high-throughput distributed (pub-sub) messaging system. It provides Messaging Infrastructure. 

Clients - LinkedIn, Netflix, Uber, AirBnb

Technology toolbox 
Database replication (Limited to RDMS to RDBMS only, db specific, tight coupling)
Log shipping (performance, cumbersome)
Extract, Transform and Load(ETL) (Proprietary and costly, custom development, scalability, performance, required multiple instances)
Messaging  (Scalability, smaller messages, requires rapid consumption, not fault-tolerant, High volume is problematic, local storage, message build up)
Custom Middleware magic(Extremely complex, consistency concerns, potentially expensive)

Multi-write pattern?
Message-broker pattern?

A better way to move data around cleanly, reliably, quickly and autonomously.

High Volume
High Velocity
High Variety

# Messaging Goals 
High throughput
Horizontally scalable
Reliable and durable
Loosely coupled producers and consumers.
Flexible publish-subscribe semantics
# Why Apache Kafka

1. High Throughput
2. Horizontally Scalable
Reliable and Durable
Loosely Coupled Consumers and Producers
Flexible Publish-Subscribe semantics

# Apache Kafka as a messaging system

Producers
Broker, Topics
Consumers

# Apache Kafka Cluster
A group of Kafka brokers.

# Apache Zookeeper

# Distributed Systems
Consistes of multiple workers or nodes(kafka brokers). 

Controller

1. Attendance
2. Work Items
3. Status

Worker availability and health
Task redundancy.

Worker becomes leader(for redundancy for task), peers become follower. Quorum. 


