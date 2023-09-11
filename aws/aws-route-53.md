# AWS Route 53

### What is DNS?

Before deep diving into AWS Route 53, we should understand the DNS and the logic behind it. Firstly DNS stands for **Domain Name System**. DNS is basically a server that maps the IP addresses of web apps and websites to easily rememberable names.

Every day we surf the internet and check lots of webpages. But we do not know their IPs. The only thing that we need to keep in mind is their names. Actually this job (remembering and knowing the IP addresses) is done by DNS for us.  Let's think that we go to a web browser and write the website name on the address bar behind the scene DNS takes the role of finding the IP addresses and turn us to the results. Thanks to it we don't need to remember lots of numbers in our minds :) It can easily be said that the backbone of the internet.

### DNS Terminologies

Not it is time to check some terminologies about DNS

* Domain Registrar: GoDaddy, AWS Route53 etc.
* DNS Records: CNAME, A, AAA, NS
* Zone File: contains the DNS records
* Name Server: Resolves the DNS queries
* Second Level Domain:
* Top Level Domain: like **.com .org .gov** etc. &#x20;

Let's examine the **https://api.www.muhammetgumus.dev.** URL part by part&#x20;

* Root: **.**
* Top Level Domain: **.dev**
* Second Level Domain: **www.muhammetgumus.dev**
* Sub Domain: **.muhammetgumus.dev**
* Fully Qualified Domain Name: **api.www.muhammetgumus.dev**&#x20;
* Protocol: **https**
* URL : **https://api.www.muhammetgumus.dev.**

After this explanation, we can look at what Route 53 is.

### AWS Route 53

Let's check the general features of Route 53

* AWS Route 53 is Amazon's highly available (100%), scalable, fully managed and authoritative (user can update DNS records) DNS service.
* It is also a Domain Registrar which means you can register any domain that you would like of course if it is not taken by any other clients.
* It also gives us the ability to check the health of our resources.&#x20;
* And finally, we may be curious about why it is named **53**. Because It comes from the traditional DNS port.

### Route 53 - Record Types

* A: maps a hostname to IPv4
* AAAA: maps a hostname to IPv6
* CNAME: maps a hostname to another hostname. Be careful target domain name must have an A or AAAA record
* NS: Name servers for the Hosted Zone

### Route 53 - Hosted Zones

It is a container for records that define how to route traffic to a domain and its subdomains

* **Public Hosted Zones:** Contains records that specify how to route traffic on the internet&#x20;
* **Private Hosted Zones:** Contain records that specify how you route traffic within one or more VPCs

### Route 53 - Routing Policies

There are more than one routing policies while working with Route 53. They are as follows

* **Simple**: Typically route traffic to a single resource but may also return multiple values. In that situation, clients can select one of those values randomly
* **Weighted**: In this type of routing policy incoming requests are routed to the different resources according to their weights. For example, let's say we have three resources and we set the weight percents like 70(Resource 1) - 30(Resource 2) - 10(Resource 3). After setting this policy every 70 of 100 requests will be handled by Resource 1, 20 by Resource 2 and 10 by Resource 3.
* **Latency**: Latency-based routing policy allows clients to be routed to the resources that latencies the lowest one to the clients.
* **Failover**: This type of routing policy is based on the Primary and Secondary resources. It means firstly requests are routed to the primary resource until they are unhealthy. If the primary resource is unhealthy then the requests are routed to the secondary resources
* **Geolocation**: Routing is based on user location. E.g. if the user's request comes from a country that is located in Europe then route it to the 1.2.3.4 IP Addressed resource, if its requests come from the USA then route the request to the 5.6.7.8 IP Addressed resource. It usually used for content localization, restriction etc.
* **Geoproximity**:  This type of routing is based on the user's geolocation and also bias values. Higher bias values holding resources will get higher traffic.
* **IP-Based Routing**: According to the user's IP address ranges traffic will be routed to the suitable resources.
* **Multi-Value**: In this type of routing policy, clients will get multi-answer when we check our request like nslookup or dig etc.
