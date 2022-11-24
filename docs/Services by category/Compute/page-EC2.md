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