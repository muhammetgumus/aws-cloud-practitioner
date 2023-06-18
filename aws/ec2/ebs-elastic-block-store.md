# EBS (Elastic Block Store)

**EBS (Elastic Block Storage)** Volume is a non-physical network drive that users can attach to instances while they are running and gives users to reach their data on their EC2 instances even after termination. Let's look at their general specifications:

* It allows users to persist data, even after termination. It can be attached and detach from instances quickly.
* Can think like a USB stick.
* It is non-physical so that while reaching them network latency is possible.
* **CCP Level** one volume can be mounted to <mark style="color:blue;">one instance</mark>, **Associate** or **Solution Architect** it is <mark style="color:blue;">multiple</mark> scenarios.
* They are bound to specific AZ. <mark style="color:red;">But if you want to move data across zones first you need to take a</mark> <mark style="color:red;"></mark><mark style="color:red;">**snapshot**</mark> <mark style="color:red;"></mark><mark style="color:red;">of it.</mark>
* There are options like **Delete on termination.**
