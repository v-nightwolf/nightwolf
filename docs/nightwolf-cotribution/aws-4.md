# AWS Interview Questions & Answers - 4
---
These are AWS interview questions for experienced professionals.  You will find these questions very helpful in your AWS professional role interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---


1. How many Elastic IP address can be associated with a single account?

        Ans: 5

2. What is the name to the additional network interfaces that can be created and attached to any Amazon EC2 instance in your VPC?

        Ans: Elastic Network Interface

3. You have configured ELB with three instances connected to that. If your instances are unhealthy or terminated, the traffic should be
automatically replaced to another instance, what type of service can be used to achieve this requirement?

        Ans: Fault Tolerance

4. After configuring ELB, you need to ensure that the user requests are always attached to a single instance. What setting can you use?

        Ans: Sticky session

5.  Which of the following metrics cannot have a cloud watch alarm?

      - EC2 instance status check failed
      - EC2 CPU utilization
      - RRS lost object
      - Auto scaling group CPU utilization

              Ans: RRS lost object

6. Which of the below mentioned service is provided by Cloud watch?

      - Monitor estimated AWS usage
      - Monitor EC2 log files
      - Monitor S3 storage
      - Monitor AWS calls using Cloud trail

            Ans: Monitor estimated AWS usage

7. A user has Launched an EC2 instance which of the below mentioned statements is not true respect to instance addressing?

      - The private IP addresses are not reachable from the internet
      - The user can communicate using the private IP across regions
      - The private IP address and pubic IP address for an instance are directly mapped to each other using NAT
      - The private IP address for the instance is assigned using DHCP

            Ans: The user can communicate using the private IP across regions

8. Which of the following service provides the edge – storage or content delivery system that caches data at different locations?

      - Amazon RDS
      - Simple DB
      - Amazon Cloud Front
      - Amazon associates web services

            Ans: Amazon Cloud Front

9. A user is launching an instance under the free usage tier from the AMI with a snapshot size of 50 GB. How can the user launch the instance under the free usage tier?

      - Launch a micro instance
      - Launch a micro instance, but in the EBS configuration modify the size of EBS to 50 GB.
      - Launch a micro instance, but do not store the data of more than 30 GB on the EBS storage.
      - It is not possible to have this instance under the free usage tier

            Ans: It is not possible to have this instance under the free usage tier

10. What are the possible connection issues you can face while connecting to your instance?

      - Connection timed out
      - Server refused our key
      - No supported authentication methods available
      - All of the above

            Ans:  All of the above

11. You are enabled sticky session with ELB. What does it do with your instance?

      - Routes all the requests to a single DNS
      - Binds the user session with a specific instance
      - Binds the user IP with a specific session
      - Provides a single ELB DNS for each IP address

            Ans: Binds the user session with a specific instance

