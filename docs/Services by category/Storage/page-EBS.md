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



<div class="table-contents disable-scroll"><table id="w915aac28c33c13c19c13b5"><thead>
            <tr>
              <th></th>
              <th colspan="2" align="center"><a href="./general-purpose.html">General Purpose SSD volumes</a></th>
              <th colspan="3" align="center"><a href="./provisioned-iops.html">Provisioned IOPS SSD volumes</a></th>
              <th><a href="./hdd-vols.html#EBSVolumeTypes_st1">Throughput Optimized HDD volumes</a></th>
              <th><a href="./hdd-vols.html#EBSVolumeTypes_sc1">Cold HDD volumes</a></th>
            </tr>
          </thead>
            <tbody><tr>
              <td><b>Volume type</b></td>
              <td align="center"><code class="code">gp3</code></td>
              <td align="center"><code class="code">gp2</code></td>
              <td align="center"><code class="code">io2</code>&nbsp;Block Express ‡</td>
              <td align="center"><code class="code">io2</code>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
              <td align="center"><code class="code">io1</code></td>
              <td align="center"><code class="code">st1</code></td>
              <td align="center"><code class="code">sc1</code></td>
            </tr>
            <tr>
                <td><b>Durability</b></td>
                <td colspan="2" align="center">99.8% - 99.9% durability (0.1% - 0.2% annual failure rate)</td>
                <td colspan="2" align="center">99.999% durability (0.001% annual failure rate)</td>
                <td>99.8% - 99.9% durability (0.1% - 0.2% annual failure rate)</td>
                <td colspan="2" align="center">99.8% - 99.9% durability (0.1% - 0.2% annual failure rate)</td>
            </tr>
            <tr>
              <td><b>Use cases</b></td>
              <td colspan="2">
                <div class="itemizedlist">   
                <ul class="itemizedlist" type="disc"><li class="listitem"><p>Transactional workloads</p></li><li class="listitem"><p>Virtual desktops</p></li><li class="listitem"><p>Medium-sized, single-instance databases</p></li><li class="listitem"><p>Low-latency interactive applications</p></li><li class="listitem"><p>Boot volumes</p></li><li class="listitem"><p>Development and test environments</p></li></ul></div>
              </td>
              <td>
                <p>Workloads that require:</p>
                <div class="itemizedlist">  
                <ul class="itemizedlist" type="disc"><li class="listitem">
                    <p>Sub-millisecond latency</p>
                  </li><li class="listitem">
                    <p>Sustained IOPS performance</p>
                  </li><li class="listitem">
                    <p>More than 64,000 IOPS or 1,000 MiB/s of throughput</p>
                  </li></ul></div>
              </td>
              <td colspan="2">
                <div class="itemizedlist">  
                <ul class="itemizedlist" type="disc"><li class="listitem">
                    <p>Workloads that require sustained IOPS performance or more than
                      16,000 IOPS</p>
                  </li><li class="listitem">
                    <p>I/O-intensive database workloads</p>
                  </li></ul></div> 
              </td>
              <td>
                <div class="itemizedlist">  
                <ul class="itemizedlist" type="disc"><li class="listitem">
                    <p>Big data</p>
                  </li><li class="listitem">
                    <p>Data warehouses</p>
                  </li><li class="listitem">
                    <p>Log processing</p>
                  </li></ul></div>
              </td>
              <td>
                <div class="itemizedlist">  
                <ul class="itemizedlist" type="disc"><li class="listitem">
                    <p>Throughput-oriented storage for data that is infrequently accessed</p>
                  </li><li class="listitem">
                    <p>Scenarios where the lowest storage cost is important</p>
                  </li></ul></div>
              </td>
            </tr>
            <tr>
              <td><b>Volume size</b></td>
              <td colspan="2" align="center">1 GiB - 16 TiB </td>
              <td>4 GiB - 64 TiB</td>
              <td colspan="2" align="center">4 GiB - 16 TiB </td>
              <td colspan="2" align="center">125 GiB - 16 TiB</td>
            </tr>
            <tr>
              <td><b>Max IOPS per volume</b> (16 KiB I/O)</td>
              <td colspan="2" align="center">16,000</td>
              <td>256,000</td>
              <td colspan="2" align="center">64,000 †</td>
              <td align="center">
                <td>500</td>
                <p>(1 MiB I/O)</p>
              </td>
            <td align="center">
                <td>250</td>
                <p>(1 MiB I/O)</p>
              </td>
            </tr>
            <tr>
              <td><b>Max throughput per volume</b></td>
              <td>1,000 MiB/s</td>
              <td>250 MiB/s *</td>
              <td>4,000 MiB/s</td>
              <td colspan="2" align="center">1,000 MiB/s †</td>
              <td align="center">500 MiB/s</td>
              <td align="center">250 MiB/s</td>
            </tr>
            <tr>
              <td><b>Amazon EBS Multi-attach</b></td>
              <td colspan="2" align="center">Not supported</td>
              <td colspan="3" align="center">Supported</td>
              <td colspan="2" align="center">Not supported</td>
            </tr>
            <tr>
              <td><b>Boot volume</b></td>
              <td colspan="5" align="center">Supported</td>
              <td colspan="2" align="center">Not supported</td>
            </tr>
          </tbody></table></div>


[Read more](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)

## Amazon EBS snapshots

You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved. This minimizes the time required to create the snapshot and saves on storage costs by not duplicating data. Each snapshot contains all of the information that is needed to restore your data (from the moment when the snapshot was taken) to a new EBS volume.

When you create an EBS volume based on a snapshot, the new volume begins as an exact replica of the original volume that was used to create the snapshot. The replicated volume loads data in the background so that you can begin using it immediately. If you access data that hasn't been loaded yet, the volume immediately downloads the requested data from Amazon S3, and then continues loading the rest of the volume's data in the background.

[Read more here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)