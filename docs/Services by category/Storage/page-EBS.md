---
title: Amazon EBS
description: serverless analyzing data in S3 using  SQL
---

Amazon Elastic Block Store (Amazon EBS) provides block level storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon EBS volume is automatically replicated within its Availability Zone to protect you from component failure, offering high availability and durability. You can use Amazon EBS to build high-availability applications that can withstand the failure of underlying hardware. You can also use Amazon EBS to build applications that require fast, predictable, and consistent disk performance.

Amazon EBS is a highly available and durable solution for an EC2 instance. 

If IOPS (Input/Output Per Second) is a significant measure in your project (e.g. a lot of small and fast reads / writes). You can use Amazon EBS to build applications that has a High I/O with fast, predictable, and consistent disk performance. 

## Amazon EBS volume types

Amazon EBS provides a range of performance levels that you can use to select the appropriate storage for your needs.

- Solid state drives (SSD) — Optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS. SSD-backed volume types include:

    * General Purpose SSD volumes
    * Provisioned IOPS SSD volumes

- Hard disk drives (HDD) — Optimized for large streaming workloads where the dominant performance attribute is throughput. HDD-backed volume types include 
    * Throughput Optimized HDD (throughput per volume: 500 MiB/s)
    * Cold HDD volumes (throughput per volume: 250 MiB/s)

- Previous generation — Hard disk drives that you can use for workloads with small datasets where data is accessed infrequently and performance is not of primary importance. We recommend that you consider a current generation volume type instead. For more information, see Previous generation Magnetic volumes.

[Read more](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)

## Amazon EBS snapshots

You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved. This minimizes the time required to create the snapshot and saves on storage costs by not duplicating data. Each snapshot contains all of the information that is needed to restore your data (from the moment when the snapshot was taken) to a new EBS volume.

When you create an EBS volume based on a snapshot, the new volume begins as an exact replica of the original volume that was used to create the snapshot. The replicated volume loads data in the background so that you can begin using it immediately. If you access data that hasn't been loaded yet, the volume immediately downloads the requested data from Amazon S3, and then continues loading the rest of the volume's data in the background.

[Read more here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)