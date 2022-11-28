---
title: Amazon EC2 Auto Scaling
description: Lorem ipsum dolor sit amet - 2
---

Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size. You can specify the maximum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes above this size. If you specify the desired capacity, either when you create the group or at any time thereafter, Amazon EC2 Auto Scaling ensures that your group has this many instances. If you specify scaling policies, then Amazon EC2 Auto Scaling can launch or terminate instances as demand on your application increases or decreases.

For example, the following Auto Scaling group has a minimum size of one instance, a desired capacity of two instances, and a maximum size of four instances. The scaling policies that you define adjust the number of instances, within your minimum and maximum number of instances, based on the criteria that you specify.

<div>
<div align="center"><img src="https://docs.aws.amazon.com/images/autoscaling/ec2/userguide/images/as-basic-diagram.png" /></div>
<div><p align="center">Example visualized</p></div>
</div>


Amazon EC2 Auto Scaling manages the launch and termination of these EC2 instances on your behalf. You define a set of criteria (such as an Amazon CloudWatch alarm) that determines when the Auto Scaling group launches or terminates EC2 instances. Adding Auto Scaling groups to your network architecture helps make your application more highly available and fault tolerant.

<div>
<div align="center"><img src="https://docs.aws.amazon.com/images/autoscaling/ec2/userguide/images/sample-3-tier-architecture-auto-scaling-diagram.png" /></div>
<div><p align="center">Capacity added only when needed</p></div>
</div>

You can create as many Auto Scaling groups as you need. For example, you can create an Auto Scaling group for each tier.

To distribute traffic between the instances in your Auto Scaling groups, you can introduce a load balancer into your architecture. For more information, see Elastic Load Balancing.

<a target="_self" href="https://aws-notes-taking.netlify.app/docs/Personal-notes/ASG">More about Auto Scaling group...</a>      
      
## Amazon EC2 Auto Scaling is serverless

Amazon EC2 Auto Scaling is serverless, so there is no infrastructure to manage, and you pay only for the instances that you run. You can use the Auto Scaling console to create and manage your Auto Scaling groups. You can also use the Auto Scaling API to create and manage your Auto Scaling groups.

## Related services

- [Amazon EC2](https://aws.amazon.com/ec2/)
- [Amazon EC2 Auto Scaling benefits](https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html#autoscaling-design-example)
- [Placement groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html)
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)
- [Amazon CloudWatch Events](https://aws.amazon.com/cloudwatch/events/)
- [Amazon CloudWatch Logs](https://aws.amazon.com/cloudwatch/logs/)
- [AWS Lambda](https://aws.amazon.com/lambda/)
- [AWS Systems Manager](https://aws.amazon.com/systems-manager/)
