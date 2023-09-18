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

### 7. What is MapReduce?

MapReduce is a programming model and processing framework that was popularized by Google for processing and generating large datasets that can be distributed across a cluster of computers. It is designed to process vast amounts of data in parallel across a distributed computing infrastructure efficiently. 

MapReduce consists of two main phases: the Map phase and the Reduce phase.

* Map Phase: During the Map phase, the input data is divided into smaller chunks, and each chunk is processed independently by a set of worker nodes. Each worker node applies a user-defined function called the "mapper" to this data, generating a set of key-value pairs as intermediate outputs. This phase is responsible for breaking down the problem into smaller tasks and extracting relevant information.

* Shuffle and Sort: After the Map phase, the intermediate key-value pairs are sorted and grouped based on their keys. This step ensures that all values associated with a particular key are brought together and ready for the next phase.

* Reduce Phase: In the Reduce phase, another user-defined function called the "reducer" is applied to each group of intermediate key-value pairs. The reducer combines, aggregates, or analyzes the data based on the keys to produce the final output. This phase is responsible for summarizing and processing the data generated in the Map phase.

MapReduce is particularly well-suited for distributed data processing tasks because it can scale horizontally, allowing it to handle massive datasets by adding more processing nodes to the cluster. It also provides fault tolerance by replicating data across nodes, ensuring that even if a node fails, the data and processing can continue on other nodes.

Hadoop, an open-source framework, has popularized the MapReduce model and made it widely accessible for processing large-scale data in distributed computing environments. While the original MapReduce implementation focused on batch processing, various other frameworks and tools have been developed to address real-time and interactive data processing needs, making it a fundamental concept in the world of big data.

----------------------------------------------

### 8. Compare mapper and reducer

Mappers and reducers are two essential components in the MapReduce programming model and framework, used for distributed data processing. They have distinct roles and responsibilities within the MapReduce process. Here's a comparison of mappers and reducers:

1. **Mappers:**

    * Input Data Processing: Mappers are responsible for processing input data. They take in chunks of data from the input dataset and apply a user-defined function to each record within the chunk. This function transforms the input data into a set of intermediate key-value pairs.

    * Parallel Execution: Mappers operate in parallel. Each chunk of data can be processed independently by a separate mapper task running on different nodes in the cluster. This parallelism is a key feature of MapReduce, enabling efficient processing of large datasets.

    * Key-Value Pair Generation: Mappers produce intermediate key-value pairs. The keys are typically used for sorting and grouping in the shuffle and sort phase, while the values carry relevant data.

    * Data Distribution: Mappers are responsible for dividing the input data into smaller manageable pieces, distributing the processing load across multiple nodes. They help break down the problem into smaller tasks.

    * Filtering and Transformation: Mappers can perform filtering and data transformation tasks. They are responsible for extracting relevant information from the input data.

    * Example: In a word count application, mappers would take in a chunk of text and emit key-value pairs with words as keys and counts as values.

2. **Reducers:**

    * Intermediate Data Processing: Reducers receive the output of mappers, which consists of grouped and sorted intermediate key-value pairs. Their primary role is to process this data and generate the final output.

    * Aggregation and Analysis: Reducers perform aggregation, analysis, or any user-defined processing tasks on the data. They typically operate on a subset of the intermediate data for a specific key, which means they have access to all values associated with that key.

    * Sequential Execution: Reducers operate sequentially, one reducer per key-group. They are responsible for combining and summarizing the data for each key.

    * Output Generation: Reducers generate the final output, which is often the result of combining and processing the values associated with a specific key.

    * Example: In a word count application, reducers would receive the intermediate key-value pairs for each word and sum up the counts to produce the final count for that word.

In summary, mappers handle the initial processing of input data, breaking it down into key-value pairs, and operate in parallel to distribute the workload. Reducers take the intermediate data generated by mappers, perform further processing and aggregation, and produce the final output. Both mappers and reducers are essential components of the MapReduce framework and work together to enable distributed and scalable data processing.

----------------------------------------------

### 9. What does Mapreduce partitioner do?

