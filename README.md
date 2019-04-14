# Apache-Kafka

Apache Kafka is a high-throughput distributed messaging system. It provides pub-sub messaging infrastructure. 

#### Technology toolbox 
  Database replication
  Log shipping
  Extract, Transform and Load(ETL)
  Messaging
  Custom Middleware

#### Limitations of existing tools in the technology toolbox. 
  Database replication is limited to RDMS to RDBMS, specific to DB, tight coupling
  Log shipping has performance limitations and is cumbersome. 
  ETL is proprietary and costly, needs custom development, not scalable easily, not highly performant, requires multiple instances.
  Messaging systems are not easily scalable, handle smaller messages, requires rapid consumption, not fault-tolerant, High volume is problematic, local storage, message build up etc.
  Custom middleware is extremely complex, consistency concerns, potentially expensive
  
Multi-write pattern?
Message-broker pattern?

A better way to move data around cleanly, reliably, quickly and autonomously.

High Volume
High Velocity
High Variety

#### Messaging Goals 
High throughput
Horizontally scalable
Reliable and durable
Loosely coupled producers and consumers.
Flexible publish-subscribe semantics
#### Why Apache Kafka

1. High Throughput
2. Horizontally Scalable
3. Reliable and Durable
4. Loosely Coupled Consumers and Producers
5. Flexible Publish-Subscribe semantics

#### Apache Kafka as a messaging system

  Producers
  Cluster, Broker, Topics
  Consumers

#### Apache Kafka Cluster
A group of Kafka brokers.

#### Apache Zookeeper
Centralized service for maintaining metadata about a cluster of distributed nodes.
Distributed system consisting of multiple nodes is called an "ensemble"


#### Characteristic of Distributed Systems
  Consists of multiple workers or nodes that has roles(Controllers, Leaders, Followers, Peers). 
  Provides reliability through replication.
  Consensus or Gossip  based communication.
  
Duties of Controller

1. Attendance
2. Work Items
3. Status

Worker availability and health
Task redundancy.

Worker becomes leader(for redundancy for task), peers become follower. One peers have committed to a leader a Quorum is formed. 
Risk policy to protect against loss is called Replication factor. 

#### Consensus or Gossip protocol
In addition to the message payload, all workers have to communicate with Peers to keep functioning. 
Worker node membership and naming
Configuration management
Leader election
Health status

#### Kafka Topics
Named feed or category of messages. Its a Logical entity. Physically represented as a log. Topics can span an entire cluster for the benefit of scalability and fault tolerance. Messages are appended to time ordered sequential stream. 
Maintaining data as events is called Event Sourcing. 

#### Message Content
Timestamp
Referenceable identifier
Payload(binary)

#### Message Offset
A placeholder for last read message position. Maintained by Consumer. Corresponds to the message identifier.

#### Message Retention Policy
It is configuratable in hours. By default it is 168 hours or 7 days. Can be set on a per topic basis. 

# Commands
#### Start Zookeeper
Change Directory to Kafka installation bin directory and enter below command 
````
./zookeeper-server-start.sh ../config/zookeeper.properties
````
To test if zookeeper installation was successful
````
telnet localhost 2181
````
````
stat
````
#### Start Kafka Broker
```
./zookeeper-server-start.sh ../config/server.properties
```
