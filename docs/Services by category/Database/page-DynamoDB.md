---
title: Amazon DynamoDB
description: Lorem ipsum dolor sit amet - 2
---

Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database, so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling.


## Use cases

### Amazon Kinesis Data Streams

Build a data lake using Amazon Kinesis Data Streams for Amazon DynamoDB and Apache Hudi to ingest, transform, and query data in Amazon S3. <a target="_self" href="https://aws.amazon.com/blogs/big-data/build-a-data-lake-using-amazon-kinesis-data-streams-for-amazon-dynamodb-and-apache-hudi/">Source</a>

You can use <a target="_self" href="https://aws-notes-taking.netlify.app/docs/Services%20by%20category/Analytics/page-Kinesis">Kinesis Data Streams</a> for DynamoDB and take advantage of managed streaming delivery of DynamoDB data to other Kinesis Data Stream by simply enabling Kinesis streaming connection from Amazon DynamoDB console. To process DynamoDB events from Kinesis, you have multiple options: Amazon Kinesis Client Library (KCL) applications, Lambda, Kinesis Data Analytics for Apache Flink, and Kinesis Data Firehose. In this post, you use Kinesis Data Firehose to save the raw data in the S3 data lake and Apache Hudi to batch process the data.

<div>
<div align="center"><img src="https://d2908q01vomqb2.cloudfront.net/b6692ea5df920cad691c20319a6fffd7a4a766b8/2021/03/01/bdb1053-dta-lake-kds-ddb-hudi-1.jpg"/></div>
<div><p align="center">Diagram illustrates the order processing system architecture. <a href="https://aws.amazon.com/blogs/big-data/build-a-data-lake-using-amazon-kinesis-data-streams-for-amazon-dynamodb-and-apache-hudi/">View source</a></p></div>
</div>

## Good to know:

DynamoDB allows you to store JSON data within items.