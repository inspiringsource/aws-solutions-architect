---
title: Compare security groups and network ACLs
---

Amazon Virtual Private Cloud provides features that you can use to increase and monitor the security for your virtual private cloud (VPC):

- Security groups: Security groups allow or deny specific inbound and outbound traffic at the resource level (such as an EC2 instance). When you launch an instance, you can associate it with one or more security groups. Each instance in your VPC could belong to a different set of security groups. If you don't specify a security group when you launch an instance, the instance is automatically associated with the default security group for its VPC. For more information, see Control traffic to resources using security groups.

- Network access control lists (ACL): Network ACLs allow or deny specific inbound and outbound traffic at the subnet level. For more information, see Control traffic to subnets using Network ACLs.

- Flow logs: Flow logs capture information about the IP traffic going to and from network interfaces in your VPC. You can create a flow log for a VPC, subnet, or individual network interface. Flow log data is published to CloudWatch Logs or Amazon S3, and it can help you diagnose overly restrictive or overly permissive security group and network ACL rules. For more information, see Logging IP traffic using VPC Flow Logs.

- Traffic mirroring: You can copy network traffic from an elastic network interface of an Amazon EC2 instance. You can then send the traffic to out-of-band security and monitoring appliances. For more information, see the Traffic Mirroring Guide.

You can use AWS Identity and Access Management (IAM) to control who in your organization has permission to create and manage security groups, network ACLs, and flow logs. For example, you can give your network administrators that permission, but not give permission to personnel who only need to launch instances. For more information, see Identity and access management for Amazon VPC.

Amazon security groups and network ACLs do not filter traffic destined to and from the following:

* Amazon Domain Name Services (DNS)

* Amazon Dynamic Host Configuration Protocol (DHCP)

* Amazon EC2 instance metadata

* Amazon ECS task metadata endpoints

* License activation for Windows instances

* Amazon Time Sync Service

* Reserved IP addresses used by the default VPC router

## Compare security groups and network ACLs

Security groups and network ACLs are stateless. This means that if you allow traffic in a security group, you must also allow the return traffic in a security group or network ACL. For example, if you allow inbound HTTP traffic (port 80) in a security group, you must also allow outbound HTTP traffic (port 80) in a security group or network ACL. If you don't, the return traffic is blocked.

| Security group                                                    	| Network ACL                                                                                                                                      	|
|-------------------------------------------------------------------	|--------------------------------------------------------------------------------------------------------------------------------------------------	|
| Operates at the instance level                                    	| Operates at the subnet level                                                                                                                     	|
| Applies to an instance only if it is associated with the instance 	| Applies to all instances deployed in the associated subnet (providing an additional layer of defense if security group rules are too permissive) 	|
| Supports allow rules only                                         	| Supports allow rules and deny rules                                                                                                              	|
| We evaluate all rules before deciding whether to allow traffic    	| We evaluate rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic                                       	|
| Stateful: Return traffic is allowed, regardless of the rules      	| Stateless: Return traffic must be explicitly allowed by rules                                                                                    	|

Source: [Compare security groups and network ACLs](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Security.html)