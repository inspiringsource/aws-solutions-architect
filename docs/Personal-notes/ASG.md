---
title: AWS ASG
---

Amazon EC2 Auto Scaling Groups (ASGs) is a collection of EC2 instances that are managed by AWS Auto Scaling. ASGs are used to automatically scale the number of EC2 instances in your EC2 environment based on the load on your application. You can also use ASGs to automatically replace unhealthy instances with new instances.


The automatic scaling can be triggered by:
- Capacity Settings: based on Min, Max and Desired Capacity.
- Health Check Replacements: If an instance is considered unhealthy it is terminated and a new instance is launched.
- Scaling Policies: step scaling or simple scaling, you choose scaling metrics and threshold values for the CloudWatch alarms that invoke the scaling process.

[Read more](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html)