---
title: Amazon VPC
description: Define and launch AWS resources in a logically isolated virtual network
---

## Reviewing VPC and its components

> This section covers a broad overview of VPC and its components. For more details, please refer to the [Amazon VPC User Guide](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html). 

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.

Amazon VPC provides multiple network connectivity options for you to use, depending on your current network designs and requirements. These connectivity options include using either the internet or an AWS Direct Connect connection as the network backbone and terminating the connection into AWS or user-managed network endpoints. Additionally, with AWS, you can choose how network routing is delivered between Amazon VPC and your networks, leveraging either AWS services or user-managed network equipment and routes.
Read the whitepaper [Amazon Virtual Private Cloud Connectivity Options - Introduction](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/introduction.html) to learn more.

## Scenario: VPC with a public and private subnet

This scenario shows how to create a VPC with a public and private subnet. The public subnet is connected to the internet, and the private subnet is not connected to the internet. The private subnet is connected to the public subnet through a NAT gateway. The NAT gateway is a managed service that provides internet access to instances in the private subnet.

![VPC with a public and private subnet](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/case-2_updated.png)

Source: [Amazon VPC User Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario2.html)


- Internet Gateway (IGW): A gateway that you attach to your VPC to enable communication between resources in your VPC and the internet. You can create a default IGW for your account. You can also create additional IGWs and attach them to your VPCs.
- Virtual Private Gateway (VPN Gateway): A gateway that you attach to your VPC to enable communication between resources in your VPC and your on-premises network. You can create a default VPN gateway for your account. You can also create additional VPN gateways and attach them to your VPCs.
- Routing Tables: A set of rules, called routes, that are used to determine where network traffic is directed. Each subnet in your VPC must be associated with a route table. If you don't explicitly associate a subnet with any route table, the subnet is automatically associated with the main route table. Each route table contains a local route for the VPC CIDR block, which you can't delete. The local route doesn't use a target. For each subnet route table, we recommend that you add a route to the internet gateway or virtual private gateway for outbound traffic.
- Network Access Control Lists (NACLs) - Stateless: A set of rules that are evaluated on traffic leaving a subnet to determine whether the traffic should be allowed to leave. Each subnet in your VPC must be associated with a network ACL. If you don't explicitly associate a subnet with any network ACL, the subnet is automatically associated with the default network ACL. Each network ACL contains a default rule that allows all outbound traffic. You can't delete this default rule. For each subnet network ACL, we recommend that you add an inbound rule that denies all traffic.
> NACL is stateless, this means the rules are enforced in both directions. For example, if you have an inbound rule that allows traffic, there must be an outbound rule that allows traffic, or the traffic is blocked. 
- Security Groups (SG) Stateful: A set of rules that are evaluated on traffic entering or leaving an instance to determine whether the traffic should be allowed to enter or leave. Each instance is automatically associated with a default security group. You can add rules to the default security group or create your own security groups. Each security group contains a default rule that allows all outbound traffic. You can't delete this default rule. For each security group, we recommend that you add an inbound rule that denies all traffic.
- Public Subnets: A subnet that is associated with a route table that has a route to an internet gateway or virtual private gateway.
- Private Subnets: A subnet that is associated with a route table that doesn't have a route to an internet gateway or virtual private gateway.
- [Nat Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.
>A NAT in a public subnet in your VPC enables instances in the private subnet to initiate outbound IPv4 traffic to the Internet, but prevents the instances from receiving inbound traffic initiated by someone on the Internet. 
- Customer Gateway: A customer gateway is the AWS side of a VPN connection. It is a software appliance that is installed on your on-premises network. It is a virtual device that is managed by AWS. You can create a default customer gateway for your account. You can also create additional customer gateways and attach them to your VPN connections.
- VPC Endpoints: A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
> There are three types of VPC endpoints: **Interface endpoints** uses an Elastic Network Interface (ENI) with Private IP that are powered by AWS PrivateLink (cost $), **Gateway endpoints** are free but only supports S3 and DynamoDB, and [**Gateway Load Balancer endpoints**](https://aws.amazon.com/blogs/architecture/reduce-cost-and-increase-security-with-amazon-vpc-endpoints/#:~:text=There%20are%20three%20types%20of,gateway%20endpoints%2C%20and%20interface%20endpoints.) intercept traffic and route it to a network or security service that you’ve configured using a Gateway Load Balancer. .
- VPC Peering: A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. You cannot peer with a VPC in a different Region.

## NAT gateways

NAT gateways are a highly available, managed service that makes it easy to connect to the internet from instances within a private subnet in an Amazon Virtual Private Cloud (VPC). NAT gateways are horizontally scaled, redundant, and highly available VPC components. You can create a NAT gateway in a public subnet and configure your instances in private subnets to use the NAT gateway for internet access. NAT gateways are available in all public AWS Regions where Amazon VPC is available.

Read more about [VPC NAT Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)

## AWS NAT vs NACLs vs Security Groups

| NAT | NACLs | Security Groups |
| --- | --- | --- |
| NAT is a network address translation service that enables instances in a private subnet to connect to the internet or other AWS services, but prevents the internet from initiating a connection with those instances. | NACLs are stateless, this means the rules are enforced in both directions. For example, if you have an inbound rule that allows traffic, there must be an outbound rule that allows traffic, or the traffic is blocked. | Security groups are stateful, this means that if you allow inbound traffic, the outbound traffic is automatically allowed. |
### Overview

Amazon Web Services (AWS) Network Address Translation (NAT) and Network Access Control Lists (NACLs) are both tools that you can use to control inbound and outbound traffic to your Amazon Virtual Private Cloud (VPC).

NAT is a network service that allows instances in a private subnet to access the internet or other resources in a public subnet, while hiding their private IP addresses. NAT can be used to allow instances to initiate outbound traffic, but not accept inbound traffic.

NACLs are stateless firewalls that operate at the subnet level and allow you to specify inbound and outbound traffic rules for your VPC. NACLs are associated with one or more subnets and operate at the network layer of the OSI model. They allow you to allow or deny traffic to your VPC based on the rules you define.

In summary, NAT is a network service that allows private instances to access the internet or other resources in a public subnet, while NACLs are firewalls that allow you to specify inbound and outbound traffic rules for your VPC.

## Further explanations

* [Amazon NAT](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat.html)       
* [Amazon NACLs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-acl.html)
* [Egress-only internet gateway basics](https://docs.aws.amazon.com/vpc/latest/userguide/egress-only-internet-gateway.html#egress-only-internet-gateway-basics)
* [AWS VPC Route Table](https://youtu.be/WfQwl3OmoUE)
> A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.
* [Amazon Virtual Private Cloud (VPC) Routing Deep Dive](https://youtu.be/LJNNMTicv1c)
* [AWS NAT Gateway and High-Availability NAT Instances with Auto-Scaling](https://www.globaldots.com/resources/blog/aws-nat-gateway-and-high-availability-nat-instances-with-auto-scaling/#:~:text=NAT%20Gateway%3A%20It%20is%20used,each%20subnet%20within%20the%20VPC.)


## Logging IP traffic using VPC Flow Logs

VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. Flow log data can be published to the following locations: Amazon CloudWatch Logs, Amazon S3, or Amazon Kinesis Data Firehose. After you create a flow log, you can retrieve and view the flow log records in the log group, bucket, or delivery stream that you configured.

* Flow logs can help you with a number of tasks, such as:

* Diagnosing overly restrictive security group rules

* Monitoring the traffic that is reaching your instance

* Determining the direction of the traffic to and from the network interfaces

[VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html)

## Connect VPCs using VPC peering

VPC peering enables you to route traffic between two VPCs using private IP addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. You cannot peer with a VPC in a different Region.

* VPC peering is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. You cannot peer with a VPC in a different Region.

[VPC Peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html)