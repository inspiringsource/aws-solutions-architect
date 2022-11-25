---
title: Amazon SNS
description: Lorem ipsum dolor sit amet - 2
---

Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. With Amazon SNS, you can send individual messages as well as to fan-out messages to large numbers of recipients. Amazon SNS makes it simple and cost-effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.

Amazon Simple Notification Service (Amazon SNS) is a web service that coordinates and manages the delivery or sending of messages to subscribing endpoints or clients.

In Amazon SNS, there are two types of clients—publishers and subscribers—also referred to as producers and consumers.

<div>
<div align="center"><img src="https://docs.aws.amazon.com/images/sdk-for-javascript/v2/developer-guide/images/code-samples-sns.png"/></div>
<div><p align="center">AWS SDK used to publish an event to an SNS Topic.</p></div>
</div>

Publishers communicate asynchronously with subscribers by producing and sending a message to a topic, which is a logical access point and communication channel. Subscribers (web servers, email addresses, Amazon SQS queues, Lambda functions) consume or receive the message or notification over one of the supported protocols (Amazon SQS, HTTP/S, email, SMS, AWS Lambda) when they are subscribed to the topic.

[Managing Topics in Amazon SNS](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/sns-examples-managing-topics.html)