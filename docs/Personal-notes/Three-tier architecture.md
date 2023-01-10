---
title: Multi-tier Application

---

<h3 align="center">WIP</h3>


## AWS single tier, two-tier, and three-tier architecture

How AWS can be used to change the way you design multi-tier architectures and implement popular patterns such as microservices, mobile backends, and single-page applications. Architects and developers can use Amazon API Gateway, AWS Lambda, and other services to reduce the development and operations cycles required to create and manage multi-tiered applications.

The multi-tier application (three-tier, n-tier, and so forth.) has been a cornerstone architecture pattern for decades, and remains a popular pattern for user-facing applications. Although the language used to describe a multi-tier architecture varies, a multi-tier application generally consists of the following components:

* Presentation tier: Component that the user directly interacts with (for example, webpages and mobile app UIs).

* Logic tier: Code required to translate user actions to application functionality (for example, CRUD database operations and data processing).

* Data tier: Storage media (for example, databases, object stores, caches and file systems) that hold the data relevant to the application.

## Single-tier architecture

The configuration for this scenario includes a virtual private cloud (VPC) with a single public subnet, and an internet gateway to enable communication over the internet. We recommend this configuration if you need to run a single-tier, public-facing web application, such as a blog or a simple website.

![single-tier, public-facing web app](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/case-1_updated.png)

## Two-tier architecture

A two-tier architecture is a client-server architecture in which the user interface, application processing, and data management functions are physically separated. The two tiers are the presentation tier and the application tier. The presentation tier is the user interface, and the application tier is the application processing and data management functions. The two-tier architecture is the simplest of the three-tier architectures. It is also known as a single-tier architecture because it has only one layer: the server layer. The server layer is the user interface, application processing, and data management functions. 

Read more about [two-tier architecture](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/two-tier-architecture-overview.html)

## Three-tier architecture

The three-tier architecture is the most popular implementation of a multi-tier architecture and consists of a single presentation tier, logic tier, and data tier. The following illustration shows an example of a simple, generic three-tier application.

![Three-tier architecture](https://docs.aws.amazon.com/images/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/images/web-application.png)


[Three-tier architecture overview](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/three-tier-architecture-overview.html)


Resources:

[AWS Serverless Multi-Tier Architectures with Amazon API Gateway and AWS Lambda](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/welcome.html)