Q137. Which is a main email platform that provides an easy, cost effective
way for you to send compliance and receive a response using your own
email address and domains?
SES
SNS
SQS
SAS
Ans: SES
Q138. Which type of load balancer makes routing decisions at either the
transport layer or the application layer and supports either EC2 or VPC.
Application Load Balancer
Classic Load Balancer
Primary Load Balancer
Secondary Load Balancer
Ans: Classic Load Balancer
Q139. AWS Cloud Front has been configured to handle the customer
requests to the web server launched in Linux machine. How many
requests per second can Amazon Cloud Front handle?
1000
100
10000
There is no such limit
Ans: There is no such limit
Q140. You are going to launched one instance with security group. While
configuring security group, what are the things you have to select?
Protocol and type
Port
Source
All of the above
Ans: Source
Q141. Which is virtual network interface that you can attach to an
instance in a VPC?
Elastic IP
AWS Elastic Interface
Elastic Network Interface
AWS Network ACL
Ans: Elastic Network Interface
Q142. You have launched a Linux instance in AWS EC2. While
configuring security group, you have selected SSH, HTTP, HTTPS
protocol. Why do we need to select SSH?
To verity that there is a rule that allows traffic from your computer to port 22
To verify that there is a rule that allows traffic from EC2 Instance to your computer
Allows web traffic from instance to your computer
Allows web traffic from your computer to EC2 instance
Ans: To verify that there is a rule that allows traffic from EC2 Instance to your computer
Q143. You need to quickly set up an email service because a client needs
to start using it in the next hour. Amazon service seems to be the logical
choice but there are several options available to set it up. Which of the
following options to set up AWS service would best meet the needs of the
client?
Amazon SES console
AWS Cloud Formation
SMTP interface
AWS Elastic Beanstalk
Ans: Amazon SES console
Q144.You have chosen a windows instance with Classic and you want to
make some change to the security group. How will these changes be
effective?
Security group rules cannot be changed
Changes are automatically applied to windows instances
Changes will be effective after rebooting the instance in that security group
Changes will be effective after 24-hours
Ans: Changes are automatically applied to windows instances
Q145. Load Balancer and DNS service comes under which type of cloud
service?
IAAS-Network
IAAS-Computational
IAAS-Storage
None of the above
Ans: IAAS-Storage
Q146. You have an EC2 instance that has an unencrypted volume. You
want to create another encrypted volume from this unencrypted volume.
Which of the following steps can achieve this?
Just simply create a copy of the unencrypted volume, you will have the option to encrypt the
volume.
Create a snapshot of the unencrypted volume and then while creating a volume from the
snapshot you can encrypt it
Create a snapshot of the unencrypted volume (applying encryption parameters), copy the
snapshot and create a volume from the copied snapshot
This is not possible, once a volume is unencrypted, there is no way to create an encrypted
volume from this
Ans: Create a snapshot of the unencrypted volume (applying encryption parameters), copy
the snapshot and create a volume from the copied snapshot
Q147. Where does the user specify the maximum number of instances
with the auto scaling commands?
Auto scaling Launch Config
Auto scaling group
Auto scaling policy
Auto scaling size
Ans: Auto scaling Launch Config
Q148. A user is identify that a huge data download is occurring on his
instance he has already set the auto scaling policy to increase the instance
count when the network Input Output increase beyond a threshold limits
how can the user ensure that this temporary event does not result in
scaling
The network I/O are not affecting during data download
The policy cannot be set on the network I/O
There is no way the can stop scaling as it already configured
Suspend scaling
Ans: Suspend scaling
Q149. Which are the types of AMI provided by AWS?
EBS Backed
Instance Store backed
None its volume type and not AMI types
Both A and B
Ans: Both A and B
AWS Interview Questions and Answers for Freshers
Q150. What is the significance of forming Subnets?
A. Because, not enough hosts
B. To manage small number of hosts
C. To utilize the Volume available across different subnets
D. Smartly utilize network that have large number of hosts
The answer is: D
Q2: If you want to launch your instance on a single-tenancy platform,
which option you would select against Instance Tenancy Attribute
parameter?
A. One to one
B. Sole Owner
C. Dedicated
D. Reserved
The answer is: C
Q151. Which AWS Service you would use to transfer objects from your
data center, when you are using Amazon CloudFront?
A. AWS CloudWatch
B. AWS SNS Service
C. AWS SMS Service
D. AWS Direct Connect
The answer is: D
Q152 _____________ is a fully managed Data Warehouse service from
AWS?
A. Amazon Redshift
B. Amazon Neptune
C. Amazon Aurora
D. Amazon DynamoDB
The answer is: A
Q153. Which of the following statements are applicable to AWS Elastic
File System(EFS)?
A. EFS provides simple, scalable file storage for use with Amazon EC2
B. EFS with MS-Windows based EC2 instances is not supported
C. EFS supports the Network File System version 4 protocol
D. All of the above
The answer is: D
Q154. What is the role of Connection Draining?
A. Helps to launch an EC2 instance
B. Automatically terminates instances which are not in use
C. Establishes connection between EC2 and RDS instances
D. Auto Scaling wait for outstanding requests to complete before terminating instances when
CD is enabled
The answer is: D
Q155. What is the use of Lambda?
A. Lambda is used for running server-less applications
B. It is a testing tool from AWS
C. It is a database service from AWS
D. It is an Anti Virus software from AWS
The answer is: A
Q156. What is Application Load Balancing?
A. It is a feature of Elastic Load Balancing
B. Use to distribute traffic to different Target Groups
C. It is a service generating Elastic IPs for AWS customers
D. It is a kind of Firewall
The answers are: A and B
Q157. What are the uses of Elastic Beanstalk?
A. Quickly deploy and manage applications in the AWS Cloud
B. Supports Java, .NET, Node.js, PHP, Python applications
C. It is an Application Server from AWS
D. Use to deploy only Java-Beans applications
The answers are: A and B
Q158. Can you connect your company’s datacenter to the Amazon Cloud
network?
A. Not possible
B. You can connect thru a Dedicated N/W line
C. By establishing a Virtual Private Network (VPN) between your datacenter and VPC
D. Connect with a hotline
The answer is: C
Q159. You have commissioned PRIVATE servers in your premises. You
also distributed some of your workloads with the PUBLIC cloud. What
type of architecture is this?
A. Virtual Private Cloud
B. Community Cloud
C. Public Cloud
D. Hybrid Cloud
The answer is: D
Q160. DynamoDB _______________________. Which one of the following
is true regarding DynamoDB?
A. Manages Notification Service
B. Stores Metadata
C. Manages Queue Service
D. None of the above
The answer is: B
Q161: What are the significances of AWS CloudTrail?
A. Takes care of Message Queuing Service
B. It enables governance, compliance, operational auditing and risk auditing of your AWS
account.
C. Used as a database service
D. It provides an event history of your AWS account activities
The answers are: B and D
Q162. Which one is a global Content Delivery Network service that
securely delivers data, videos, applications, and APIs to your viewers with
low latency and high transfer speeds?
A. Amazon CloudWatch
B. Amazon CloudFront
C. Amazon CloudTrail
D. Amazon VPC
The answer is: B
Q163. Is AWS offering Reserved Instances facility for Multiple-Subnet
deployments?
A. Yes, available for all kind of instances
B. No, available only for Dedicated Tenancy
C. Offering only for LINUX based instances
D. None of the above
The answer is: A
Q164. Select the correct statement from the below:
A. You can have multiple ACLs for a subnet
B. Security Group is not necessary for an EC2 instance
C. You can attach multiple Zones/Subnets to a Route Table
D. You can create S3 bucket using AWS AMI templates
The answer is: C
Q165. Name the AWS DB Service which is Server-Less and NoSQL DB
which delivers consistent single-digit millisecond latency at any scale?
A. Amazon Redshift
B. Amazon Neptune
C. Amazon Aurora
D. Amazon DynamoDB
The answer is: D
Q166. Is this advisable to keep your Standby-Database instance in the
same zone where your primary instance is running?
A. Yes, you can keep
B. Possible only for MySQL instance
C. No, not recommended for any kind of DB instance
D. Recommended only for MS-SQL instance
The answer is: C
Q167. Can objects in S3 be delivered by Amazon CloudFront?
A. Yes, you can place any objects in S3 which CloudFront quickly delivers
B. CloudFront delivers only movie type objects
C. No, S3 cannot be integrated with CloudFront
D. Amazon VPC will deliver the objects
The answer is: A
Q168. What you should do if you want to launch an EC2 instance with a
pre-allocated private IP address?
A. Launch it in a Subnet Group
B. Launch the instance from a Private AMI
C. Assign EIP address to that instance
D. Launch that instance in AWS VPC cloud
The answer is: D
Q169. Can you edit a Security Group (SG) rules when it is used by
multiple EC2 instances? Will new rules apply to all previously running
EC2 instances?
A. No, you cannot edit a SG when used by a EC2 instance
B. Yes, you can edit. Immediately apply to all instances.
C. You can edit only the Outbound rules
D. Only Outbound rules apply to all EC2 instances
The answer is: B
Q170. Which of the following statements are true with Route 53?
A. Amazon Route 53 is a scalable and highly available Domain Name System (DNS)
B. Amazon Route 53 is fully compliant with IPv6 as well
C. Will automatically configure DNS settings for your domains
D. Route 53 provides low latency database service
The answers are: A,B and C
Q171. What is a Virtual Private Cloud (VPC)?
A. VPC enables you to launch AWS resources into a virtual network
B. VPC is a virtual network dedicated to your AWS account
C. VPC is used to create domain name for your organization
D. VPC can also be connected to your own office data center
The answers are: A,B and D
Q172. What is an Elastic IP?
A. There is no such IP. Only public & private IPs are valid.
B. Used in Elastic Load Balancing
C. An Elastic IP address is a static IPv4 address
D. An Elastic IP address is for use in a specific region only
The answers are: C and D
Q173. _____________ is a fully managed in-memory data store service
offered by Amazon Web Services (AWS)?
A. Amazon Neptune
B. Amazon Redshift
C. Amazon ElastiCache
D. Amazon Aurora
The answer is: C
Q174. In AWS which service is used to create Domain Name for their
customers?
A. Amazon CloudWatch
B. Amazon Route53
C. Amazon CloudDomain
D. Amazon VPC
The answer is: B
Q175. Which one is a valid statement regarding EBS-Volumes?
A. You can attach maximum of 5 volumes to an instance
B. You can attach multiple instances to one volume
C. You can attach multiple volumes to a single EC2 instance
D. You cannot attach a additional volume to an instance
The answer is: C
Q176. Which one is a valid statement regarding EBS-Snapshots?
A. You can access Snapshots thru S3 APIs
B. You can store your Snapshots in a S3 BUCKET
C. Snapshots are available only thru EC2 instances
D. You can access your Snapshots thru VPC APIs
The answer is: C
Q178. Which one is the valid scenario?
A. Creating PEERING connection to a VPC in a Different Region
B. Creating PEERING connection between VPCs in Same Region
C. Attaching VOLUME in one subnet/zone with EC2 instance in another subnet/zone
D. Keeping your primary db and secondary db in the same zone
The answer is: B
Q179. How do you connect a VPC to your Office Datacenter?
A. By keeping AWS VPC and Office Datacenter in same IP range
B. Establishing VPN connection between VPC and Datacenter
C. Establishing a dedicated hotlink between VPC and Datacenter
D. You cannot connect VPC and your Datacenter
The answer is: B
Q180. Choose the valid scenarios regarding VPC?
A. You can delete the Default VPC available in your region
B. VPC can span across multiple Availability Zones
C. Trying to launch an instance without having VPC in a region
D. Launching an instance onto a VPC created by you
The answers are: A,B and D
Q181. How the EC2 instances inside a VPC directly access the internet?
A. With the help of instance’s Public IP
B. By attaching a Elastic IP to that instance
C. Internet Gateway enables the access to the internet
D. With the help of Route Table
The answer is: C
Q182. Which one is the highly secured design?
A. Keeping both EC2 and Database instances in a public subnet
B. Keep EC2 in public subnet and Database in private subnet
C. Keep EC2 in public subnet and Database in a S3 bucket
D. Defining ANYWHERE in the DB security group INBOUND rule
The answer is: B
Q183. Keeping your instance in a public subnet and database in a private
subnet. What type of cloud deployment model is this?
A. Community Cloud
B. Private Cloud
C. Public Cloud
D. Hybrid Cloud
The answer is: D
Q184. Which service distribute the contents from Edge Locations to the
end users to reduce the latency?
A. Amazon CloudWatch
B. Amazon CloudTrail
C. Amazon CloudFront
D. Amazon PushData
The answer is: C
Q185. I am a cloud web service used for hosting your application. Who am
I?
A. AWS Route 53
B. AWS VPC
C. AWS S3
D. AWS EC2
The answer is: D
Q186. You can add ________________ to your Auto Scaling group so that
you can perform custom actions when instances launch or terminate.
A. CloudWatch
B. CloudTrail
C. Load Balancer
D. Lifecycle Hooks
The answer is: D
Q187. What is Auto Scaling?
A. Accelerating VPC Speed
B. Creating/Terminating duplicate instances using Scale IN/OUT
C. Automating backup/restore service
D. None of the above
The answer is: B
Q188. You want complex querying capabilities but don’t want data
warehouse. Which database service you would choose?
A. Amazon DynamoDB
B. Amazon Redshift
C. Amazon RDS
D. Amazon ElastiCache
The answer is: C
Q189. What is an Availability Zone?
A. A Container where all your S3 buckets are stored
B. Denotes an Entire Region
C. A location inside a Region which is protected from failures
D. Collection of Regions
The answer is: C
Q190. The cloud infrastructure is shared by several organizations and
supports specific group that has shared concerns. Government
departments, universities, central banks etc. often find this type of cloud
useful. What kind of cloud deployment model is this?
A. Private Cloud
B. Hybrid Cloud
C. Community Cloud
D. Public Cloud
The answer is: C
Q191. How many Buckets you can create in S3?
A. 150
B. 250
C. 500
D. 100
The answer is: D
Q192. What is the maximum size of a S3 Bucket?
A. 3 Terabytes
B. 10 Terabytes
C. 5 Terabytes
D. 7 Terabytes
The answer is: C
Q193. Which service of Amazon AWS is used to host a static website?
A. Amazon Simple Storage Service(S3)
B. Amazon CloudFront
C. Amazon Route53
D. Amazon CloudWatch
The answer is: A
Q194. Which of the following is not a Part of Security groups?
A. List of Protocols
B. List of Users
C. Ports
D. IP Address
The answer is: B
Q195. A data transport solution that accelerates moving terabytes to
petabytes of data into and out of AWS using storage devices designed to
be secure for physical transport. Name this solution.
A. Amazon EFS
B. Amazon S3
C. Amazon Glacier
D. Amazon Snowball
The answer is: D
Q196. What type of IP address do you use for your CGW (Customer
Gateway) address?
A. You will use PRIVATE IP address of your NAT device
B. You will use PUBLIC IP address of your NAT device
C. You will use ELASTIC IP address of your NAT device
D. You will use VPN
The answer is: B
Q197. How many subnets you can have per VPC?
A. 100
B. 300
C. 250
D. 200
The answer is: D
Q198. I have a REST API interface and uses secure HMAC-SHA1
authentication keys. I am also a data storage system. Who am I?
A. SS3
B. Elastic Block Store
C. S3
D. Snapshots
The answer is: C
Q199. I am a structured data store. I support indexing and data queries to
both EC2 and S3. Who am I?
A. DynamoDB
B. SimpleDB
C. MySQL
D. Aurora
The answer is: B
Q200. How many Elastic IP address can be associated with a single
account?
A) 4
B) 10
C) 5
D) None the above
Q201. After configuring ELB, you need to ensure that the user requests
are always attached to a single instance. What setting can you use?
A) Session cookie
B) Cross one load balancing
C) Connection drainage
D) Sticky session
Q202. Which of the following metrics cannot have a cloud watch alarm?
A) EC2 instance status check failed
B) EC2 CPU utilization
C) RRS lost object
D) Auto scaling group CPU utilization
Q203. Which of the below mentioned service is provided by Cloud watch?
A) Monitor estimated AWS usage
B) Monitor EC2 log files
C) Monitor S3 storage
D) Monitor AWS calls using Cloud trail
Q204. Which of the following service provides the edge – storage or
content delivery system that caches data at different locations?
A) Amazon RDS
B) Simple DB
C) Amazon Cloud Front
D) Amazon associates web services
Q205. What are the possible connection issues you can face while
connecting to your instance?
A) Connection timed out
B) Server refused our key
C) No supported authentication methods available
D) All of the above
Q206. You are enabled sticky session with ELB. What does it do with your
instance?
A) Routes all the requests to a single DNS
B) Binds the user session with a specific instance
C) Binds the user IP with a specific session
D) Provides a single ELB DNS for each IP address
Q207. Which is an email platform that provides an easy, cost effective way
for you to send and receive email using your own email address and
domains?
A) SES
B) SNS
C) SQS
D) SAS
Q208. AWS Cloud Front has been configured to handle the customer
requests to the web server launched in Linux machine. How many
requests per second can Amazon Cloud Front handle?
A) 1000
B) 100
C) 10000
D) There is no such limit
Q209. Which is virtual network interface that you can attach to an
instance in a VPC?
A) Elastic IP
B) AWS Elastic Interface
C) Elastic Network Interface
D) AWS Network ACL
Q210. You have launched an instance in EC2-Classic and you want to
make some change to the security group rule. How will these changes be
effective?
A) Security group rules cannot be changed
B) Changes are automatically applied to all instances that are associated with the security
group
C) Changes will be effective after rebooting the instance in that security group
D) Changes will be effective after 24-hours
Q211. Load Balancer and DNS service comes under which type of cloud
service?
A) IAAS-Network
B) IAAS-Computational
C) IAAS-Storage
D) None of the above
Q212. You have an EC2 instance that has an unencrypted volume. You
want to create another encrypted volume from this unencrypted volume.
Which of the following steps can achieve this?
A) Just simply create a copy of the unencrypted volume, you will have the option to encrypt
the volume.
B) Create a snapshot of the unencrypted volume and then while creating a volume from the
snapshot you can encrypt it
C) Create a snapshot of the unencrypted volume (applying encryption parameters), copy the
snapshot and create a volume from the copied snapshot
D) This is not possible, once a volume is unencrypted, there is no way to create an encrypted
volume from this
Q213. Where does the user specify the maximum number of instances
with the auto scaling commands?
A) Auto scaling Launch Config
B) Auto scaling group
C) Auto scaling policy
D) Auto scaling size
Q214. A user is aware that a huge download is occurring on his instance
he has already set the auto scaling policy to increase the instance count
when the network I/O increase beyond a certain limits how can the user
ensure that this temporary event does not result in scaling
A) The network I/O are not affecting during data download
B) The policy cannot be set on the network I/O
C) There is no way the can stop scaling as it already configured
D) Suspend scaling
Q.215.Which are the types of AMI provided by AWS?
A) EBS Backed
B) Instance Store backed
C) None its volume type and not AMI types
D) Both A and B
Q 216. Name some cloud service providers for public & private cloud ?
Public: Amazon web services, Microsoft Azure, Google Cloud, Oracle Cloud, Alibaba Cloud.
Private: Redhat-Openstack, Rackspace, VMware, IBM Private Cloud.
Q 217. What are all the different Instance categories based on pricing and
explain them briefly ?
On-demand Instances: On-demand instances are the virtual servers that are provisioned by
AWS EC2 service at an hourly price basis.
Reserved Instances: Instances which are reserved for a time, 1 year or 3 years , is called
reserved Instances. Hourly prices are reduced significantly compared to on-demand
Instances with reservation.
Spot Instances: Spot Instances are the special instance category where you request the unused
resources of EC2 from the datacenter for steep discounts. Spot prices are fixed by AWS EC2
and you need to bid the spot price more than the pricing of AWS EC2.
Q 218. I have some private servers on my premises, also I have distributed
some of my workload on the public cloud, what is this architecture called
?
Hybrid Cloud
Q 219. What is the difference between S3 and Glacier storage ?
S3 is a simple storage service, which is used to store and retrieve data. We can store any
amount of data and any type of data. Data that we are storing here are referred as objects.
Whereas the Glacier storage is an archival store which is used to store infrequently accessed
data or cold data. Major use case of glacier is data archiving and backup.
Q 220. Name some Database engines available natively in RDS services ?
MYSQL
MSSQL server
Oracle DB
Postgres DB
Amazon AURORA
Maria DB
Q 221. How can you automate resource provisioning in AWS ?
We can use the native service tool called AWS Cloud Formation for automation. It is also a
good option to consider the third-party tools like Ansible, Chef, Puppet etc. to automate the
services.
Q 222. What is autoscaling & mentions some of its benefits ?
Autoscaling is a service that automatically scales EC2 instance capacity out and in based on
the criteria’s that we are going to set. Autoscaling benefits its use for dynamic workloads like
web spikes, retail shop flash sales, ticket booking system on the vacations etc.,
Q 223. What is the difference between S3 availability & durability ?
Availability and durability are closely related to each other, but they are not the same.
Availability refers to the uptime of the service i.e.., S3 storage system’s uptime and can able to
deliver the requests and data. Durability on the other hand, refers to the data that is stored
should not suffer from degradation and corruption.
Q 224. Mention some important features of S3 buckets ?
Static web hosting
Versioning
Encryption
Object lifecycle management
Unlimited storage
Q 225. What are all the measures that you take to protect the data in S3 ?
lists and pre-signed Encrypt the data using Server-Side Encryption or Client-Side
Encryption.
Enable MFA delete to protect data against accidental deletion.
Usage of access control URL’s.
Q 226. What is Elastic IP address ?
Elastic IP address(EIP) is a static, internet routable address that is managed by the AWS
platform. Each Elastic IP address are assigned to the Instances from a Pool of IP address in
each region. Charges are applied once you allocate the EIP address no matter whether you
associate the IP to an Instance or not. When you release the allocated IP Address, EIP will to
returned to the pool.
Q 227. You have a webserver running on an Amazon EC2 instances that is
approaching 100% CPU utilization. Which option will reduce load on the
Amazon EC2 instance and describe why ?
We should create an Elastic load balancer with Autoscaling , and associate it with the EC2
instances. Layer 7 or Application layer Load balancers are used for this use case. ELB should
be used because ELB can balance the incoming load across the EC2 resources.
Q 228.what is CloudWatch and mention what can we do with it ?
CloudWatch is native service used to monitor our resources and applications in the AWS
cloud. CloudWatch does this by collecting information in the form of logs, metrics and events
from the resources that we provisioned in the AWS environment. We can define alarms,
troubleshoot issues using logs to optimize our infrastructure using CloudWatch.
Q 229.How will you classify the cloud, based on the services ?
We can classify the cloud computing platform into three types based on the services.
Infrastructure As A Service.
Platform As A Service.
Software As A Service.
Q 230.Name the messaging service available in AWS and point out a use
case of it ?
Simple Notification Services is a complete messaging service to deliver the messages end to
end. It is shortly referred to as SNS. A real time use case would be a banking system where
SNS will be sending a real time message (Email, SMS etc.,) to the end users who debits his
account by withdrawing some amount of money.
Q 231.Your company wants to use AWS for their newly designed analytics
platform. They have got around 20 TB of data In the on-premises. They
want to construct an analytics platform in AWS with this 20 TB of data
for analysis. Once analysis is done they want to archive this data for best
backup and recovery. What are the services that best matches this use
case and say why ?
Redshift would be the proper analytics platform which AWS provides. For data storage S3 is
the ideal option and once data analytics is done, data must get moved to glacier for backup &
Archival system. To do this data migration from s3 to glacier wee need to setup a lifecycle
management policy in S3 to get moved to glacier.
Q232.Your Relational database engine in AWS got crashes often when the
traffic to your RDS instance is high. The Replica of the RDS instance is
not promoted as master instance. What would you do to handle this
situation ??
Under these circumstances, we need to choose a bigger RDS instance type for handling the
huge amount of traffic. Creation of manual or automated snapshots is a must to recover from
the disaster cases.
Q 233.There is a production DB server running in a EC2 Linux instance
which has a ext4 formatted EBS volumes/disks attached. The database is
about to run out of storage space. How can you address this problem ?
First, we need to increase the EBS volumes level to a consistent amount in the AWS
management console. Next step we should use resize2fs command to use the provisioned space
in the Operating system level because an increase in the EBS volumes doesn’t guarantee the
increase in the OS level. For this to happen we should consider increasing the provisioned
space in the operating system level.
Q 234.A company wants to migrate the on-premises servers to the AWS
cloud platform. The company wants to estimate the cost of the machines
that is going to get provisioned in the cloud. How would you proceed to
determine the cost ?
Perform a mapping of the on-premises server’s cores and RAM to the nearest machine types
in the AWS Cloud. Then use the online AWS pricing calculator to estimate the cost of the
machines in the AWS Cloud.
Q 235. A XYZ company is using AWS services for the past one month for
its production servers. They have established a VPN connectivity from onpremises to AWS with a single IPSEC tunnel. During peak production
hours, servers are not reachable in the AWS Cloud due to network
problem. How would you mitigate this problem with minimal cost ?
Considering the cost factor, we should first consider increasing the number if IPSEC tunnels
that are used for the secure connectivity to AWS. If the problem persists even after increasing
the tunnels, consider the other options for better a network.
Q236: What is the Cloud Computing?
Practice of using a network of the remote servers, hosted on the Internet to store, manage,
and process data,
Rather more than a local server or a personal computer is called Cloud Computing.
Companies offering the computing services are called “cloud providers” and typically charge
for cloud.
Computing services based on the usage, similar to how you are billed for water or electricity
at home.
E.g.: AWS, AZURE, IBM BLUEMIX, GOOGLE CLOUD
This cloud model is composed of the five essential characteristics, three service models and
four deployment models.
The primary reasons for the moving to the cloud are: –
 It will never run out of the capacity, since it is a virtually infinite.
 You can access your cloud-based on applications from anywhere, you just need a
