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

## Review

Amazon Anthena analyzes data in Amazon S3 using standard SQL.
Amazon Aurora is a fully managed relational database service (RDS).
Amazon DynamoDB is a fully managed NoSQL database service.
Amazon ElastiCache is a fully managed in-memory cache service.
Amazon Kinesis allows you to collect, process, and analyze real-time, streaming data.
Amazon RDS is a fully managed relational database service.
Amazon Redshift is a fully managed, petabyte-scale data warehouse service.
<div>
<div align="center"><img src={require('@site/static/img/create-an-RDS-Instance.png').default} /></div>
<div><p align="center">When creating an RDS Instance</div>
</div>
Note that, Amazon Aurora and RDS are fully managed relational database services. RDS is a single-instance database, while Aurora is a multi-instance database.

### Amazon Aurora
Amazon Aurora is a fully managed warehouse featuring high performance, while Athena is a query service to analyze data in Amazon S3 using standard SQL.

### What is a database?
What is the difference between storage and database? Storage (e.g. S3) is a place to store data with an [object storage architecture](https://en.wikipedia.org/wiki/Object_storage), file storage and object storage while database uses other storage architectures that include unifying information about how data is arranged and / or related when stored and queried.

### SQL and NoSQL
SQL and NoSQL are two different types of databases. SQL, which stands for Structured Query Language, is a type of relational database that is designed to store and manage data using a structured format, such as a table with rows and columns. This allows for data to be easily accessed, organized, and updated. NoSQL, on the other hand, stands for "not only SQL" and refers to a non-relational database that does not use the traditional table-based structure of SQL databases. NoSQL databases are often designed to be flexible, scalable, and capable of handling a large amount of data that may have different structures. NoSQL databases are often used for big data applications. [Source](https://www.ibm.com/cloud/learn/sql-vs-nosql) 

### Graph database
A graph database is a type of database that uses graph structures for semantic queries with nodes, edges, and properties to represent and store data. This makes it easier to represent and query relationships between data, as compared to more traditional relational databases, which use tables and rows to represent data. Graph databases are often used for applications that require complex queries or highly connected data, such as social networks or recommendation engines. [Source](https://www.ibm.com/cloud/learn/graph-databases)
AWS solutions for graph databases include **Amazon Neptune** which is a fully managed graph database service that makes it easy to build and run applications that work with highly connected datasets.
## Further reading:

[Choosing a Database](https://aws.amazon.com/startups/start-building/how-to-choose-a-database/)

[AWS Cloud Databases](https://aws.amazon.com/products/databases/)

[AWS Whitepapper Overview](https://d0.awsstatic.com/whitepapers/aws-overview.pdf)

[Relational vs. NoSQL data](https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/relational-vs-nosql-data?source=docs)