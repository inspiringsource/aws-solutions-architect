---
title: Amazon S3 Glacier
description: Lorem ipsum dolor sit amet - 2
---

Amazon S3 Glacier is a storage service for data archiving and long-term backup. It is a fully managed service that provides a simple, scalable, elastic, and cost-effective way to store and access data in the cloud. Amazon S3 Glacier provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon S3 Glacier, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon S3 Glacier, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it. Amazon S3 Glacier is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it.

## Archive Retrieval Options

<div class="table-contents"><table id="w1774aac21c12c39b9"><thead>
                    <tr>
                        <th>Storage class or tier</th>
                        <th>Expedited</th>
                        <th>Standard</th>
                        <th>Bulk</th>
                    </tr>
                </thead>
                    <tbody><tr>
                        <td>
                            <p>S3 Glacier Flexible Retrieval or S3 Intelligent-Tiering Archive Access</p>
                        </td>
                        <td>
                            <p>1–5 minutes</p>
                        </td>
                        <td>
                            <p>3–5 hours</p>
                        </td>
                        <td>
                            <p>5–12 hours</p>
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <p>S3 Glacier Deep Archive or S3 Intelligent-Tiering Deep Archive Access</p>
                        </td>
                        <td>
                            <p>Not available</p>
                        </td>
                        <td>
                            <p>Within 12 hours</p>
                        </td>
                        <td>
                            <p>Within 48 hours</p>
                        </td>
                    </tr>
                </tbody></table></div>

[Archive retrieval options](https://docs.aws.amazon.com/AmazonS3/latest/userguide/restoring-objects-retrieval-options.html)

[Read more](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html#api-downloading-an-archive-two-steps-retrieval-options)

S3 Glacier Vault Lock helps you to easily deploy and enforce compliance controls for individual S3 Glacier vaults with a Vault Lock policy. You can specify controls such as "Write Once Read Many" (WORM) in a Vault Lock policy and lock the policy from future edits.

> &#9888 Important After a Vault Lock policy is locked, the policy can no longer be changed or deleted.
[Read more](https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html)