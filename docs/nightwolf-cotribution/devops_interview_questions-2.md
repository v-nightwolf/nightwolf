# DevOps Interview Question and Answered for Freshers and Experienced - 2 
---

 We have consolidated a list of frequently asked DevOps interview questions for Freshers and Experienced. This will help DevOps Engineers in their preparations for Interview.
  You will find these questions very helpful in your DevOps interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

1. List of Docker components?

        1. Docker image: – Contains OS (very small) (almost negligible) + soft wares 
        2. Docker Container: – Container like a machine which is created from Docker image.
        3. Docker file: – Describes steps to create a docker image.
        4. Docker hub/registry: – Stores all docker images publicly.
        5. Docker daemon: – Docker service runs at back end Above five components we call as Docker components

2. What is Docker workflow?

        First we create Docker file by mentioning instructions to build docker image. Form this Docker image, we
        are going to create Docker container. This Docker image we can push to docker hub as well. This image can
        be pulled by others to create docker containers. We can create docker images from docker containers.
        Like this we can create Docker images form either docker file or docker containers. We can create docker
        containers from docker images. This is the work flow of docker.

3. Sample Docker file instructions?

         FROM ubuntu
         WORKDIR /tmp
         RUN echo “Hello” > /tmp/testfile
         ENV myname user1
         COPY testfile1 /tmp
         ADD test.tar.gz /tmp

4. What is the importance of volumes in Docker? 

        1. Volume is a directory inside your container   
        2. First declare directory as a volume and then share volume   
        3. Even if we stop container, still we can access volume  
        4. Volume will be created in one container  
        5. You can share one volume across any no of containers  
        6. Volume will not be included when you update an image  
        7. Map volumes in two ways   
        8. Share host – container   
        9. Share container – container

5. What do you mean by port mapping in Docker? 

        Suppose if you want to make any container as web server by installing web package in it, you need to
        provide containers IP address to public in order to access website which is running inside docker 
        container. But Docker containers don’t have an IP address. So, to address this issue, we have a concept
        called Docker port mapping. We map host port with container port and customers use public IP of host
        machine. Then their request will be routed from host port to container’s port and will be loaded webpage
        which is running inside docker container. This is how we can access website which is running inside
        container through port mapping.

6. What is Registry server in Docker? 

        Registry server is our own docker hub created to store private docker images instead of storing in public
        Docker hub. Registry server is one of the docker containers. We create this Registry server from “registry”
        image, especially provided by docker to create private docker hub. We can store any no of private docker
        images in this Registry server. We can give access to others, so that, they also can store their docker
        images whomever you provide access. Whenever we want, we can pull these images and can create containers
        out of these images.

7. Important docker commands? 

        1. Docker ps (to see list of running containers) 
        2. Docker ps -a (to see list of all containers) 
        3. Docker images (to see list of all images) 
        4. Docker run (to create docker container) 
        5. Docker attach (to go inside container) 
        6. Docker stop (to stop container) 
        7. Docker start (to start container) 
        8. Docker commit (to create image out of docker file) 
        9. Docker rm (to delete container) 
        10. Docker rmi (to delete image)

8. What is Ansible? 

        Ansible is one of the configuration Management Tools. It is a method through we automate system admin tasks.
        Configuration refers to each and every minute details of a system. If we do any changes in system means we 
        are changing the configuration of a machine. That means we are changing the configuration of the machine.
        All windows/Linux system administrators manage the configuration of a machine manually. All DevOps engineers
        are managing this configuration automatic way by using some tools which are available in the market. One such
        tool is Ansible. That’s why we call Ansible as configuration management tool.

9. Working process of Ansible?

        Here we crate file called playbook and inside playbook we write script in YAML format to create infrastructure.
        Once we execute this playbook, automatically code will be converted into Infrastructure. We call this process
        as IAC (Infrastructure as Code). We have open source and enterprise editions of Ansible. Enterprise edition
        we call Ansible Tower.

