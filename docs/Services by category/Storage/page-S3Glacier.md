---
title: Amazon S3 Glacier
description: Lorem ipsum dolor sit amet - 2
---

Amazon S3 Glacier is a storage service for data archiving and long-term backup. It is a fully managed service that provides a simple, scalable, elastic, and cost-effective way to store and access data in the cloud. Amazon S3 Glacier provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon S3 Glacier, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon S3 Glacier, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it.

## Archive Retrieval Options

- Expedited – Expedited retrievals allow you to quickly access your data that's stored in the S3 Glacier Flexible Retrieval storage class or the S3 Intelligent-Tiering Archive Access tier when occasional urgent requests for a subset of archives are required. For all but the largest archives (more than 250 MB), data accessed by using Expedited retrievals is typically made available within 1–5 minutes. Provisioned capacity ensures that retrieval capacity for Expedited retrievals is available when you need it. For more information, see Provisioned Capacity.

- Standard – Standard retrievals allow you to access any of your archives within several hours. Standard retrievals are typically completed within 3–5 hours. This is the default option for retrieval requests that do not specify the retrieval option.

- Bulk – Bulk retrievals are the lowest-cost S3 Glacier retrieval option, which you can use to retrieve large amounts, even petabytes, of data inexpensively in a day. Bulk retrievals are typically completed within 5–12 hours.

[Source](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html#api-downloading-an-archive-two-steps-retrieval-options)