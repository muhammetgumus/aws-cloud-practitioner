# Amazon EFS(Elastic File System)

The official document of EFS describes EFS really succinctly. Let's look at it.

> Amazon Elastic File System (EFS) is designed to provide serverless, fully elastic file storage that lets you share file data without provisioning or managing storage capacity and performance.

* Managed NFS (Network File System) that can be mounted on many EC2.
* EFS works with EC2 instances with multi-AZ
* Highly available, scalable and expensive.
* Use cases: content management, web serving, data sharing etc.
* <mark style="color:red;">Compatible with Linux-based AMIs.(Not Windows)</mark>
* <mark style="color:red;">Scales automatically and based on the</mark> <mark style="color:red;"></mark><mark style="color:red;">**Pay Per Use**</mark> <mark style="color:red;"></mark><mark style="color:red;">billing type.</mark>

