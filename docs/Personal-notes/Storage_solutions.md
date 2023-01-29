---
title: AWS Storage Solutions
---

## AWS offers several different storage types

*this secition should be included in the storage section*
Object storage is a type of data storage that is designed for storing and retrieving unstructured data, such as photos, videos, and documents. AWS's object storage service is called <a href="../Services by category/Storage/page-S3">Amazon S3</a> (Simple Storage Service). It allows users to store and retrieve any amount of data, at any time, from anywhere on the web.

Block storage is a type of data storage that is designed for use with traditional, file-based applications. AWS's block storage service is called <a href="../Services by category/Storage/page-EBS">Amazon Elastic Block Store (EBS)</a>. It allows users to create and attach virtual storage volumes to Amazon Elastic Compute Cloud (EC2) instances. These volumes can be used as raw block devices, and can be formatted with a file system of the user's choice.

File storage is a type of data storage that is designed for use with file-based applications, such as network-attached storage (NAS) and distributed file systems. AWS's file storage service is called <a href="../Services by category/Storage/page-EFS">Amazon Elastic File System (EFS)</a>. It allows users to create and mount file systems that can be accessed by multiple Amazon EC2 instances at the same time.

## AWS Storage Solutions

| Object | Block | File |
|--------|-------|------|
| S3     | EBS   | EFS  |


## Storage cost optimization

Optimizing storage cost in AWS can be achieved by using the following methods:

1. AWS S3: Use S3 Intelligent-Tiering, which automatically moves data to lower-cost storage classes when access patterns change. Use S3 infrequent access for data that is infrequently accessed to reduce costs.

2. EFS: Store data in the One Zone storage class for lower-cost, single-availability-zone data storage.

3. EBS: Use Provisioned IOPS SSDs for bursty I/O workloads and general purpose SSDs for steady state I/O workloads.

4. EC2: Store data on instance storage if the data is ephemeral and can be recreated if the instance is lost. Use EBS volumes for persistent data that needs to be preserved after instance termination.

In general, the right storage solution will depend on the specific needs of your workload.

## Visibility for cost optimization

Improving visibility for cost optimization in AWS can be achieved through the following methods:

1. AWS Cost Explorer: Use AWS Cost Explorer to view costs, usage, and trend reports, and set up alerts for cost optimization.

2. Tag resources: Tagging of AWS resources can help in tracking and allocating costs, and also identify underutilized or idle resources.

3. Utilize the AWS Budgets dashboard: Use the AWS Budgets dashboard to set custom budgets and alerts for cost optimization.

4. Enable AWS Cost and Usage reports: Enable AWS Cost and Usage reports to get detailed information on resource usage and cost, which can help with cost optimization.

5. Use AWS Trusted Advisor: AWS Trusted Advisor helps identify cost optimization opportunities, such as idle or underutilized resources.

By using these methods, you can gain visibility into your AWS infrastructure, track costs, and identify opportunities for cost optimization.

## Setting up alarms for cost optimization

you can set up alarms to monitor costs in AWS using Amazon CloudWatch. Here are the steps to set up an alarm:

1. Open the CloudWatch console in the AWS Management Console.
2. Choose Alarms, then choose Create Alarm.
3. Choose the metric you want to use to trigger the alarm. You can choose from a variety of metrics, including AWS service-specific metrics, custom metrics, and CloudWatch Logs metrics.
4. Set the alarm threshold and choose the appropriate comparison operator.
5. Choose the actions to take when the alarm state is breached, such as sending an SNS notification, autoscaling, or stopping or terminating an EC2 instance.
6. Choose the frequency for how often CloudWatch should evaluate the alarm and the number of times the breach must occur before the alarm changes state.
7. Give the alarm a descriptive name and choose Create Alarm.

By setting up CloudWatch Alarms, you can monitor your AWS costs in real-time, and take appropriate action when costs exceed your specified thresholds.

## Exam focus areas

You should be familiar with the following topics:

* Integrate AWS Auto Scaling and EC2 Auto Scaling with Amazon CloudWatch alarms
* Recognize AWS services that scale automatically
* Right-size storage
* Implement data lifecycle rules
* Manage S3 storage costs and use S3 lifecycle policies
* Select the appropriate backup and archival solution
* Select the appropriate serice for data migration to storage services

All these solution should be optimized for cost and understand the tradeoffs between cost and performance.