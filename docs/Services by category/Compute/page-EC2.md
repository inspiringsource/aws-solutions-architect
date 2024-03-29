---
title: Amazon EC2
description: Secure and resizable compute capacity for virtually any workload
---

Amazon EC2 is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2 is an example of IaaS, which stands for Infrastructure as a Service.

## Instance types

Amazon EC2 provides a wide selection of instance types optimized to fit different use cases. Instances are virtual servers that can run applications. They have varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications. IaaS means that users can access and manage virtual servers that are hosted by a cloud provider, such as AWS. Users can choose from different types of instances, processors, storage, networking, operating systems, and purchase models to suit their needs.

- General purpose
- Compute optimized
- Memory optimized
- Accelerated computing
- Storage optimized

## Instance Profile

Always avoid embedding AWS credentials in your code. Instead, use IAM roles for Amazon EC2. An IAM role is an IAM identity with permission policies that determine what the identity can and cannot do in AWS. You can use an IAM role to delegate access to your Amazon EC2 instances. You can also use IAM roles to delegate access to code that runs on your Amazon EC2 instances.

An instance profile holds the IAM role for an instance. You can use an instance profile to pass a role to an instance when the instance is launched. You can also use an instance profile to pass a role to an instance that is already running.

Read more: [Using instance profiles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2_instance-profiles.html)

## Instance purchasing options

Amazon EC2 provides the following purchasing options to enable you to optimize your costs based on your needs:

* On-Demand Instances – Pay, by the second, for the instances that you launch.

* Savings Plans – Reduce your Amazon EC2 costs by making a commitment to a consistent amount of usage, in USD per hour, for a term of 1 or 3 years.

* Reserved Instances – Reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years.

* Spot Instances – Request unused EC2 instances, which can reduce your Amazon EC2 costs significantly. 
> Spot Instances are normally used in batch processing jobs.

* Dedicated Hosts – Pay for a physical host that is fully dedicated to running your instances, and bring your existing per-socket, per-core, or per-VM software licenses to reduce costs.

* Dedicated Instances – Pay, by the hour, for instances that run on single-tenant hardware.

* Capacity Reservations – Reserve capacity for your EC2 instances in a specific Availability Zone for any duration.
Source: [Click here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html)

## Overview of Amazon EC2

<div>
<div align="center"><img src={require('@site/static/img/Highly_Available_web-app.png').default} /></div>
<div><p align="center">Elastic Load Balancing will re-route connections from unhealthy instances, it still needs new instances to route connections to. Thus, auto scaling will initiate these new instances, and your load balancing will attach connections to them</p></div>
</div>

Keep reading: [Amazon EC2 Auto Scaling](https://www.aws-practical-handbook.link/docs/Services%20by%20category/Compute/page-EC2AutoScaling)
