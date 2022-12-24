---
title: Aurora Serverless
description: Lorem ipsum dolor sit amet - 2
---

Amazon Aurora Serverless is a new deployment option for Amazon Aurora that automatically starts up, shuts down, and scales capacity up or down based on your application's needs. It is available in all AWS Regions where Amazon Aurora is available.

## Use cases
### Variable workloads
You're running an infrequently-used application, with peaks of 30 minutes to several hours a few times each day or several times per year, such as a human resources, budgeting, or operational reporting application. You no longer have to provision to peak capacity, which would require you to pay for resources you don't continuously use, or to average capacity, which would risk performance problems and a poor user experience.
### Unpredictable workloads
You're running workloads with database usage throughout the day, and also peaks of activity that are hard to predict. For example, a traffic site that might see a surge of activity when it starts raining. Your database will automatically scale capacity to meet the needs of the application's peak load and scale back down when the surge of activity is over.
### Enterprise database fleet management NEW
Enterprises with hundreds or thousands of applications, each backed by one or more databases, must manage resources for their entire database fleet. As application requirements fluctuate, continuously monitoring and adjusting capacity for each and every database to ensure high performance, high availability, and remaining under budget is a daunting task. With Aurora Serverless v2, database capacity is automatically adjusted based on application demand. You no longer need to manually manage thousands of databases in your database fleet. Features such as global database and Multi-AZ deployments ensure high availability and fast recovery.
### Software as a service applications NEW
Software as a service (SaaS) vendors typically operate hundreds or thousands of Aurora databases, each supporting a different customer, in a single cluster to improve utilization and cost efficiency. But they still need to manage each database individually, including monitoring for and responding to colocate databases in the same cluster that may take up more shared resources than originally planned. With Aurora Serverless v2, SaaS vendors can provision Aurora database clusters for each individual customer without worrying about costs of provisioned capacity. It automatically shuts down databases when they are not in use to save costs and instantly adjusts databases capacity to meet changing application requirements.
### Scaled-out databases split across multiple servers NEW
Customers with high write or read requirements often split databases across several instances to achieve higher throughput. However, customers often provision too many or too few instances, increasing cost or limiting scale. With Aurora Serverless v2, customers split databases across several Aurora instances and let the service adjust capacity instantly and automatically based on need. It seamlessly adjusts capacity for each node with no downtime or disruption, and uses only the amount of capacity needed to support applications.

## Advantages of Aurora Serverless v2
Aurora Serverless v2 is intended for variable or "spiky" workloads. With such unpredictable workloads, you might have difficulty planning when to change your database capacity. You might also have trouble making capacity changes quickly enough using the familiar mechanisms such as adding DB instances or changing DB instance classes.

[User Guide](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.html)