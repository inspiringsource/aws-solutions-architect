---
title: Amazon Kinesis
description: Easily collect, process, and analyze video and data streams
---

Amazon Kinesis is one of the best-managed services, which particularly scales elastically especially for real-time processing of the data at a massive point. These services can be used to collect the large streams of data records that are especially consumed by the application process that runs on Amazon EC2 instances.

Services include:
- Amazon Kinesis Video Streams
- Kinesis Data Streams allows consumers to READ streaming data. And it gives you a plenty of options to do so. It is best suitable for use cases that require custom processing, choice of stream processing frameworks, and sub-second processing latency. Data is reliably stored in streams up to 7 days and distributed across 3 Availability Zones.*
- Kinesis Firehose is used to LOAD streaming data to a target destination (S3, Elasticsearch, Splunk, etc). You can also transform streaming data (by using Lambda) before loading it to destination. Data from failed attempts will be saved to S3. [*source](https://stackoverflow.com/a/64154811/11464527)
- Amazon Kinesis Data Analytics
