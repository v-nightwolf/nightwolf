# AWS Interview Questions & Answers 
---
These are AWS interview questions for experienced professionals.  You will find these questions very helpful in your AWS professional role interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

1. List the components required to build Amazon VPC?

        Subnet, Internet Gateway, NAT Gateway, HW VPN Connection, Virtual Private Gateway, Customer Gateway, Router,
        Peering Connection, VPC Endpoint for S3, Egressonly Internet Gateway.

2. How do you safeguard your EC2 instances running in a VPC?

        Security Groups can be used to protect your EC2 instances in a VPC. We can configure both INBOUND and
        OUTBOUND traffic in a Security Group which enables secured access to your EC2 instances. Security Group
        automatically denies any unauthorized access to your EC2 instances.

3. In a VPC how many EC2 instances can you use?

        Initially you are limited to launch 20 EC2 Instances at one time. Maximum VPC size is 65,536 instances.

4. Can you establish a peering connection to a VPC in a different REGION?

        Not possible. Peering Connection are available only between VPC in the same region.

5. Can you connect your VPC with a VPC owned by another AWS account?

        Yes, Possible. Provided the owner of other VPCs accepts your connection.

6. What are all the different connectivity options available for your VPC?

        Internet Gateway, Virtual Private Gateway, NAT, EndPoints, Peering Connections.

7. Can a EC2 instance inside your VPC connect with the EC2 instance belonging to other VPCs?

        Yes, Possible. Provided an Internet Gateway is configured in such a way that traffic bounded for EC2
        instances running in other VPCs.

8. How can you monitor network traffic in your VPC?

        It is possible using Amazon VPC Flow-Logs feature.

9. Difference between Security Groups and ACLs in a VPC?

        A Security Group defines which traffic is allowed TO or FROM EC2 instance. Whereas ACL, controls at the
        SUBNET level, scrutinize the traffic TO or FROM a Subnet.

10. Hon an EC2 instance in a VPC establish the connection with the internet?

        Using either a Public IP or an Elastic IP.

11. Different types of Cloud Computing as per services?

        PAAS (Platform As A Service), IAAS (Infrastructure As A Service), SAAS (Software As A Service)

12. What is Auto Scaling?

        Automatically adding duplicate instances to application farm during heavy business hours. Scale-IN and
        Scale-OUT are two different types of Scaling. 

        Scale-IN: Reducing the instances.
        Scale-OUT: Increasing the instances by duplicating.

13. What is AMI?

        AMI is defined as Amazon Machine Image. Basically it’s a template comprising software configuration part.
        For example, Operating System, DB Server, Application Server, etc.


14. Difference between Stopping and Terminating the Instances?

        When you STOP an instance it is a normal shutdown. The corresponding EBS volume attached to that instance
        remains attached and you can restart the instance later. When you TERMINATE an instance it gets deleted and
        you cannot restart that instance again later. And any EBS volume attached with that instance also deleted.

15. When you launch a standby Relational Database Service instance will it be available in the same Available Zone?

        Not advisable. Because the purpose of having standby RDS instance is to avoid an infrastructure failure.
        So you have to keep your standby RDS service in a different Availability Zone, which may have different
        infrastructure.

16. Difference between Amazon RDS, DynamoDB and Redshift?

        RDS is meant for structured data only. DynamoDB is meant for unstructured data which is a NoSQL service.
        Redshift is a data warehouse product used for data analysis.

17. What are Lifecycle Hooks?

        Lifecycle Hooks are used in Auto Scaling. Lifecycle hooks enable you to perform custom actions by pausing
        instances as an Auto Scaling group launches or terminates them. Each Auto Scaling group can have multiple
        lifecycle hooks.

18. What is S3?

        S3 stands for Simple Storage Service, with a simple web service interface to store and retrieve any amount
        of data from anywhere on the web.

19. What is AWS Lambada?

        Lambda is an event-driven platform. It is a compute service that runs code in response to events and
        automatically manages the compute resources required by that code.

20. In S3 how many buckets can be created?

        By default 100 buckets can be created in a region.

21. What is CloudFront?

        Amazon CloudFront is a content delivery network operated by Amazon Web Services. It is a service that speeds
        up transfer of your static and dynamic web content such as HTML files, IMAGE files., etc., CloudFront
        delivers your particulars thru worldwide data centers named Edge Locations.

22. Brief about S3 service in AWS?

        S3, a Simple Storage Service from Amazon. You can move your files TO and FROM S3. Its like a FTP storage.
        You can keep your SNAPSHOTS in S3. You can also ENCRYPT your sensitive data in S3.

23. Explain Regions and Available Zones in EC2?

        Amazon has hosted EC2 in various locations around the world. These locations are called REGIONS. For example
        in Asia, Mumbai is one region and Singapore is another region. Each region is composed of isolated locations
        which are known as AVAILABLE ZONES. Region is independent. But the Available Zones are linked thru low-latency
        links.

