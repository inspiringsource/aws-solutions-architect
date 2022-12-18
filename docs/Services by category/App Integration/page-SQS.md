---
title: Amazon SQS
description: Fully managed message queuing for microservices, distributed systems, and serverless applications
---

Amazon Simple Queue Service (Amazon SQS) is a fully managed message queuing service that makes it easy to decouple and scale microservices, distributed systems, and serverless applications. Amazon SQS moves data between distributed application components and helps you decouple these components.

## Amazon SQS queue types

Amazon SQS offers two types of message queues: standard queues and FIFO queues. Standard queues offer best-effort ordering, at-least-once delivery, and unlimited throughput. FIFO queues provide limited throughput, but they guarantee that messages are delivered in the order in which they are sent and exactly once.

- SQS Standard allows for a nearly unlimited amount of messages per second. There is no requirement that the requests be in order so SQS Standard is suitable

- SQS First-in-First-Out without batching has a hard limit of 300 messages per second.

[Amazon SQS queue types](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-queue-types.html)
