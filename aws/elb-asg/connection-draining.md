# Connection Draining

Connection draining is a concept that the load balancer detects if some EC2 instances are not giving a response(in the situation of deregistering or unhealthy etc.) for a specific time period then the load balancer starts the dispatching new incoming requests to other EC2 instances and stops sending new requests the that EC2 instance.

<figure><img src="https://docs.aws.amazon.com/images/AmazonECS/latest/bestpracticesguide/images/load-balancer-connection-draining.png" alt=""><figcaption></figcaption></figure>

* The default time period is 300 but it can be set between 1 to 3600 secs
* Can be disabled by setting the value to 0
* Prefer to set low value if requests are short
