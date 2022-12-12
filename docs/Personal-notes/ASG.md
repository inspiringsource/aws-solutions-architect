---
title: AWS ASG
---

Amazon EC2 Auto Scaling Groups (ASGs) is a collection of EC2 instances that are managed by AWS Auto Scaling. ASGs are used to automatically scale the number of EC2 instances in your EC2 environment based on the load on your application. You can also use ASGs to automatically replace unhealthy instances with new instances.


The automatic scaling can be triggered by:
- Capacity Settings: based on Min, Max and Desired Capacity.
- Health Check Replacements: If an instance is considered unhealthy it is terminated and a new instance is launched.
- Scaling Policies: step scaling or simple scaling, you choose scaling metrics and threshold values for the CloudWatch alarms that invoke the scaling process.

<div>
<div align="center"><img src="https://docs.aws.amazon.com/images/autoscaling/ec2/userguide/images/elb-tutorial-architecture-diagram.png" /></div>
<div><p align="center">Elastic Load Balancing supports an Application Load Balancer <a href="https://docs.aws.amazon.com/autoscaling/ec2/userguide/tutorial-ec2-auto-scaling-load-balancer.html">Source</a></p></div>
</div>

Elastic Load Balancing supports an Application Load Balancer (ALB) that can distribute traffic across multiple targets, such as EC2 instances, in multiple Availability Zones. You can use an ALB with Auto Scaling to automatically scale the number of instances that are registered with your load balancer. For more information, see [Load Balancing Your Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-load-balancer.html).

[Read more](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html)