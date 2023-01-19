---
title: Disaster Recovery
---

## RPO and RTO Explained

RPO: Recovery Point Objective

Recovery Point Objective (RPO) is the maximum amount of data loss that a business is willing to tolerate. For example, if an RPO of 24 hours is set, then the business is willing to lose up to 24 hours of data.

RTO: Recovery Time Objective

Recovery Time Objective (RTO) is the maximum amount of time that a business is willing to tolerate for its systems to be unavailable. For example, if an RTO of 4 hours is set, then the business is willing to tolerate up to 4 hours of downtime.

<div>
<div align="center"><img src="https://d2908q01vomqb2.cloudfront.net/972a67c48192728a34979d9a35164c1295401b71/2022/05/31/ClouldOps_913_1.png" /></div>
<div><p align="center">RTO and RPO in disaster recovery 
</p></div>
</div>

Source:  [Establishing RPO and RTO ](https://aws.amazon.com/blogs/mt/establishing-rpo-and-rto-targets-for-cloud-applications/)

[Disaster recovery options in the cloud](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

## Disaster recovery options in the cloud

Disaster recovery strategies available to you within AWS can be broadly categorized into four approaches, ranging from the low cost and low complexity of making backups to more complex strategies using multiple active Regions. Active/passive strategies use an active site (such as an AWS Region) to host the workload and serve traffic. The passive site (such as a different AWS Region) is used for recovery. The passive site does not actively serve traffic until a failover event is triggered.

<div>
<div align="center"><img src={require('@site/static/img/Disaster-recovery-strategie.png').default} /></div>
<div><p align="center">Disaster recovery strategies</p></div>
</div>

When choosing your strategy, and the AWS resources to implement it, keep in mind that within AWS, we commonly divide services into the data plane and the control plane. The data plane is responsible for delivering real-time service while control planes are used to configure the environment. For maximum resiliency, you should use only data plane operations as part of your failover operation. This is because the data planes typically have higher availability design goals than the control planes.

### Active/Passive

Active/Passive is a strategy where the active site is the primary site and the passive site is the secondary site. The secondary site is used for failover in the event of a failure at the primary site. The secondary site is not used for failover until the primary site fails.
# Active/Active

Active/Active is a strategy where both the active and passive sites are active and serving traffic. This strategy is often used for high availability and load balancing. In this strategy, the active site is the primary site and the passive site is the secondary site. The secondary site is used for failover in the event of a failure at the primary site. The secondary site is not used for failover until the primary site fails. The secondary site is not used for failover until the primary site fails.

Understanding key performance indicators (KPIs) for your application is important when choosing a disaster recovery strategy. For example, if your application is a web application, then you should consider the following KPIs:

* Latency
* Throughput
* Availability
* Error rate

## Further resources:

[RPO-and-RTO](https://aws.amazon.com/blogs/mt/establishing-rpo-and-rto-targets-for-cloud-applications/)


[Disaster recovery options in the cloud](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

[RPO and RTO Explained](https://youtu.be/rD3nBaS3OG4)

[Disaster Recovery Demystified](https://youtu.be/wgvq9y8wwNQ)