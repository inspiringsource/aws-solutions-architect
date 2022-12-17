---
title: Amazon Kinesis
description: Easily collect, process, and analyze video and data streams
---

<h3 align="center">
  "Serverless service for <u>real-time</u> processing of <u>streaming</u> data at massive scale"
</h3>

Amazon Kinesis is one of the best-managed services, which particularly scales elastically especially for real-time processing of the data at a massive point. These services can be used to collect the large streams of data records that are especially consumed by the application process that runs on Amazon EC2 instances.

Services include:
<table>
  <tr>
    <td><img width="700" src={require('@site/static/img/kinesis-video-streams.png').default} /></td>
    <td>Amazon Kinesis Video Streams is a fully managed service that stream video from connected devices to AWS for analytics, machine learning (ML), and other processing.</td>

  </tr>
  <tr>
    <td><img width="700" src={require('@site/static/img/kinesis-data-stream.png').default} /></td>
    <td>Kinesis Data Streams allows consumers to <b>READ</b> streaming data. And it gives you a plenty of options to do so. It is best suitable for use cases that require custom processing, choice of stream processing frameworks, and sub-second processing latency. Data is reliably stored in streams up to 7 days and distributed across 3 Availability Zones.</td>
  </tr>
    <tr>
    <td><img width="700" src={require('@site/static/img/kinesis-data-firehose.png').default} /></td>
    <td>Kinesis Firehose is used to <b>LOAD</b> streaming data to a target destination (S3, Elasticsearch, Splunk, etc). You can also transform streaming data (by using Lambda) before loading it to destination. Data from failed attempts will be saved to S3. <a href="https://stackoverflow.com/a/64154811/11464527">Source</a></td>
  </tr>
    <tr>
    <td><img width="700" src={require('@site/static/img/kinesis-data-analytics.png').default} /></td>
    <td>Amazon Kinesis Data Analytics is used to <b>ANALYZE</b> streaming data. It is best suitable for use cases that require real-time analytics and dashboards. It supports SQL and Java/Scala for processing streaming data. It also supports Apache Flink for processing streaming data. It is best suitable for use cases that require custom processing, choice of stream processing frameworks, and sub-second processing latency. Data is reliably stored in streams up to 7 days and distributed across 3 Availability Zones.</td>
  </tr>
</table>

## Use cases:

Business Intelligent System with Lambda Architecture such that consists of real-time data processing and batch data processing layers.

<div>
<div align="center"><img src="https://static.us-east-1.prod.workshops.aws/public/418ebbf4-ce79-4cc1-8038-7d66be4823c3/static/images/aws-analytics-system-arch.png" /></div>
<div><p align="center">Amazon Kinesis Data Streams and Kinesis Data Firehose are used for data collection.</p></div>
</div>

Amazon S3 is for data storage. AWS Lambda, Amazon Athena, and Amazon Elasticsearch Service are for data analysis and processing. Amazon QuickSight and Kibana are for Visualization.

[Link to lab](https://catalog.us-east-1.prod.workshops.aws/workshops/a861fb26-12b0-4669-b3c3-ae1def49735d/en-US/introduction)