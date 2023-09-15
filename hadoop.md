# Basic Hadoop Concepts

*Following are some of the important Hadoop concepts.*


### 1. What is CAP theory?
CAP theory, also known as the CAP theorem, is a fundamental concept in distributed computing and database systems. It was formulated by computer scientist Eric Brewer in 2000 and is often used to describe the trade-offs that exist in designing and operating distributed systems.

The CAP theorem states that in a distributed system, you can have at most two out of the following three guarantees simultaneously:

1. Consistency (C): All nodes in the system see the same data at the same time. In other words, every read operation will return the most recent write.

2. Availability (A): Every request made to the system receives a response, without guaranteeing that it contains the most recent version of the data. In other words, the system remains operational and responsive to client requests.

3. Partition Tolerance (P): The system continues to function even in the presence of network partitions or communication failures between nodes. In a distributed system, network partitions can occur when some nodes are unable to communicate with others.

The CAP theorem implies that when a network partition occurs (P), you have to choose between maintaining consistency (C) or availability (A). In other words:

* If you prioritize Consistency and want all nodes to have the most recent data, you may have to sacrifice Availability during network partitions.

* If you prioritize Availability and want the system to remain responsive even in the presence of network partitions, you may have to sacrifice Consistency, meaning that different nodes may temporarily see different versions of the data.

It's important to note that the CAP theorem doesn't mean that distributed systems can only have two of these properties at all times. Instead, it highlights the trade-offs that must be made in designing and operating distributed systems, particularly in scenarios where network partitions are a possibility.


![cap picture](./assets/cap.jpg)


The CAP theorem categorizes systems into three categories:

1. CA (Consistency and Availability)
    * The system prioritizes availability over consistency and can respond with possibly stale data.

    * Example databases: Cassandra, CouchDB, Riak, Voldemort.

2. AP (Availability and Partition Tolerance)
    * The system prioritizes availability over consistency and can respond with possibly stale data.
    * The system can be distributed across multiple nodes and is designed to operate reliably even in the face of network partitions.
    
    * Example databases: Amazon DynamoDB, Google Cloud Spanner.

3. CP (Consistency and Partition Tolerance)
    * The system prioritizes consistency over availability and responds with the latest updated data.
    * The system can be distributed across multiple nodes and is designed to operate reliably even in the face of network partitions.
           
    * Example databases: Apache HBase, MongoDB, Redis


----------------------------------------------

### 2. What's Hadoop?
### 3. Which Hadoop Distribution have you used?
### 4. Which Hadoop version have you used?
### 5. Have you created your own Hadoop cluster? and how?
### 6. What are some Hadoop components?
### 7. What's MapReduce?
### 8. Compare mapper and reducer
### 9. What does Mapreduce partitioner do?
### 10. What's a combiner? Why?
### 11. What is distcp?
### 12. How distcp works?
### 13. What's data locality
### 14. What is metadata in hdfs?
### 15. What is hive
### 16. What is partition in hive
### 17. What is heartbeat in hdfs