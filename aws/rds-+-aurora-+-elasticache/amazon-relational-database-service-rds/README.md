# Amazon Relational Database Service (RDS)

### RDS Features

Let's look at the features of RDS.

* RDS is a <mark style="color:red;">managed</mark> (so that you can't SSH into this instance)service
  * Automated provisioning, OS patching
  * Continuous backups and restore to a specific timestamp
  * Monitoring dashboard
  * Read replicas for improved read performance
  * Multi-AZ setup for DR(Disaster Recovery)
  * Maintenance windows for upgrades
  * Scaling capability(vertical and horizontal)
  * Storage backed by <mark style="color:red;">EBS</mark>

### RDS Autoscaling

* RDS helps to automatically increase the storage on your RDS DB instance
* When it detects you are running out of free database storage, it scales automatically
* Avoid manual scaling
* You have to set <mark style="color:red;">**Maximum Storage Threshold**</mark>
* <mark style="color:red;">**Useful for unpredictable workloads**</mark>
* Support all RDS database engines (MariaDB, MySQL, PostgreSQL, Oracle, SQL Server)