device which can Connect to the Internet.
Q237:What is merits of the Cloud Computing?
 Totally free from Maintenance i.e., You do not have to maintain or administer any
infrastructurefor the same.
 Lower Computing Cost.
 Improved Performance.
 Reduced Software Cost.
 Instant Software Updates.
 Unlimited Storage Capacity i.e., It will never run out of the capacity, since it is
virtually infinite.
 Increased Data Reliability.
 Device Independence and the “always on! Anywhere and any of place” i.e., You can
access your Cloud – based on applications from anywhere, you just need a device
which can connect to the Internet.Cloud Computing is the fastest growing part
of the network-based computing. It provides to tremendous.Benefits to customers
of the all sizes: simple users, developers, enterprises and all types of organizations.
Q238:What are the Cloud Computing?
 Lower TCO.
 Reliability, Scalability & Sustainability.
 Secure Store Management.
 Low Capital Expenditure.
 Frees from Internal Resources.
 Utility Based.
 Easy & Agile Deployment.
 Device & Location Independent.
 24 * 7 Support.
 Pay As You Use.
Q239:What are the top 10 advantages of Cloud Computing?
 Pay as you Go Model.
 Increased Mobility.
 Less or No CAPEX.
 High Availability.
 Easy to Manage.
 High Productivity.
 Environment Friendly.
 Less Deployment Time.
 Dynamic Scaling.
 Shared Resources.
