---
title: Amazon Elasticsearch
description: Securely unlock real-time search, monitoring, and analysis of business and operational data
---
<b>Amazon OpenSearch Service (Amazon Elasticsearch Service)</b>

Amazon Elasticsearch Service is a managed service that makes it easy to deploy, operate, and scale Elasticsearch in the AWS Cloud. Elasticsearch is a popular open-source search and analytics engine for use cases such as log analytics, real-time application monitoring, and click stream analytics.

OpenSearch is a fully open-source search and analytics engine for use cases such as log analytics, real-time application monitoring, and clickstream analysis. OpenSearch is a fork of Elasticsearch and Kibana, and is 100% compatible with Elasticsearch and Kibana plugins. OpenSearch is developed by the same team that created Elasticsearch and Kibana.

Amazon OpenSearch Service provisions all the resources for your OpenSearch cluster and launches it. It also automatically detects and replaces failed OpenSearch Service nodes, reducing the overhead associated with self-managed infrastructures. You can scale your cluster with a single API call or a few clicks in the console.

Read more about [Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html).

## How does Elasticsearch work?

You can send data in the form of JSON documents to Elasticsearch using the API or ingestion tools such as Logstash and Amazon Kinesis Firehose. Elasticsearch automatically stores the original document and adds a searchable reference to the document in the cluster’s index. You can then search and retrieve the document using the Elasticsearch API. You can also use Kibana, a visualization tool, with Elasticsearch to visualize your data and build interactive dashboards.
Source: [Amazon Elasticsearch](https://aws.amazon.com/opensearch-service/the-elk-stack/what-is-elasticsearch/).