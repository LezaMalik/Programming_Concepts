# Basic Hadoop Concepts

*Following are some of the important Hadoop concepts.*


### 1. What is CAP theory?
CAP theory, also known as the CAP theorem, is a fundamental concept in distributed computing and database systems. It was formulated by computer scientist Eric Brewer in 2000 and is often used to describe the trade-offs that exist in designing and operating distributed systems.

The CAP theorem states that in a distributed system, you can have at most two out of the following three guarantees simultaneously:

1. Consistency (C): All nodes in the system see the same data at the same time. In other words, every read operation will return the most recent write.

2. Availability (A): Every request made to the system receives a response, without guaranteeing that it contains the most recent version of the data. In other words, the system remains operational and responsive to client requests.

3. Partition Tolerance (P): The system continues to function even in the presence of network partitions or communication failures between nodes. In a distributed system, network partitions can occur when some nodes are unable to communicate with others.

The CAP theorem implies that when a network partition occurs (P), you have to choose between maintaining consistency (C) or availability (A). In other words :

* If you prioritize Consistency and want all nodes to have the most recent data, you may have to sacrifice Availability during network partitions.

* If you prioritize Availability and want the system to remain responsive even in the presence of network partitions, you may have to sacrifice Consistency, meaning that different nodes may temporarily see different versions of the data.

It's important to note that the CAP theorem doesn't mean that distributed systems can only have two of these properties at all times. Instead, it highlights the trade-offs that must be made in designing and operating distributed systems, particularly in scenarios where network partitions are a possibility.


![cap picture](./assets/cap.jpg)


The CAP theorem categorizes systems into three categories as shown in the image above: 

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

### 2. What is Hadoop?

Hadoop is an open-source framework for distributed storage and processing of large datasets. It was originally developed by Doug Cutting and Mike Cafarella and is now maintained by the Apache Software Foundation. Hadoop is designed to handle massive amounts of data and process it in a distributed and fault-tolerant manner. It has become a cornerstone technology for big data analytics and processing.

Key components of the Hadoop ecosystem include:

1. Hadoop Distributed File System (HDFS): HDFS is a distributed file system that stores data across multiple machines. It is designed to provide high-throughput access to data and to replicate data across nodes to ensure fault tolerance. HDFS is the storage layer of Hadoop.

2. MapReduce: MapReduce is a programming model and processing engine for distributed data processing. It allows developers to write programs that can process vast amounts of data in parallel across a Hadoop cluster. The MapReduce model consists of two main steps: a "Map" step for processing and filtering data and a "Reduce" step for aggregating and summarizing the results.

3. YARN (Yet Another Resource Negotiator): YARN is the resource management and job scheduling component of Hadoop. It enables multiple data processing frameworks, including MapReduce, to share and manage cluster resources efficiently. This flexibility allows Hadoop to support a variety of data processing workloads beyond MapReduce.

4. Hadoop Common: This includes libraries, utilities, and APIs that support the other components of the Hadoop ecosystem. It provides a set of common tools and utilities that are used by various Hadoop modules.

5. Hadoop Ecosystem Projects: Hadoop has a rich ecosystem of related projects and tools that extend its functionality. Some popular ones include Apache Hive (for SQL-like querying of data), Apache Pig (for data transformation and analysis), Apache HBase (a NoSQL database), Apache Spark (a fast, in-memory data processing engine), and Apache Kafka (a distributed messaging system), among many others.

Hadoop is known for its scalability, fault tolerance, and the ability to handle large volumes of data across clusters of commodity hardware. It has been widely adopted in industries such as finance, healthcare, retail, and more for tasks like log processing, data warehousing, and large-scale data analytics.


----------------------------------------------


### 3. Which Hadoop Distribution have you used?

----------------------------------------------

### 4. Which Hadoop version have you used?
----------------------------------------------


### 5. Have you created your own Hadoop cluster? and how?
----------------------------------------------

### 6. What are some Hadoop components?

Hadoop is a comprehensive ecosystem with various components and subprojects that work together to provide distributed storage and processing capabilities for big data. Here are some of the core components of the Hadoop ecosystem:

* Hadoop Distributed File System (HDFS): HDFS is the primary storage system in Hadoop. It is designed to store and manage large datasets by distributing them across a cluster of commodity hardware. HDFS ensures data reliability through data replication and fault tolerance.

* MapReduce: MapReduce is a programming model and processing framework for distributed data processing. It allows developers to write parallel processing jobs to analyze and manipulate data stored in HDFS. While MapReduce is one of the original components of Hadoop, other processing frameworks like Apache Spark have gained popularity for more advanced data processing tasks.

* YARN (Yet Another Resource Negotiator): YARN is the resource management and job scheduling component of Hadoop. It manages cluster resources and allows multiple data processing engines to coexist on the same Hadoop cluster. This flexibility enables the execution of various workloads, including MapReduce, Spark, and more.

* Hadoop Common: Hadoop Common includes libraries, utilities, and APIs that are used by other Hadoop components. It provides a common set of tools and resources for Hadoop ecosystem projects.

* Apache Hive: Hive is a data warehousing and SQL-like query language for Hadoop. It allows users to query and analyze data stored in HDFS using a familiar SQL syntax. Hive translates SQL queries into MapReduce or Tez jobs to perform data processing.

* Apache Pig: Pig is a high-level platform for creating data analysis programs. It provides a scripting language called Pig Latin, which abstracts the complexities of MapReduce programming. Pig is used for data transformation, ETL (Extract, Transform, Load) tasks, and data analysis.

* Apache HBase: HBase is a NoSQL, column-family database that runs on top of Hadoop. It provides real-time, random read/write access to large volumes of data and is suitable for use cases where low-latency data retrieval is essential.

* Apache Spark: While not originally part of the Hadoop ecosystem, Apache Spark has become an integral component for big data processing. It offers in-memory data processing, a rich set of libraries, and support for batch processing, stream processing, and machine learning. Spark can run on Hadoop YARN and HDFS or other storage systems.

* Apache Kafka: Kafka is a distributed messaging system used for real-time data streaming and event-driven architectures. It is often used in conjunction with Hadoop for ingesting and processing large volumes of data in real-time.

* Apache ZooKeeper: ZooKeeper is a distributed coordination service that helps manage and synchronize distributed applications. It is used for maintaining configuration information, providing distributed locks, and ensuring high availability of critical services in a Hadoop cluster.

* Ambari: Apache Ambari is a management and monitoring tool for Hadoop clusters. It simplifies cluster provisioning, configuration, and monitoring, making it easier to manage large Hadoop deployments.

These are just some of the core components of the Hadoop ecosystem. There are many other projects and tools within the Hadoop ecosystem, each designed to address specific needs and use cases in the world of big data processing and analytics. Organizations often choose and combine these components based on their requirements and data processing workflows.

----------------------------------------------

### 7. What's MapReduce?

----------------------------------------------

### 8. Compare mapper and reducer

----------------------------------------------

### 9. What does Mapreduce partitioner do?

----------------------------------------------

### 10. What's a combiner? Why?

----------------------------------------------

### 11. What is distcp?

----------------------------------------------

### 12. How distcp works?

----------------------------------------------

### 13. What's data locality

----------------------------------------------

### 14. What is metadata in hdfs?
----------------------------------------------

### 15. What is hive
----------------------------------------------

### 16. What is partition in hive
----------------------------------------------

### 17. What is heartbeat in hdfs
----------------------------------------------
