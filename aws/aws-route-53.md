# AWS Route 53



### What is DNS?

Before deep diving into AWS Route 53, we should understand the DNS and the logic behind it. Firstly DNS stands for **Domain Name System**. DNS is basically a server that maps the IP addresses of web apps and websites to easily rememberable names.

Every day we surf the internet and check lots of webpages. But we do not know their IPs. The only thing that we need to keep in mind is their names. Actually this job (remembering and knowing the IP addresses) is done by DNS for us.  Let's think that we go to a web browser and write the website name on the address bar behind the scene DNS takes the role of finding the IP addresses and turn us to the results. Thanks to it we don't need to remember lots of numbers in our minds :) It can easily be said that the backbone of the internet.



### DNS Terminologies

Not it is time to check some terminologies about DNS

* Domain Registrar: GoDaddy , AWS Route53 etc.
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
