# Amazon Aurora

<figure><img src="https://docs.aws.amazon.com/images/AmazonRDS/latest/AuroraUserGuide/images/AuroraArch001.png" alt=""><figcaption></figcaption></figure>

### General Features

* Amazon proprietary technology **(NOT OPEN SOURCE)**
* Aurora is <mark style="color:red;">**"AWS Cloud optimized"**</mark> It claims 5x performance over MYSQL on RDS and 3x performance over Postgres on RDS
* Aurora <mark style="color:red;">**storage grows automatically**</mark>
* Aurora can have up to 15 read replicas
* It is 20% more expensive than RDS. But it is efficient.
* Automatic failover
* Backup and Recovery
* Isolation and security
* Advanced Monitoring
* Routine Maintenance
* Backtrack: restore data at any point of time without using backups



### Aurora High Availability and Read Scaling

* 6 copies of your data across 3 AZ (4/6 for writes, 3/6 for reads)
* Self-healing with peer-to-peer replication.
* Automated failover for master in less than 30 seconds
* One Aurora instance takes writes (master)
* Master + up to 15 Aurora Read Replicas serve reads
* Support cross-region replication
* Clients when they want to write data, establish a connection with the Writer Endpoint (points to the master) in the case of read data it points to the Reader Endpoint (points to the Load balancer for read instances)

### Security (RDS and Aurora)

* **At-rest Encryption** :  When it first launched you may set encryption otherwise you need to take snapshot and you need to restore as encrypted&#x20;
* **In-flight Encryption** : TLS ready by default
* **IAM Authentication** : IAM roles to connect databases
* **Security Groups** : Control network access to RDS and Aurora
* <mark style="color:red;">**No SSH available except RDS Custom**</mark>
