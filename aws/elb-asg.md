---
description: Elastic Load Balancing & Auto Scaling Groups
---

# ELB & ASG

Before diving into the explanations of ELB & ASG we should understand what they are. So let's start with the Load Balancers.&#x20;

#### What is a Load Balancer?

Load balancers are the servers that forward traffic to multiple servers (like EC2 instances) downstream.

#### Why use a Load Balancer?

* Spread the loads to multiple downstream instances
* Expose a single point of access (DNS) to your application
* Handle failures seamlessly and do regular <mark style="color:red;">**health checks**</mark>
* Provide SSL termination for your websites
* High availability across zones
* Separate public traffic from private traffic

#### What is AWS Elastic Load Balancer ?

Elastic Load Balancer (ELB) is managed load balancer.

* AWS takes care of upgrades, maintenance and availability
* AWS guarantees that it will be working
* It costs less setup your own load balancers
* Integrated with lots of AWS services

#### ELB Types

You will see the types of load balancers. It is always recommended to use new generations.

* **Classic Load Balancer **<mark style="color:red;">**(Deprecated)**</mark> -> Old generation. HTTP, HTTPS, TCP, SSL
* **Application Load Balancer** -> HTTP, HTTPS, Websocket
* **Network Load Balancer** -> TCP, TLS, UDP
* **Gateway Load Balancer** -> Operates at layer 3 (IP Protocol)

### What is ALB?

Application Load Balancers is Layer 7

* Load balancing to multiple applications on the same machine
* Load balancing to multiple HTTP apps across machines
* Support HTTP/2 and WebSocket
* Support redirects (HTTP to HTTPS etc.)
* Routing tables to different target groups
* Great fit for microservices and containerized apps

#### Target Groups

We can think of target groups as the destinations that load balancer routes the traffic&#x20;

* EC2 Instances
* ECS tasks
* Lambda Functions
* IP Addresses (private IPs)

ALB can route multiple target groups

