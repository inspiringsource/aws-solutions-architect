---
title: Week 1
---
# Designing Resilient Architectures

This credential helps organizations identify and develop talent with critical skills for implementing cloud initiatives. Earning AWS Certified Solutions Architect – Associate validates the ability to design and implement distributed systems on AWS.

To learn more, see:    
[AWS Certified Solutions Architect - Associate](https://aws.amazon.com/certification/certified-solutions-architect-associate/)    
[status: reviewed &#9745; ]

To earn this certification, you will need to take and pass the AWS Certified Solutions Architect – Associate exam. The exam features a combination of two question formats: multiple choice and multiple response. Additional information, such as the exam content outline and passing score, is in the exam guide.

To learn more, see:   
[AWS Certified Solutions Architect - Associate Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)   
[status: reviewed &#9745; ]

The multi-tier application has been a cornerstone architecture pattern for decades, and remains a popular pattern for user-facing applications. Although the language used to describe a multi-tier architecture varies, a multi-tier application generally consists of a presentation tier, a logic tier, and a data tier.

To learn more, see:     
[AWS Serverless Multi-Tier Architectures with Amazon API Gateway and AWS Lambda](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/introduction.html)    
[status: reviewed &#9745; ]

AWS Well-Architected helps cloud architects build secure, high-performing, resilient, and efficient infrastructure for their applications and workloads. Based on five pillars—operational excellence, security, reliability, performance efficiency, and cost optimization—AWS Well-Architected provides a consistent approach for customers and AWS Partner Network (APN) Partners to evaluate architectures and implement designs that can scale over time.

To learn more, see:     
[AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)    
[status: reviewed &#9745; ]

Achieving reliability can be challenging in traditional on-premises environments because of single points of failure, lack of automation, and lack of elasticity. By focusing on best practices and recommendations, you will be enabled to build architectures that have strong foundations, resilient architecture, consistent change management, and proven failure recovery processes.

To learn more, see:   
[Reliability Pillar - AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)      
[status: reviewed &#9745; ]

Event-driven architecture can help you decouple services and simplify dependencies as your applications grow. In this session, you learn how Amazon EventBridge provides new options for developers who want to gain the benefits of this approach.

To learn more, see:      
 [Decoupling serverless workloads with Amazon EventBridge (video)](https://youtu.be/VI79XQW4dIM?t=141)    
 [status: WIP ⏳ ]

The pattern provided in the following documentation link shows asynchronous communication between microservices by using an asynchronous poll model. A loosely coupled architecture can be built, which avoids bottlenecks caused by synchronous communication, latency, and I/O. In the pattern's use case, Amazon Simple Queue Service (Amazon SQS) and Lambda are used to implement asynchronous communication between different microservices.

To learn more, see:     
[Decouple messaging pattern](https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-integrating-microservices/decouple-messaging.html)     
[status: reviewed &#9745; ]

Amazon Elastic File System (Amazon EFS) file systems are resilient to one or more Availability Zone failures in an AWS Region. Mount targets themselves are designed to be highly available. As you design for high availability and failover to other Availability Zones, remember that though the IP addresses and DNS for your mount targets in each Availability Zone are static, they are redundant components backed by multiple resources.

To learn more see:     
[Resilience in Amazon Elastic File System](https://docs.aws.amazon.com/efs/latest/ug/disaster-recovery-resiliency.html)     
[status: reviewed &#9745; ]

Each object in Amazon Simple Storage Service (Amazon S3) has a storage class associated with it. For example, if you list the objects in an S3 bucket, the console shows the storage class for all the objects in the list. Amazon S3 offers a range of storage classes for the objects that you store. You choose a class depending on your use-case scenario and your requirements for performance access. All Amazon S3 storage classes are designed to offer high durability.

> **Legend:**
       
| WIP | reviewed |
| --------- | ------- |
| ⏳ | &#9745; |
         