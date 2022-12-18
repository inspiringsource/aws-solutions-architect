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

## Amazon SQS short and long polling

Amazon SQS provides short polling and long polling to receive messages from a queue. By default, queues use short polling.

With short polling, the ```ReceiveMessage``` request queries only a subset of the servers (based on a weighted random distribution) to find messages that are available to include in the response. Amazon SQS sends the response right away, even if the query found no messages.

With long polling, the ```ReceiveMessage``` request queries all of the servers for messages. Amazon SQS sends a response after it collects at least one available message, up to the maximum number of messages specified in the request. Amazon SQS sends an empty response only if the polling wait time expires. This is the inexpensive way to receive messages from a queue. Most use cases require long polling.

Read more about [Amazon SQS short and long polling](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html)