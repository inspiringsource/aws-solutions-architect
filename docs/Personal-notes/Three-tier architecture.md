---
title: Multi-tier Application

---

<h3 align="center">WIP</h3>


## AWS single tier, two-tier, and three-tier architecture

How AWS can be used to change the way you design multi-tier architectures and implement popular patterns such as microservices, mobile backends, and single-page applications. Architects and developers can use Amazon API Gateway, AWS Lambda, and other services to reduce the development and operations cycles required to create and manage multi-tiered applications.

The multi-tier application (three-tier, n-tier, and so forth.) has been a cornerstone architecture pattern for decades, and remains a popular pattern for user-facing applications. Although the language used to describe a multi-tier architecture varies, a multi-tier application generally consists of the following components:

* Presentation tier (front-end layer): Component that the user directly interacts with (for example, webpages and mobile app UIs).

* Logic tier (middleware layer): Code required to translate user actions to application functionality (for example, CRUD database operations and data processing).

* Data tier (back-end layer): Storage media (for example, databases, object stores, caches and file systems) that hold the data relevant to the application.

![Overview of a three-tier application.](https://en.wikipedia.org/wiki/Multitier_architecture#/media/File:Overview_of_a_three-tier_application_vectorVersion.svg)
Source: [Wikipedia](https://en.wikipedia.org/wiki/Multitier_architecture)
## Single-tier architecture

A single-tier architecture is the simplest type of architecture, where all components of the application are deployed on a single layer. Typically, this means that all application components, such as the web server, application server, and database, run on the same set of servers. This type of architecture is most commonly used for small, simple applications that don't require a lot of scalability or fault tolerance.

The configuration for this scenario includes a virtual private cloud (VPC) with a single public subnet, and an internet gateway to enable communication over the internet. We recommend this configuration if you need to run a single-tier, public-facing web application, such as a blog or a simple website.

![single-tier, public-facing web app](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/case-1_updated.png)

## Two-tier architecture

A two-tier architecture is more complex than a single-tier architecture, and typically involves separating the application into two layers: a front-end layer and a back-end layer. The front-end layer is responsible for handling user requests and serving web pages, while the back-end layer handles the business logic and data storage. The two layers are typically separated by a load balancer, which distributes incoming requests among the front-end servers. This type of architecture is commonly used for medium-sized applications that require some level of scalability and fault tolerance.

Read more about [two-tier architecture](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/two-tier-architecture-overview.html)

## Three-tier architecture

A three-tier architecture is the most complex type of architecture, and typically involves separating the application into three layers: a front-end layer, a middleware layer, and a back-end layer. The front-end layer handles user requests and serves web pages, while the middleware layer handles the business logic and application services. The back-end layer handles data storage and retrieval. The three layers are typically separated by load balancers, which distribute incoming requests among the front-end servers and middleware servers. This type of architecture is most commonly used for large, complex applications that require a high level of scalability, fault tolerance, and performance.

AWS offers a wide range of services that can be used to implement each of these architectural patterns, including Amazon S3, Amazon EC2, Amazon RDS, and Amazon Elastic Load Balancing. AWS also offers a number of higher-level services that can simplify the process of building and deploying applications on AWS, such as AWS Elastic Beanstalk and AWS Lambda.

It's important to note that the architectural pattern you choose will depend on the specific needs and requirements of your application. Some projects are more suited for a single-tier, other can greatly benefit from a three-tier and different solutions are better suited for different use-cases.

![Three-tier architecture](https://docs.aws.amazon.com/images/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/images/web-application.png)


[Three-tier architecture overview](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/three-tier-architecture-overview.html)


## Further readings:

[AWS Serverless Multi-Tier Architectures with Amazon API Gateway and AWS Lambda](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/welcome.html)

[Multi-tier architecture](https://en.wikipedia.org/wiki/Multitier_architecture)
