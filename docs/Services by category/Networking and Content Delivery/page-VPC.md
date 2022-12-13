---
title: Amazon VPC
description: Lorem ipsum dolor sit amet - 2
---

What is Amazon VPC?

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.

Amazon VPC provides multiple network connectivity options for you to use, depending on your current network designs and requirements. These connectivity options include using either the internet or an AWS Direct Connect connection as the network backbone and terminating the connection into AWS or user-managed network endpoints. Additionally, with AWS, you can choose how network routing is delivered between Amazon VPC and your networks, leveraging either AWS services or user-managed network equipment and routes.
Read the whitepaper [Amazon Virtual Private Cloud Connectivity Options - Introduction](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/introduction.html) to learn more.

## Scenario: VPC with a public and private subnet

This scenario shows how to create a VPC with a public and private subnet. The public subnet is connected to the internet, and the private subnet is not connected to the internet. The private subnet is connected to the public subnet through a NAT gateway. The NAT gateway is a managed service that provides internet access to instances in the private subnet.

![VPC with a public and private subnet](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/case-2_updated.png)

Source: [Amazon VPC User Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario2.html)