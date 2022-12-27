---
title: Amazon VPC
description: Lorem ipsum dolor sit amet - 2
---

**What is Amazon VPC?**

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
> NACL is stateless, this means the rules are enforced in both directions. For example, if you have an inbound rule that allows traffic, there must be an outbound rule that allows traffic, or the traffic is blocked. If you have an outbound rule that allows traffic, there must be an inbound rule that allows traffic, or the traffic is blocked.
- Security Groups (SG) Stateful: A set of rules that are evaluated on traffic entering or leaving an instance to determine whether the traffic should be allowed to enter or leave. Each instance is automatically associated with a default security group. You can add rules to the default security group or create your own security groups. Each security group contains a default rule that allows all outbound traffic. You can't delete this default rule. For each security group, we recommend that you add an inbound rule that denies all traffic.
- Public Subnets: A subnet that is associated with a route table that has a route to an internet gateway or virtual private gateway.
- Private Subnets: A subnet that is associated with a route table that doesn't have a route to an internet gateway or virtual private gateway.
- [Nat Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.
- Customer Gateway: A customer gateway is the AWS side of a VPN connection. It is a software appliance that is installed on your on-premises network. It is a virtual device that is managed by AWS. You can create a default customer gateway for your account. You can also create additional customer gateways and attach them to your VPN connections.
- VPC Endpoints: A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
> There are three types of VPC endpoints: **Interface endpoints** uses an Elastic Network Interface (ENI) with Private IP that are powered by AWS PrivateLink (cost $), **Gateway endpoints** are free but only supports S3 and DynamoDB, and [**Gateway Load Balancer endpoints**](https://aws.amazon.com/blogs/architecture/reduce-cost-and-increase-security-with-amazon-vpc-endpoints/#:~:text=There%20are%20three%20types%20of,gateway%20endpoints%2C%20and%20interface%20endpoints.) intercept traffic and route it to a network or security service that you’ve configured using a Gateway Load Balancer. .
- VPC Peering: A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. You cannot peer with a VPC in a different Region.

## Further explanations

[AWS VPC Route Table](https://youtu.be/WfQwl3OmoUE)

[Amazon Virtual Private Cloud (VPC) Routing Deep Dive](https://youtu.be/LJNNMTicv1c)

[AWS NAT Gateway and High-Availability NAT Instances with Auto-Scaling](https://www.globaldots.com/resources/blog/aws-nat-gateway-and-high-availability-nat-instances-with-auto-scaling/#:~:text=NAT%20Gateway%3A%20It%20is%20used,each%20subnet%20within%20the%20VPC.)