24. What are the two types of Load Balancer?

        Classic LB and Application LB. ALB is the Content Based Routing.

25. Can a AMI be shared?

        Yes. A developer can create an AMI and share it with other developers for their use. A shared AMI is packed
        with the components you need and you can customize the same as per your needs. As you are not an owner of a
        shared AMI there is a risk always involved.

26. What is a Hypervisor?

        A Hypervisor is a kind of software that enables Virtualization. It combines physical hardware resources into
        a platform which is delivered virtually to one or more users. XEN is the Hypervisor for EC2.

27. Key Pair and its uses?

        You use Key Pair to login to your Instance in a secured way. You can create a key pair using EC2 console. When
        your instances are spread across regions you need to create key pair in each region.

28. What is the feature of ClassicLink?

        ClassicLink allows instances in EC2 classic platform to communicate with instances in VPC using Private IP
        address. EC2 classic platform instances cannot not be linked to more than one VPC at a time.
        
29. Can you edit a Route Table in VPC?

        Yes. You can always modify route rules to specify which subnets are routed to the Internet gateway, the virtual
        private gateway, or other instances.

30. How many Elastic IPs can you create?

        5 VPC Elastic IP addresses per AWS account per region.

31. Can you ping the router or default gateway that connects your subnets?

        NO, you cannot. It is not supported. However you can ping EC2 instances within a VPC, provided your
        firewall, Security Groups and network ACLs allows such traffic.

32. How will you monitor the network traffic in a VPC?

        Using Amazon VPC Flow Logs feature.

33. Can you make a VPC available in multiple Available Zones?

        Yes.

34. How do you ensure an EC2 instance is launched in a particular Available Zone?

        After selecting your AMI Template and Instance Type, in the third step while configuring the instance
        you must select the SUBNET in which you wish to launch your instance. It will be launched in the AZ
        associated with that SUBNET.

35. For Internet Gateways do you find any Bandwidth constraints?

        NO. Normally an IG is HORIZONTALLY SCALLED, Redundant and Highly Available. It is not having nay Bandwidth
        constraints usually.

36. What is the significance of a Default VPC?

        When you launch your instances in a Default VPC in a Region, you would be getting the benefit of advanced
        Network Functionalities. You can also make use of Security Groups, multiple IP addresses, and multiple
        Network interfaces.

37. Can you make use of default EBS Snapshots?

        You can use, provided if it is located in the same region where your VPC is presented.

38. What will happen when you delete a PEERING CONNECTION in your side?

        The PEERING CONNECTION available in the other side would also get terminated. There will no more traffic
        flow.

39. Can you establish a Peering connection to a VPC in a different region?

        NO. Its possible between VPCs in the same region.

40. Can you connect your VPC with a VPC created by another AWS account?

        Yes. Only when that owner accepts your peering connection request.

41. When you delete your DB instance what will happen to your backups and DB snapshots?

        When a DB instance is deleted, RDS retains the user-created DB snapshot along with all other manually
        created DB snapshots. Also automated backups are deleted and only manually created DB Snapshots are
        retained.
        
42. What is the significance of an Elastic IP?

        The Public IP is associated with the instance until it is stopped or terminated Only. A Public IP is not
        static. Every time your instance is stopped or terminated the associated Public IP gets vanished and a
        new Public IP gets assigned with that instance. To over come this issue a public IP can be replaced by an
        Elastic IP address, which stays with the instance as long as the user doesn’t manually detach it.
        Similarly when if you are hosting multiple websites on your EC2 server, in that case you may require more
        than one Elastic IP address.

43. How will you use S3 with your EC2 instances?

        Websites hosted on your EC2 instances can load their static contents directly from S3. It provides highly
        scalable, reliable, fast, inexpensive data storage infrastructure.

44. Is this possible to connect your company datacenter to Amazon Cloud?

        Yes, you can very well do this by establishing a VPN connection between your company’s network and Amazon
        VPC.

45. Can you change the Private IP of an EC2 instance while it is running or stopped?

        A Private IP is STATIC. And it is attached with an instance throughout is lifetime and cannot be changed.

46. What is the use of Subnets?

        When a network has more number of HOSTS, managing these hosts can be tedious under a single large network.
        Therefore we divide this large network into easily manageable sub-networks (subnets) so that managing hosts
        under each subnet becomes easier.

47. What is the use of Route Table?

        Route Table is used to route the network pockets. Generally one route table would be available in each
        subnet. Route table can have any no. of records or information, hence attaching multiple subnets to a
        route table is also possible.

48. Can you use the Standby DB instance for read and write along with your Primary DB instance?

        Standby server cannot be used in parallel with primary server unless your Primary instance goes down.

