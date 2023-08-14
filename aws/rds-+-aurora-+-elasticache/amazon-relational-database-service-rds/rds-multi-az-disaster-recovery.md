# RDS Multi AZ (Disaster Recovery)

<figure><img src="https://d2908q01vomqb2.cloudfront.net/887309d048beef83ad3eabf2a79a64a389ab1c9f/2022/05/04/DBBLOG-2322-image001.png" alt=""><figcaption></figcaption></figure>

* <mark style="color:red;">**SYNC**</mark> <mark style="color:red;">**replication**</mark><mark style="color:red;">**!!! So all changes on the primary are replicated immediately by standby too**</mark>
* Used for disaster recovery
* One DNS name and <mark style="color:green;">**AUTOMATIC FAILOVER**</mark>. If any failure happens on the primary database standby database takes control and is promoted to the master database
* Increase availability
* No manual intervention in apps
* Not used for scaling. It means the standby database is not used for reading and writing by apps until any problem occurs on the master primary database
* <mark style="color:red;">**The read replicas can be set up as Multi-AZ for recovery disaster**</mark>
* <mark style="color:red;">**FROM SINGLE AZ TO MULTI AZ CAN BE SET UP BY MODIFYING PRIMARY DB SO ZERO DOWNTIME IS POSSIBLE**</mark>

<mark style="color:red;">**SINGLE TO MULTI AZ STEPS**</mark>

Snapshot is taken from the primary db AZ then it is recovered from the other AZ.