In the MapReduce framework, a partitioner is a component responsible for determining which reducer will receive the intermediate key-value pairs produced by the mappers. It plays a crucial role in the distribution of data to reducer tasks, ensuring that related data is sent to the same reducer. The primary purpose of a partitioner is load balancing and optimizing the performance of the MapReduce job.

Here's how the MapReduce partitioner works:

* Mapping Phase: During the mapping phase of a MapReduce job, mappers generate intermediate key-value pairs. Each key is associated with a specific value or set of values.

* Shuffle and Sort Phase: After the mapping phase, the intermediate key-value pairs are sorted and grouped by their keys. This step is essential to bring together all values associated with a particular key.

* Partitioning: The partitioner takes the sorted and grouped key-value pairs and decides which reducer should receive each key. It uses a hashing or custom logic based on the key to make this determination. The goal is to evenly distribute the data across the reducer tasks to ensure that they have a similar amount of work to do.

* Reducer Assignment: Once the partitioner has assigned keys to reducers, the MapReduce framework sends the key-value pairs to their respective reducers for further processing. Each reducer is responsible for processing a subset of the data associated with specific keys.

* Parallel Processing: Reducers work in parallel, independently processing the data assigned to them. This parallelism is a key feature of MapReduce, as it allows for efficient processing of large datasets across multiple nodes in a distributed computing cluster.

The choice of a good partitioner function is essential for optimizing the performance of a MapReduce job. A well-designed partitioner ensures that the workload is evenly distributed among reducers, preventing data skew and reducing the chances of some reducers becoming bottlenecks.

By distributing the data effectively to reducers, the partitioner helps achieve load balancing, reduces data transfer overhead, and ensures efficient resource utilization in a MapReduce cluster. Different partitioning strategies can be employed based on the specific characteristics of the data and the use case to improve the overall performance of the MapReduce job.

----------------------------------------------

### 10. What's a combiner? Why?

A combiner, in the context of MapReduce and distributed data processing, is a function or mini-reducer that operates on the output of the mapper phase before the data is sent over the network to the reducer tasks. The primary purpose of a combiner is to perform local aggregation and reduction of data in order to minimize data transfer and improve the efficiency of a MapReduce job.

Here's why combiners are used and their key benefits:

* Reduction of Data Transfer: Combiners reduce the amount of data that needs to be transferred over the network from the mappers to the reducers. By aggregating and summarizing data locally on each mapper node, a combiner can significantly reduce the volume of intermediate key-value pairs that need to be transmitted. This reduces network congestion and speeds up data processing, especially in scenarios with limited bandwidth.

* Improved Performance: Combiners can lead to faster job execution because they reduce the amount of data that the reducer phase needs to process. Smaller data volumes are processed more efficiently, leading to quicker job completion times. This is especially beneficial in large-scale data processing tasks where data transfer can become a bottleneck.

* Lower Resource Usage: With combiners, the reducer tasks receive smaller input datasets, which results in reduced memory and processing requirements for reducers. This can lead to improved overall cluster resource utilization, allowing for more parallelism and accommodating larger MapReduce jobs on the same cluster.

* Reduced Disk I/O: Combiners can help minimize disk I/O, as they reduce the amount of intermediate data that is written to disk by the mappers and read by the reducers. This is beneficial for both local disk I/O and network I/O.

* Custom Aggregation: Combiners allow for custom aggregation and reduction logic tailored to the specific requirements of the MapReduce job. This means you can apply specific business logic to locally aggregate data on each mapper node.

It's important to note that while combiners can improve the efficiency and performance of a MapReduce job, they are not always applicable. They are most effective when the reduce operation is both commutative and associative (meaning the order of input data does not affect the result), as the output of the combiner may not be the same as the output of the reducer in all cases. Additionally, the use of combiners should not change the final result of the MapReduce job; they should only optimize the intermediate data transfer and processing.

----------------------------------------------

### 11. What is distcp?
distcp, short for Distributed Copy, is a command-line tool in the Hadoop ecosystem that is used for efficiently copying large volumes of data between Hadoop Distributed File System (HDFS) clusters or from HDFS to other file systems, such as local file systems or remote file systems. It's a valuable utility for tasks involving data migration, backup, replication, or synchronization within a Hadoop environment.