49. What is the use of Connection Draining?

        Connection Draining is a service under Elastic Load Balancing. It keeps monitoring the healthiness of the
        instances. If any instance fails Connection Draining pulls all the traffic from that particular failed
        instance and re-route the traffic to other healthy instances.

50. What is the role of AWS CloudTrail?

        CloudTrail is designed for logging and tracking API calls. Also used to audit all S3 bucket accesses.

51. What is the use of Amazon Transfer Acceleration Service?

        ATA service speeds up your data transfer with the use of optimized network paths. Also, speed up your
        CDN up to 300% compared to normal data transfer speed.

52. What is the name of AWS CEO or Chief ? Jeff Bezos or Lisa Su or Denise Morrison ?

        Jeff Bezos

53. EC2 officially launch in …..   2002 or 2006 or  2008 ?

        2006

54. S3 Launched officially lunched in …..
2002 or 2006 or 2008 ?

        2006

55. You cannot store unlimited data in Amazon Web Services. True or False ?

        False

56. Rapid provisioning allows you to very quickly spin up a new virtual machine with minimal effort. True or false ?

        True

57. A hybrid setup is one in which part of your resources are AWS and the rest are with another cloud provider. True or False ?

        False

58. As an added layer of security for AWS management, which of the following should be you do ?
    - Create multiple Admin accounts
    - Generate a new security key each time you log in
    - Create IAM users

            Ans:  Create IAM users

59. Is AMI template ?

        True

60. EC2 Instances are Virtual Server in AWS. True or False ?

        True

61. What does “elastic” refer to in Elastic Compute Cloud(EC2)? Select all that apply.
    1. Increasing and decreasing capacity as needed
    2. Monitoring services on multiple devices
    3. Operating on Mac, Windows and Linux
    4. Paying only for running virtual machines
    5. Stretching applications across virtual machines

            Ans:
                1. Increasing and decreasing capacity as needed  
                AND
                4. Paying only for running virtual machines

62. You can upload a custom configuration virtual image and sell it on the AWS Marketplace. True or false ?

        True

63. EC2 Machine types define which of the following ?

    1. AWS Region
    2. Core Count
    3. User Location

            Ans: Core Count

64. Which is default instance type ?

    1. On-demand
    2. RI
    3. Spot instance

            Ans: On-demand

65. What is Elastic Computing ?

    1. Data will be replicate to different AZs
    2. You can spin up and spin down VMs
    3. Automatically VMs will be add and remove

            Ans: You can spin up and spin down VMs

            In cloud computing, elasticity is defined as "the degree to which a system is able to adapt to workload
            changes by provisioning and de-provisioning resources in an autonomic manner, such that at each pointi
            in time the available resources match the current demand as closely as possible"

66. Can We launch multiple instances with same AMI ? 

        True

67. PEM file is one time physical password ?

        True

68. Windows user required PPK file to connect Linux instance hosted on AWS. True or False ?

        True

69. You can purchase time on EC2 directly from other users and specify the price you want to pay. True or false ?

        True

70. Which of the following might prevent your EC2 instance from appearing in the list of instances?

    1. EC2 is not selected
    2. Correct region is not selected
    3. AWS marketplace is not selected

            Ans: Correct region is not selected

71. Which of the following main reason to terminate an unused EC2 instance ?

    1. Security Concerns
    2. Additional fees
    3. Data Loss

            Ans: Additional fees

72. Which AWS service exists only to redundantly cache data and images ?

    1. AWS Availability Zones
    2. AWS Edge Locations
    3. AWS Regions

            Ans: AWS Edge Locations

73. Regions, AZs and Edge Locations all terms are same… True or False ?

        Ans: False

74. AWS every service is available at every regions…. True or False ?

        Ans: False

75. Premium support is Available in AWS for Developer, Business & Enterprise level ? 

        Ans: True

76. Can you add new Debit/Credit card in your AWS Account ? 

        Ans: True

77. Can you increase micro to large of instance ?

        Ans: True

78. On-demand instances is based on a bid mechanism. True or False ?

        Ans: False

79. RI can be sold on the AWS marketplace?

        Ans: True

80. What are different options in instances ? Which instance is best on Production?

        - On-demand
        - RI
        - Depends on Application or Website

        Ans: Depends on Application or Website

81. Which is most expensive options in instance ?

        Ans: On-demand

82. Amazon S3 is internet accessible storage via HTTP /HTTPS. True or False ?

        Ans: True

83. Amazon S3 is not a object level of storage. True or False?

        Ans: False

84. Amazon S3 is storage for the Internet. True or False?

        Ans: True

85. Temporary storage access speed is not guaranteed. True or False?

        Ans: True

86. There is 99.99% SLA(Service Level Agreement) for temporary storage. True or False?

        Ans: False

87. Ephemeral storage is block-level storage ?

        Ans: True

