# Architecting on AWS
Architecting on AWS covers the fundamentals of building IT infrastructure on AWS. The course is designed to teach solutions architects how to optimize the use of the 
AWS cloud by understanding AWS services and how these services fit into cloud-based solutions. Because architectural solutions may differ depending on industry, 
type of applications, and size of business, this course emphasizes AWS cloud best practices and recommended design patterns to help students think through the process of 
architecting optimal IT solutions on AWS. It also presents case studies throughout the course that showcase how some AWS customers have designed their infrastructures and 
the strategies and services they implemented. Opportunities to build a variety of infrastructures via a guided, hands-on approach are also provided.


### Module 3 - NETWORK

in AWS Networking
192.168.0.0 - Network ID
192.168.0.1 - Gateway
192.168.0.2/3 - Reserve ID
192.168.0.255 - Broadcast ID

Address can be assign using 2 methods 

1. Static IP
2. DHCP

APIPA - 169.254.xxx.xxx

-----------------------------------------------

IPv6 = 128bits addressing scheme = 2^128 = 3.4 undercillions = trilions of trilions of trilions

AA:BB:CC:DD:EE:FF:GG:HH = 8 octets (1 octet = 2 bytes = 16 bits), so 8 octets * 16 bits = 128 bits  

global ip - internet/public
link local - apipa in ipv4
local add - private

AWS IP addresss
Define subnet 192.168.10.0/24 --- 192.168.10.0 ---> 192.168.10.255 ---> Usable 192.168.10.1 - 192.168.10.254

**IANA - organization managa IP address**

192.168.0.177

|Class|Range|SubnetMask/CIDR|Network or Host|
|:---:|:---:|:-------------:|:-------------:|
|A|1.0.0.0 ---> 126.255.255.255|255.0.0.0 OR /8|126 Networks / 16,777,216 Hosts minus 2 (but for AWS minus 5)|
|B|128.0.0.0 ---> 191.255.255.255|255.255.0.0 OR /16| 16,384 Networks / 65, 536 Hosts minus 2 (but for AWS minus 5)|
|C|192.0.

No need to calculate, we got online calculator : [IP Subnet Calculator](https://www.calculator.net/ip-subnet-calculator.html) 

### VPC fundamentals



