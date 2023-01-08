---
title: AWS PrivateLink
description: Establish connectivity between VPCs and AWS services without exposing data to the internet
---

AWS PrivateLink is a network service that enables you to privately access services hosted on AWS in a VPC without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in a VPC can communicate with AWS PrivateLink endpoints without exposing the endpoint to the internet. Traffic between your VPC and the endpoint stays within the AWS network and doesn't traverse the internet.

## Examples: Services using VPC peering and AWS PrivateLink

While VPC peering enables you to privately connect VPCs, AWS PrivateLink enables you to configure applications or services in VPCs as endpoints that your VPC peering connections can connect to.

An AWS PrivateLink service provider configures instances running services in their VPC with a Network Load Balancer as the front end. Use intra-region VPC peering (VPCs are in the same Region) and inter-region VPC peering (VPCs are in different Regions) with AWS PrivateLink to allow private access to consumers across VPC peering connections.

Read more about [VPC peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html) and [AWS PrivateLink](https://docs.aws.amazon.com/vpc/latest/userguide/privatelink.html).

[Example](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-peering.html#vpc-peer-region-example)