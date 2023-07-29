# EBS (Elastic Block Store)

**EBS (Elastic Block Storage)** Volume is a non-physical network drive that users can attach to instances while they are running and gives users to reach their data on their EC2 instances even after termination. Let's look at their general specifications:

* It allows users to persist data, even after termination. It can be attached and detach from instances quickly.
* Can think like a USB stick.
* It is non-physical so that while reaching them network latency is possible.
* **CCP Level** one volume can be mounted to <mark style="color:blue;">one instance</mark>, **Associate** or **Solution Architect** it is <mark style="color:blue;">multiple</mark> scenarios.
* They are bound to specific AZ. <mark style="color:red;">But if you want to move data across zones first you need to take a</mark> <mark style="color:red;"></mark><mark style="color:red;">**snapshot.**</mark>
* There are options like **Delete on termination.**

If you would like to backup your data from one EBS volume to another one you should use the EBS snapshot feature. After obtaining a snapshot you could easily attach the data to instances that launched on the diffrent availability zones (AZ). Now let's check the features of snapshots together.

#### EBS Snapshot Features

* **EBS Snapshot Archive:** Restore data operation may take time between 24 to 72 hours.
* **Recycle Bin for EBS:** It gives a chance to recycle deleted snapshots from 1 day to a year.
* **Fast Snapshot Restore:** It forces to restore snapshot without latency but it is more expensive than a regular process.