10. The architecture of Ansible?

        We create Ansible server by installing Ansible package in it. Python is pre-requisite to install ansible. 
        We need not to install ansible package in nodes. Because, communication establishes from server to node 
        through “ssh” client. By default all Linux machine will have “ssh” client. Server is going to push the code
        to nodes that we write in playbooks. So Ansible follows pushing mechanism.

11. Ansible components? 

        1. Server:– It is the place where we create playbooks and write code in YML format
        2. Node:– It is the place where we apply code to create infrastructure. Server pushes code to nodes.
        3. SSH:– It is an agent through ansible server pushes code to nodes.
        4. Setup:– It is a module in ansible which gathers nodes information. 
        5. Inventory file:- In this file we keep IP/DNS of nodes.

12. Disadvantages in other SCM (Source Code Management) tools?  

        - Huge overhead of Infrastructure setup   
        - Complicated setup   
        - Pull mechanism   
        - Lot of learning required

13. Advantages of Ansible over other SCM (Source Code Management) tools?   

        - Agentless  
        - Relies on “ssh”  
        - Uses python  
        - Push mechanism

14. How does Ansible work?
 
        We give nodes IP addresses in hosts file by creating any group in ansible server why because, ansible 
        doesn’t recognize individual IP addresses of nodes. We create playbook and write code in YAML script.
        The group name we have to mention in a playbook and then we execute the playbook. By default, playbook 
        will be executed in all those nodes which are under this group. This is how ansible converts code into
        infrastructure.

15. What do you mean by Ad-Hoc commands in Ansible? 

        These are simple one liner Linux commands we use to meet temporary requirements without actually saving
        for later. Here we don’t use ansible modules. So there, Idempotency will not work with Ad-Hoc commands.
        If at all we don’t get required YAML module to write to create infrastructure, then we go for it. Without
        using playbooks we can use these Ad-Hoc commands for temporary purpose.

16. Differences between Chef and Ansible?

       |Ansible   |   Chef       |     
       |----------|--------------|
       | Playbook  |Recipe       |
       | Module    | Resource    |
       | Host     | Node         |
       | Setup    | Ohai         |
       | SSH      | Knife        |
       | mechanism: Push | mechanism: Pull  |

17. What is Playbook in Ansible?

        Playbook is a file where we write YAML script to create infrastructure in nodes. Here, we use modules to 
        create infrastructure. We create so many sections in playbook. We mention all modules in task section. 
        You can create any no of playbooks. There is no limit. Each playbook defines one scenario. All sections
        begin with “-” & its attributes & parameters beneath it.

18. Mention some list of sections that we mention in Playbook?

        1. Target section
        2. Task section
        3. Variable section
        4. Handler section

19. What is Target section in Ansible playbook?

        This is one of the important sections in Playbook. In this section, we mention the group name which
        contains either IP addresses or Hostnames of nodes. When we execute playbook, then code will be pushed
        too all nodes which are there in the group that we mention in Target section. We use “all” key word to
        refer all groups.

20. What is Task section in Ansible playbook?

        This is second most important section in playbook after target section. In this section, we are going
        to mention list of all modules. All tasks we mention in this task section. We can mention any no of 
        modules in one playbook. There is no limit. If there is only one task, then instead of going with big
        playbook, simply we can go with arbitrary command where we can use one module at a time. If more than
        one module, then there is no option except going with big playbook.

21. What is Variable section?
 
        In this section we are going to mention variables. Instead of hard coding, we can mention as variables
        so that during runtime it pulls the actual value in place of key. We have this concept in each and every
        programming language and scripting language. We use “vars” key word to use variables.

