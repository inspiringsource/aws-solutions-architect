---
title: AWS Elastic Beanstalk
description: Deploy and scale web applications
---

Amazon Web Services (AWS) provides two different options for creating a Network Address Translation (NAT) gateway: NAT instances and NAT gateways. Both options allow you to access the internet from instances in a private subnet, but there are important differences between the two that you should be aware of.

A NAT instance is a Linux EC2 instance that you configure to forward traffic from your private subnet to the internet. NAT instances provide a simple way to enable internet access for instances in a private subnet, but they come with some limitations and challenges. For example, NAT instances must be managed as EC2 instances, which means you have to perform tasks such as patching the operating system and handling the potential failure of the instance. Additionally, NAT instances can become a bottleneck if you have a large amount of traffic to the internet, as they have limited network bandwidth.

A NAT gateway, on the other hand, is a managed service that makes it easier to provide internet access to instances in a private subnet. NAT gateways are highly available, highly scalable, and automatically update their software. They can also handle a large amount of traffic, making them a good choice for applications with significant internet-bound traffic. NAT gateways are more expensive than NAT instances, but they simplify the process of providing internet access and relieve you of the operational overhead associated with managing NAT instances.
## Summary

If you need a simple and low-cost option for providing internet access to instances in a private subnet, you may consider using a NAT instance. However, if you have a high-traffic application or if you prefer a managed service that is highly available and scalable, you should consider using a NAT gateway.

## Source code deployment

Elastic Beanstalk supports the deployment of web applications from source code stored in AWS CodeCommit, AWS CodeStar, or GitHub. You can also deploy applications from source code stored in Amazon S3 buckets. For more information, see [Deploying Source Code from AWS CodeCommit, AWS CodeStar, or GitHub](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_codecommit.html) and [Deploying Source Code from Amazon S3](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_s3.html).

## Docker container deployment

Elastic Beanstalk supports the deployment of web applications from Docker containers. You can use Elastic Beanstalk to deploy and manage Docker containers on Amazon EC2 instances or on AWS Fargate. You can also use Elastic Beanstalk to deploy and manage Docker containers on Amazon ECS clusters. For more information, see [Deploying Docker Containers on AWS Elastic Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_docker.html).


