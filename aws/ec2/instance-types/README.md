# EC2 Instance Types

EC2 Instance Types can be classified for their use purposes. There are mainly 4 different EC2 instance types available. They named like following patterns:

{% hint style="info" %}
For example <mark style="color:red;">**gp3.2xlarge**</mark>

**gp**: Instance class. (In this example General Purpose)

**3**: It notifies the generation of the instance.

**2xlarge:** Size of the instance. Let's say if you increased this value, specifications like memory, CPU etc will be increased too.
{% endhint %}

Now let's look at the instance types, their general use cases and general abbreviations. They are as follows:

* **General Purpose(abbr: 'gp')**
  * It is great for a diversity of workloads. For example web servers, code repositories etc.
  * Balance between computing, memory and networking.
  * Free-tier instance offers usually include general-purpose ones.
* **Compute Optimized (abbr: 'c' )**
  * These types of instances are much better for CPU-intense tasks or projects that need high-performance processors. for example machine learning, batch processing workloads, high-performance heavy traffic web servers etc.&#x20;
* **Memory Optimized (abbr: 'r' - > Think the first letter of RAM)**
  * They are useful for memory intense workloads. It provides high performance for processing large data sets in memory. For example, it is useful for distributed web-scale caches, high-performance relational and nonrelational dbs, in-memory databases and apps performing real-time processing of big unstructured data.
* **Storage Optimized(abbrs: 'i', 'd', 'h1')**
  * These instances are more convenient for storage-intensive tasks that require high sequential read and write access to large data sets on local storage. Its use cases like Relational and NoSQL Databases, Caches (like Redis), data warehouse apps, distributed file systems.
