---
title: Amazon EC2
description: Lorem ipsum dolor sit amet - 2
---

Amazon EC2 is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers.

## Instance types

Amazon EC2 provides a wide selection of instance types optimized to fit different use cases. Instances are virtual servers that can run applications. They have varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications.

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

## Particular important for the exam

<div>
<div align="center"><img src={require('@site/static/img/Highly_Available_web-app.png').default} /></div>
<div><p align="center">Elastic Load Balancing will re-route connections from unhealthy instances, it still needs new instances to route connections to. Thus, auto scaling will initiate these new instances, and your load balancing will attach connections to them</p></div>
</div>

## Question examples

A Cloud Engineer has created an entirely new VPC to isolate development environments from production. When the new EC2 instance with the development environment was launched within the public subnet, visiting the public IP address does not appear to resolve. The EC2 instance has a public subnet which allows access on port 80. What configuration changes must be made to the VPC so that the EC2 instance is reachable over the internet?

- [x] Add a route to the Internet Gateway
- [x] Add a route to the NAT Gateway
- [x] Add a route to the VPC Endpoint
- [x] Update the main route table with route out to 0.0.0.0/0

[Connect to the internet using an internet gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)