22. What is Handler section?

        All tasks we mention in tasks section. But some tasks where dependency is there, we should not mention
        in tasks section. That is not good practice. For example, installing package is one task and starting
        service is one more task. But there is dependency between them. I.e. after installing package only,
        we have to start service. Otherwise it throws error. These kind of tasks, we mention in handler section.
        In above example, package task we mention in task section and service task we mention in handler section 
        so that after installing task only service will be started.

23. What is Dry run in playbook? 

        Dry run is to test playbook. Before executing playbook in nodes, we can test whether the code in playbook
        is written properly or not. Dry run won’t actually executes playbook, but it shows output as` if it 
        executed playbook. Then by seeing the output, we can come to know whether the playbook is written properly
        or not. It checks whether the playbook is formatted correctly or not. It tests how the playbook is going
        to behave without running the tasks.

24. Why are we using loops concept in Ansible?

        Sometimes we might need to deal with multiple tasks. For instance, Installing multiple packages, Creating
        many users, creation many groups..etc. In this case, mentioning module for every task is complex process.
        So, to address this issue, we have a concept of loops. We have to use variables in combination with loops.


25. Where do we use conditionals in Playbooks? 

        Sometimes, your nodes could be mixture of different flavors of Linux OS. Linux commands vary in different
        Linux operating systems. In this case, we can’t execute common set of commands in all machines, at the same
        time, we can’t execute different commands in each node separately. To address this issue, we have
        conditionals concept where commands will be executed based up on certain condition that we give.

26. What is Ansible vault? 

        Sometimes, we use sensitive information in playbooks like passwords, keys …etc. So any one can open these
        playbooks and get to know about this sensitive information. So we have to protect our playbooks from being
        read by others. So by using Ansible vault, we encrypt playbooks so that, those who ever is having password,
        only those can read this information. It is the way of protecting playbooks by encrypting them.

27. What do you mean by Roles in Ansible? 

        Adding more & more functionality to the playbooks will make it difficult to maintain in a single file. 
        To address this issue, we organize playbooks into a directory structure called “roles”. We create separate
        file to each section and we just mention the names of those sections in playbook instead of mentioning all
        modules in main playbook. When you call main playbook, main playbook will call all sections files respectively
        in the order whatever order you mention in playbook. So, by using this Roles, we can maintain small playbook
        without any complexity.

28. Write a sample playbook to install any package? 

        — # My First YAML playbook 
        – hosts: demo 
          user: ansible 
          become: yes 
          connection: ssh
          tasks: 
            – name: Install HTTPD on centos 7 
                action: yum name=httpd state=installed

29. Write a sample playbook by mentioning variables instead of hard coding?

        — # My First YAML playbook 
        – hosts: demo 
          user: nightwolf
          become: yes 
          connection: ssh
          vars: pkgname: httpd
          tasks: 
           – name: Install HTTPD server on centos 7 
             action: yum name=‘{{pkgname}}’ state=installed

30. What is CI & CD? 

        CI means Continues Integration and CD means Continues Delivery/Deploy. Whenever developers write code, we
        integrate all that code of all developers at that point of time and we build, test and deliver/deploy to 
        the client. This process we call CI & CD. Jenkins helps in achieving this. So instead of doing night builds,
        build as and when commit occurs by integrating all code in SCM tool, build, test and checking the quality
        of that code is what we call Continues Integration.

31. Key terminology that we use in Jenkins?

        - Integrate: Combine all code written by developers till some point of time.
        - Build: Compile the code and make a small executable package.
        - Test: Test in all environments whether application is working properly or not.
        - Archived: Stored in an artifactory so that in future we may use/deliver again.
        - Deliver: Handing the product to Client Deploy: Installing product in client’s machines.

32. What is Jenkins Workflow? 

        We attach Git, Maven, Selenium & Artifactory plug-ins to Jenkins. Once Developers put the code in Git,
        Jenkins pulls that code and send to Maven for build. Once build is done, Jenkins pulls that built code
        and send to selenium for testing. Once testing is done, then Jenkins will pull that code and send to
        Artifactory as per requirement and finally we can deliver the end product to client we call Continues 
        delivery. We can also deploy with Jenkins into clients machine directly as per the requirement. This is
        what Jenkins work flow.

33. What are the ways through which we can do Continues Integration? 

        There are total three ways through which we can do Continues Integration:

          1. Manually:– Manually write code, then do build manually and then test manually by writing test cases
                        and deploy manually into clients machine. 
          2. Scripts:– Can do above process by writing scripts so that these scripts do CI&CD automatically. 
                       here complexity is, writing script is not so easy. 
          3. Tool:– Using tools like Jenkins is very handy. Everything is preconfigured in these type of tools.
                    So less manual intervention. This is the most preferred way.

34. Benefits of CI? 

        1. Detects bugs as soon as possible, so that bug will be rectified fast and development happens fast.
        2. Complete automation. No need manual intervention. 
        3. We can intervene manually whenever we want i.e. we can stop any stage at any point of time so have 
           better control.
        4. Can establish complete and continues work flow.

35. Why only Jenkins?  

        - It has so many plug-ins. 
        - You can write your own plug-in  
        - You can use community plug-ins  
        - Jenkins is not just a tool. It is a framework i.e. you can do what ever you want. All you need is plugins.
        - We can attach slaves to Jenkins master. It instructs others(slaves) to do Job.
        - If slaves are not available, Jenkins itself does the job.  
        - Jenkins also acts as cron server replacement i.e. can do repeated tasks automatically.  
        - Running some scripts regularly E.g.: Automatic daily alarm.  
        - Can create Labels (Group of slaves) (Can restrict where the project has to run).

36. What is Jenkins Architecture? 

        Jenkins architecture is Client-Server model. Where ever, we install Jenkins, we call that server is Jenkins
        master. We can also create slaves in Jenkins, so that server load will be distributed to slaves. Jenkins
        Master randomly assigns tasks to slaves. But if you want to restrict any job to run in particular slave, 
        then we can do it, so that particular job will be executed in that slave only. We can group some slaves
        by using “Label”.

37. How to install Jenkins? 

        - You can install Jenkins in any OS. All OSs supports Jenkins. We access Jenkins through web page only.
           That’s why it doesn’t make any difference whether you install Jenkins in Windows or Linux.   
        - Choose Long Term Support release version, so that you will get support from Jenkins community. If you
           are using Jenkins for testing purpose, you can choose weekly release. But for production environments,
           we prefer Long Term Support release version.
        - Need to install JAVA. Java is pre-requisite to install Jenkins.  
        - Need to install web package. Because, we are going to access Jenkins through web page only.

38. Does Jenkins open source? 

        There are two editions in Jenkins 1. Open source 2. Enterprise edition Open source edition we call Jenkins.
        Here we get support from community if we need it. Enterprise edition we call Hudson. Here Jenkins company 
        will provide support.

39. How many types of configurations in Jenkins?

        There are total 3 types of configurations in Jenkins:
         1. Global:– Here, whatever configuration changes we do, applicable to whole Jenkins including jobs as well
                     as nodes. This configuration has high priority. 
         2. Job:– These configurations applicable to only Jobs. Jobs also we call as projects or items in Jenkins. 
         3. Node:– These configurations applicable to only nodes. Also we call Slaves. These are kind of helpers to
                   Jenkins master to distribute the excessive load.

40. What do you mean by workspace in Jenkins? 

        The workspace is the location on your computer where Jenkins places all files related to the Jenkins
        project. By default each project or job is assigned a workspace location and it contains Jenkins-specific
        project metadata, temporary files like logs and any build artifacts, including transient build files.
        Jenkins web page acts like a window through which we are actually doing work in workspace.

41. List of Jenkins services?

           - localhost:8080/restart (to restart Jenkins). 
           - localhost:8080/stop (to stop Jenkins).
           - localhost:8080/start (to start Jenkins).

42. How to create a free style project in Jenkins?   

        - Create project by giving any name  
        - Select Free style project  
        - Click on build  
        - Select execute windows batch command  
        - Give any command (echo “Hello Dear Students!!”)  
        - Select Save  
        - Click on Build now  
        - Finally can see Console output

43. What do you mean by Plugins in Jenkins?   

        - With Jenkins, nearly everything is a plugin and that nearly all functionality is provided by plugins. 
          You can think of Jenkins as little more than an executor of plugins.  
        - Plugins are small libraries that add new abilities to Jenkins and can provide integration points to other
          tools.  
        - Since nearly everything Jenkins does is because of a plugin, Jenkins ships with a small set of default
          plugins, some of which can be upgraded independently of Jenkins.

44. How to create Maven Project?   

        - Select new item 
        - Copy the git hub maven project link and paste in git section in Jenkins  
        - Select build  
        - Click on clean package  
        - Select save  
        - Click on Build now  
        - Verify workspace contents with GitHub sideSee console output

45. How can we Schedule projects? 

        Sometimes, we might need some jobs to be executed after frequent intervals. To schedule a job:  

         - Click on any project 
         - Click on Configure  
         - Select on Build triggers  
         - Click on Build periodically  
         - Give timing (In format : * * * * * )  
         - Select Save  
         - Can see automatic builds every 1 min  
         - You can manually trigger build as well if you want.

46. What do you mean by Upstream and Downstream projects? 
 
        We can also call them as linked projects. These are the ways through which, we connect jobs one with other. 
        In Upstream jobs, first job will trigger second job after build is over. In Downstream jobs, second job
        will wait till first job finishes its build. As and when first job finishes its work, then second job will
        be triggered automatically. In Upstream, first job will be active. In Downstream jobs, second job will be 
        active. We can use any one type to link multiple jobs.

47. What is view in Jenkins?

        We can customize view as per our needs. We can modify Jenkins home page. We can segregate jobs as per the 
        type of jobs like free style jobs and maven jobs and so on. To create custom view:

            - Select List of Related Projects  
            - Select Default views  
            - Click on All  
            - Click on + and select Freestyle
            - Select List Views  
            - Select Job filter  
            - Select required jobs to be segregated  
            - Now, you can see different view

48. What is User Administration in Jenkins? 

        In Jenkins, we can create users, groups and can assign limited privileges to them so that, we can have
        better control on Jenkins. Users will not install Jenkins in their machines. They access Jenkins as a user.
        Here we can’t assign permissions directly to users. Instead we create “Roles” and assign permissions to 
        those roles. These roles we attach to users so that users get the permissions whatever we assign to those
        roles.

49. What is Global tool configuration in Jenkins?

        We install Java, Maven, Git and many other tools in our server. Whenever Jenkins need those tools, by 
        default Jenkins will install them automatically every time. But it’s not a good practice. That’s why we 
        give installed path of all these tools in Jenkins so that whenever Jenkins need them, automatically Jenkins
        pull them form local machine instead of downloading every time. This way of giving path of these tools in
        Jenkins we call “Global tool configuration”

50. What is Build?

        Build means, Compile the source code, assembling of all class files and finally creating deliverable

        Compile:– Convert Source code into machine-readable format 
        Assembly (Linking):– Grouping all class files 
        Deliverable:– .war, .jar 

        The above process is same for any type of code. This process we call Build.

51. What is Maven?

        Maven is one of the Build tools. It is the most advance build tool in the market. In this, everything is
        already pre-configured. Maven belongs to Apache Company. We use maven to build Java code only. We can’t
        build other codes by using Maven. By default, we get so many plugins with Maven. You can write your own
        plugins as well. Maven’s local repository is “.M2” where we can get required compilers and dependencies.
        Maven’s main configuration file is “pom.xml” where we keep all instructions to build.

52. Advantages of Maven?  

        - Automated tasks (Mention all in pom.xml)   
        - Multiple Tasks at a time   
        - Quality product  
        - Minimize bad builds
        - Keep history
        - Save time – Save money   
        - Gives set of standards
        - Gives define project life cycle (Goals)   
        - Manage all dependencies   
        - Uniformity in all projects   
        - Re-usability

53. List of Build tools available in Market?   

        - C and C++: Make file   
        - .Net: Visual studio   
        - Java: Ant, Maven

54. What is the architecture of Maven? 

        Maven main configuration file is pom.xml. For one project, there will be one workspace and one pom.xml.
        Requirements for build:–  

          - Source code (Will be pulled from Git hub)
          - Compiler (Pulls from remote repo and then put them in local repo, from there, maven pulls into 
            Workspace)
          - Dependencies (Pulls from remote repo and then put them in local repo, from there, maven pulls into
            Workspace)

55. What is Maven’s Build Life Cycle?

        In maven, we have different goals. These are:

           - Generate resources (Dependencies)
           - Compile code
           - Unit test
           - Package (Build)
           - Install (in to local repo & artifactory)
           - Deploy (to servers)
           - Clean (delete all run time files)

56. What does POM.XML contains? 

        POM.XML is maven’s main configuration file where we keep all details related to project. It contains:

          - Metadata about that project
          - Dependencies required to build the project
          - The kind of project
          - Kind of output you want (.jar, .war)
          - Description about that project

57. What is Multi-Module Project in Maven?

        - Dividing big project into small modules, we call Multi Module Project. 
        - Each module must have its own SRC folder & pom.xml so that build will happen separately.
        - To build all modules with one command, there should be a parent pom.xml file. This calls all child
          pom.xml files automatically.
        - In parent pom.xml file, need to mention the child pom.xml files in an order.

58. What is Nagios? 

        Nagios is one of the monitoring tools. By using Nagios we can monitor and give alerts. Where ever you
        install Nagios that becomes Nagios server. Monitoring is important, because we need to make sure that
        our servers should never go down. If at all in some exceptional cases server goes down, immediately we
        need alert in the form of intimation so that we can take required action to bring the server up immediately.
        So for this purpose, we use Nagios.

59. Why do we have to use Nagios?

        There are many advantages in using Nagios:

          - It is oldest & Latest (every now and then, it is getting upgraded as per current market requirements)
          - Stable (we have been using this since so many years and it is performing well)
          - By default, we get so many Plug-ins
          - It is having its own Database.
          - Nagios is both Monitoring & Alerting tool.

60. How does Nagios works?

        - We mention all details in configuration files what data to be collected from which machine.
        - Nagios daemon reads those details about what data to be collected.
        - Daemon use NRPE (Nagios Remote Plug-in Executer) plug-in to collect data form nodes and stores in its
          own database.
        - Finally displays in Nagios dashboard.

61. What is the Directory structure of Nagios? 

         /usr/local/nagios/bin – binary files 
         /usr/local/nagios/sbin – CGI files (to get web page)
         /usr/local/nagios/libexec – plugins
         /usr/local/nagios/share – PHP Files
         /usr/local/nagios/etc – configuration files
         /usr/local/nagios/var – logs
         /usr/local/nagios/var/status.dat(file) – database


62. What are the Important Configuration files in Nagios?

        Nagios main configuration file is /usr/local/nagios/etc/nagios.cfg 

        /usr/local/nagios/etc/objects/localhost.cfg (where we keep hosts information)
        /usr/local/nagios/etc/objects/contacts.cfg (whom to be informed (emails))
        /usr/local/nagios/etc/objects/timeperiods.cfg (at what time to monitor)
        /usr/local/nagios/etc/objects/commands.cfg (plugins to use)
        /usr/local/nagios/etc/objects/templates.cfg (sample templates)


<br>
<br>
<br>
<br>
{!footer.md!}
