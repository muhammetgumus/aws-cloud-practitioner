# Auto Scaling Groups



### What are Auto Scaling Groups?

Auto Scaling Groups are the structure that allows the scale servers quickly when the load on the system changed over time. So that when the traffic on your application increased, it automatically scale-out(increases) the number of EC2 instances that your apps run on. The vice-versa of this rule (scale-in: decrease) is valid too.

<figure><img src="https://docs.aws.amazon.com/images/autoscaling/ec2/userguide/images/as-basic-diagram.png" alt=""><figcaption></figcaption></figure>

* Easily can be set to minimum and maximum running instances number
* Automatically registers new EC2 instances to load balancer
* Re-create an EC2 instance in case a previous one is terminated(unhealthy)
* ASG is free
* It is also possible to scale ASG with CloudWatch triggering(according to the metrics ASG is triggered)



### Auto Scaling Group Policies

There is more than one ASG policy. They are as below

* **Target Tracking Scaling**: e.g. we want the average ASG CPU to stay at around %40
* **Simple / Step Tracking**: e.g. when a Cloud Watch alarm is triggered CPU is more than %70 adds the 2 more instances or the CPU is less than %30 percent removes instances
* **Scheduled Actions**: Let's say you know every Friday between 5 P.M. to 3 A.M. you are hitting the most traffic then rules to set minimum capacity to your min capacity + new 3 instances these time periods.
* **Predictive Scaling**: continually forecast load and schedule scaling ahead. Steps are like that           **Analyze historical load** -> **Generate forecast** -> **Schedule scaling actions.** This scaling type is <mark style="color:red;">**ML powered**</mark>

**Some Useful Metrics to scale on**

* CPU Utilization
* RequestCountPerTarget
* Average Network In / Out
* Any Custom metric

<mark style="color:red;">**Cooldown Period**</mark> :  After scaling you are in cooldown period so that. In this time ASG will not start or terminate new instances.
