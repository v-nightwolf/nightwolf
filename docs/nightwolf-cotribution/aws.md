# AWS Certified SysOps Administrator - Questions and Answers

<br>
These are AWS interview questions for experienced professionals.  You will find these questions very helpful in your AWS professional role interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---
   QUESTION NO: 1

       You are currently hosting multiple applications in a VPC and have logged numerous port scans
       coming in from a specific IP address block. Your security team has requested that all access
       from the offending IP address block be denied tor the next 24 hours.
       Which of the following is the best method to quickly and temporarily deny access from
       the specified IP address block?

       A. Create an AD policy to modify Windows Firewall settings on all hosts in the VPC to deny access 
          from the IP address block
       B. Modify the Network ACLs associated with all public subnets in the VPC to deny access from the IP
          address block
       C. Add a rule to all of the VPC 5 Security Groups to deny access from the IP address block
       D. Modify the Windows Firewall settings on all Amazon Machine Images (AMIs) that your organization 
          uses in that VPC to deny access from the IP address block

       Answer: C
       Reference:
       http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html

   QUESTION NO: 2

       When preparing for a compliance assessment of your system built inside of AWS. what are three best practices
       for you to prepare for anaudit? Choose any 3 answers.

       A. Gather evidence of your IT operational controls
       B. Request and obtain applicable third-party audited AWS compliance reports and certifications
       C. Request and obtain a compliance and security tour of an AWS data center for a
          pre-assessment security review
       D. Request and obtain approval from AWS to perform relevant network scans and indepth penetration tests of
          your system  and endpoints
       E. Schedule meetings with AWS third-party auditors to provide evidence of AWS compliance that maps to 
          your control objectives
       Answer: B,D,E

   QUESTION NO: 3

       You have started a new job and are reviewing your company infrastructure on AWS You notice one web
       application where they have an Elastic Load Balancer (&B) in front of web instances in an Auto Scaling Group.
       When you check the metrics for the ELB in CloudWatch you see four healthy instances In Availability Zone (AZ) A 
       and zero in AZ B There are zero unhealthy instances.
       What do you need to fix to balance the instances across AZs?

       A. Set the ELB to only be attached to another AZ
       B. Make sure Auto Scaling is configured to launch in both AZs
       C. Make sure your AMI is available in both AZs
       D. Make sure the maximum size of the Auto Scaling Group is greater than 4

       Answer: B

   QUESTION NO: 4

       You have been asked to leverage Amazon VPC BC2 and SOS to implement an application that submits and receives 
       millions of messages per second to a message queue. You want to ensure your application has sufficient
       bandwidth between your EC2 instances and SQS Which option will provide (he most scalable solution for
       bandwidth between the application and SOS?

       A. Ensure the application instances are properly configured with an Elastic Load Balancer.
       B. Ensure the application instances are launched in private subnets with the EBS-optimized option enabled.
       C. Ensure the application instances are launched in public subnets with the associate-publicIP-address=true
          option enabled
       D. Launch application instances in private subnets with an Auto Scaling group and Auto Scaling triggers 
          configured to watch the SOS queue size

       Answer: C
       Reference:
       http://www.cardinalpath.com/autoscaling-your-website-with-amazon-web-services-part-2/

   QUESTION NO: 5

       You have identified network throughput as a bottleneck on your ml small EC2 instance when uploading data 
       into Amazon S3 In the same region. How do you remedy this situation?

       A. Add an additional ENI
       B. Change to a larger Instance
       C. Use DirectConnect between EC2 and S3
       D. Use EBS PIOPS on the local volume

       Answer: B
       Reference:
       https://media.amazonwebservices.com/AWS_Amazon_EMR_Best_Practices.pdf

   QUESTION NO: 6

       When attached to an Amazon VPC which two components provide connectivity with external networks? 
       Choose 2 answers

       A. Elastic IPS (EIP)
       B. NAT Gateway (NAT)
       C. Internet Gateway {IGW)
       D. Virtual Private Gateway (VGW)

       Answer: C,D

   QUESTION NO: 7

       Your application currently leverages AWS Auto Scaling to grow and shrink as load Increases/decreases 
       and has been performing well. Your marketing team expects a steady ramp up in traffic to follow an upcoming
       campaign that will result in a 20x growth in traffic over 4 weeks. Your forecast for the approximate number
       of Amazon EC2 instances necessary to meet the peak demand is 175.
       What should you do to avoid potential service disruptions during the ramp up in traffic? 456789

       A. Ensure that you have pre-allocated 175 Elastic IP addresses so that each server will be able to obtain 
          one as it launches
       B. Check the service limits in Trusted Advisor and adjust as necessary so the forecasted count remains 
          within limits.
       C. Change your Auto Scaling configuration to set a desired capacity of 175 prior to the launch of the 
          marketing campaign.
       D. Pre-warm your Elastic Load Balancer to match the requests per second anticipated during peak demand prior
          to the marketing campaign.

       Answer: D

   QUESTION NO: 8

       You have an Auto Scaling group associated with an Elastic Load Balancer (ELB). You have noticed that instances
       launched via the Auto Scaling group are being marked unhealthy due to an ELB health check, but these unhealthy
       instances are not being terminated. What do you need to do to ensure trial instances marked unhealthy by the 
       ELB will be terminated and replaced?

       A. Change the thresholds set on the Auto Scaling group health check
       B. Add an Elastic Load Balancing health check to your Auto Scaling group
       C. Increase the value for the Health check interval set on the Elastic Load Balancer
       D. Change the health check set on the Elastic Load Balancer to use TCP rather than HTTP checks

       Answer: B

       Reference:
       http://docs.aws.amazon.com/AutoScaling/latest/DeveloperGuide/as-add-elb-healthcheck.html

       Add an Elastic Load Balancing Health Check to your Auto Scaling GroupBy default, an Auto Scaling group
       periodically reviews the results of EC2 instance status to determine the health state of each instance. However,
       if you have associated your Auto Scaling group with an Elastic Load Balancing load balancer, you can choose to use
       the Elastic Load Balancing health check. In this case, Auto Scaling determines the health status of your instances
       by checking the results of both the EC2 instance status check and the Elastic Load Balancing instance health check.
       For information about EC2 instance status checks, see Monitor Instances With Status Checks in the Amazon EC2 User 
       Guide for Linux Instances. For information about Elastic Load Balancing health checks, see Health Check in the
       Elastic Load Balancing Developer Guide. This topic shows you how to add an Elastic Load Balancing health check to
       your Auto Scaling group, assuming that you have created a load balancer and have registered the load balancer
       with your Auto Scaling group. If you have not registered the load balancer with your Auto Scaling group, see Set 
       Up a Scaled and Load-Balanced Application. Auto Scaling marks an instance unhealthy if the calls to the Amazon EC2
       action DescribeInstanceStatus return any state other than running, the system status shows impaired, or the calls
       to Elastic Load Balancing action DescribeInstanceHealth returns OutOfService in the instance state field.
       If there are multiple load balancers associated with your Auto Scaling group, Auto Scaling checks the health state
       of your EC2 instances by making health check calls to each load balancer. For each call, if the Elastic Load 
       Balancing action returns any state other than InService, the instance is marked as unhealthy. After Auto Scaling
       marks an instance as unhealthy, it remains in that state, even if subsequent calls from other load balancers return
       an InService state for the same instance.

   QUESTION NO: 9

       Which two AWS services provide out-of-the-box user configurable automatic backup-as-a-service and backup 
       rotation options? Choose any 2 answers.

       A. Amazon S3
       B. Amazon RDS
       C. Amazon EBS
       D. Amazon Red shift

       Answer: C,D

   QUESTION NO: 10

       An organization has configured a VPC with an Internet Gateway (IGW). pairs of public and private subnets 
       (each with one subnet per Availability Zone), and an Elastic Load Balancer (ELB) configured to use the public
       subnets. The application web tier leverages the ELB, Auto Scaling and a mum-AZ RDS database instance.
       The Organization would like to eliminate any potential single points ft failure in this design. What step 
       should you take to achieve this organization's objective?

       A. Nothing, there are no single points of failure in this architecture.
       B. Create and attach a second IGW to provide redundant internet connectivity.
       C. Create and configure a second Elastic Load Balancer to provide a redundant load balancer.
       D. Create a second multi-AZ RDS instance in another Availability Zone and configurereplication to provide 
          a redundant database.

       Answer: C

   QUESTION NO: 11

       Which of the following are characteristics of Amazon VPC subnets? Choose any 2 answers.

       A. Each subnet maps to a single Availability Zone
       B. A CIDR block mask of /25 is the smallest range supported
       C. Instances in a private subnet can communicate with the internet only if they have an Elastic IP.
       D. By default, all subnets can route between each other, whether they are private or public
       E. V Each subnet spans at least 2 Availability zones to provide a high-availability environment.

       Answer: C,E

   QUESTION NO: 12

       You are creating an Auto Scaling group whose Instances need to insert a custom metric into CloudWatch.
       Which method would be the best way to authenticate your CloudWatch PUT request?

       A. Create an IAM role with the Put MetricData permission and modify the Auto Scaling launch configuration to
          launch instances in that role.
       B. Create an IAM user with the PutMetricData permission and modify the Auto Scaling launch configuration to
          inject the userscredentials into the instance User Data.
       C. Modify the appropriate Cloud Watch metric policies to allow the Put MetricData permission to instances from
          the Auto Scaling group.
       D. Create an IAM user with the PutMetricData permission and put the credentials in a private repository and
          have applications on the server pull the credentials as needed.

       Answer: B

   QUESTION NO: 13

       When an EC2 instance that is backed by an S3-based AMI Is terminated, what happens to the data on me root volume?
       A. Data is automatically saved as an E8S volume.
       B. Data is automatically saved as an ESS snapshot.
       C. Data is automatically deleted.
       D. Data is unavailable until the instance is restarted.

       Answer: D

       Reference:
       http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ComponentsAMIs.html

   QUESTION NO: 14

       You have a web application leveraging an Elastic Load Balancer (ELB) In front of the web
       servers deployed using an Auto Scaling Group Your database is running on Relational Database
       Service (RDS) The application serves out technical articles and responses to them in general
       there are more views of an article than there are responses to the article. On occasion, an article
       on the site becomes extremely popular resulting in significant traffic Increases that causes the
       site to go down.
       What could you do to help alleviate the pressure on the infrastructure while maintaining availability
       during these events?
       Choose 3 answers

       A. Leverage CloudFront for the delivery of the articles.
       B. Add RDS read-replicas for the read traffic going to your relational database
       C. Leverage ElastiCache for caching the most frequently used data.
       D. Use SOS to queue up the requests for the technical posts and deliver them out of the queue.
       E. Use Route53 health checks to fail over to an S3 bucket for an error page.

       Answer: A,C,E

   QUESTION NO: 15

       The majority of your Infrastructure is on premises and you have a small footprint on AWS Your
       company has decided to roll out a new application that is heavily dependent on low latency
       connectivity to LOAP for authentication Your security policy requires minimal changes to the
       company's existing application user management processes.
       What option would you implement to successfully launch this application1?

       A. Create a second, independent LOAP server in AWS for your application to use
       for authentication
       B. Establish a VPN connection so your applications can authenticate against your existing
       on-premises LDAP servers
       C. Establish a VPN connection between your data center and AWS create a LDAP replica
       on AWS and configure your application to use the LDAP replica for authentication
       D. Create a second LDAP domain on AWS establish a VPN connection to establish a trust
       relationship between your new and existing domains and use the new domain for authentication

       Answer: D

       Reference:
       http://msdn.microsoft.com/en-us/library/azure/jj156090.aspx


   QUESTION NO: 16

       You need to design a VPC for a web-application consisting of an Elastic Load Balancer (ELB). a
       fleet of web/application servers, and an RDS database The entire Infrastructure must be
       distributed over 2 availability zones.
       Which VPC configuration works while assuring the database is not available from the Internet?

       A. One public subnet for ELB one public subnet for the web-servers, and one private subnet for
       the database
       B. One public subnet for ELB two private subnets for the web-servers, two private subnets for
       RDS
       C. Two public subnets for ELB two private subnets for the web-servers and two private subnets
       for RDS
       D. Two public subnets for ELB two public subnets for the web-servers, and two public subnets
       for RDS

       Answer: A

   QUESTION NO: 17

       An application that you are managing has EC2 instances & Dynamo OB tables deployed to
       several AWS Regions In order to monitor the performance of the application globally, you would
       like to see two graphs 1) Avg CPU Utilization across all EC2 instances and 2) Number of Throttled
       Requests for all DynamoDB tables.
       How can you accomplish this?

       A. Tag your resources with the application name, and select the tag name as the dimension in
       the Cloudwatch Management console to view the respective graphs
       B. Use the Cloud Watch CLI tools to pull the respective metrics from each regional
       endpoint Aggregate the data offline & store it for graphing in CloudWatch.
       C. Add SNMP traps to each instance and DynamoDB table Leverage a central monitoring
       server to capture data from each instance and table Put the aggregate data into Cloud Watch for
       graphing.
       D. Add a CloudWatch agent to each instance and attach one to each DynamoDB table. When
       configuring the agent set the appropriate application name & view the graphs in CloudWatch.

       Answer: C

   QUESTION NO: 18

       When assessing an organization s use of AWS API access credentials which of the following three
       credentials should be evaluated?
       Choose 3 answers

       A. Key pairs
       B. Console passwords
       10
       C. Access keys
       D. Signing certificates
       E. Security Group memberships

       Answer: A,C,D

       Reference:
       http://media.amazonwebservices.com/AWS_Operational_Checklists.pdf

   QUESTION NO: 19

       You have a Linux EC2 web server instance running inside a VPC The instance is In a public
       subnet and has an EIP associated with it so you can connect to It over the Internet via HTTP or
       SSH The instance was also fully accessible when you last logged in via SSH. and was also
       serving web requests on port 80.
       Now you are not able to SSH into the host nor does it respond to web requests on port 80 that were
       working fine last time you checked You have double-checked that all networking configuration
       parameters (security groups route tables. IGW'EIP. NACLs etc) are properly configured {and you
       haven’t made any changes to those anyway since you were last able to reach the Instance). You
       look at the EC2 console and notice that system status check shows "impaired."
       Which should be your next step in troubleshooting and attempting to get the instance back to a
       healthy state so that you can log in again?

       A. Stop and start the instance so that it will be able to be redeployed on a healthy host system
       that most likely will fix the "impaired" system status
       B. Reboot your instance so that the operating system will have a chance to boot in a clean healthy
       state that most likely will fix the 'impaired" system status
       C. Add another dynamic private IP address to me instance and try to connect via mat new path,
       since the networking stack of the OS may be locked up causing the “impaired” system status.
       D. Add another Elastic Network Interface to the instance and try to connect via that new path
       since the networking stack of the OS may be locked up causing the "impaired" system status
       E. un-map and then re-map the EIP to the instance, since the IGWVNAT gateway may not
       be working properly, causing the "impaired" system status

       Answer: B

   QUESTION NO: 20

       What is a placement group?

       A. A collection of Auto Scaling groups in the same Region
       B. Feature that enables EC2 instances to interact with each other via nigh bandwidth, low
       latency connections
       C. A collection of Elastic Load Balancers in the same Region or Availability Zone
       D. A collection of authorized Cloud Front edge locations for a distribution

       Answer: C

       Reference:
       http://aws.amazon.com/ec2/faqs/

   QUESTION NO: 21

       Your entire AWS infrastructure lives inside of one Amazon VPC You have an Infrastructure
       monitoring application running on an Amazon instance in Availability Zone (AZ) A of the region,
       and another application instance running in AZ B. The monitoring application needs to make use
       of ICMP ping to confirm network reachability of the instance hosting the application.
       Can you configure the security groups for these instances to only allow the ICMP ping to pass
       from the monitoringinstance to the application instance and nothing else" If so how?

       A. No Two instances in two different AZ's can't talk directly to each other via ICMP ping as
       that protocol is not allowed across subnet (iebroadcast) boundaries
       B. Yes Both the monitoring instance and the application instance have to be a part of the
       same security group, and that security group needs to allow inbound ICMP
       C. Yes, The security group for the monitoring instance needs to allow outbound ICMP and
       the application instance's security group needs to allow Inbound ICMP
       D. Yes, Both the monitoring instance's security group and the application instance's security
       group need to allow both inbound and outbound ICMP ping packets since ICMP is not a
       connection-oriented protocol

       Answer: D

   QUESTION NO: 22

       You have two Elastic Compute Cloud (EC2) instances inside a Virtual Private Cloud (VPC) in the
       same Availability Zone (AZ) but in different subnets.One instance is running a database and the
       other instance an application that will interface with the database. You want to confirm that they
       can talk to each other for your application to work properly.
       Which two things do we need to confirm in the VPC settings so that these EC2 instances can
       communicate inside the VPC?
       Choose 2 answers

       A. A network ACL that allows communication between the two subnets.
       B. Both instances are the same instance class and using the same Key-pair.
       C. That the default route is set to a NAT instance or internet Gateway (IGW) for them
       to communicate.
       D. Security groups are set to allow the application host to talk to the database on the right
       port/protocol.

       Answer: A,C

   QUESTION NO: 23

       Which services allow the customer to retain full administrative privileges of the underlying
       EC2 instances?
       Choose 2 answers

       A. Amazon Elastic Map Reduce
       B. Elastic Load Balancing
       C. AWS Elastic Beanstalk
       D. I" Amazon Elasticache
       E. Amazon Relational Database service

       Answer: B,C

   QUESTION NO: 24

       You have a web-style application with a stateless but CPU and memory-intensive web tier running
       on a cc2 8xlarge EC2 instance inside of a VPC The instance when under load is having 134
       problems returning requests within the SLA as defined by your business The application maintains
       its state in a DynamoDB table, but the data tier is properly provisioned and responses are
       consistently fast.
       How can you best resolve the issue of the application responses not meeting your SLA?
       A. Add another cc2 8xlarge application instance, and put both behind an Elastic Load Balancer
       B. Move the cc2 8xlarge to the same Availability Zone as the DynamoDB table
       C. Cache the database responses in ElastiCache for more rapid access
       D. Move the database from DynamoDB to RDS MySQL in scale-out read-replica configuration

       Answer: B

       Reference:
       http://aws.amazon.com/elasticmapreduce/faqs/

   QUESTION NO: 25

       You are managing a legacy application Inside VPC with hard coded IP addresses in its configuration.
       Which two mechanisms will allow the application to failover to new instances without the need for
       reconfiguration?
       Choose 2 answers

       A. Create an ELB to reroute traffic to a failover instance
       B. Create a secondary ENI that can be moved to a failover instance
       C. Use Route53 health checks to fail traffic over to a failover instance
       D. Assign a secondary private IP address to the primary ENIO that can De moved to a failover instance

       Answer: A,D

 {!inpage-ads.md!}

   QUESTION NO: 26

       You are designing a system that has a Bastion host. This component needs to be highly available
       without human intervention.
       Which of the following approaches would you select?

       A. Run the bastion on two instances one in each AZ
       B. Run the bastion on an active Instance in one AZ and have an AMI ready to boot up in the event
       of failure
       C. Configure the bastion instance in an Auto Scaling group Specify the Auto Scaling group
       to include multiple AZs but have a min-size of 1 and max-size of 1
       D. Configure an ELB in front of the bastion instance

       Answer: C

   QUESTION NO: 27

       Which of the following statements about this S3 bucket policy is true?
       15
       
       A. Denies the server with the IP address 192 168 100 0 full access to the "mybucket" bucket
       B. Denies the server with the IP address 192 168 100 188 full access to the "mybucket" bucket
       C. Grants all the servers within the 192 168 100 0/24 subnet full access to the "mybucket" bucket
       D. Grants all the servers within the 192 168 100 188/32 subnet full access to the "mybucket"
       bucket

       Answer: C

   QUESTION NO: 28

       Which of the following requires a custom CloudWatch metric to monitor?

       A. Data transfer of an EC2 instance
       B. Disk usage activity of an EC2 instance
       C. Memory Utilization of an EC2 instance
       D. CPU Utilization of an EC2mstance

       Answer: B

       Reference:
       http://aws.amazon.com/cloudwatch/

   QUESTION NO: 29

       You run a web application where web servers on EC2 Instances are In an Auto Scaling group
       Monitoring over the last 6 months shows that 6 web servers are necessary to handle the minimum
       load During the day up to 12 servers are needed Five to six days per year, the number of web
       servers required might go up to 15.
       What would you recommend to minimize costs while being able to provide hill availability?

       A. 6 Reserved instances (heavy utilization). 6 Reserved instances {medium utilization),
       rest covered by On-Demand instances
       B. 6 Reserved instances (heavy utilization). 6 On-Demand instances, rest covered by
       Spot Instances
       C. 6 Reserved instances (heavy utilization) 6 Spot instances, rest covered by OnDemand instances
       D. 6 Reserved instances (heavy utilization) 6 Reserved instances (medium utilization) rest covered
       by Spot instances 1678

       Answer: C

   QUESTION NO: 30

       You have been asked to propose a multi-region deployment of a web-facing application where a
       controlled portion of your traffic is being processed by an alternate region.
       Which configuration would achieve that goal?

       A. Route53 record sets with weighted routing policy
       B. Route53 record sets with latency based routing policy
       C. Auto Scaling with scheduled scaling actions set
       D. Elastic Load Balancing with health checks enabled

       Answer: D

       Reference:
       http://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/TerminologyandKeyConcepts.html

   QUESTION NO: 31

       You have set up Individual AWS accounts for each project. You have been asked to make sure
       your AWS Infrastructure costs do not exceed the budget set per project for each month.
       Which of the following approaches can help ensure that you do not exceed the budget each month?

       A. Consolidate your accounts so you have a single bill for all accounts and projects
       B. Set up auto scaling with CloudWatch alarms using SNS to notify you when you are running too
       many Instances in a given account
       C. Set up CloudWatch billing alerts for all AWS resources used by each project, with a notification
       occurring when the amount for each resource tagged to a particular project matches the budget
       allocated to the project.
       D. Set up CloudWatch billing alerts for all AWS resources used by each account, with email
       notifications when it hits 50%. 80% and 90% of its budgeted monthly spend

       Answer: C

   QUESTION NO: 32

       When creation of an EBS snapshot Is initiated but not completed the EBS volume?

       A. Cannot De detached or attached to an EC2 instance until me snapshot completes
       B. Can be used in read-only mode while me snapshot is in progress
       C. Can be used while me snapshot Is in progress
       D. Cannot be used until the snapshot completes

       Answer: C

       Reference:
       http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-copy-snapshot.html

   QUESTION NO: 33

       You are using ElastiCache Memcached to store session state and cache database queries in your
       infrastructure You notice in Cloud Watch that Evictions and GetMisses are Doth very high.
       What two actions could you take to rectify this?
       Choose 2 answers

       A. Increase the number of nodes in your cluster
       B. Tweak the max-item-size parameter
       C. Shrink the number of nodes in your cluster
       D. Increase the size of the nodes in the duster

       Answer: B,D

   QUESTION NO: 34

       You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS)
       for persistence At times throughout the day, you are seeing large variance in the response times of
       the database queries Looking into the instance with the isolate command you see a lot of wait time
       on the disk volume that the database's data is stored on.
       What two ways can you improve the performance of the database's storage while maintaining the
       current persistence of the data?
       Choose 2 answers

       A. Move to an SSD backed instance
       B. Move the database to an EBS-Optimized Instance
       C. T Use Provisioned IOPs EBS
       D. Use the ephemeral storage on an m2 4xiarge Instance Instead

       Answer: A,B

   QUESTION NO: 35

       Your EC2-Based Multi-tier application includes a monitoring instance that periodically makes
       application -level read only requests of various application components and if any of those fail
       more than three times 30 seconds calls CloudWatch lo fire an alarm, and the alarm notifies your
       operations team by email and SMS of a possible application health problem. However, you also
       need to watch the watcher -the monitoring instance itself - and be notified if it becomes unhealthy.
       Which of the following Is a simple way to achieve that goal?

       A. Run another monitoring instance that pings the monitoring instance and fires a could watch
       alarm mat notifies your operations teamshould the primary monitoring instance become unhealthy.
       B. Set a Cloud Watch alarm based on EC2 system and instance status checks and have the
       alarm notify your operations team of anydetected problem with the monitoring instance.
       C. Set a Cloud Watch alarm based on the CPU utilization of the monitoring instance and nave
       the alarm notify your operations team if C r the CPU usage exceeds 50% few more than one
       minute: then have your monitoring application go into a CPU-bound loop should itDetect any
       application problems.
       D. Have the monitoring instances post messages to an SOS queue and then dequeue those
       messages on another instance should D c- the queue cease to have new messages, the second
       instance should first terminate the original monitoring instance start anotherbackup monitoring
       instance and assume (he role of the previous monitoring instance and beginning adding messages
       to the SOSqueue.
       19

       Answer: D

   QUESTION NO: 36

       You have decided to change the Instance type for instances running In your application tier that
       are using Auto Scaling.
       In which area below would you change the instance type definition?

       A. Auto Scaling launch configuration
       B. Auto Scaling group
       C. Auto Scaling policy
       D. Auto Scaling tags

       Answer: B

       Reference:
       http://docs.aws.amazon.com/AutoScaling/latest/DeveloperGuide/WhatIsAutoScaling.html

   QUESTION NO: 37

       You are attempting to connect to an instance in Amazon VPC without success You have already
       verified that the VPC has an Internet Gateway (IGW) the instance has an associated Elastic IP
       (EIP) and correct security group rules are in place.
       Which VPC component should you evaluate next?

       A. The configuration of a MAT instance
       B. The configuration of the Routing Table
       C. The configuration of the internet Gateway (IGW)
       D. The configuration of SRC/DST checking

       Answer: C

       Reference:
       http://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/UserScenariosForVPC.html

   QUESTION NO: 38

       You are tasked with the migration of a highly trafficked Node JS application to AWS In order
       to comply with organizational standards Chef recipes must be used to configure the
       application servers that host this application and to support application lifecycle events.
       Which deployment option meets these requirements while minimizing administrative burden?

       A. Create a new stack within Opsworks add the appropriate layers to the stack and deploy
       the application
       B. Create a new application within Elastic Beanstalk and deploy this application to a
       new environment
       C. Launch a Mode JS server from a community AMI and manually deploy the application to the
       launched EC2 instance
       D. Launch and configure Chef Server on an EC2 instance and leverage the AWS CLI to
       launch application servers and configure those instances using Chef.

       Answer: B

       Reference:
       http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deployment.html

   QUESTION NO: 39

       You have been asked to automate many routine systems administrator backup and recovery
       activities Your current plan is to leverage AWS-managed solutions as much as possible and
       automate the rest with the AWS CU and scripts.
       Which task would be best accomplished with a script?

       A. Creating daily EBS snapshots with a monthly rotation of snapshots
       B. Creating daily ROS snapshots with a monthly rotation of snapshots
       C. Automatically detect and stop unused or underutilized EC2 instances
       D. Automatically add Auto Scaled EC2 instances to an Amazon Elastic Load Balancer

       Answer: C

   QUESTION NO: 40

       Your organization's security policy requires that all privileged users either use frequently
       rotated passwords or one-time access credentials in addition to username/password.
       Which two of the following options would allow an organization to enforce this policy for
       AWS users?
       Choose 2 answers

       A. Configure multi-factor authentication for privileged 1AM users
       B. Create 1AM users for privileged accounts
       C. Implement identity federation between your organization's Identity provider leveraging the
       1AM Security Token Service
       D. Enable the 1AM single-use password policy option for privileged users

       Answer: C,D

   QUESTION NO: 41

       What are characteristics of Amazon S3?
       Choose 2 answers

       A. Objects are directly accessible via a URL
       B. S3 should be used to host a relational database
       C. S3 allows you to store objects or virtually unlimited size
       D. S3 allows you to store virtually unlimited amounts of data
       E. S3 offers Provisioned IOPS

       Answer: B,C

   QUESTION NO: 42

       You receive a frantic call from a new DBA who accidentally dropped a table containing all your
       customers.
       Which Amazon RDS feature will allow you to reliably restore your database to within 5 minutes of
       when the mistake was made?

       A. Multi-AZ RDS
       B. RDS snapshots
       C. RDS read replicas
       D. RDS automated backup

       Answer: B

       Reference:
       http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.BackingUpAndRestoringAmazonRDSInstances.html

   QUESTION NO: 43

       A media company produces new video files on-premises every day with a total size of around
       100GBS after compression All files have a size of 1 -2 GB and need to be uploaded to Amazon
       S3 every night in a fixed time window between 3am and 5am Current upload takes almost 3
       hours, although less than half of the available bandwidth is used.
       What step(s) would ensure that the file uploads are able to complete in the allotted time window?

       A. Increase your network bandwidth to provide faster throughput to S3
       B. Upload the files in parallel to S3
       C. Pack all files into a single archive, upload it to S3, then extract the files in AWS
       D. Use AWS Import/Export to transfer the video files

       Answer: D

       Reference:
       http://aws.amazon.com/importexport/faqs/

   QUESTION NO: 44

       You are running a web-application on AWS consisting of the following components an Elastic
       Load Balancer (ELB) an Auto-Scaling Group of EC2 instances running Linux/PHP/Apache, and
       Relational DataBase Service (RDS) MySQL.
       Which security measures fall into AWS's responsibility?

       A. Protect the EC2 instances against unsolicited access by enforcing the principle of
       least-privilege access
       B. Protect against IP spoofing or packet sniffing
       C. Assure all communication between EC2 instances and ELB is encrypted
       D. Install latest security patches on ELB. RDS and EC2 instances

       Answer: B

   QUESTION NO: 45

       You use S3 to store critical data for your company Several users within your group currently have
       lull permissions to your S3 buckets You need to come up with a solution mat does not impact
       your users and also protect against the accidental deletion of objects.
       Which two options will address this issue?
       Choose 2 answers

       A. Enable versioning on your S3 Buckets
       B. Configure your S3 Buckets with MFA delete
       C. Create a Bucket policy and only allow read only permissions to all users at the bucket level
       D. Enable object life cycle policies and configure the data older than 3 months to be archived
       in Glacier

       Answer: B,C

   QUESTION NO: 46

       An organization's security policy requires multiple copies of all critical data to be replicated across
       at least a primary and backup data center. The organization has decided to store some critical
       data on Amazon S3. 245
       Which option should you implement to ensure this requirement is met?

       A. Use the S3 copy API to replicate data between two S3 buckets in different regions
       B. You do not need to implement anything since S3 data is automatically replicated
       between regions
       C. Use the S3 copy API to replicate data between two S3 buckets in different facilities within
       an AWS Region
       D. You do not need to implement anything since S3 data is automatically replicated
       between multiple facilities within an AWS Region

       Answer: C

   QUESTION NO: 47

       You are tasked with setting up a cluster of EC2 Instances for a NoSOL database The database
       requires random read 10 disk performance up to a 100.000 IOPS at 4KB block side per node
       Which of the following EC2 instances will perform the best for this workload?

       A. A High-Memory Quadruple Extra Large (m2 4xlarge) with EBS-Optimized set to true and
       a PIOPs EBS volume
       B. A Cluster Compute Eight Extra Large (cc2 8xlarge) using instance storage
       C. High I/O Quadruple Extra Large (hil 4xiarge) using instance storage
       D. A Cluster GPU Quadruple Extra Large (cg1 4xlarge) using four separate 4000 PIOPS
       EBS volumes in a RAID 0 configuration

       Answer: B

       Reference:
       http://aws.amazon.com/ec2/instance-types/

   QUESTION NO: 48

       When an EC2 EBS-backed (EBS root) instance is stopped, what happens to the data on any
       ephemeral store volumes?

       A. Data will be deleted and win no longer be accessible
       B. Data Is automatically saved in an EBS volume.
       C. Data Is automatically saved as an E8S snapshot
       D. Data is unavailable until the instance is restarted

       Answer: D

   QUESTION NO: 49

       Your team Is excited about theuse of AWS because now they have access to programmable
       Infrastructure" You have been asked to manage your AWS infrastructure In a manner similar to
       the way you might manage application code You want to be able to deploy exact copies of
       different versions of your infrastructure, stage changes into different environments, revert back to
       previous versions, and identify what versions are running at any particular time (development test
       QA. production).
       Which approach addresses this requirement?

       A. Use cost allocation reports and AWS Opsworks to deploy and manage your infrastructure.
       B. Use AWS CloudWatch metrics and alerts along with resource tagging to deploy and manage
       your infrastructure.
       C. Use AWS Beanstalk and a version control system like GIT to deploy and manage
       your infrastructure.
       D. Use AWS CloudFormation and a version control system like GIT to deploy and manage your
       infrastructure.

       Answer: B

       Reference:
       http://aws.amazon.com/opsworks/faqs/

   QUESTION NO: 50

       You have a server with a 5O0GB Amazon EBS data volume. The volume is 80% full. You need
       to back up the volume at regular intervals and be able to re-create the volume in a new
       Availability Zone in the shortest time possible. All applications using the volume can be paused
       for a period of a few minutes with no discernible user impact.
       Which of the following backup methods will best fulfill your requirements?

       A. Take periodic snapshots of the EBS volume 2678930
       B. Use a third party Incremental backup application to back up to Amazon Glacier
       C. Periodically back up all data to a single compressed archive and archive to Amazon S3 using
       a parallelized multi-part upload
       D. Create another EBS volume in the second Availability Zone attach it to the Amazon
       EC2 instance, and use a disk manager to mirror me two disks

       Answer: D

       Reference:
       http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-creating-snapshot.html

 {!inpage-ads.md!}

   QUESTION NO: 51

       Your company Is moving towards tracking web page users with a small tracking Image loaded
       on each page Currently you are serving this image out of US-East, but are starting to get
       concerned about the time It takes to load the image for users on the west coast.
       What are the two best ways to speed up serving this image?
       Choose 2 answers

       A. Use Route 53's Latency Based Routing and serve the image out of US-West-2 as well as
       US-East-1
       B. Serve the image out through CloudFront
       C. Serve the image out of S3 so that it isn't being served oft of your web application tier
       D. Use EBS PIOPs to serve the image faster out of your EC2 instances

       Answer: A,B

   QUESTION NO: 52

       If you want to launch Amazon Elastic Compute Cloud (EC2) Instances and assign each Instance
       a predetermined private IP address you should:

       A. Assign a group or sequential Elastic IP address to the instances
       B. Launch the instances in a Placement Group
       C. Launch the instances in the Amazon virtual Private Cloud (VPC).
       D. Use standard EC2 instances since each instance gets a private Domain Name Service (DNS)
       already
       E. Launch the Instance from a private Amazon Machine image (Mil)

       Answer: C

       Reference:
       http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-ip-addressing.html

   QUESTION NO: 53

       A customer has a web application that uses cookie Based sessions to track logged in users It Is
       deployed on AWS using ELB and Auto Scaling The customer observes that when load increases.
       Auto Scaling launches new Instances but the load on the easting Instances does not decrease,
       causing all existing users to have a sluggish experience.
       Which two answer choices independently describe a behavior that could be the cause of the
       sluggish user experience?
       Choose 2 answers

       A. ELB's normal behavior sends requests from the same user to the same backend instance
       B. ELB's behavior when sticky sessions are enabled causes ELB to send requests in the same
       session to the same backend instance
       C. A faulty browser is not honoring the TTL of the ELB DNS name.
       D. The web application uses long polling such as comet or websockets. Thereby keeping a
       connection open to a web server tor a long time
       E. The web application uses long polling such as comet or websockets. Thereby keeping a
       connection open to a web server for a long time.

       Answer: B,D

   QUESTION NO: 54

       What would happen to an RDS (Relational Database Service) multi-Availability Zone deployment
       of the primary OB instance fails?

       A. The IP of the primary DB instance is switched to the standby OB instance
       B. The RDS (Relational Database Service) DB instance reboots
       C. A new DB instance is created in the standby availability zone
       D. The canonical name record (CNAME) is changed from primary to standby

       Answer: B

   QUESTION NO: 55

       How can the domain's zone apex for example "myzoneapexdomain com" be pointed towards an
       Elastic Load Balancer?
       A. By using an AAAA record
       B. By using an A record
       C. By using an Amazon Route 53 CNAME record
       D. By using an Amazon Route 53 Alias record

       Answer: C

       Reference:
       http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosingalias-non-alias.html
       Topic 2, Volume B

   QUESTION NO: 56

       An organization has created 5 IAM users. The organization wants to give them the same login ID
       but different passwords. How can the organization achieve this?

       A. The organization should create a separate login ID but give the IAM users the same alias
       so that each one can login with their alias
       B. The organization should create each user in a separate region so that they have their own
       URL to login
       C. It is not possible to have the same login ID for multiple IAM users of the same account
       D. The organization should create various groups and add each user with the same login ID
       to different groups. The user can login with their own group ID

       Answer: C

       Explanation:
       AWS Identity and Access Management is a web service which allows organizations to manage
       users and user permissions for various AWS services. Whenever the organization is creating an
       IAM user, there should be a unique ID for each user. It is not possible to have the same login ID
       for multiple users. The names of users,groups, roles, instance profiles must be alphanumeric,
       including the following common characters: plus(+), equal(=), comma(,), period(.), at(@), and dash (-)

   QUESTION NO: 57

       A user is planning to evaluate AWS for their internal use. The user does not want to incur any
       charge on his account during the evaluation. Which of the below mentioned AWS services would
       incur a charge if used?

       A. AWS S3 with 1 GB of storage
       B. AWS micro instance running 24 hours daily
       C. AWS ELB running 24 hours a day
       D. AWS PIOPS volume of 10 GB size

       Answer: D

       Explanation:
       AWS is introducing a free usage tier for one year to help the new AWS customers get started in
       Cloud. The free tier can be used for anything that the user wants to run in the Cloud. AWS offers
       a handful of AWS services as a part of this which includes 750 hours of free micro instances and
       750 hours of ELB. It includes the AWS S3 of 5 GB and AWS EBS general purpose volume upto
       30 GB. PIOPS is not part of free usage tier.

   QUESTION NO: 58

       A user has developed an application which is required to send the data to a NoSQL database.
       The user wants to decouple the data sending such that the application keeps processing and
       sending data but does not wait for an acknowledgement of DB. Which of the below mentioned
       applications helps in this scenario?

       A. AWS Simple Notification Service
       B. AWS Simple Workflow
       C. AWS Simple Queue Service
       D. AWS Simple Query Service

       Answer: C

       Explanation:
       Amazon Simple Queue Service (SQS. is a fast, reliable, scalable, and fully managed message
       queuing service. SQS provides a simple and cost-effective way to decouple the components of an
       application. In this case, the user can use AWS SQS to send messages which are received from
       an application and sent to DB. The application can continue processing data without waiting for
       any acknowledgement from DB. The user can use SQS to transmit any volume of data without
       losing messages or requiring other services to always be available.

   QUESTION NO: 59

       An organization has created 50 IAM users. The organization has introduced a new policy which
       will change the access of an IAM user. How can the organization implement this effectively so that
       there is no need to apply the policy at the individual user level?

       A. Use the IAM groups and add users as per their role to different groups and apply policy
       to group
       B. The user can create a policy and apply it to multiple users in a single go with the AWS CLI
       C. Add each user to the IAM role as per their organization role to achieve effective policy setup
       D. Use the IAM role and implement access at the role level

       Answer: A

       Explanation:
       With AWS IAM, a group is a collection of IAM users. A group allows the user to specify
       permissions for a
       collection of users, which can make it easier to manage the permissions for those users. A group
       helps an organization manage access in a better way; instead of applying at the individual level,
       the organization can apply at the group level which is applicable to all the users who are a part
       of that group.

   QUESTION NO: 60

       A user is planning to use AWS Cloud formation for his automatic deployment requirements. Which
       of the below mentioned components are required as a part of the template?

       A. Parameters
       B. Outputs
       C. Template version
       D. Resources

       Answer: D

       Explanation:
       AWS Cloud formation is an application management tool which provides application modelling,
       deployment, configuration, management and related activities. The template is a JSON-format,
       text-based file that describes all the AWS resources required to deploy and run an application. It
       can have option fields, such as Template Parameters, Output, Data tables, and Template file
       format version. The only mandatory value is Resource. The user can define the AWS services
       which will be used/ created by this template inside the Resource section

   QUESTION NO: 61

       A user has recently started using EC2. The user launched one EC2 instance in the default subnet
       in EC2-VPC Which of the below mentioned options is not attached or available with the EC2
       instance when it is launched?

       A. Public IP address
       B. Internet gateway
       C. Elastic IP
       D. Private IP address

       Answer: C

       Explanation:
       A Virtual Private Cloud (VPC. is a virtual network dedicated to a user’s AWS account. A subnet is a
       range of IP addresses in the VPC. The user can launch the AWS resources into a subnet. There
       are two supported platforms into which a user can launch instances: EC2-Classic and EC2-VPC
       (default subnet.. A default VPC has all the benefits of EC2-VPC and the ease of use of EC2-
       Classic. Each instance that the user launches into a default subnet has a private IP address and a
       public IP address. These instances can communicate with the internet through an internet
       gateway. An internet gateway enables the EC2 instances to connect to the internet through the
       Amazon EC2 network edge.

   QUESTION NO: 62

       A user has launched an EC2 instance. The user is planning to setup the CloudWatch alarm.
       Which of the
       below mentioned actions is not supported by the CloudWatch alarm?

       A. Notify the Auto Scaling launch config to scale up
       B. Send an SMS using SNS
       C. Notify the Auto Scaling group to scale down
       D. Stop the EC2 instance

       Answer: B

       Explanation:
       A user can create a CloudWatch alarm that takes various actions when the alarm changes state.
       An alarm watches a single metric over the time period that the user has specified, and performs
       one or more actions based on the value of the metric relative to a given threshold over a number
       of time periods. The actions could be sending a notification to an Amazon Simple Notification
       Service topic (SMS, Email, and HTTP end point.,notifying the Auto Scaling policy or changing the
       state of the instance to Stop/Terminate.

   QUESTION NO: 63

       A user is trying to delete an Auto Scaling group from CLI. Which of the below mentioned steps are
       to be performed by the user?

       A. Terminate the instances with the ec2-terminate-instance command
       B. Terminate the Auto Scaling instances with the as-terminate-instance command
       C. Set the minimum size and desired capacity to 0
       D. There is no need to change the capacity. Run the as-delete-group command and it will reset
       all values to 0

       Answer: C

       Explanation:
       If the user wants to delete the Auto Scaling group, the user should manually set the values of the
       minimum and desired capacity to 0. Otherwise Auto Scaling will not allow for the deletion of the
       group from CLI. While trying from the AWS console, the user need not set the values to 0 as the
       Auto Scaling console will automatically do so.

   QUESTION NO: 64

       An organization is planning to create 5 different AWS accounts considering various security
       requirements. The organization wants to use a single payee account by using the consolidated
       billing option. Which of the below mentioned statements is true with respect to the above
       information?

       A. Master (Payee. account will get only the total bill and cannot see the cost incurred by
       each account
       B. Master (Payee. account can view only the AWS billing details of the linked accounts
       C. It is not recommended to use consolidated billing since the payee account will have access
       to the linked accounts
       D. Each AWS account needs to create an AWS billing policy to provide permission to the
       payee account

       Answer: B

       Explanation:
       AWS consolidated billing enables the organization to consolidate payments for multiple Amazon
       Web Services (AWS. accounts within a single organization by making a single paying account.
       Consolidated billing enables the organization to see a combined view of the AWS charges
       incurred by each account as well as obtain a detailed cost report for each of the individual AWS
       accounts associated with the paying account. The payee account will not have any other
       access than billing data of linked accounts.

   QUESTIONNO: 64-A

       A user has deployed an application on his private cloud. The user is using his own monitoring tool.
       He wants to configure that whenever there is an error, the monitoring tool should notify him via
       SMS. Which of the below mentioned AWS services will help in this scenario?

       A. None because the user infrastructure is in the private cloud/
       B. AWS SNS
       C. AWS SES
       D. AWS SMS

       Answer: B

       Amazon Simple Notification Service (Amazon SNS. is a fast, flexible, and fully managed push
       messaging service. Amazon SNS can be used to make push notifications to mobile devices.
       Amazon SNS can deliver notifications by SMS text message or email to the Amazon Simple
       Queue Service (SQS. queues or to any HTTP endpoint. In this case user can use the SNS apis
       to send SMS.

   QUESTION NO: 65

       A user has created a web application with Auto Scaling. The user is regularly monitoring the
       application and he observed that the traffic is highest on Thursday and Friday between 8 AM to
       6 PM. What is the best solution to handle scaling in this case?

       A. Add a new instance manually by 8 AM Thursday and terminate the same by 6 PM Friday
       B. Schedule Auto Scaling to scale up by 8 AM Thursday and scale down after 6 PM on Friday
       C. Schedule a policy which may scale up every day at 8 AM and scales down by 6 PM
       D. Configure a batch process to add a instance by 8 AM and remove it by Friday 6 PM

       Answer: B

       Explanation:
       Auto Scaling based on a schedule allows the user to scale the application in response to
       predictable load changes. In this case the load increases by Thursday and decreases by Friday.
       Thus, the user can setup the scaling activity based on the predictable traffic patterns of the web
       application using Auto Scaling scale by Schedule.

   QUESTION NO: 66

       A user has setup a CloudWatch alarm on an EC2 action when the CPU utilization is above 75%.
       The alarm sends a notification to SNS on the alarm state. If the user wants to simulate the alarm
       action how can he achieve this?

       A. Run activities on the CPU such that its utilization reaches above 75%
       B. From the AWS console change the state to ‘Alarm’
       C. The user can set the alarm state to ‘Alarm’ using CLI
       D. Run the SNS action manually

       Answer: C

       Explanation:
       Amazon CloudWatch alarms watch a single metric over a time period that the user specifies and
       performs one or more actions based on the value of the metric relative to a given threshold over
       a number of time periods.The user can test an alarm by setting it to any state using the
       SetAlarmState API (mon-set-alarm-state command.. This temporary state change lasts only until
       the next alarm comparison occurs.

   QUESTION 13

       A user is trying to setup a scheduled scaling activity using Auto Scaling. The user wants to setup
       the recurring schedule. Which of the below mentioned parameters is not required in this case?

       A. Maximum size
       B. Auto Scaling group name
       C. End time
       D. Recurrence value

       Answer: A

       Auto Scaling based on a schedule allows the user to scale the application in response to
       predictable load changes. The user can also configure the recurring schedule action which will
       follow the Linux cron format. If the user is setting a recurring event, it is required that the user
       specifies the Recurrence value (in a cron format., end time (not compulsory but recurrence will
       stop after this. and the Auto Scaling group for which the scaling activity is to be scheduled.

   QUESTION NO: 67

       A user has setup a billing alarm using CloudWatch for $200. The usage of AWS exceeded $200
       after some days. The user wants to increase the limit from $200 to $400? What should the user do?

       A. Create a new alarm of $400 and link it with the first alarm
       B. It is not possible to modify the alarm once it has crossed the usage limit
       C. Update the alarm to set the limit at $400 instead of $200
       D. Create a new alarm for the additional $200 amount

       Answer: C

       Explanation:
       AWS CloudWatch supports enabling the billing alarm on the total AWS charges. The estimated
       charges are calculated and sent several times daily to CloudWatch in the form of metric data.
       This data will be stored for 14 days. This data also includes the estimated charges for every
       service in AWS used by the user, as well as the estimated overall AWS charges. If the user
       wants to increase the limit, the user can modify the alarm and specify a new threshold.

   QUESTION NO: 68

       A sys admin has created the below mentioned policy and applied to an S3 object named aws.jpg.
       The aws.jpg is inside a bucket named cloudacademy. What does this policy define?
       "Statement": [{
       "Sid": "Stmt1388811069831",
       "Effect": "Allow",
       "Principal": { "AWS": "*"},
       "Action": [ "s3:GetObjectAcl", "s3:ListBucket", "s3:GetObject"],
       "Resource": [ "arn:aws:s3:::cloudacademy/*.jpg"]
       }]

       A. It is not possible to define a policy at the object level
       B. It will make all the objects of the bucket cloudacademy as public
       C. It will make the bucket cloudacademy as public
       D. the aws.jpg object as public

       Answer: A

       Explanation:
       A system admin can grant permission to the S3 objects or buckets to any user or make objects
       public using the bucket policy and user policy. Both use the JSON-based access policy
       language. Generally if the user is defining the ACL on the bucket, the objects in the bucket do not
       inherit it and vice a versa. The bucket policy can be defined at the bucket level which allows the
       objects as well as the bucket to be public with a single policy applied to that bucket. It cannot be
       applied at the object level.

   QUESTION NO: 69

       A user is trying to save some cost on the AWS services. Which of the below mentioned options
       will not help him save cost?
       A. Delete the unutilized EBS volumes once the instance is terminated
       B. Delete the AutoScaling launch configuration after the instances are terminated
       C. Release the elastic IP if not required once the instance is terminated
       D. Delete the AWS ELB after the instances are terminated

       Answer: B

       Explanation:
       AWS bills the user on a as pay as you go model. AWS will charge the user once the AWS
       resource is allocated. Even though the user is not using the resource, AWS will charge if it is in service or
       allocated. Thus, it is advised that once the user’s work is completed he should: Terminate the EC2 
       instance Delete the EBS volumes Release the unutilized Elastic IPs Delete ELB The AutoScaling launch
       configuration does not cost the user. Thus, it will not make any difference to the cost whether it is 
       deleted or not.

   QUESTION NO: 70

       A user is trying to aggregate all the CloudWatch metric data of the last 1 week. Which of the
       below mentioned statistics is not available for the user as a part of data aggregation?

       A. Aggregate
       B. Sum
       C. Sample data
       D. Average

       Answer: A

       Explanation:
       Amazon CloudWatch is basically a metrics repository. Either the user can send the custom data
       or an AWS product can put metrics into the repository, and the user can retrieve the statistics
       based on those metrics. The statistics are metric data aggregations over specified periods of time.
       Aggregations are made using the namespace, metric name, dimensions, and the data point unit
       of measure, within the time period that is specified by the user. CloudWatch supports Sum, Min,
       Max, Sample Data and Average statistics aggregation.

   QUESTION NO: 71

       An organization is planning to use AWS for their production roll out. The organization wants to
       implement automation for deployment such that it will automatically create a LAMP stack, download the
       latest PHP installable from S3 and setup the ELB. Which of the below mentioned AWS services meets the
       quirement for making an orderly deployment of the software?

       A. AWS Elastic Beanstalk
       B. AWS Cloudfront
       C. AWS Cloudformation
       D. AWS DevOps

       Answer: C

       Explanation:
       AWS Cloudformation is an application management tool which provides application modelling,
       deployment, configuration, management and related activities. Cloudformation provides an easy
       way to create and delete the collection of related AWS resources and provision them in an orderly
       way. AWS CloudFormation automates and simplifies the task of repeatedly and predictably
       creating groups of related resources that power the user’s applications. AWS Cloudfront is a CDN;
       Elastic Beanstalk does quite a few of the required tasks. However, it is a PAAS which uses a
       ready AMI. AWS Elastic Beanstalk provides an environment to easily develop and run
       applications in the cloud.

   QUESTION NO: 72

       A user has created a subnet with VPC and launched an EC2 instance in that subnet with only
       default settings.Which of the below mentioned options is ready to use on the EC2 instance as
       soon as it is launched?

       A. Elastic IP
       B. Private IP
       C. Public IP
       D. I nternet gateway

       Answer: B

       Explanation:
       A Virtual Private Cloud (VPC. is a virtual network dedicated to a user’s AWS account. A subnet is
       a range of IP addresses in the VPC. The user can launch the AWS resources into a subnet.
       There are two supported platforms into which a user can launch instances: EC2-Classic and
       EC2-VPC. When the user launches an instance which is not a part of the non-default subnet, it
       will only have a private IP assigned to it. The instances part of a subnet can communicate with
       each other but cannot communicate over the internet or to the AWS services, such as RDS / S3.

   QUESTION NO: 73

       An organization is setting up programmatic billing access for their AWS account. Which of the
       below mentioned services is not required or enabled when the organization wants to use
       programmatic access?

       A. Programmatic access
       B. AWS bucket to hold the billing report
       C. AWS billing alerts
       D. Monthly Billing report

       Answer: C

       Explanation:
       AWS provides an option to have programmatic access to billing. Programmatic Billing Access
       leverages the existing Amazon Simple Storage Service (Amazon S3. APIs. Thus, the user can
       build applications that reference his billing data from a CSV (comma-separated value. file stored
       in an Amazon S3 bucket. To enable programmatic access, the user has to first enable the
       monthly billing report. Then the user needs to provide an AWS bucket name where the billing
       CSV will be uploaded. The user should also enable the Programmatic access option.

   QUESTION NO: 74

       A user has configured the Auto Scaling group with the minimum capacity as 3 and the maximum capacity
       as 5. When the user configures the AS group, how many instances will Auto Scaling launch?

       A. 3
       B. 0
       C. 5
       D. 2

       Answer: C

       Explanation:
       When the user configures the launch configuration and the Auto Scaling group, the Auto Scaling
       group will start instances by launching the minimum number (or the desired number, if specified.
       of EC2 instances. If there are no other scaling conditions attached to the Auto Scaling group, it
       will maintain the minimum number of running instances at all times.

   QUESTION NO: 75

       An admin is planning to monitor the ELB. Which of the below mentioned services does not help
       the admin capture the monitoring information about the ELB activity?

       A. ELB Access logs
       B. ELB health check
       C. CloudWatch metrics
       D. ELB API calls with CloudTrail

       Answer: B

       Explanation:
       The admin can capture information about Elastic Load Balancer using either:
       CloudWatch Metrics ELB Logs files which are stored in the S3 bucket CloudTrail with API calls
       which can notify the user as well generate logs for each API calls The health check is
       internally performed by ELB and does not help the admin get the ELB activity.

 {!inpage-ads.md!}

   QUESTION NO: 76

       A user is planning to use AWS Cloudformation. Which of the below mentioned functionalities does
       not help him to correctly understand Cloudfromation?

       A. Cloudformation follows the DevOps model for the creation of Dev & Test
       B. AWS Cloudfromation does not charge the user for its service but only charges for the
          AWS resources created with it
       C. Cloudformation works with a wide variety of AWS services, such as EC2, EBS, VPC, IAM,
          S3, RDS, ELB, etc
       D. CloudFormation provides a set of application bootstrapping scripts which enables the user
          to install Software

       Answer: A

       Explanation:
       AWS Cloudformation is an application management tool which provides application modelling,
       deployment, configuration, management and related activities. It supports a wide variety of AWS
       services, such as EC2, EBS, AS, ELB, RDS, VPC, etc. It also provides application bootstrapping
       scripts which enable the user to install software packages or create folders. It is free of the cost
       and only charges the user for the services created with it. The only challenge is that it does not
       follow any model, such as DevOps; instead customers can define templates and use them to
       provision and manage the AWS resources in an orderly way.

   QUESTION NO: 77

       A user has launched 10 instances from the same AMI ID using Auto Scaling. The user is trying to
       see the average CPU utilization across all instances of the last 2 weeks under the CloudWatch
       console. How can the user achieve this?

       A. View the Auto Scaling CPU metrics
       B. Aggregate the data over the instance AMI ID
       C. The user has to use the CloudWatchanalyser to find the average data across instances
       D. It is not possible to see the average CPU utilization of the same AMI ID since the instance ID
       is different

       Answer: B

       Explanation:
       Amazon CloudWatch is basically a metrics repository. Either the user can send the custom data
       or an AWS product can put metrics into the repository, and the user can retrieve the statistics
       based on those metrics. The statistics are metric data aggregations over specified periods of time.
       Aggregations are made using the namespace, metric name, dimensions, and the data point unit
       of measure, within the time period that is specified by the user. To aggregate the data across
       instances launched with AMI, the user should select the AMI ID under EC2 metrics and select the
       aggregate average to view the data.

   QUESTION NO: 78

       A user is trying to understand AWS SNS. To which of the below mentioned end points is SNS
       unable to send a notification?

       A. Email JSON
       B. HTTP
       C. AWS SQS
       D. AWS SES

       Answer: D

       Explanation:
       Amazon Simple Notification Service (Amazon SNS. is a fast, flexible, and fully managed push
       messaging service. Amazon SNS can deliver notifications by SMS text message or email to the
       Amazon Simple Queue Service (SQS. queues or to any HTTP endpoint. The user can select one
       the following transports as part of the subscription requests: “HTTP”, “HTTPS”,”Email”, “EmailJSON”,
       “SQS”, “and SMS”.

   QUESTION NO: 79

       A user has configured an Auto Scaling group with ELB. The user has enabled detailed
       CloudWatch monitoring on Auto Scaling. Which of the below mentioned statements will help
       the user understand the functionality better?

       A. It is not possible to setup detailed monitoring for Auto Scaling
       B. In this case, Auto Scaling will send data every minute and will charge the user extra
       C. Detailed monitoring will send data every minute without additional charges
       D. Auto Scaling sends data every minute only and does not charge the user

       Answer: B

       Explanation:
       CloudWatch is used to monitor AWS as well as the custom services. It provides either basic or
       detailed monitoring for the supported AWS products. In basic monitoring, a service sends data points to
       CloudWatch every five minutes, while in detailed monitoring a service sends data points to CloudWatch every 
       minute. Auto Scaling includes 7 metrics and 1 dimension, and sends data to CloudWatch every 5 minutes by default.
       The user can enable detailed monitoring for Auto Scaling, which sends data to CloudWatch every minute. However,
       this will have some extra-costs.


   QUESTION NO: 80

       A system admin is planning to setup event notifications on RDS. Which of the below mentioned
       services will help the admin setup notifications?

       A. AWS SES
       B. AWS Cloudtrail
       C. AWS Cloudwatch
       D. AWS SNS

       Answer: D

       Explanation:
       Amazon RDS uses the Amazon Simple Notification Service to provide a notification when an
       Amazon RDS event occurs. These notifications can be in any notification form supported by
       Amazon SNS for an AWS region, such as an email, a text message or a call to an HTTP endpoint

   QUESTION NO: 81

       You are building an online store on AWS that uses SQS to process your customer orders. Your backend
       system needs those messages in the same sequence the customer orders have been put in. How can you achieve that?

       A. It is not possible to do this with SQS
       B. You can use sequencing information on each message
       C. You can do this with SQS but you also need to use SWF
       D. Messages will arrive in the same order by default

       Answer: B

       Explanation:
       Amazon SQS is engineered to always be available and deliver messages. One of the resulting
       tradeoffs is that SQSdoes not guarantee first in, first out delivery of messages. For many
       distributed applications, each message can stand on its own, and as long as all messages are
       delivered, the order is not important. If your system requires that order be preserved, you can
       place sequencing information in each message, so that you can reorder the messages when
       the queue returns them.

   QUESTION NO: 82

       An organization wants to move to Cloud. They are looking for a secure encrypted database
       storage option. Which of the below mentioned AWS functionalities helps them to achieve this?

       A. AWS MFA with EBS
       B. AWS EBS encryption
       C. Multi-tier encryption with Redshift
       D. AWS S3 server side storage

       Answer: B

       Explanation:
       AWS EBS supports encryption of the volume while creating new volumes. It also supports
       creating volumes from existing snapshots provided the snapshots are created from encrypted
       volumes. The data at rest, the I/O as well as all the snapshots of EBS will be encrypted. The
       encryption occurs on the servers that host the EC2 instances, providing encryption of data as it
       moves between the EC2 instances and EBS storage. EBS encryption is based on the AES-256
       cryptographic algorithm, which is the industry standard

   QUESTION NO: 83

       A user wants to disable connection draining on an existing ELB. Which of the below mentioned
       statements helps the user disable connection draining on the ELB?

       A. The user can only disable connection draining from CLI
       B. It is not possible to disable the connection draining feature once enabled
       C. The user can disable the connection draining feature from EC2 -> ELB console or from CLI
       D. The user needs to stop all instances before disabling connection draining

       Answer: C

       Explanation:
       The Elastic Load Balancer connection draining feature causes the load balancer to stop
       sending new requests to the back-end instances when the instances are deregistering or
       become unhealthy, while ensuring that inflight requests continue to be served. The user can
       enable or disable connection draining from the AWS EC2 console -> ELB or using CLI.

   QUESTION NO: 84

       A user has a refrigerator plant. The user is measuring the temperature of the plant every 15
       minutes. If the user wants to send the data to CloudWatch to view the data visually, which of the
       below mentioned statements is true with respect to the information given above?

       A. The user needs to use AWS CLI or API to upload the data
       B. The user can use the AWS Import Export facility to import data to CloudWatch
       C. The user will upload data from the AWS console
       D. The user cannot upload data to CloudWatch since it is not an AWS service metric

       Answer: A
       Explanation:
       AWS CloudWatch supports the custom metrics. The user can always capture the custom data
       and upload the data to CloudWatch using CLI or APIs. While sending the data the user has to
       include the metric name, namespace and timezone as part of the request.

   QUESTION NO: 85

       A system admin is managing buckets, objects and folders with AWS S3. Which of the below mentioned
       statements is true and should be taken in consideration by the sysadmin?

       A. The folders support only ACL
       B. Both the object and bucket can have an Access Policy but folder cannot have policy
       C. Folders can have a policy
       D. Both the object and bucket can have ACL but folders cannot have ACL

       Answer: A

       Explanation:
       A sysadmin can grant permission to the S3 objects or the buckets to any user or make objects
       public using the bucket policy and user policy. Both use the JSON-based access policy
       language. Generally if user is defining the ACL on the bucket, the objects in the bucket do not
       inherit it and vice a versa. The bucket policy can be defined at the bucket level which allows the
       objects as well as the bucket to be public with a single policy applied to that bucket. It cannot be
       applied at the object level. The folders are similar to objects with no content. Thus, folders can
       have only ACL and cannot have a policy.

   QUESTION NO: 86

       A user has created an ELB with three instances. How many security groups will ELB create by
       default?

       A. 3
       B. 5
       C. 2
       D. 1

       Answer: C

       Explanation:
       Elastic Load Balancing provides a special Amazon EC2 source security group that the user can
       use to ensure that back-end EC2 instances receive traffic only from Elastic Load Balancing. This
       feature needs two security groups: the source security group and a security group that defines
       the ingress rules for the back-end instances. To ensure that traffic only flows between the load
       balancer and the back-end instances, the user can add or modify a rule to the back-end security
       group which can limit the ingress traffic. Thus, it can come only from the source security group
       provided by Elastic load Balancing.

   QUESTION NO: 87

       An organization has created 50 IAM users. The organization wants that each user can change
       their password but cannot change their access keys. How can the organization achieve this?

       A. The organization has to create a special password policy and attach it to each user
       B. The root account owner has to use CLI which forces each IAM user to change their password on 
          first login
       C. By default each IAM user can modify their passwords
       D. The root account owner can set the policy from the IAM console under the password policy screen

       Answer: D

       Explanation:
       With AWS IAM, organizations can use the AWS Management Console to display, create, change
       or delete a password policy. As a part of managing the password policy, the user can enable all
       users to manage their own passwords. If the user has selected the option which allows the IAM
       users to modify their password, he does not need to set a separate policy for the users. This
       option in the AWS console allows changing only the password.

   QUESTION NO: 88

       A user has created a photo editing software and hosted it on EC2. The software accepts
       requests from the user about the photo format and resolution and sends a message to S3 to
       enhance the picture accordingly.Which of the below mentioned AWS services will help make a
       scalable software with the AWS infrastructure in this scenario?

       A. AWS Glacier
       B. AWS Elastic Transcoder
       C. AWS Simple Notification Service
       D. AWS Simple Queue Service

       Answer: D

       Explanation:
       Amazon Simple Queue Service (SQS. is a fast, reliable, scalable, and fully managed message
       queuing service. SQS provides a simple and cost-effective way to decouple the components of
       an application. The user can configure SQS, which will decouple the call between the EC2
       application and S3. Thus, the application does not keep waiting for S3 to provide the data.

   QUESTION NO: 89

       An application is generating a log file every 5 minutes. The log file is not critical but may be
       required only for verification in case of some major issue. The file should be accessible over the
       internet whenever required. Which of the below mentioned options is a best possible storage
       solution for it?

       A. AWS S3
       B. AWS Glacier
       C. AWS RDS
       D. AWS RRS

       Answer: D

       Explanation:
       Amazon S3 stores objects according to their storage class. There are three major storage
       classes: Standard, Reduced Redundancy Storage and Glacier. Standard is for AWS S3 and
       provides very high durability. However, the costs are a little higher. Glacier is for archival and the
       files are not available over the internet. Reduced Redundancy Storage is for less critical files.
       Reduced Redundancy is little cheaper as it provides less durability in comparison to S3. In this
       case since the log files are not mission critical files, RRS will be a better option.

   QUESTION NO: 90

       A user has created a VPC with CIDR 20.0.0.0/24. The user has created a public subnet with
       CIDR 20.0.0.0/25. The user is trying to create the private subnet with CIDR 20.0.0.128/25. Which
       of the below mentioned statements is true in this scenario?

       A. It will not allow the user to create the private subnet due to a CIDR overlap
       B. It will allow the user to create a private subnet with CIDR as 20.0.0.128/25
       C. This statement is wrong as AWS does not allow CIDR 20.0.0.0/25
       D. It will not allow the user to create a private subnet due to a wrong CIDR range

       Answer: B

       Explanation:
       When the user creates a subnet in VPC, he specifies the CIDR block for the subnet. The CIDR
       block of a subnet can be the same as the CIDR block for the VPC (for a single subnet in the
       VPC., or a subset (to enable multiple subnets.. If the user creates more than one subnet in a
       VPC, the CIDR blocks of the subnets must not overlap. Thus, in this case the user has created a
       VPC with the CIDR block 20.0.0.0/24, which supports 256 IP addresses (20.0.0.0 to 20.0.0.255..
       The user can break this CIDR block into two subnets, each supporting 128 IP addresses. One
       subnet uses the CIDR block 20.0.0.0/25 (for addresses 20.0.0.0 - 20.0.0.127. and the other uses
       the CIDR block 20.0.0.128/25 (for addresses 20.0.0.128 - 20.0.0.255..

   QUESTION NO: 91

       A user has created an S3 bucket which is not publicly accessible. The bucket is having thirty
       objects which are also private. If the user wants to make the objects public, how can he configure
       this with minimal efforts?

       A. The user should select all objects from the console and apply a single policy to mark
          them public
       B. The user can write a program which programmatically makes all objects public using S3 SDK
       C. Set the AWS bucket policy which marks all objects as public
       D. Make the bucket ACL as public so it will also mark all objects as public

       Answer: C

       Explanation:
       A system admin can grant permission of the S3 objects or buckets to any user or make the
       objects public using the bucket policy and user policy. Both use the JSON-based access policy
       language. Generally if the user is defining the ACL on the bucket, the objects in the bucket do not
       inherit it and vice a versa. The bucket policy can be defined at the bucket level which allows the
       objects as well as the bucket to be public with a single policy applied to that bucket.

   QUESTION NO: 92

       A sys admin is maintaining an application on AWS. The application is installed on EC2 and user
       has configured ELB and Auto Scaling. Considering future load increase, the user is planning to
       launch new servers proactively so that they get registered with ELB. How can the user add these
       instances with Auto Scaling?

       A. Increase the desired capacity of the Auto Scaling group
       B. Increase the maximum limit of the Auto Scaling group
       C. Launch an instance manually and register it with ELB on the fly
       D. Decrease the minimum limit of the Auto Scaling grou

       Answer: A

       Explanation:
       A user can increase the desired capacity of the Auto Scaling group and Auto Scaling will launch a
       new instance as per the new capacity. The newly launched instances will be registered with ELB if
       Auto Scaling group is configured with ELB. If the user decreases the minimum size the instances
       will be removed from Auto Scaling. Increasing the maximum size will not add instances but only
       set the maximum instance cap.

   QUESTION NO: 93

       An organization, which has the AWS account ID as 999988887777, has created 50 IAM users. All
       the users are added to the same group cloudacademy. If the organization has enabled that each
       IAM user can login with the AWS console, which AWS login URL will the IAM users use?

       A. https:// 999988887777.signin.aws.amazon.com/console/
       B. https:// signin.aws.amazon.com/cloudacademy/
       C. https:// cloudacademy.signin.aws.amazon.com/999988887777/console/
       D. https:// 999988887777.aws.amazon.com/ cloudacademy/

       Answer: A

       Explanation:
       AWS Identity and Access Management is a web service which allows organizations to manage
       users and user permissions for various AWS services. Once the organization has created the IAM
       users, they will have a separate AWS console URL to login to the AWS console. The console login
       URL for the IAM user will be https:// AWS_Account_ID.signin.aws.amazon.com/console/. It uses
       only the AWS account ID and does not depend on the group or user ID.

   QUESTION NO: 94

       A user has setup connection draining with ELB to allow in-flight requests to continue while the
       instance is being deregistered through Auto Scaling. If the user has not specified the draining
       time, how long will ELB allow inflight requests traffic to continue?

       A. 600 seconds
       B. 3600 seconds
       C. 300 seconds
       D. 0 seconds

       Answer: C

       Explanation:
       The Elastic Load Balancer connection draining feature causes the load balancer to stop sending
       new requests to the back-end instances when the instances are deregistering or become unhealthy,
       while ensuring that inflight requests continue to be served. The user can specify a maximum time
       (3600 seconds. for the load balancer to keep the connections alive before reporting the instance as
       deregistered. If the user does not specify the maximum timeout period, by default, the load balancer
       will close the connections to the deregistering instance after 300 seconds.

   QUESTION NO: 95

       A root AWS account owner is trying to understand various options to set the permission to AWS
       S3. Which of the below mentioned options is not the right option to grant permission for S3?

       A. User Access Policy
       B. S3 Object Access Policy
       C. S3 Bucket Access Policy
       D. S3 ACL

       Answer: B

       Explanation:
       Amazon S3 provides a set of operations to work with the Amazon S3 resources. Managing S3
       resource access refers to granting others permissions to work with S3. There are three ways
       the root account owner can define access with S3:
       S3 ACL: The user can use ACLs to grant basic read/write permissions to other AWS accounts.
       S3 Bucket Policy: The policy is used to grant other AWS accounts or IAM users permissions for
       the bucket and the objects in it.
       User Access Policy: Define an IAM user and assign him the IAM policy which grants him access to S3.

   QUESTION NO: 96

       A sys admin has created a shopping cart application and hosted it on EC2. The EC2 instances
       are running behind ELB. The admin wants to ensure that the end user request will always go to
       the EC2 instance where the user session has been created. How can the admin configure this?

       A. Enable ELB cross zone load balancing
       B. Enable ELB cookie setup
       C. Enable ELB sticky session
       D. Enable ELB connection draining

       Answer: C

       Explanation:
       Generally AWS ELB routes each request to a zone with the minimum load. The Elastic Load
       Balancer provides a feature called sticky session which binds the user’s session with a specific
       EC2 instance. If the sticky session is enabled the first request from the user will be redirected to
       any of the EC2 instances. But, henceforth, all requests from the same user will be redirected to
       the same EC2 instance. This ensures that all requests coming from the user during the session
       will be sent to the same application instance.

   QUESTION NO: 97

       A user has configured ELB with three instances. The user wants to achieve High Availabilityi as well
       as redundancy with ELB. Which of the below mentioned AWS services helps the user achieve this for
       ELB?

       A. Route 53
       B. AWS Mechanical Turk
       C. Auto Scaling
       D. AWS EMR

       Answer: A

       Explanation:
       The user can provide high availability and redundancy for applications running behind Elastic
       Load Balancer by enabling the Amazon Route 53 Domain Name System (DNS. failover for the
       load balancers. Amazon Route 53 is a DNS service that provides reliable routing to the user’s
       infrastructure.

   QUESTION NO: 98

       An organization is using AWS since a few months. The finance team wants to visualize the pattern
       of AWS spending. Which of the below AWS tool will help for this requirement?

       A. AWS Cost Manager
       B. AWS Cost Explorer
       C. AWS CloudWatch
       D. AWS Consolidated Billing

       Answer: B

       Explanation:
       The AWS Billing and Cost Management console includes the Cost Explorer tool for viewing AWS
       cost data as a graph. It does not charge extra to user for this service. With Cost Explorer the user
       can filter graphs using resource tags or with services in AWS. If the organization is using
       Consolidated Billing it helps generate report based on linked accounts. This will help organization
       to identify areas that require further inquiry. The organization can view trends and use that to
       understand spend and to predict future costs.

   QUESTION NO: 99

       A user has launched an ELB which has 5 instances registered with it. The user deletes the ELB by
       mistake. What will happen to the instances?

       A. ELB will ask the user whether to delete the instances or not
       B. Instances will be terminated
       C. ELB cannot be deleted if it has running instances registered with it
       D. Instances will keep running

       Answer: D

       Explanation:
       When the user deletes the Elastic Load Balancer, all the registered instances will be deregistered.
       However, they will continue to run. The user will incur charges if he does not take any action on
       those instances.

   QUESTION NO: 100

       A user is planning to setup notifications on the RDS DB for a snapshot. Which of the below
       mentioned event categories is not supported by RDS for this snapshot source type?

       A. Backup
       B. Creation
       C. Deletion
       D. Restoration

       Answer: A

       Explanation:
       Amazon RDS uses the Amazon Simple Notification Service to provide a notification when an
       Amazon RDS event occurs. Event categories for a snapshot source type include: Creation,
       Deletion, and Restoration. The Backup is a part of DB instance source type.

 {!inpage-ads.md!}

   QUESTION NO: 101

       A customer is using AWS for Dev and Test. The customer wants to setup the Dev environment
       with Cloudformation. Which of the below mentioned steps are not required while using Cloudformation?

       A. Create a stack
       B. Configure a service
       C. Create and upload the template
       D. Provide the parameters configured as part of the template

       Answer: B

       Explanation:
       AWS Cloudformation is an application management tool which provides application modelling,
       deployment, configuration, management and related activities. AWS CloudFormation introduces
       two concepts: the template and the stack. The template is a JSON-format, text-based file that
       describes all the AWS resources required to deploy and run an application. The stack is a
       collection of AWS resources which are created and managed as a single unit when AWS
       CloudFormation instantiates a template. While creating a stack, the user uploads the template
       and provides the data for the parameters if required.

   QUESTION NO: 102

       A user has configured the AWS CloudWatch alarm for estimated usage charges in the US East
       region. Which of the below mentioned statements is not true with respect to the estimated
       charges?

       A. It will store the estimated charges data of the last 14 days
       B. It will include the estimated charges of every AWS service
       C. The metric data will represent the data of all the regions
       D. The metric data will show data specific to that region

       Answer: D

       Explanation:
       When the user has enabled the monitoring of estimated charges for the AWS account with AWS
       CloudWatch, the estimated charges are calculated and sent several times daily to CloudWatch in
       the form of metric data. This data will be stored for 14 days. The billing metric data is stored in the
       US East (Northern Virginia. Region and represents worldwide charges. This data also includes
       the estimated charges for every service in AWS used by the user, as well as the estimated overall
       AWS charges.

   QUESTION NO: 103

       A user is accessing RDS from an application. The user has enabled the Multi AZ feature with the
       MS SQL RDS DB. During a planned outage how will AWS ensure that a switch from DB to a standby replica
       will not affect access to the application?

       A. RDS will have an internal IP which will redirect all requests to the new DB
       B. RDS uses DNS to switch over to stand by replica for seamless transition
       C. The switch over changes Hardware so RDS does not need to worry about access
       D. RDS will have both the DBs running independently and the user has to manually switch over

       Answer: B

       Explanation:
       In the event of a planned or unplanned outage of a DB instance, Amazon RDS automatically
       switches to a standby replica in another Availability Zone if the user has enabled Multi AZ. The
       automatic failover mechanism simply changes the DNS record of the DB instance to point to the
       standby DB instance. As a result, the user will need to re-establish any existing connections to
       the DB instance. However, as the DNS is the same, the application can access DB seamlessly.

   QUESTION NO: 104

       An organization is generating digital policy files which are required by the admins for verification.
       Once the files are verified they may not be required in the future unless there is some compliance
       issue. If the organization wants to save them in a cost effective way, which is the best possible
       solution?

       A. AWS RRS
       B. AWS S3
       C. AWS RDS
       D. AWS Glacier

       Answer: D

       Explanation:
       Amazon S3 stores objects according to their storage class. There are three major storage classes:
       Standard, Reduced Redundancy and Glacier. Standard is for AWS S3 and provides very high
       durability. However, the costs are a little higher. Reduced redundancy is for less critical files.
       Glacier is for archival and the files which are accessed infrequently. It is an extremely low-cost
       storage service that provides secure and durable storage for data archiving and backup.

   QUESTION NO: 105

       A user has launched an EBS backed instance. The user started the instance at 9 AM in the
       morning. Between 9 AM to 10 AM, the user is testing some script. Thus, he stopped the instance
       twice and restarted it. In the same hour the user rebooted the instance once. For how many
       instance hours will AWS charge the user?

       A. 3 hours
       B. 4 hours
       C. 2 hours
       D. 1 hour

       Answer: A

       Explanation:
       A user can stop/start or reboot an EC2 instance using the AWS console, the Amazon EC2 CLI or
       the Amazon EC2 API. Rebooting an instance is equivalent to rebooting an operating system.
       When the instance is rebooted AWS will not charge the user for the extra hours. In case the user
       stops the instance, AWS does not charge the running cost but charges only the EBS storage
       cost. If the user starts and stops the instance multiple times in a single hour, AWS will charge the
       user for every start and stop. In this case, since the instance was rebooted twice, it will cost the
       user for 3 instance hours.

   QUESTION NO: 106

       An organization has configured the custom metric upload with CloudWatch. The organization has
       given permission to its employees to upload data using CLI as well SDK. How can the user track
       the calls made to CloudWatch?

       A. The user can enable logging with CloudWatch which logs all the activities
       B. Use CloudTrail to monitor the API calls
       C. Create an IAM user and allow each user to log the data using the S3 bucket
       D. Enable detailed monitoring with CloudWatch

       Answer: B

       Explanation:
       AWS CloudTrail is a web service which will allow the user to monitor the calls made to the
       Amazon CloudWatch API for the organization’s account, including calls made by the AWS
       Management Console, Command Line Interface (CLI., and other services. When CloudTrail
       logging is turned on, CloudWatch will write log files into the Amazon S3 bucket, which is specified
       during the CloudTrail configuration.

   QUESTION NO: 107

       A user has created a queue named “myqueue” with SQS. There are four messages published to
       queue which are not received by the consumer yet. If the user tries to delete the queue, what will
       happen?

       A. A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue
       B. It will delete the queue
       C. It will initiate the delete but wait for four days before deleting until all messages are
          deleted automatically.
       D. It will ask user to delete the messages first
 
       Answer: B

       Explanation:
       SQS allows the user to move data between distributed components of applications so they can
       perform different tasks without losing messages or requiring each component to be always
       available. The user can delete a queue at any time, whether it is empty or not. It is important to
       note that queues retain messages for a set period of time. By default, a queue retains messages
       for four days.

   QUESTION NO: 108

       A user has launched a large EBS backed EC2 instance in the US-East-1a region. The user wants
       to achieve Disaster Recovery (DR. for that instance by creating another small instance in Europe.
       How can the user achieve DR?

       A. Copy the running instance using the “Instance Copy” command to the EU region
       B. Create AMI of the instance and copy the AMI to the EU region. Then launch the instance from the EU AMI.
       C. Copy the instance from the US East region to the EU region
       D. Use the “Launch more like this” option to copy the instance from one region to another

       Answer: B

       Explanation:
       To launch an EC2 instance it is required to have an AMI in that region. If the AMI is not available
       in that region, then create a new AMI or use the copy command to copy the AMI from one region
       to the other region.

   QUESTION NO: 109

       A user has created numerous EBS volumes. What is the general limit for each AWS account for
       the maximum number of EBS volumes that can be created?

       A. 10000
       B. 5000
       C. 100
       D. 1000

       Answer: B

       Explanation:
       A user can attach multiple EBS volumes to the same instance within the limits specified by his
       AWS account. Each AWS account has a limit on the number of Amazon EBS volumes that the
       user can create, and the total storage available. The default limit for the maximum number of
       volumes that can be created is 5000.

   QUESTION NO: 110

       A user has created a VPC with CIDR 20.0.0.0/16 using the wizard. The user has created a public
       subnet CIDR (20.0.0.0/24. and VPN only subnets CIDR (20.0.1.0/24. along with the VPN
       gateway (vgw-12345. to connect to the user’s data centre. Which of the below mentioned options
       is a valid entry for the main route table in this scenario?

       A. Destination: 20.0.0.0/24 and Target: vgw-12345
       B. Destination: 20.0.0.0/16 and Target: ALL
       C. Destination: 20.0.1.0/16 and Target: vgw-12345
       D. Destination: 0.0.0.0/0 and Target: vgw-12345

       Answer: D

       Explanation:
       The user can create subnets as per the requirement within a VPC. If the user wants to connect
       VPC from his own data centre, he can setup a public and VPN only subnet which uses hardware
       VPN access to connect with his data centre. When the user has configured this setup with
       Wizard, it will create a virtual private gateway to route all traffic of the VPN subnet. Here are the
       valid entries for the main route table in this scenario: Destination: 0.0.0.0/0 & Target: vgw-12345
       (To route all internet traffic to the VPN gateway.
       Destination: 20.0.0.0/16 & Target: local (To allow local routing in VPC.

   QUESTION NO: 111

       A user has stored data on an encrypted EBS volume. The user wants to share the data with his
       friend’s AWS account. How can user achieve this?

       A. Create an AMI from the volume and share the AMI
       B. Copy the data to an unencrypted volume and then share
       C. Take a snapshot and share the snapshot with a friend
       D. If both the accounts are using the same encryption key then the user can share the
       volume directly

       Answer: B

       Explanation:
       AWS EBS supports encryption of the volume. It also supports creating volumes from existing
       snapshots provided the snapshots are created from encrypted volumes. If the user is having data on an
       encrypted volume and is trying to share it with others, he has to copy the data from the encrypted
       volume to a new unencrypted volume. Only then can the user share it as an encrypted volume
       data. Otherwise the snapshot cannot be shared.

   QUESTION NO: 112

       A user has enabled the Multi AZ feature with the MS SQL RDS database server. Which of the
       below mentioned statements will help the user understand the Multi AZ feature better?

       A. In a Multi AZ, AWS runs two DBs in parallel and copies the data asynchronously to the
          replica copy
       B. In a Multi AZ, AWS runs two DBs in parallel and copies the data synchronously to the replica
          copy
       C. In a Multi AZ, AWS runs just one DB but copies the data synchronously to the standby replica
       D. AWS MS SQL does not support the Multi AZ feature

       Answer: C

       Explanation:
       Amazon RDS provides high availability and failover support for DB instances using Multi-AZ
       deployments. In a Multi-AZ deployment, Amazon RDS automatically provisions and maintains a
       synchronous standby replica in a different Availability Zone. The primary DB instance is
       synchronously replicated across Availability Zones to a standby replica to provide data
       redundancy, eliminate I/O freezes, and minimize latency spikes during system backups. Running
       a DB instance with high availability can enhance availability during planned system maintenance,
       and help protect your databases against DB instance failure and Availability Zone disruption.Note
       that the high-availability feature is not a scaling solution for read-only scenarios; you cannot use a
       standby replica to serve read traffic. To service read-only traffic, you should use a read replica.

   QUESTION NO: 113

       An organization is using cost allocation tags to find the cost distribution of different departments
       and projects. One of the instances has two separate tags with the key/ value as “InstanceName/
       HR”, “CostCenter/HR”. What will AWS do in this case?

       A. InstanceName is a reserved tag for AWS. Thus, AWS will not allow this tag
       B. AWS will not allow the tags as the value is the same for different keys
       C. AWS will allow tags but will not show correctly in the cost allocation report due to the
          same value of the two separate keys
       D. AWS will allow both the tags and show properly in the cost distribution report

       Answer: D

       Explanation:
       AWS provides cost allocation tags to categorize and track the AWS costs. When the user applies
       tags to his AWS resources, AWS generates a cost allocation report as a comma-separated value
       (CSV file. with the usage and costs aggregated by those tags. Each tag will have a key-value and
       can be applied to services, such as EC2, S3, RDS, EMR, etc. It is required that the key should be
       different for each tag. The value can be the same for different keys. In this case since the value is
       different, AWS will properly show the distribution report with the correct values.

   QUESTION NO: 114

       A user is publishing custom metrics to CloudWatch. Which of the below mentioned statements will
       help the user understand the functionality better?

       A. The user can use the CloudWatch Import tool
       B. The user should be able to see the data in the console after around 15 minutes
       C. If the user is uploading the custom data, the user must supply the namespace, timezone,
          and metric name as part of the command
       D. The user can view as well as upload data using the console, CLI and APIs

       Answer: B

       Explanation:
       AWS CloudWatch supports the custom metrics. The user can always capture the custom data and
       upload the data to CloudWatch using CLI or APIs. The user has to always include the
       namespace as a part of the request. However, the other parameters are optional. If the user has
       uploaded data using CLI, he can view it as a graph inside the console. The data will take around
       2 minutes to upload but can be viewed only after around 15 minutes.

   QUESTION NO: 115

       A user is launching an EC2 instance in the US East region. Which of the below mentioned options
       is recommended by AWS with respect to the selection of the availability zone?

       A. Always select the US-East-1-a zone for HA
       B. Do not select the AZ; instead let AWS select the AZ
       C. The user can never select the availability zone while launching an instance
       D. Always select the AZ while launching an instance

       Answer: B

       Explanation:
       When launching an instance with EC2, AWS recommends not to select the availability zone
       (AZ.. AWS specifies that the default Availability Zone should be accepted. This is because it 
       enables AWS to select the best Availability Zone based on the system health and available capacity. 
       If the user launches additional instances, only then an Availability Zone should be specified. 
       This is to specify the same or different AZ from the running instances.

   QUESTION NO: 116

       A user has created a VPC with CIDR 20.0.0.0/16 with only a private subnet and VPN connection
       using the VPC wizard. The user wants to connect to the instance in a private subnet over SSH.
       How should the user define the security rule for SSH?

       A. Allow Inbound traffic on port 22 from the user’s network
       B. The user has to create an instance in EC2 Classic with an elastic IP and configure the security
          group of a private subnet to allow SSH from that elastic IP
       C. The user can connect to a instance in a private subnet using the NAT instance
       D. Allow Inbound traffic on port 80 and 22 to allow the user to connect to a private subnet over the
          Internet

       Answer: A

       Explanation:
       The user can create subnets as per the requirement within a VPC. If the user wants to connect
       VPC from his own data centre, the user can setup a case with a VPN only subnet (private. which
       uses VPN access to connect with his data centre. When the user has configured this setup with
       Wizard, all network connections to the instances in the subnet will come from his data centre. The
       user has to configure the security group of the private subnet which allows the inbound traffic on
       SSH (port 22. from the data centre’s network range.

   QUESTION NO: 117

       A user has created an ELB with the availability zone US-East-1A. The user wants to add more
       zones to ELB to achieve High Availability. How can the user add more zones to the existing ELB?

       A. It is not possible to add more zones to the existing ELB
       B. The only option is to launch instances in different zones and add to ELB
       C. The user should stop the ELB and add zones and instances as required
       D. The user can add zones on the fly from the AWS console

       Answer: D

       Explanation:
       The user has created an Elastic Load Balancer with the availability zone and wants to add more
       zones to the existing ELB. The user can do so in two ways:
       From the console or CLI, add new zones to ELB;
       Launch instances in a separate AZ and add instances to the existing ELB.

   QUESTION NO: 118

       A user has configured an Auto Scaling group with ELB. The user has enabled detailed
       CloudWatch monitoring on Elastic Load balancing. Which of the below mentioned statements
       will help the user understand this functionality better?

       A. ELB sends data to CloudWatch every minute only and does not charge the user
       B. ELB will send data every minute and will charge the user extra
       C. ELB is not supported by CloudWatch
       D. It is not possible to setup detailed monitoring for ELB

       Answer: A

       Explanation:
       CloudWatch is used to monitor AWS as well as the custom services. It provides either basic or
       detailed monitoring for the supported AWS products. In basic monitoring, a service sends data points
       to CloudWatch every five minutes, while in detailed monitoring a service sends data points to
       CloudWatch every minute. Elastic Load Balancing includes 10 metrics and 2 dimensions, and
       sends data to CloudWatch every minute. This does not cost extra.

   QUESTION NO: 119

       A user has configured ELB with two EBS backed EC2 instances. The user is trying to
       understand the DNS access and IP support for ELB. Which of the below mentioned statements
       may not help the user understand the IP mechanism supported by ELB?

       A. The client can connect over IPV4 or IPV6 using Dualstack
       B. ELB DNS supports both IPV4 and IPV6
       C. Communication between the load balancer and back-end instances is always through IPV4
       D. The ELB supports either IPV4 or IPV6 but not both

       Answer: D

       Explanation:
       Elastic Load Balancing supports both Internet Protocol version 6 (IPv6. and Internet Protocol
       version 4 (IPv4.. Clients can connect to the user’s load balancer using either IPv4 or IPv6 (in EC2-
       Classic. DNS. However, communication between the load balancer and its back-end instances
       uses only IPv4. The user can use the Dualstack-prefixed DNS name to enable IPv6 support for
       communications between the client and the load balancers. Thus, the clients are able to access
       the load balancer using either IPv4 or IPv6 as their individual connectivity needs dictate.

   QUESTION NO: 120

       A user has received a message from the support team that an issue occurred 1 week back
       between 3 AM to 4 AM and the EC2 server was not reachable. The user is checking the
       CloudWatch metrics of that instance. How can the user find the data easily using the CloudWatch
       console?

       A. The user can find the data by giving the exact values in the time Tab under CloudWatch metrics
       B. The user can find the data by filtering values of the last 1 week for a 1 hour period in
          the Relative tab under CloudWatch metrics
       C. It is not possible to find the exact time from the console. The user has to use CLI to provide the
          specific time
       D. The user can find the data by giving the exact values in the Absolute tab under
           CloudWatch metrics

       Answer: D

       Explanation:
       If the user is viewing the data inside the CloudWatch console, the console provides options to filter
       values either using the relative period, such as days /hours or using the Absolute tab where the user
       can provide data with a specific date and time. The console also provides the option to search using
       the local timezone under the time range caption in the console.

   QUESTION NO: 121

       A user has setup Auto Scaling with ELB on the EC2 instances. The user wants to configure that
       whenever the CPU utilization is below 10%, Auto Scaling should remove one instance. How can
       the user configure this?

       A. The user can get an email using SNS when the CPU utilization is less than 10%. The user can
          use the desired capacity of Auto Scaling to remove the instance
       B. Use CloudWatch to monitor the data and Auto Scaling to remove the instances
          using scheduled actions
       C. Configure CloudWatch to send a notification to Auto Scaling Launch configuration when the CPU
          utilization is less than 10% and configure the Auto Scaling policy to remove the instance
       D. Configure CloudWatch to send a notification to the Auto Scaling group when the CPU Utilization
          is less than 10% and configure the Auto Scaling policy to remove the instance

       Answer: D

       Explanation:
       Amazon CloudWatch alarms watch a single metric over a time period that the user specifies and
       performs one or more actions based on the value of the metric relative to a given threshold over
       a number of time periods. The user can setup to receive a notification on the Auto Scaling group
       with the CloudWatch alarm when the CPU utilization is below a certain threshold. The user can
       configure the Auto Scaling policy to take action for removing the instance. When the CPU
       utilization is below 10% CloudWatch will send an alarm to the Auto Scaling group to execute the
       policy.

   QUESTION NO: 122

       A user has enabled detailed CloudWatch metric monitoring on an Auto Scaling group. Which of
       the below mentioned metrics will help the user identify the total number of instances in an Auto
       Scaling group cluding pending, terminating and running instances?

       A. GroupTotalInstances
       B. GroupSumInstances
       C. It is not possible to get a count of all the three metrics together. The user has to find
          the individual number of running, terminating and pending instances and sum it
       D. GroupInstancesCount

       Answer: A

       Explanation:
       CloudWatch is used to monitor AWS as well as the custom services. For Auto Scaling,
       CloudWatch provides various metrics to get the group information, such as the Number of
       Pending, Running or Terminating instances at any moment. If the user wants to get the total
       number of Running, Pending and Terminating instances at any moment, he can use the
       GroupTotalInstances metric.

   QUESTION NO: 123

       A user is trying to configure the CloudWatch billing alarm. Which of the below mentioned steps
       should be performed by the user for the first time alarm creation in the AWS Account Management 
       section?

       A. Enable Receiving Billing Reports
       B. Enable Receiving Billing Alerts
       C. Enable AWS billing utility
       D. Enable CloudWatch Billing Threshold

       Answer: B

       Explanation:
       AWS CloudWatch supports enabling the billing alarm on the total AWS charges. Before the user
       can create an alarm on the estimated charges, he must enable monitoring of the estimated AWS
       charges, by selecting the option “Enable receiving billing alerts”. It takes about 15 minutes
       before the user can view the billing data. The user can then create the alarms.

   QUESTION NO: 124
   
       A user is checking the CloudWatch metrics from the AWS console. The user notices that the
       CloudWatch data is coming in UTC. The user wants to convert the data to a local time zone. How
       can the user perform this?

       A. In the CloudWatch dashboard the user should set the local timezone so that CloudWatch
          shows the data only in the local time zone
       B. In the CloudWatch console select the local timezone under the Time Range tab to 712
          view the data as per the local timezone
       C. The CloudWatch data is always in UTC; the user has to manually convert the data
       D. The user should have send the local timezone while uploading the data so that CloudWatch will
          show the data only in the local timezone

       Answer: B

       Explanation:
       If the user is viewing the data inside the CloudWatch console, the console provides options to filter
       values either using the relative period, such as days/hours or using the Absolute tab where the use
       can provide data with a specific date and time. The console also provides the option to search using
       the local timezone under the time range caption in the console because the time range tab allows
       the user to change the time zone.

 {!inpage-ads.md!}

   QUESTION NO: 125

       An organization (Account ID 123412341234. has attached the below mentioned IAM policy to a
       user. What does this policy statement entitle the user to perform?
       "Statement": [
       {
       "Sid": "AllowUsersAllActionsForCredentials",
       "Effect": "Allow",
       "Action": [
       "iam:*AccessKey*",
       ],
       "Resource": ["arn:aws:iam:: 123412341234:user/${aws:username}"]
       }
       ]

       Explanation:
       AWS Identity and Access Management is a web service which allows organizations to manage
       users and user permissions for various AWS services. If the organization (Account ID
       123412341234. wants some of their users to manage keys (access and secret access keys. of all
       IAM users, the organization should set the below mentioned policy which entitles the IAM user to
       modify keys of all IAM users with CLI, SDK or API.
       "Statement": [
       {
       "Sid": "AllowUsersAllActionsForCredentials",
       "Effect": "Allow",
       "Action": [
       "iam:*AccessKey*",
       ],
       "Resource": ["arn:aws:iam:: 123412341234:user/${aws:username}"]
       }
       ]

   QUESTION NO: 126

       A user is trying to connect to a running EC2 instance using SSH. However, the user gets a
       connection time out error. Which of the below mentioned options is not a possible reason for
       rejection?

       A. The access key to connect to the instance is wrong
       B. The security group is not configured properly
       C. The private key used to launch the instance is not correct
       D. The instance CPU is heavily loaded

       Answer: A

       Explanation:
       If the user is trying to connect to a Linux EC2 instance and receives the connection time out error
       the probable reasons are:
       - Security group is not configured with the SSH port
       - The private key pair is not right
       - The user name to login is wrong
       - The instance CPU is heavily loaded, so it does not allow more connections

   QUESTION NO: 127

       A user has configured Elastic Load Balancing by enabling a Secure Socket Layer (SSL) negotiation 
       configuration known as a Security Policy. Which of the below mentioned options is not part of
       this secure policy while negotiating the SSL connection between the user and the client?

       A. SSL Protocols
       B. Client Order Preference
       C. SSL Ciphers
       D. Server Order Preference

       Answer: B

       Explanation:
       Elastic Load Balancing uses a Secure Socket Layer (SSL. negotiation configuration which
       is known as a Security Policy. It is used to negotiate the SSL connections between a client and 
       the load balancer. A security policy is a combination of SSL Protocols, SSL Ciphers, and the Server
       order Preference option.

   QUESTION NO: 128

       A user has configured CloudWatch monitoring on an EBS backed EC2 instance. If the user has
       not attached any additional device, which of the below mentioned metrics will always show a 0
       value?

       A. DiskReadBytes 7456
       B. NetworkIn
       C. NetworkOut
       D. CPUUtilization

       Answer: A

       Explanation:
       CloudWatch is used to monitor AWS as the well custom services. For EC2 when the user is
       monitoring the EC2 instances, it will capture the 7 Instance level and 3 system check parameters
       for the EC2 instance. Since this is an EBS backed instance, it will not have ephermal storage
       attached to it. Out of the 7 EC2 metrics, the 4 metrics DiskReadOps, DiskWriteOps,
       DiskReadBytes and DiskWriteBytes are disk related data and available only when there is
       ephermal storage attached to an instance. For an EBS backed instance without any additional
       device, this data will be 0.

   QUESTION NO: 129

       A user has launched an EBS backed EC2 instance. What will be the difference while performing
       the restart or stop/start options on that instance?

       A. For restart it does not charge for an extra hour, while every stop/start it will be charged as
          a separate hour
       B. Every restart is charged by AWS as a separate hour, while multiple start/stop actions during
          a single hour will be counted as a single hour
       C. For every restart or start/stop it will be charged as a separate hour
       D. For restart it charges extra only once, while for every stop/start it will be charged as a
          separate hour

       Answer: A

       Explanation:
       For an EC2 instance launched with an EBS backed AMI, each time the instance state is
       changed from stop to start/ running, AWS charges a full instance hour, even if these transitions
       happen multiple times within a single hour. Anyway, rebooting an instance AWS does not charge
       a new instance billing hour.

   QUESTION NO: 130

       A user has created a queue named “myqueue” in US-East region with AWS SQS. The user’s
       AWS account ID is 123456789012. If the user wants to perform some action on this queue, which
       of the below Queue URL should he use?

       A. http://sqs.us-east-1.amazonaws.com/123456789012/myqueue
       B. http://sqs.amazonaws.com/123456789012/myqueue
       C. http://sqs. 123456789012.us-east-1.amazonaws.com/myqueue
       D. http:// 123456789012.sqs. us-east-1.amazonaws.com/myqueue

       Answer: A

       Explanation:
       When creating a new queue in SQS, the user must provide a queue name that is unique within
       the scope of all queues of user’s account. If the user creates queues using both the latest WSDL
       and a previous version, he will have a single namespace for all his queues. Amazon SQS assigns
       each queue created by user an identifier called a queue URL, which includes the queue name
       and other components that Amazon SQS determines. Whenever the user wants to perform an
       action on a queue, he must provide its queue URL. The queue URL for the account id
       123456789012 & queue name “myqueue” in US-East-1 region will be http:// sqs.us-east1.amazonaws.com/123456789012/myqueue.

   QUESTION NO: 131

       A sys admin is trying to understand the Auto Scaling activities. Which of the below mentioned
       processes is not performed by Auto Scaling?

       A. Reboot Instance
       B. Schedule Actions
       C. Replace Unhealthy
       D. Availability Zone Balancing

       Answer: A

       Explanation:
       There are two primary types of Auto Scaling processes: Launch and Terminate, which launch or
       terminate instances, respectively. Some other actions performed by Auto Scaling are: AddToLoadbalancer,
       AlarmNotification, HealthCheck, AZRebalance, ReplaceUnHealthy, and ScheduledActions.

   QUESTION NO: 132

       A sys admin is trying to understand EBS snapshots. Which of the below mentioned statements will
       not be useful to the admin to understand the concepts about a snapshot?

       A. The snapshot is synchronous
       B. It is recommended to stop the instance before taking a snapshot for consistent data
       C. The snapshot is incremental
       D. The snapshot captures the data that has been written to the hard disk when the
          snapshot command was executed

       Answer: A

       Explanation:
       The AWS snapshot is a point in time backup of an EBS volume. When the snapshot command is
       executed it will capture the current state of the data that is written on the drive and take a backup.
       For a better and consistent snapshot of the root EBS volume, AWS recommends stopping the
       instance. For additional volumes it is recommended to unmount the device. The snapshots are
       asynchronous and incremental.

   QUESTION NO: 133

       A root account owner has created an S3 bucket testmycloud. The account owner wants to allow
       everyone to upload the objects as well as enforce that the person who uploaded the object
       should manage the permission of those objects. Which is the easiest way to achieve this?

       A. The root account owner should create a bucket policy which allows the IAM users to upload the
          object
       B. The root account owner should create the bucket policy which allows the other account owners
          to set the object policy of that bucket
       C. The root account should use ACL with the bucket to allow everyone to upload the object
       D. The root account should create the IAM users and provide them the permission to upload content
           to the bucket

       Answer: C

       Explanation:
       Each AWS S3 bucket and object has an ACL (Access Control List. associated with it. An ACL is a
       list of grants identifying the grantee and the permission granted. The user can use ACLs to grant
       basic read/write permissions to other AWS accounts. ACLs use an Amazon S3–specific XML
       schema. The user cannot grant permissions to other users in his account. ACLs are suitable for
       specific scenarios. For example, if a bucket owner allows other AWS accounts to upload objects,
       permissions to these objects can only be managed using the object ACL by the AWS account that
       owns the object.

   QUESTION NO: 134

       An organization has setup consolidated billing with 3 different AWS accounts. Which of the below
       mentioned advantages will organization receive in terms of the AWS pricing?

       A. The consolidated billing does not bring any cost advantage for the organization
       B. All AWS accounts will be charged for S3 storage by combining the total storage of
          each account
       C. The EC2 instances of each account will receive a total of 750*3 micro instance hours free
       D. The free usage tier for all the 3 accounts will be 3 years and not a single year

       Answer: B

       Explanation:
       AWS consolidated billing enables the organization to consolidate payments for multiple Amazon
       Web Services (AWS. accounts within a single organization by making a single paying account.
       For billing purposes, AWS treats all the accounts on the consolidated bill as one account. Some
       services, such as Amazon EC2 and Amazon S3 have volume pricing tiers across certain usage
       dimensions that give the user lower prices when he uses the service more.

   QUESTION NO: 135

       A user has launched two EBS backed EC2 instances in the US-East-1a region. The user wants
       to change the zone of one of the instances. How can the user change it?

       A. Stop one of the instances and change the availability zone
       B. The zone can only be modified using the AWS CLI
       C. From the AWS EC2 console, select the Actions - > Change zones and specify new zone
       D. Create an AMI of the running instance and launch the instance in a separate AZ

       Answer: D

       Explanation:
       With AWS EC2, when a user is launching an instance he can select the availability zone (AZ. at
       the time of launch. If the zone is not selected, AWS selects it on behalf of the user. Once the
       instance is launched, the user cannot change the zone of that instance unless he creates an
       AMI of that instance and launches a new instance from it.

   QUESTION NO: 136

       A user wants to make so that whenever the CPU utilization of the AWS EC2 instance is above
       90%, the redlight of his bedroom turns on. Which of the below mentioned AWS services is helpful
       for this purpose?

       A. AWS CloudWatch + AWS SES
       B. AWS CloudWatch + AWS SNS
       C. None. It is not possible to configure the light with the AWS infrastructure services
       D. AWS CloudWatch and a dedicated software turning on the light

       Answer: B

       Explanation:
       Amazon Simple Notification Service (Amazon SNS. is a fast, flexible, and fully managed push
       messaging service. Amazon SNS can deliver notifications by SMS text message or email to the Amazon
       Simple Queue Service (SQS. queues or to any HTTP endpoint. The user can configure some
       sensor devices at his home which receives data on the HTTP end point (REST calls. and turn on
       the red light. The user can configure the CloudWatch alarm to send a notification to the AWS SNS
       HTTP end point (the sensor device. and it will turn the light red when there is an alarm condition.

   QUESTION NO: 137

       An organization has added 3 of his AWS accounts to consolidated billing. One of the
       AWS accounts has purchased a Reserved Instance (RI. of a small instance size in the US-East-1a zone.
       All other AWS accounts are running instances of a small size in the same zone. What will happen in 
       this case for the RI pricing?

       A. Only the account that has purchased the RI will get the advantage of RI pricing
       B. One instance of a small size and running in the US-East-1a zone of each AWS account will
          get the benefit of RI pricing
       C. Any single instance from all the three accounts can get the benefit of AWS RI pricing if they are
          running in the same zone and are of the same size
       D. If there are more than one instances of a small size running across multiple accounts in
          the same zone no one will get the benefit of RI

       Answer: C

       Explanation:
       AWS consolidated billing enables the organization to consolidate payments for multiple Amazon
       Web Services (AWS. accounts within a single organization by making a single paying account.
       For billing purposes, consolidated billing treats all the accounts on the consolidated bill as one
       account. This means that all accounts on a consolidated bill can receive the hourly cost benefit of
       the Amazon EC2 Reserved Instances purchased by any other account. In this case only one
       Reserved Instance has been purchased by one account. Thus, only a single instance from any of
       the accounts will get the advantage of RI. AWS will implement the blended rate for each instance
       if more than one instance is running concurrently.

   QUESTION NO: 138

       An organization is planning to use AWS for 5 different departments. The finance department is
       responsible to pay for all the accounts. However, they want the cost separation for each
       account to map with the right cost centre. How can the finance department achieve this?

       A. Create 5 separate accounts and make them a part of one consolidate billing
       B. Create 5 separate accounts and use the IAM cross account access with the roles for better
          management
       C. Create 5 separate IAM users and set a different policy for their access
       D. Create 5 separate IAM groups and add users as per the department’s employees

       Answer: A

       Explanation:
       AWS consolidated billing enables the organization to consolidate payments for multiple Amazon
       Web Services (AWS. accounts within a single organization by making a single paying account.
       Consolidated billing enables the organization to see a combined view of the AWS charges
       incurred by each account as well as obtain a detailed cost report for each of the individual AWS
       accounts associated with the paying account.

   QUESTION NO: 139

       A user has setup an EBS backed instance and a CloudWatch alarm when the CPU utilization is
       more than 65%. The user has setup the alarm to watch it for 5 periods of 5 minutes each. The
       CPU utilization is 60% between 9 AM to 6 PM. The user has stopped the EC2 instance for 15
       minutes between 11 AM to 11:15 AM. What will be the status of the alarm at 11:30 AM?

       A. Alarm
       B. OK
       C. Insufficient Data
       D. Error

       Answer: B

       Explanation:
       Amazon CloudWatch alarm watches a single metric over a time period the user specifies and
       performs one or more actions based on the value of the metric relative to a given threshold over a
       number of time periods. The state of the alarm will be OK for the whole day. When the user stops
       the instance for three periods the alarm may not receive the data

   QUESTION NO: 140

       A user is running one instance for only 3 hours every day. The user wants to save some cost with
       the instance. Which of the below mentioned Reserved Instance categories is advised in this case?

       A. The user should not use RI; instead only go with the on-demand pricing
       B. The user should use the AWS high utilized RI
       C. The user should use the AWS medium utilized RI
       D. The user should use the AWS low utilized RI

       Answer: A

       Explanation:
       The AWS Reserved Instance provides the user with an option to save some money by paying a
       one-time fixed amount and then save on the hourly rate. It is advisable that if the user is having
       30% or more usage of an instance per day, he should go for a RI. If the user is going to use an
       EC2 instance for more than 2200-2500 hours per year, RI will help the user save some cost.
       Here, the instance is not going to run for less than 1500 hours. Thus, it is advisable that the user
       should use the on-demand pricing.

   QUESTION NO: 141

       A user has setup an RDS DB with Oracle. The user wants to get notifications when
       someone modifies the security group of that DB. How can the user configure that?

       A. It is not possible to get the notifications on a change in the security group
       B. Configure SNS to monitor security group changes
       C. Configure event notification on the DB security group
       D. Configure the CloudWatch alarm on the DB for a change in the security group

       Answer: C

       Explanation:
       Amazon RDS uses the Amazon Simple Notification Service to provide a notification when an
       Amazon RDS event occurs. These events can be configured for source categories, such as DB
       instance, DB security group, DB snapshot and DB parameter group. If the user is subscribed to
       a Configuration Change category for a DB security group, he will be notified when the DB
       security group is changed.

   QUESTION NO: 142

       A user is trying to setup a recurring Auto Scaling process. The user has setup one process to
       scale up every day at 8 am and scale down at 7 PM. The user is trying to setup another
       recurring process which scales up on the 1st of every month at 8 AM and scales down the same
       day at 7 PM. What will Auto Scaling do in this scenario?

       A. Auto Scaling will execute both processes but will add just one instance on the 1st
       B. Auto Scaling will add two instances on the 1st of the month
       C. Auto Scaling will schedule both the processes but execute only one process randomly
       D. Auto Scaling will throw an error since there is a conflict in the schedule of two separate Auto
          Scaling Processes

       Answer: D

       Explanation:
       Auto Scaling based on a schedule allows the user to scale the application in response to
       predictable load changes. The user can also configure the recurring schedule action which will
       follow the Linux cron format. As per Auto Scaling, a scheduled action must have a unique time value.
       If the user attempts to schedule an activity at a time when another existing activity is already 
       scheduled, the call will be rejected with an error message noting the conflict.

   QUESTION NO: 143

       A user is planning to setup infrastructure on AWS for the Christmas sales. The user is planning to
       use Auto Scaling based on the schedule for proactive scaling. What advise would you give to the
       user?

       A. It is good to schedule now because if the user forgets later on it will not scale up
       B. The scaling should be setup only one week before Christmas
       C. Wait till end of November before scheduling the activity
       D. It is not advisable to use scheduled based scaling

       Answer: C

       Explanation:
       Auto Scaling based on a schedule allows the user to scale the application in response to
       predictable load changes. The user can specify any date in the future to scale up or down during that 
       period. As per Auto Scaling the user can schedule an action for up to a month in the future. Thus, 
       it is recommended to wait until end of November before scheduling for Christmas.

   QUESTION NO: 144

       A user is trying to understand the ACL and policy for an S3 bucket. Which of the below
       mentioned policy permissions is equivalent to the WRITE ACL on a bucket?

       A. s3:GetObjectAcl
       B. s3:GetObjectVersion
       C. s3:ListBucketVersions
       D. s3:DeleteObject

       Answer: D

       Explanation:
       Amazon S3 provides a set of operations to work with the Amazon S3 resources. Each AWS S3
       bucket can have an ACL (Access Control List. or bucket policy associated with it. The WRITE
       ACL list allows the other AWS accounts to write/modify to that bucket. The equivalent S3 bucket
       policy permission for it is s3:DeleteObject.

   QUESTION NO: 145

       A user has created an ELB with Auto Scaling. Which of the below mentioned offerings from ELB
       helps the user to stop sending new requests traffic from the load balancer to the EC2 instance
       when the instance is being deregistered while continuing in-flight requests?

       A. ELB sticky session
       B. ELB deregistration check
       C. ELB connection draining
       D. ELB auto registration Off

       Answer: C

       Explanation:
       The Elastic Load Balancer connection draining feature causes the load balancer to stop
       sending new requests to the back-end instances when the instances are deregistering or
       become unhealthy, while ensuring that inflight requests continue to be served.

   QUESTION NO: 146

       A user has launched an EC2 instance from an instance store backed AMI. The infrastructure team
       wants to create an AMI from the running instance. Which of the below mentioned steps will not be
       performed while creating the AMI?

       A. Define the AMI launch permissions
       B. Upload the bundled volume
       C. Register the AMI
       D. Bundle the volume

       Answer: A

       Explanation:
       When the user has launched an EC2 instance from an instance store backed AMI, it will need to
       follow certain steps, such as “Bundling the root volume”, “Uploading the bundled volume” and
       “Register the AMI”. Once the AMI is created the user can setup the launch permission. However,
       it is not required to setup during the launch.

   QUESTION NO: 147

       You are managing the AWS account of a big organization. The organization has more than 1000+
       employees and they want to provide access to the various services to most of the employees.
       Which of the below mentioned options is the best possible solution in this case?

       A. The user should create a separate IAM user for each employee and provide access to them as
          per the policy
       B. The user should create an IAM role and attach STS with the role. The user should attach
          that role to the EC2 instance and setup AWS authentication on that server
       C. The user should create IAM groups as per the organization’s departments and add each user
          to the group for better access control
       D. Attach an IAM role with the organization’s authentication service to authorize each user
          for various AWS services

       Answer: D

       Explanation:
       AWS Identity and Access Management is a web service which allows organizations to manage
       users and user permissions for various AWS services. The user is managing an AWS account for
       an organization that already has an identity system, such as the login system for the corporate
       network (SSO.. In this case, instead of creating individual IAM users or groups for each user who
       need AWS access, it may be more practical to use a proxy server to translate the user identities
       from the organization network into the temporary AWS security credentials. This proxy server will
       attach an IAM role to the user after authentication.

   QUESTION NO: 148

       A user has configured a VPC with a new subnet. The user has created a security group. The user
       wants to configure that instances of the same subnet communicate with each other. How can the
       user configure this with the security group?

       A. There is no need for a security group modification as all the instances can communicate
          with each other inside the same subnet
       B. Configure the subnet as the source in the security group and allow traffic on all the
          protocols and ports
       C. Configure the security group itself as the source and allow traffic on all the protocols and ports
       D. The user has to use VPC peering to configure this

       Answer: C

       Explanation:
       A Virtual Private Cloud (VPC. is a virtual network dedicated to the user’s AWS account. AWS
       provides two features that the user can use to increase security in VPC: security groups and
       network ACLs. Security groups work at the instance level. If the user is using the default security
       group it will have a rule which allows the instances to communicate with other. For a new security
       group the user has to specify the rule, add it to define the source as the security group itself, and
       select all the protocols and ports for that source.

   QUESTION NO: 149

       A user is launching an instance. He is on the “Tag the instance” screen. Which of the below
       mentioned information will not help the user understand the functionality of an AWS tag?

       A. Each tag will have a key and value
       B. The user can apply tags to the S3 bucket
       C. The maximum value of the tag key length is 64 unicode characters
       D. AWS tags are used to find the cost distribution of various resources

       Answer: C

       Explanation:
       AWS provides cost allocation tags to categorize and track the AWS costs. When the user applies
       tags to his AWS resources, AWS generates a cost allocation report as a comma-separated value
       (CSV file. with the usage and costs aggregated by those tags. Each tag will have a key-value and
       can be applied to services, such as EC2, S3, RDS, EMR, etc. The maximum size of a tag key is
       128 unicode characters.

   QUESTION NO: 150

       A user has created a VPC with CIDR 20.0.0.0/16. The user has created public and VPN only
       subnets along with hardware VPN access to connect to the user’s datacenter. The user wants to
       make so that all traffic coming to the public subnet follows the organization’s proxy policy. How
       can the user make this happen?
       A. Setting up a NAT with the proxy protocol and configure that the public subnet receives
          traffic from NAT
       B. Settin up a proxy policy in the internet gateway connected with the public subnet
       C. It is not possible to setup the proxy policy for a public subnet
       D. Setting the route table and security group of the public subnet which receives traffic
          from a virtual private gateway

       Answer: D

       Explanation:
       The user can create subnets within a VPC. If the user wants to connect to VPC from his own data
       centre, he can setup public and VPN only subnets which uses hardware VPN access to connect
       with his data centre. When the user has configured this setup, it will update the main route table
       used with the VPN-only subnet, create a custom route table and associate it with the public
       subnet. It also creates an internet gateway for the public subnet. By default the internet traffic of
       the VPN subnet is routed to a virtual private gateway while the internet traffic of the public subnet
       is routed through the internet gateway. The user can set up the route and security group rules.
       These rules enable the traffic to come from the organization’s network over the virtual private
       gateway to the public subnet to allow proxy settings on that public subnet.

---
[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](aws-2.md)

---

<br>

{!footer.md!}
