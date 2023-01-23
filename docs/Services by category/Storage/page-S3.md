---
title: Amazon S3
description: Object storage service
---

Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, data availability, security, and performance. Customers of all sizes and industries can store and protect any amount of data for virtually any use case, such as data lakes, cloud-native applications, and mobile apps. With cost-effective storage classes and easy-to-use management features, you can optimize costs, organize data, and configure fine-tuned access controls to meet specific business, organizational, and compliance requirements.

Amazon S3 is the perfect storage layer for storing documents and other types of objects

## Features

* **Scalable** - Amazon S3 is designed to scale to the largest internet-connected applications. Amazon S3 provides a simple web services interface that can be used to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites. The service aims to maximize benefits of scale and to pass those benefits on to developers.

* **Secure** - Amazon S3 is designed to provide 99.999999999% durability and 99.99% availability of objects over a given year. Amazon S3 provides developers and IT teams with tools to configure rules that can be applied to objects in buckets. These rules can be used to automatically perform actions on objects, such as tiering objects to Amazon Glacier or Amazon S3 Standard-Infrequent Access, or to encrypt objects using server-side encryption with Amazon S3-managed keys (SSE-S3) or AWS Key Management Service-managed keys (SSE-KMS).

* **Highly Available** - Amazon S3 provides developers and IT teams with tools to configure rules that can be applied to objects in buckets. These rules can be used to automatically perform actions on objects, such as tiering objects to Amazon Glacier or Amazon S3 Standard-Infrequent Access, or to encrypt objects using server-side encryption with Amazon S3-managed keys (SSE-S3) or AWS Key Management Service-managed keys (SSE-KMS).

* **Cost-Effective** - Amazon S3 provides developers and IT teams with tools to configure rules that can be applied to objects in buckets. These rules can be used to automatically perform actions on objects, such as tiering objects to Amazon Glacier or Amazon S3 Standard-Infrequent Access, or to encrypt objects using server-side encryption with Amazon S3-managed keys (SSE-S3) or AWS Key Management Service-managed keys (SSE-KMS).

* **Easy to Use** - Amazon S3 provides developers and IT teams with tools to configure rules that can be applied to objects in buckets. These rules can be used to automatically perform actions on objects, such as tiering objects to Amazon Glacier or Amazon S3 Standard-Infrequent Access, or to encrypt objects using server-side encryption with Amazon S3-managed keys (SSE-S3) or AWS Key Management Service-managed keys (SSE-KMS).

## S3 Storage tiers

<div>
<div align="center"><img src={require('@site/static/img/S3storageTiers.png').default} /></div>
<div><p align="center">Amazon S3 Storage Classes</p></div>
</div>

## Replicating objects

Amazon S3 supports Cross-Region Replication (CRR).

Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. Buckets that are configured for object replication can be owned by the same AWS account or by different accounts. You can replicate objects to a single destination bucket or to multiple destination buckets. The destination buckets can be in different AWS Regions or within the same Region as the source bucket.

To automatically replicate new objects as they are written to the bucket use live replication, such as Same-Region Replication (SRR) or Cross-Region Replication (CRR). To replicate existing objects to a different bucket on demand, use S3 Batch Replication.

## Bucket policy that complies with S3-bucket

For example, the following bucket policy complies with the rule. The policy explicitly denies all actions on the bucket and objects when the request meets the condition "aws:SecureTransport": "false":

```json    
{
  "Id": "ExamplePolicy",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowSSLRequestsOnly",
      "Action": "s3:*",
      "Effect": "Deny",
      "Resource": [
        "arn:aws:s3:::DOC-EXAMPLE-BUCKET",
        "arn:aws:s3:::DOC-EXAMPLE-BUCKET/*"
      ],
      "Condition": {
        "Bool": {
          "aws:SecureTransport": "false"
        }
      },
      "Principal": "*"
    }
  ]
}
```
Source: [S3 bucket policy for config rule](https://aws.amazon.com/premiumsupport/knowledge-center/s3-bucket-policy-for-config-rule/)


## Lifecycle rules example

You can use lifecycle rules to define actions that you want Amazon S3 to take during an object's lifetime (for example, transition objects to another storage class, archive them, or delete them after a specified period of time).

Amazon S3 to transition a subset of objects to the S3 Standard-IA storage class 30 days after creation.

```
<LifecycleConfiguration>
    <ID>Archive Rule</ID>
    <Filter>
      <Prefix>logs/</Prefix>
    </Filter>
    <Status>Enabled</Status>
    <Transition>
      <StorageClass>STANDARD_IA<StorageClass>
      <Days>30</Days>
    </Transition>
   </Rule>
</LifecycleConfiguration>
```


Source: [lifecycle configuration](https://docs.aws.amazon.com/AmazonS3/latest/userguide/how-to-set-lifecycle-configuration-intro.html)

## S3 bucket policy example

To deny the none HTTPS access:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "DenyNonHttps",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::mybucket/*",
            "Condition": {
                "Bool": {
                    "aws:SecureTransport": "false"
                }
            }
        }
    ]
}
```

## Best practices design patterns: optimizing Amazon S3 performance

Your applications can easily achieve thousands of transactions per second in request performance when uploading and retrieving storage from Amazon S3. Amazon S3 automatically scales to high request rates. For example, your application can achieve at least 3,500 PUT/COPY/POST/DELETE or 5,500 GET/HEAD requests per second per partitioned prefix. There are no limits to the number of prefixes in a bucket. You can increase your read or write performance by using **parallelization**. For example, if you create 10 prefixes in an Amazon S3 bucket to parallelize reads, you could scale your read performance to 55,000 read requests per second. Similarly, you can scale write operations by writing to multiple prefixes. Read more [Optimizing Amazon S3 performance](https://docs.aws.amazon.com/AmazonS3/latest/userguide/optimizing-performance.html)
## References:

[Replicating objects](https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html)
[Amazon-S3-Storage-Classes](https://d1.awsstatic.com/reInvent/re21-pdp-tier1/s3/Amazon-S3-Storage-Classes.pdf)
[Amazon S3 cost optimization](https://aws.amazon.com/blogs/storage/amazon-s3-cost-optimization-for-predictable-and-dynamic-access-patterns/)
[Storage Architecture Selection](https://docs.aws.amazon.com/wellarchitected/latest/performance-efficiency-pillar/storage-architecture-selection.html)