# VPC Fundamentals

VPC (Virtual Private Cloud) is a private network that allows you to deploy your resources. With VPC we need to know some concepts. They are like this:

* **Subnets**: allow us to partition our network inside our VPC. Two different types of subnets are we can be mentioned about it.
  * **Public** **Subnet**: This type of subnet is accessible over the internet
  * **Private** **Subnet**: Unlike the Public Subnets these ones are not accessible over the internet.
* **Route Table**: It allows us to define routing between the internet and subnets
* **Internet Gateway**: It helps VPC instances to connect with the Internet. It can be both way connection internet to subnet and subnet to internet
* **NAT Gateway:** They are separated by management types like Self( NAT Instances) and AWS-Managed (NAT Gateway). An important point is thanks to NAT,  Private subnets are available to access the internet while remaining private. It is one way connection subnet to internet.
* **Network Access Control List (NACL)**:&#x20;
  * It is a firewall which controls traffic **from** and **to** <mark style="color:red;">subnets</mark>.
  * Can ALLOW and DENY rules
  * Rules include only IP addresses.
  * NACL is attached at the Subnet level
* **Security Groups**:
  * It is a firewall that controls traffic to and from <mark style="color:red;">Elastic Network Interface (ENI)/ EC2 instance</mark>
  * Can have only ALLOW rules
  * Rules include IP addresses and other security groups
* **VPC Flow Logs**:
  * Capture information about IP traffic going into your interfaces
  * Helps to monitor and kind of connectivity issues like subnet to subnet, internet to subnet or subnet to the internet.
  * Also allows us to capture network information from AWS-managed interfaces. Like ElastiCache, Elastic Load Balancers, Aurora, RDS etc.
  * VPC Flow logs data can be reachable S3, Kinesis and CloudWatch too.
* **VPC Peering**:
  * It allows us to connect two VPCs each others
  * Their IP addresses must not be overlapped
  * VPC Peering Connection is <mark style="color:red;">not transitive in case of more than three VPC etc</mark>. Each VPC peering must be set between all pairs
* **VPC Endpoints:**
  * They are extremely important. It allows us to connect AWS services privately without going to public www network
  * It enhances the security and decreases the latency to reach the AWS services&#x20;
  * VPC Endpoints for S3 and DynamoDB rest of the services VPC Endpoint Interface
  * <mark style="color:red;">**Only used within your VPC**</mark>&#x20;
* **Site-to-Site VPN**: It allows connection of an On-Premise VPN to AWS on the internet publicly (Connection is encrypted)
* **Direct Connect**: Establishing a <mark style="color:red;">**physical**</mark> connection between AWS and on-premises. Even connection is private, fast and secure, the connection takes at least a month.
