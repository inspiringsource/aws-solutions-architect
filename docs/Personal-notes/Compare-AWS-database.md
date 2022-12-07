---
title: Choosing a Database
---

<div class="table-contents"><table id="w596aac17c27b7b3"><thead>
     <tr>
      <th>Database</th>
      <th>Use cases</th>
      <th>AWS services</th>
     </tr>
    </thead>
     <tbody><tr>
      <td>Relational</td>
      <td>
       <p>Traditional applications, enterprise resource planning (ERP), customer relationship
        management (CRM), ecommerce</p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/rds/aurora/" rel="noopener noreferrer" target="_blank"><span>Amazon Aurora</span></a></b> — Designed for unparalleled high performance and availability at global scale with full MySQL and PostgreSQL compatibility</p>
        </li><li class="listitem">
         <p><b><a href="https://aws.amazon.com/rds/" rel="noopener noreferrer" target="_blank"><span>Amazon RDS</span></a></b> — Set up, operate, and scale a relational database in the cloud with just a few clicks</p>
        </li><li class="listitem">
        <p><b><a href="https://aws.amazon.com/redshift/" rel="noopener noreferrer" target="_blank"><span>Amazon Redshift</span></a></b> — Accelerate your time to insights with fast, easy, and secure cloud data warehousing at scale</p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>Key-value</td>
      <td>
       <p>High-traffic web applications, ecommerce systems, gaming applications </p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/dynamodb/" rel="noopener noreferrer" target="_blank"><span>Amazon DynamoDB</span></a></b> — Fast, flexible NoSQL database service for single-digit millisecond performance at any scale</p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>In-memory</td>
      <td>
       <p>Caching, session management, gaming leaderboards, geospatial applications </p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/elasticache/" rel="noopener noreferrer" target="_blank"><span>Amazon ElastiCache</span></a></b> — Unlock microsecond latency and scale with in-memory caching</p>
        </li><li class="listitem">
         <p><b><a href="https://aws.amazon.com/memorydb/" rel="noopener noreferrer" target="_blank"><span>Amazon MemoryDB for Redis</span></a></b> — Redis-compatible, durable, in-memory database service for ultra-fast performance</p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>Document</td>
      <td>
       <p>Content management, catalogs, user profiles</p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/documentdb/" rel="noopener noreferrer" target="_blank"><span>Amazon DocumentDB (with MongoDB compatibility)</span></a></b> — Scale JSON workloads with ease using a fully managed document database service</p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>Wide column</td>
      <td>
       <p>High-scale industrial apps for equipment maintenance, fleet management, and route
        optimization</p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/keyspaces/" rel="noopener noreferrer" target="_blank"><span>Amazon Keyspaces</span></a></b> — A scalable, highly available, and managed Apache Cassandra–compatible database service </p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>Graph</td>
      <td>
       <p>Fraud detection, social networking, recommendation engines </p>
      </td>
      <td>
       <div class="itemizedlist">
       <ul class="itemizedlist" type="disc"><li class="listitem">
         <p><b><a href="https://aws.amazon.com/neptune/" rel="noopener noreferrer" target="_blank"><span>Amazon Neptune</span></a></b> — Build and run graph applications with highly connected datasets</p>
        </li></ul></div>
      </td>
     </tr>
     <tr>
      <td>Time series</td>
      <td>
       <p>Internet of Things (IoT) applications, DevOps, industrial telemetry </p>
      </td>
      <td>     
      <div class="itemizedlist">
      <ul class="itemizedlist" type="disc"><li class="listitem">
        <p><b><a href="https://aws.amazon.com/timestream/" rel="noopener noreferrer" target="_blank"><span>Amazon Timestream</span></a></b> — Fast, scalable, serverless time series database</p>
       </li></ul></div></td>
     </tr>
     <tr>
      <td>Ledger</td>
      <td>
       <p> Systems of record, supply chain, registrations, banking transactions </p>
      </td>
      <td>     
      <div class="itemizedlist">
      <ul class="itemizedlist" type="disc"><li class="listitem">
        <p><b><a href="https://aws.amazon.com/qldb/" rel="noopener noreferrer" target="_blank"><span>Amazon Ledger Database
         Service (QLDB)</span></a></b> — Maintain an immutable, cryptographically verifiable log of data changes</p>
       </li></ul></div></td>
     </tr>
    </tbody></table></div>

Source: [Overview of Amazon Web Services: Database](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/database.html)

## Key highlights:

Amazon Aurora is a fully managed warehouse featuring high performance, while Athena is a query service to analyze data in Amazon S3 using standard SQL.

Both Aurora and RDS are fully managed relational database services. RDS is a single-instance database, while Aurora is a multi-instance database.

## Further reading:

[Choosing a Database](https://aws.amazon.com/startups/start-building/how-to-choose-a-database/)

[AWS Cloud Databases](https://aws.amazon.com/products/databases/)

[AWS Whitepapper Overview](https://d0.awsstatic.com/whitepapers/aws-overview.pdf)

[Relational vs. NoSQL data](https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/relational-vs-nosql-data?source=docs)