Q240:What are the different layers (Service Models) of cloud computing?
Cloud computing consists of the 3 layers in the hierarchy and these are as follows:
1. Infrastructure as a Service (IAAS) provides cloud infrastructure in terms of the
hardware like memory, processor speed etc.
2. Platform as a Service (PAAS) provides cloud applications platform for the
developers.
3. Software as a Service (SAAS) provides cloud applications which is used by the user
directly without Installing anything on the system.
Q241:How do disable Password-Based Logins for the Root in Amazon
EC2 Instance?
Using a fixed for the root password for a public AMI is a security risk that can be quickly
become known. Even Relying on users to change the password after to the first login opens a
small window of the opportunity for potential abuses.
Following are the steps to disable password-based on remote logins for the root users.
1.Open the /etc/ssh/sshd config file with an text editor and locate to the following line:
#PermitRootLogin yes.
2.Change to the line to:
PermitRoot Login without-password.
Q242:How can I take an Snapshot of a RAID Array?
Problem – Take an snapshot excludes data held in the cache by the applications and the OS.
This tends not to matter on a single volume, however using a multiple volumes in the RAID
Array, this can be a problem due to inter dependencies of arrays.
Q243:What is the difference between Volume and Snapshot in the
Amazon Web Services?
In Amazon Web Services, a Volume is durables, block level storage can device that can be
attached to a singles EC2 instance. In plain words it is like an hard disk on which we can be
write or read from.A Snapshot is created by copying the data of volume to the another
location at a specific time. We can even replicate samen of Snapshot to multiple availability
zones. So, Snapshot is the single point in time view of a volume. We can create an Snapshot
only when we have a Volumes. Also, from a Snapshot we can create an Volumes. In AWS, we
have to pay for the storage that is used by Volume as well as the one used by a Snapshots.
Q244:What happens if my application to stops responding to requests in
beanstalk?
AWS Beanstalk applications have an system in place for avoiding to failures in the
underlying infrastructures.
Q245:How to update AMI tools at the Boot Time?
AWS is recommends that your AMIs downloads and upgrade to the Amazon EC2 AMI
creation tools during the startup. This ensures that a new AMIs based on your shared AMIs
have to the
latest AMI tools.
Q246:How to update AMI tools at the Boot Time on linux?
# Update to Amazon EC2 AMI tools
echo ” + Updating EC2 AMI tools”
yum update -y aws-amitools-ec2
echo ” + Updated EC2 AMI tools”
Q247:How does AWS Lambda to handle failure during event processing?
In AWS Lambda we can run a function of synchronous or asynchronous modes. In
synchronous mode, if AWS Lambda function is fails, then it will just give on the exception to
the calling application. In asynchronous modes, if AWS Lambda function is fails then it will
retry to the same function at least 3 times. If AWS Lambda is running in response to an
event in the Amazon DynamoDB or Amazon Kinesis, then event will be retried till that
Lambda function succeeds or the data expires. In DynamoDB or Kinesis, AWS maintains
datas for at least 24 hours.
Q248:What are the Storage of classes of Amazon?
 Amazon S3
 Scalable Storage in Cloud
 Amazon EBS
 Block Storage for EC2
 AWS Elastic File System
 Managed File Storage for EC2
 Amazon Glacier
 Low-cost Achieve Storage in the
 cloud
 AWS Storage Gateway
 Hybrid Storage Integration
 Amazon Snowball
 Petabyte-Scale Data Transport
 AWS Snowball Edge
 Petabyte-scale Data to Transport with
 On-Demand Compute
 AWS Snowmobile
 Exabyte-scale Data to Transport
Q249:How do Encryption is done in S3?
 In Transit: SSL/TLS
 At Rest
 Server-Side in Encryption
 S3 Managed Keys – SSE-S3
 AWS Key Management Service, Managed of Keys – SSE-KMS
 6.Server-Side Encryption with Customer Provided Keys – SSE-C
 Client-Side Encryptions
Q250:How will do upload a file greater than 100 megabytes in Amazon
S3?
Amazon S3 supports of storing objects or files up to 5 terabytes. To upload an file greater
than 100 megabytes, we have to use of Multipart upload utility from AWS. By using
Multipart upload we can upload an large file in multiple parts. Each part will be
independently to be uploaded. It doesn’t matter in what order to each part is uploaded. It
even to supports uploading these parts of parallel to decrease overall time. Once of all the
parts are uploaded, this utility makes a these as one single objects or file from which the parts
were do created.


---

<br>

{!footer.md!}
