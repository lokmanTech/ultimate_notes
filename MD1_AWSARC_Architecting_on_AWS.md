# Architecting on AWS
Architecting on AWS covers the fundamentals of building IT infrastructure on AWS. The course is designed to teach solutions architects how to optimize the use of the 
AWS cloud by understanding AWS services and how these services fit into cloud-based solutions. Because architectural solutions may differ depending on industry, 
type of applications, and size of business, this course emphasizes AWS cloud best practices and recommended design patterns to help students think through the process of 
architecting optimal IT solutions on AWS. It also presents case studies throughout the course that showcase how some AWS customers have designed their infrastructures and 
the strategies and services they implemented. Opportunities to build a variety of infrastructures via a guided, hands-on approach are also provided.

|Contents|Description|
|:------:|:---------:|
|Module 1|Architecting Fundamentals|
|Module 2|Account Security|
|Module 3|Networking 1|
|Module 4|Compute|
|Module 5|Storage|
|Module 6|Database Services|
|Module 7|Monitoring and Scaling|
|Module 8|Automation|
|Module 9|Containers|
|Module 10|Networking 2|
|Module 11|Serverless|
|Module 12|Edge Services|
|Module 13|Backup and Recovery|

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


## Module 5: Storage

Module Overview:
- Business requests
- Storage services
- Amazon Simple Storage Service (Amazon S3)
- Shared file systems
- Data migration tools
- Present solutions
- Capstone check-in
- knowledge check

### Business requests
We need to understand on;
- What are some services to consider when looking at block, file and object storage?
- How do we choose the right object storage solution for my use case?
- What are some file-based options for building secure and scalable storage in the AWS Cloud?
- How can we move lots of data to the cloud in a relatively short time period?

### Cloud Storage
In cloud in consist three main type, **Block storage**, **File Storage** & **Object storage**.

**Block Storage**
Raw storage. Data organized as an array of unrelated blocks.

AWS: Amazon Elastic Block Store (Amazon EBS)

**File Storage**
Unrelated data blocks managed by a file (serving) system. Native file system places data on disk.

AWS:
- Amazon Elastic File System (Amazon EFS)
- Amazon FSx

**Object Storage**
Stores virtual containers that encapsulate the data, data attributes, metadata and object IDs.

AWS:
- Amazon Simple Storage Service (Amazon S3)
- Amazon S3 Glacier

### Amazon S3 overview


### Securing Objects
#### Amazon S3 access control
#### Bucket policies
#### Amazon S3 Block Public Access
#### Amazon S3 Access Points
#### Server-side encryption key types

### Storing Object

