# RDS Read Replicas

<div align="center" data-full-width="false">

<figure><img src="https://d1.awsstatic.com/asset-repository/read-replicas-scaling-disaster-recovery.3b8da7093daeb1e87426225caf49e32efe7ae01a.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

RDS Read Replicas are the replication of the primary database that allows applications to read data from this or these replicas.

* Up to 15 Read replicas
* Within AZ, cross AZ or cross-region
* Replication is <mark style="color:red;">**ASYNC**</mark> so reads are eventually consistent
* Applications must update the connection string to leverage read replicas.
* It is useful if some new applications want to read the same data e.g. reporting apps. In this scenario, instead of making a bottleneck on the primary database, we may create new replicas and give the other apps to consume data from replicas so the production app will be unaffected.
* It is only useful for <mark style="color:red;">**SELECT**</mark> queries&#x20;

### Network Costs

* If async replication is on the <mark style="color:green;">**same region**</mark> but different AZs it <mark style="color:green;">**FREE**</mark>
* If replication is <mark style="color:red;">**cross-regions**</mark> it causes  <mark style="color:red;">**EXTRA COST**</mark>

