---
title: Amazon CloudFront
description: Securely deliver content with low latency and high transfer speeds
---

Amazon CloudFront is a global content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer friendly environment.

<div>
<div align="center"><img src={require('@site/static/img/CloudFront_global_content_delivery_network(CDN).png').default} /></div>
<div><p align="center"><a href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html">CloudFront to deliver content</a></p></div>
</div>

## Features

S3, EC2, ELB, Route53 can be used as origin for CloudFront. 

When you use CloudFront with an Amazon S3 bucket as the origin, you can configure CloudFront and Amazon S3 in a way that provides the following benefits:

- Restricts access to the Amazon S3 bucket so that it's not publicly accessible

- Makes sure that viewers (users) can access the content in the bucket only through the specified CloudFront distribution—that is, prevents them from accessing the content directly from the bucket, or through an unintended CloudFront distribution

To do this, configure CloudFront to send authenticated requests to Amazon S3, and configure Amazon S3 to only allow access to authenticated requests from CloudFront. CloudFront provides two ways to send authenticated requests to an Amazon S3 origin: origin access control (OAC) and origin access identity (OAI). We recommend using OAC because it supports:

- All Amazon S3 buckets in all AWS Regions, including opt-in Regions launched after December 2022

- Amazon S3 server-side encryption with AWS KMS (SSE-KMS)

- Dynamic requests (```PUT``` and ```DELETE```) to Amazon S3

[Read more here](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)