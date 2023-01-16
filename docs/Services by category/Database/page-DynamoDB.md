---
title: Amazon DynamoDB
description: Fast, flexible NoSQL database service for single-digit millisecond performance at any scale
---

Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database, so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling.

DynamoDB Streams captures a time-ordered sequence of item-level modifications in any DynamoDB table, and stores this information in a log for up to 24 hours. This enables you to build applications that react to changes in your DynamoDB tables. [Read more here](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html)

DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement. DAX also provides seamless integration with DynamoDB, so you can build applications that are fast and scalable. 
### DAX is ideal for the following types of applications:

- Applications that require the fastest possible response time for reads. Some examples include real-time bidding, social gaming, and trading applications. DAX delivers fast, in-memory read performance for these use cases.

- Applications that read a small number of items more frequently than others. For example, consider an ecommerce system that has a one-day sale on a popular product. During the sale, demand for that product (and its data in DynamoDB) would sharply increase, compared to all of the other products. To mitigate the impacts of a "hot" key and a non-uniform traffic distribution, you could offload the read activity to a DAX cache until the one-day sale is over.

- Applications that are read-intensive, but are also cost-sensitive. With DynamoDB, you provision the number of reads per second that your application requires. If read activity increases, you can increase your tables' provisioned read throughput (at an additional cost). Or, you can offload the activity from your application to a DAX cluster, and reduce the number of read capacity units that you need to purchase otherwise.

- Applications that require repeated reads against a large set of data. Such an application could potentially divert database resources from other applications. For example, a long-running analysis of regional weather data could temporarily consume all the read capacity in a DynamoDB table. This situation would negatively impact other applications that need to access the same data. With DAX, the weather analysis could be performed against cached data instead. [Read more here](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.html)


## Use cases

### Amazon Kinesis Data Streams

Build a data lake using Amazon Kinesis Data Streams for Amazon DynamoDB and Apache Hudi to ingest, transform, and query data in Amazon S3. <a target="_self" href="https://aws.amazon.com/blogs/big-data/build-a-data-lake-using-amazon-kinesis-data-streams-for-amazon-dynamodb-and-apache-hudi/">Source</a>

You can use <a target="_self" href="https://www.aws-practical-handbook.link/docs/Services%20by%20category/Analytics/page-Kinesis">Kinesis Data Streams</a> for DynamoDB and take advantage of managed streaming delivery of DynamoDB data to other Kinesis Data Stream by simply enabling Kinesis streaming connection from Amazon DynamoDB console. To process DynamoDB events from Kinesis, you have multiple options: Amazon Kinesis Client Library (KCL) applications, Lambda, Kinesis Data Analytics for Apache Flink, and Kinesis Data Firehose. In this post, you use Kinesis Data Firehose to save the raw data in the S3 data lake and Apache Hudi to batch process the data.

<div>
<div align="center"><img src="https://d2908q01vomqb2.cloudfront.net/b6692ea5df920cad691c20319a6fffd7a4a766b8/2021/03/01/bdb1053-dta-lake-kds-ddb-hudi-1.jpg"/></div>
<div><p align="center">Diagram illustrates the order processing system architecture. <a href="https://aws.amazon.com/blogs/big-data/build-a-data-lake-using-amazon-kinesis-data-streams-for-amazon-dynamodb-and-apache-hudi/">View source</a></p></div>
</div>


[DynamoDB Streams and AWS Lambda triggers](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.Lambda.html)

## Good to know:

DynamoDB allows you to store JSON data within items.
DynamoDB is NoSQL and is good at storing millions of records of flat data with simple sorting.

[Managing indexes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SQLtoNoSQL.Indexes.html)

### Partition key design and distributing workloads

Using write sharding to distribute workloads evenly

One way to better distribute writes across a partition key space in Amazon DynamoDB is to expand the space. You can do this in several different ways. You can add a random number to the partition key values to distribute the items among partitions. Or you can use a number that is calculated based on something that you're querying on. Regardless of the method you use, the goal is to distribute the writes across the partition key space. Read more about [partition key design](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-partition-key-uniform-load.html).

### Best practices for partition keys

- Use a partition key that is highly distributed. A highly distributed partition key is one that has a large number of unique values. A highly distributed partition key is more likely to be evenly distributed across partitions than a partition key with a small number of unique values. A highly distributed partition key is also more likely to be evenly distributed across partitions than a partition key that is not distributed at all.

- Use a partition key that is evenly distributed. A partition key is evenly distributed if the number of items with the same partition key value is roughly the same for all partition key values. A partition key that is not evenly distributed is more likely to cause uneven distribution of items across partitions than a partition key that is evenly distributed.

- Use a partition key that is not too large. A partition key that is too large can cause performance issues. For example, a partition key that is too large can cause a partition to become too large. A partition that is too large can cause performance issues. For more information, see Partitioning and performance.

- Use a partition key that is not too small. A partition key that is too small can cause performance issues. For example, a partition key that is too small can cause a partition to become too small. A partition that is too small can cause performance issues. For more information, see Partitioning and performance.

- Use a partition key that is not too skewed. A partition key that is too skewed can cause performance issues. For example, a partition key that is too skewed can cause a partition to become too large. A partition that is too large can cause performance issues. For more information, see Partitioning and performance.

- Use a partition key that is not too random. A partition key that is too random can cause performance issues. For example, a partition key that is too random can cause a partition to become too small. A partition that is too small can cause performance issues. For more information, see Partitioning and performance.

## Good to know:

>DynamoDB Streams allows you to trigger a Lambda function when records are inserted into a table.