Here are some key features and use cases of distcp:

* Parallel Data Transfer: distcp is designed to perform parallel data transfers, which means it can copy data in parallel across multiple nodes or clusters, making it faster and more efficient for large-scale data copying.

* Preservation of File Attributes: distcp can preserve various file attributes, including permissions, timestamps, and ownership, during the copying process. This ensures that the copied data retains its original characteristics.

* Atomic Copy: distcp aims to provide an atomic copy operation, which means that if the copying process fails for any reason, it should not leave partially copied or inconsistent data in the destination. Either the copy operation succeeds in full, or it fails without affecting the existing data.

* Support for Different File Systems: While distcp is commonly used for copying data within HDFS clusters, it can also copy data to and from other file systems, such as Amazon S3, Azure Data Lake Storage, and Google Cloud Storage, using their respective connectors.

* Efficient Copying: distcp optimizes data copying by minimizing network traffic. It achieves this by only copying the differences (delta) between the source and destination files. This is particularly useful for incremental backups and data synchronization.

* Cross-Cluster Data Migration: It's often used when you need to move data from one Hadoop cluster to another, which could be located in a different geographical region or managed by a different organization.

* Data Replication: distcp can be used to replicate data across multiple HDFS clusters, enhancing data availability and fault tolerance.

Here's a basic example of using distcp to copy data from one HDFS location to another:

```
hadoop distcp hdfs://source-cluster/source-path hdfs://destination-cluster/destination-path
```

In this command, source-cluster and destination-cluster are the HDFS cluster URIs, and source-path and destination-path are the source and destination directories, respectively.

distcp is a versatile and powerful tool in the Hadoop ecosystem, allowing data engineers and administrators to efficiently manage and transfer large datasets across distributed environments.


----------------------------------------------

### 12. How distcp works?

distcp (Distributed Copy) in Hadoop is a tool used for efficiently copying large volumes of data between Hadoop Distributed File System (HDFS) clusters or within the same cluster. It operates in a parallel and distributed manner, which makes it suitable for handling big data scenarios. 

Here's an overview of how distcp works:

1. Distributed Execution: distcp leverages the distributed nature of Hadoop by running multiple map tasks in parallel. Each map task is responsible for copying a portion of the data.

2. Input and Output Paths: You specify the source and destination paths when you run distcp. These paths can point to directories, files, or even subsets of files within directories.

3. Path Expansion: distcp recursively expands the source path to include all the files and directories within it. It then creates a list of files and directories to be copied.

4. Mapping Phase: distcp starts the mapping phase, where it assigns each file or directory in the list to a separate map task. Each map task is responsible for copying a specific file or directory.

5. Copying Data: The map tasks copy data from the source to the destination. They do this by reading data from the source file or directory and writing it to the destination location. Data is transferred block by block, which allows parallelism and efficient data transfer.

6. Parallel Execution: Multiple map tasks run simultaneously, copying data in parallel. This parallelism speeds up the copying process significantly, especially when dealing with large datasets.

7. Preserving Metadata: distcp ensures that the metadata of the copied files and directories (e.g., permissions, timestamps, ownership) are preserved as closely as possible to the source.

8. Atomicity: distcp aims for an atomic copy operation, which means that if any map task fails during the copy operation, it will not leave the destination in an inconsistent state. The copying process either succeeds in full or fails without affecting the destination.

9. Reporting Progress: distcp provides progress reporting so that you can monitor the status of the copying operation. It shows the number of files and data blocks copied, the percentage of completion, and any errors encountered.

10. Completion and Cleanup: Once all map tasks have completed their copying tasks, distcp finishes the job. It ensures that all data is successfully copied to the destination.

11. Verification: After the copying process, distcp can perform an optional verification step to ensure that the data in the source and destination matches. This is particularly useful for data integrity checks.

In summary, distcp works by parallelizing the copy operation across multiple map tasks, ensuring efficient and reliable data transfer while preserving metadata and maintaining atomicity. It is a valuable tool for moving or replicating data within and between HDFS clusters, facilitating data migration, backup, and synchronization tasks in distributed computing environments.

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