[USE AWS POLICY GENERATOR](https://awspolicygen.s3.amazonaws.com/policygen.html)

#### Amazon S3 Storage Classes
From Lower Cost (infrequent access) to Higher cost (frequent access)
- S3 Glacier Deep Archive
- S3 Glacier Flexible Retrieval
- S3 Glacier Instant Retrieval
- S3 One Zone-IA
- S3 Standard-IA
- S3 Standard

**Amazon S3 Intelligent-Tiering**
Amazon S3 Intelligent-tiering is the only storage class that delivers automatic storage cost savings when data access patterns change, withou performance impact or operational overhead. Your data moves between access tier as usage patterns change.

**Amazon S3 Glacier storage class benefits**
1. Cost-effective storage
2. Flexible data retrieval
3. Secure and compliant
4. Scalable and durable

**Amazon S3 Versioning**
Amazon S3 uses object storage. Thus, if you want to change a part of a file, you must make the change and then re-upload the entire modified file.

Bucket that use versioning can help you recover objects from accidental deletion or overwrite: 
- If you delete an object, instead of removing it permanently, Amazon S3 inserts a delete marker, which becomes the current object version.
- If you overwrite an object, it results in a new object version in the bucket.
When S3 Versioning is turned on, you can restore the previous version of the object to correct the mistake.

You can use S3 Object Lock for data retention or protection. By using the write once, read many (WORM) model, you can prevent accidental overwrites or deletions within Amazon S3 storage. Use retention periods for locking an object for a fixed period of time, or a legal hold for a lock until explicitly removed.

**Lifecycle Policies**
With S3 lifecycle policies, you can delete or move objects based on age. You should automate the lifecycle of your data that is stored in Amazon S3. Using S3 Lifecycle policies, you can have data cycled at regular intervals between different Amazon S3 storage types.

In this way, you reduce your overall cost because you are paying less for data as it becomes less important with time. In addition to beign able to set lifecycle rules per object, you can also set lifecycle rules per bucket.

**Replicating S3 Objects**

**Amazon S3 Multipart upload**

**Amazon S3 Event Notifications**

**Amazon S3 cost factors**

#### Shared file systems overview

**Shared file systems**

**Amazon EFS**

**Amazon EFS Benefits**

**Amazon FSx**

#### Data migration tools

**AWS Data migration tools**

**AWS Storage Gateway**

**Storage Gateway Types**
- Amazon S3 File Gateway
- Amazon FSx File Gateway
- Tape Gateway
- Volume Gateway

**Storage Gateway Architecture**

**AWS DataSync**

**AWS Snow Family Service models**


### Module 6:  Database Service

**AWS Database Services**

**Relational and nonrelational databases**

**Choosing the right database**

**Managed and unmanaged services**

### Amazon RDS

**Amazon RDS features**

**Amazon RDS database engines**

**Amazon RDS Multi-AZ deployments**

**Amazon RDS Multi-AZ failover**

**Read replicas**

**Data encryption at rest**

**Amazon Aurora**

**Aurora DB Clusters**

**Aurora Serverless v2 for PostgreSQL and MySQL**

#### Amazon DynamoDB

**DynamoDB**

**Key-value data**

**DynamoDB use case 1**

**DynamoDB use case 2**

**DynamoDB tables**

**DynamoDB capacity and scaling**

**DynamoDB Consistency options**

When your application writes data to a DynamoDB table and receives an HTTP 200 responses (OK), the write has occured and is durable. The data is eventually consistent across all storage locations, usually within one second or less. DynamoDB supports eventually consistent and strongly consistend reads

Eventually consistent reads

Strongly consistent read

**DynamoDB global tables**

#### Database caching
**What should you cache?**
- data that requires a slow and expensive query
- Frequently accessed data
- information that is relatively static

**Caching architecture**

**Common caching strategies - Lazy loading**
1. Data request to the cache by the application
2. Cache miss
3. Missing data that the application requested from the database
4. Data returned from the db
5. Returned value that the application writes to the caches

**Commong caching strategies - write-through**

1. Application writes data to the db
2. Application also writes data to the cache

**Managing your cache**

Cache Validity

To min stale data you can add a time to live (TTL) value to each application writes

Managing memory

When your cache memory is full, your cache evicts data based on your selected eviction policy. Eviction policies can evaluated any combination of the following

**Amazon ElasticCache**

- Extreme performance
- Fully managed
- Easily scalable

**Elasticache engines**

**Amazon DynamoDB Accelerator (DAX)**

#### Database migration tools

**AWS databases migration service**

**AWS Schema Conversion tool**

### Module 7: Monitoring and Scaling

**Monitoring**

**Reasons for monitoring**

**Amazon CloudWatch**

**CloudWatch metrics**

**Types of logs**

**CloudWatch Logs example**

**AWS CloudTrail**

**Example: CloudTrail Log**

**VPC Flow Logs**

**Contents of a flow log record**

#### Alarms and events

**CloudWatch alarms**

**Alarm states**

**Alarm components**

**Amazon EventBridge**

**Example: CloudWatch alarm automated response**

#### Load balancing

**Elastic Load Balancing (ELB)**

**ELB load balancer types**

**ELB load balancer components**

**ELB common features**

|Feature|Application Load Balancer|Network Load Balancer|Gateway Load Balancer|
|:-----:|:-----:|:-----:|:-----:|
|Health Checks|YES|YES|YES|
|CloudWatch metrics|YES|YES|YES|
|Logging|YES|YES|YES|
|SSL offloading|YES|YES| |
|Connection draining|YES|YES|YES|
|Preserve source IP address|YES|YES|YES|
|Static IP address|**|YES||
|Lambda function as a target|YES|||
|Redirects|YES|||
|Fixed-response actions|YES|||

#### Auto scaling

**AWS Auto Scaling**
1. Explore your application
2. Discover what you can scale
3. Choose what to optimize
4. Track scaling as it happens

**Amazon EC2 Auto Scaling**
- Helps you control EC2 instances available to handle load for your application
- Launches or terminates your AWS resources based on specified conditions
- Registered new instances with load balancers, when specified

**Elasticity: Scaling in and out**
Using cloud tech, you can fit supply to demand through elastic cllud resources.

**Amazon EC2 Auto Scaling Components**

1. Launch templates: What resources do you need?
2. Amazon EC2 Auto Scaling Group: Where and how many do you need?
3. Auto scaling policy: When and for how long do you need them?

**Launch Template**

**Group capacity**

**Invoke Amazon EC2 Auto Scaling**
Invoke scaling with:
- Health status checks
- Cloudwatch alarm
- Schedules
- Manual scaling

**Ways to scale with Amazon EC2 Auto Scaling**
1. Scheduled
2. Dynamic: according to demand eg. touch 70% will scale it
3. Predictive: this is AI will review accound previous report to predict accordingly.

**Optimize cost with Amazon EC2 Auto Scaling**
- On-demand Instances
- Savings Plans
- Spot Instances

### Module 8: Automation

**Infrastructure as code (IaC)**


**Benefits of IaC - Reusability**

**Benefits of IaC - Updates**

**AWS CloudFormation**

**Understanding CloudFormation**
- Written as JSON or YAML
- Describes the resources to be created or modified
- Treated as source code
  - Code review
  - Version controlled

**Stacks**

**Using Multiples templates**


A layered architecture

- Identity: AWS identity and Access management (IAM) users, groups, roles
- Base network: VPCs, Internet gateways, Virtual Private Networks (VPNs), NAT Gateway
- Shared: Databases, common monitoring or alarms, subnets, security groups
- Backend: Customers, campaign, products, analytics, marketing collateral
- Frontend: Web interface, admin interface, analytics dashboard

#### Infrastructure management

**Infrastructure tools**

Deployments tools from Control to Convenience
1. AWS CloudFormation
2. AWS Cloud Development Kit (AWS CDK)
3. AWS Solutions Library
4. AWS Elastic Beanstalk

Management tools
1. AWS Systems Manager

**AWS Elastic Beanstalk**

**AWS Solutions Library**

**AWS CDK**

**AWS Systems Manager**

**Amazon CodeWhisperer**

**What is Amazon CodeWhisperer?**
AI-powered code generator for IDEs and code editors

AI coding companions:
- Generates code suggestions based on comments and existing code
- Offers real-time support for code authoring directly within your integrated development environment (IDE)
AI Security scanner:
- Helps identify hard-to-find vulnerabilities
- References multiple standards and best practices

**Code generation**

**Security Scan**

**Benefits of Amazon CodeWhisperer**

Value to developers
- Increase velocity
- Spend less time writing code
- Receive help directly within your IDE
- Find security vulnerabilities in your code

Value to organizations
- Use at all experience levels
- Support open-source attribution
- Reduce the risk of security vulnerabilities
- Increase code quality and developer productivity



[AWS got Quick Start Template](https://aws.amazon.com/quickstart/?solutions-all.sort-by=item.additionalFields.sortDate&solutions-all.sort-order=desc&awsf.filter-content-type=*all&awsf.filter-tech-category=*all&awsf.filter-industry=*all)


### Module 9: Containers

#### Microservices overview

**Loose coupling**

Anti-pattern
- Web servers tightly coupled to application servers

Best practice
- Decouple with a load balancer via Elastic Load Balancing

Traditional monolithics infrastructure revolve around chains of tightly integrated servers, each with a specific purpose.

**Microservices**

Microservices are an architectural and organizational approach to software development. Using a microservices approach, you design software as a collection of small services. Each service is deployed independently and commnunicates over well-defined APIs. This process speeds up your deployments cycles, foster innovation, and improves both maintainbility and scalability of your applications.

**Containers**
The benefits of a microservices-oriented architecture should trickle down to an infrastructure level. You can achieve that with containers.

Containers are:
- Repeatable
- Self-contained environments
- Faster to spin up and down than VMs
- Portable
- Scalable

**Containers and microservices**
Containers are an ideal choice for microservices architecture because they are scalable, portable and continuously deployable.

**Levels of abstraction and virtualization**
A bare metal server runs a standalone operating system (OS) with one or many application by using libraries. Costs remain constant, whether the server is running at 0% usage or 100% usage. To scale you must buy and configure additional servers. It is also difficult to build applications that work on multiple servers because the OS on those servers would need to be the same, You also must synchronize the application lib ver.

**Containers on AWS**
- Running containers directly on Amazon EC2 requires you to manage scalling, connectivity and maintenance.
- Using an orchestrating tool helps manage:
    - Scheduling
    - Placement
    - Networking
    - Monitoring

#### Container Services

**Running containers on AWS**

**Amazon ECR**

**Amazon ECS Orchestration**

**Amazon ECS features**
- Fully managed
- Service discovery
- AWS integrations
- Work with common dev workflows

**Monolithic to container-based microservices**

**Amazon EKS**
Kubernetes
- Run applications at scale
- Run anywhere
- Seamlessly move applications
- Add new functionality

**Amazon EKS solutions**
1. Amazon EKS run kubernetes on AWS
2. Provision an Amazon EKS cluster
3. Fargate Deploy Serverless containers or Amazon EC2 Deploy worker nodes for your Amazon EKS cluster
4. Connect to Amazon EKS
5. Run Kubernetes application

**AWS Fargate**
1. Build a container image
2. Amazon ECS or Amazon EKS to Define the images and resources needed for your app
3. AWS Fargate Launch containers, and fargate manages all of the underlying containers infrastructure
4. Launch containers Fargate runs your containers for you
5. Manage containers Amazon ECS scales your application and manages your containers for availability.

**Choosing AWS containers services**

### Module 11: Serverless

#### Amazon Simple Queue Service (Amazon SQS)

**Amazon SQS**

**Loose coupling with Amazon SQS**
- Loosely couples application components
- Uses asynchronous processing
- Creates tolerance for failed steps
- Absorbs demand spikes

In this example, a producer application creates customer orders and sends them to an Amazon SQS queue. A consumer application processes orders from the producer application tier. The consumer application polls the queue and receives messages. It then records the messages in an Amazon Relational Database Service (Amazon RDS) database and deletes the processed messages from the SQS queue. Amazon SQS sends messages that cannot be processed to a dead-letter queue where they can be processed later.

**Amazon SQS use cases**
There are many differents ways to use SQS queues
1. Work queues: using FIFO
2. Buffering and batch operations: messages will que and will be deliver by batch
3. Request offloading: enqueue slower requests
4. Auto Scaling: add another process to scale up the rate of messages

**SQS queue types**
Amazon SQS offers two types of message queues.

1. Standard queue: support at least once message delivery and provide best effort order. Messages are generally delivered in the same order in which they are sent. However, because of the hihgly distributed architecture, more than one copy of a message might be delivered out of order. Standard queues can hanlde a nearly unlimited number of API calls per second. You can use standard messages queues if your application can process messages that arrive more than once and out of order.
2. FIFO queue: designed to enhance messaging between application when the order of operation and events is critical or where duplicates can't be tolerated. FIFO queues also provide exactly once processing, but have a limited number of API calls per second.

**Optimizing your amazon SQS queue configurations**

**When to use message queues**

|Good to use|Not Good to use|
|:------:|:-------:|
|Service-to-service communication|Selecting specific messages|
|Asynchronous work items|Large messages|
|State change notification||

#### Amazon Simple Notification Service (Amazon SNS)

**Amazon SNS**
|Type of subscribers|
|:----:|
|Email/Email-JSON|
|Mobile text messaging (SMS)|
|Mobile push notification|
|HTTP/HTTPS|
|AWS Lambda|
|Amazon SQS|
Kinensis Data Firehouse|

**Use cases for Amazon SNS**
- Amazon CloudWatch alarm notification
- Email and SMS messages for a mailing list
- push notifications for app updates

**Characteristic of Amazon SNS**
- Single published message
- No recall options
- HTTP or HTTPS retry
- Standard of FIFO topics

**Amazon SNS publish to multiple SQS queues
- Using highly available services such as Amazon SNS to perform basic message routing is an effetive way of distributing messages to microservices. The two main forms of communication between microservices are request-responses and observer.

**Amazon SNS and Amazon SQS**

|Features|Amazon SNS|Amazon SQS|
|:----:|:-----:|:-----:|
|Message persistence|No|Yes|
|Delivery mechanism|Push(passive|Poll(active)|
|Producer and consumer|Publisher and subscriber|Send or receive|
|Distribution model|One to many|One to one|

#### Amazon Kinesis

**Collecting and analyzing streaming data**

**Kinesis Data Streams Overview**

**Kinesis Data Firehose overview**

**































