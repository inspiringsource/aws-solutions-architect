---
title: Elastic Load Balancing (ELB)
description: Lorem ipsum dolor sit amet - 2
---

Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs).

You can select the appropriate load balancer based on your application needs. If you need flexible application management, we recommend that you use an Application Load Balancer. If extreme performance and static IP is needed for your application, we recommend that you use a Network Load Balancer. If you have an existing application that was built within the EC2-Classic network, then you should use a Classic Load Balancer.


Three types of load balancers are available:
* Application Load Balancer ALB (HTTP/HTTPS)
* Network Load Balancer NLB (TCP/UDP)
* Classic Load Balancer CLB (Legacy)

<div>
<div align="center"><img src={require('@site/static/img/Load_balancer-types.png').default} /></div>
<div><p align="center">Load balancer types</p></div>
</div>

## What is a load balancer?

A load balancer is a server that receives incoming traffic from the internet and routes it to multiple targets, such as EC2 instances, in multiple Availability Zones. The load balancer also monitors the health of its registered targets and ensures that it routes traffic only to healthy targets. You configure your load balancer to accept incoming traffic on one or more listeners, and to route traffic to one or more registered targets, based on the protocol and port number for each listener.

## How does a load balancer work?

A load balancer has one or more listeners configured with a protocol and port number for connections from clients to the load balancer. You configure rules for routing traffic to targets, based on the protocol and port number for each listener. You register targets with the load balancer, and the load balancer routes incoming traffic to the registered targets, based on the rules that you configure. You can configure your load balancer to use either static or dynamic routing.