88. Single object size is up to 5 TB in Amazon S3. True or False ?

        Ans: True

89. You can create unlimited bucket size in Amazon S3. True or False ?

        Ans: True

90. By default, Instance-Backed and EBS-Backed root volumes delete all data. However, when using EBS-Backed storage, you can configure it to
save the data on the root volume. True or false ?

        Ans: True

91. You can switch from an Instance-Backed to an EBS-Backed root volume at any time. True or False ?

        Ans: False

92. When using an EBS-Backed machine, you can override the terminate option and save the root volume. True or False ?

        Ans: True

93. Which of the following is a service of AWS Simple Storage Service(S3)? Select all that apply.

    1. Database Indexing
    2. File searching
    3. Secure Hosting
    4. Storage Scaling

              Ans: 3. Secure Hosting & 4. Storage Scaling

94. What’s the difference between instance store and EBS?

        Issue: 
          I’m not sure whether to store the data associated with my Amazon EC2 instance in instance store or in an
          attached Amazon Elastic Block Store (Amazon EBS) volume. Which option is best for me?

        Resolution: 
          Some Amazon EC2 instance types come with a form of directly attached, block-device storage known as the
          instance store. The instance store is ideal for temporary storage, because the data stored in instance
          store volumes is not persistent through instance stops, terminations, or hardware failures. You can find
          more detailed information about the instance store at Amazon EC2 Instance Store.
          For data you want to retain longer-term, or if you need to encrypt the data, we recommend using EBS
          volumes instead. EBS volumes preserve their data through instance stops and terminations, can be easily
          backed up with EBS snapshots, can be removed from instances and reattached to another, and support
          full-volume encryption. For more detailed information about EBS volumes, see Features of Amazon EBS.

95. BS can be attached to any running instance that is in the same Availability Zone ?

        Ans: True

96. EBS is internet accessible. True or False ?

        Ans: False

95. EBS has persistent file system for EC2. True or False ?

        Ans: True

96. EBS supports incremental snapshots. True or False ?

        Ans: True

97. Amazon Glacier enables customers to offload the administrative burdens of operating and scaling storage to AWS. True or False ?

        Ans: True

98. Amazon Glacier is a great storage choice when low storage cost is paramount. True or False ?

        Ans: True

99. Data is rarely retrieved, and retrieval latency of several hours is acceptable in Glacier. True or False ?

        Ans: True

100. Glacier is basically for data archival. True or False ?

        Ans: True

101. It is very cheap storage. True or False ?

        Ans: True

102. Glacier has very, very slow retrieval times. True or False ?

        Ans: True

103. By Default, Instance-Backed and EBS-Backed root volumes delete all data. However, when using EBS-Backed storage, you can configure it
to save the data on the root volume. True or False ?

        Ans: True

104. You can switch from an Instance-Backed to an EBS-Backed root volume at any time. True or False ?

        Ans: False

105. When using an EBS-Backed machine, you can override the terminate option and save the root volume. True or False ?

        Ans: True

106. VPC is Private, Isolated, Virtual Network. True or False ?

        Ans: True

107. VPC would be logically isolated network in AWS cloud. True or False ?

        Ans: True

108. VPC is also give control of network architecture. True or False ?

        Ans: True

109. VPC is also going to enhanced security. True or False ?

        Ans: True

110. VPC has ability to interwork with other organizations. True or False ?

        Ans: True

111. VPC does not enable hybrid cloud(site-to-site VPN). True or False ?

        Ans: False

112. Route Table is a set of Rules tells the direction of network. True or False ?

        Ans: True

113. Security Group is a subnet level of security. True or False ?

        Ans: False

114. NACLs(Network Access Lists) is a resource level of security. True or False ?

        Ans: False

115. Any default stack is available in Cloud Formation ?

        Ans: You can not create default stack but you can choose the type of stack to create e.g : A sample stack

        A Linux-based chef 12 stack
        A Windows-based Chef 12.2 stack
        A Linux-based Chef 11.10 stack

116. What is the difference between Stack and Template in Cloud Formation ?

        Ans: Stack : Cloud-based applications usually require a group of related resources— application servers,
             database servers, and so on—that must be created and managed collectively. This collection of
             instances is called a stack.

117. We can create multiple server for same stack ?

        Ans: you can select one “instance type” e.g: t2.micro at a time but you can set more then one
             “Webserver Capacity” which is “The initial number of Webserver instances“ means
             automatically same kind of instances will launch.

118. Can you explain the term SQS is pull based, not pushed base.

        Ans: It means that you have to actively poll the queue in order to receive a messages. The messages are
             pushed into the queue by the producers but pulled out of the queue by the consumers.You have to call
             the Receive Message action from the consumer in order to get the messages, they are not pushed to you
             automatically when they arrive.

---
[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](aws-4.md)

---

<br>

{!footer.md!}
