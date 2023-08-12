# Auto Scaling Groups



#### What are Auto Scaling Groups?

Auto Scaling Groups are the structure that allows the scale servers quickly when the load on the system changed over time. So that when the traffic on your application increased, it automatically scale-out(increases) the number of EC2 instances that your apps run on. The vice-versa of this rule (scale-in: decrease) is valid too.

<figure><img src="https://docs.aws.amazon.com/images/autoscaling/ec2/userguide/images/as-basic-diagram.png" alt=""><figcaption></figcaption></figure>

* Easily can be set to minimum and maximum running instances number
* Automatically registers new EC2 instances to load balancer
* Re-create an EC2 instance in case a previous one is terminated(unhealthy)
* ASG is free
* It is also possible to scale ASG with CloudWatch triggering(according to the metrics ASG is triggered)

