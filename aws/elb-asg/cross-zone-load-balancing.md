# Cross-Zone Load Balancing

Check the below image taken from the original AWS documentation. If the cross-zone load balancing would be inactive, the incoming requests would be divided equally between the first and second load balancer. But when we think of this situation behind the first load balancer there are two ec2 instances so all incoming requests would be handled by these two instances out of ten. So that this may be the cause of imbalances and unwanted situations.

<div align="center" data-full-width="true">

<figure><img src="https://docs.aws.amazon.com/images/elasticloadbalancing/latest/userguide/images/cross_zone_load_balancing_enabled.png" alt=""><figcaption></figcaption></figure>

</div>

As you see in the image when we activate the cross-zone load balancing all incoming requests will be divided between total ec2 instances. So in the end every instance behind the load balancers will face the same amount of load.



* **Application Load Balancer**: <mark style="color:red;">**(default enabled)**</mark> and <mark style="color:red;">**no charges**</mark>
* **Network & Gateway Load Balancer**: (**disabled by default**) and **extra fees if it is enabled**
* **Classic Load Balancer: (disabled by default) **<mark style="color:red;">**no charges if it is enabled**</mark>

