---
title: Disaster Recovery
---

## RPO and RTO Explained

RPO: Recovery Point Objective

RPO refers to the maximum acceptable data loss, as you explained. It is the point in time to which the data must be recovered in the event of a disaster or failure. The lower the RPO, the more recent the data must be recovered, which means that less data will be lost, but the recovery process may be more complex and time-consuming.

RTO: Recovery Time Objective

RTO, on the other hand, refers to the maximum amount of time that a system or service can be unavailable in the event of a disaster or failure. The RTO is used to plan and implement disaster recovery procedures, and it should be aligned with the overall business goals and objectives. The lower the RTO, the faster the systems must be recovered, which means that the business will experience less downtime, but the recovery process may be more complex and costly.

In summary, RPO and RTO are important concepts in disaster recovery planning and are used to ensure that critical systems and data can be restored in a timely manner in the event of a failure.

<div>
<div align="center"><img src="https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/disaster-recovery-strategies.png" /></div>
<div><p align="center">RTO and RPO in disaster recovery 
</p></div>
</div>

[Disaster recovery options in the cloud](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

## Disaster recovery options in the cloud

Disaster recovery strategies available to you within AWS can be broadly categorized into four approaches, ranging from the low cost and low complexity of making backups to more complex strategies using multiple active Regions. Active/passive strategies use an active site (such as an AWS Region) to host the workload and serve traffic. The passive site (such as a different AWS Region) is used for recovery. The passive site does not actively serve traffic until a failover event is triggered.


[Figure 6 - Disaster recovery strategies](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

When choosing your strategy, and the AWS resources to implement it, keep in mind that within AWS, we commonly divide services into the data plane and the control plane. The data plane is responsible for delivering real-time service while control planes are used to configure the environment. For maximum resiliency, you should use only data plane operations as part of your failover operation. This is because the data planes typically have higher availability design goals than the control planes.

### Active/Passive configuration

Active/Passive is a strategy where the active site is the primary site and the passive site is the secondary site. The secondary site is used for failover in the event of a failure at the primary site. The secondary site is not used for failover until the primary site fails.

- Backup and Restore: This solution involves regularly backing up data and systems and having the ability to restore them in the event of a disaster. It typically has a Recovery Point Objective (RPO) and a Recovery Time Objective (RTO) measured in hours or days. This solution is the simplest and least expensive option for disaster recovery, but it is also the least resilient. It is not recommended for production workloads due to its lower level of availability.

- Pilot Light: This solution involves having a minimal infrastructure set up in a secondary location that can be quickly scaled up in the event of a disaster. It has a lower RPO than Backup and Restore, typically measured in minutes, and an RTO measured in hours. This solution is less expensive than Warm Standby, but it is also less resilient. 

- Warm Standby: This solution involves having a secondary system running and periodically updated with data from the primary system, but not actively serving workloads. In the event of a disaster, the secondary system can be manually switched over to take over the workloads of the primary system. This solution typically has a lower RPO measured in seconds and an RTO measured in minutes, but it is also less resilient than Active/Active. 


Read more: [Plan for Disaster Recovery (DR)](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/plan-for-disaster-recovery-dr.html)
### Active/Active configuration

> RPO and an RTO in real time!

Active/Active is a strategy where both the active and passive sites are active and serving traffic. This strategy is often used for high availability and load balancing. In this strategy, the active site is the primary site and the passive site is the secondary site. The secondary site is used for failover in the event of a failure at the primary site. 

Understanding key performance indicators (KPIs) for your application is important when choosing a disaster recovery strategy. For example, if your application is a web application, then you should consider the following KPIs

* Latency
* Throughput
* Availability
* Error rate

## Further resources:

[RPO-and-RTO](https://aws.amazon.com/blogs/mt/establishing-rpo-and-rto-targets-for-cloud-applications/)


[RPO and RTO Explained](https://youtu.be/rD3nBaS3OG4)

[Disaster Recovery Demystified](https://youtu.be/wgvq9y8wwNQ)

[Establishing RPO and RTO ](https://aws.amazon.com/blogs/mt/establishing-rpo-and-rto-targets-for-cloud-applications/)