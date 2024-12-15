# Top 250 Questions and Answers For Terraform Associate Certification
---

 We have consolidated a list of frequently asked questions in Terraform AssociateCertification. Same list consists of frequently asked Terraform interview questions. This will help DevOps Engineers in their preparations for Interview.
  You will find these questions very helpful in your DevOps interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

1. What is Infrastructure as Code?

        You write and execute the code to define, deploy, update, and destroy your infrastructure

2. What are the benefits of IaC?

        a. Automation => We can bring up the servers with one script and scale up and down based on our load with
           the same script.
        b. Reusability of the code =>  We can reuse the same code
        c. Versioning => We can check it into version control and we get versioning. Now we can see an incremental
           history of who changed what, how is our infrastructure actually defined at any given point of time, and
           wehave this transparency of documentation. 
           IaC makes changes idempotent, consistent, repeatable, and predictable.

3. How using IaC make it easy to provision infrastructure?

        IaC makes it easy to provision and apply infrastructure configurations, saving time. It standardizes 
        workflows across different infrastructure providers (e.g., VMware, AWS, Azure, GCP, etc.) by using a common
        syntax across all of them.

4. What is Ideompodent in terms of IaC?

        The idempotent characteristic provided by IaC tools ensures that, even if the same code is applied multiple
        times, the result remains the same.

5. What are Day 0 and Day 1 activities?

        IaC can be applied throughout the lifecycle, both on the initial build, as well as throughout the life of 
        the infrastructure. Commonly, these are referred to as Day 0 and Day 1 activities.

        "Day 0" code provisions and configures your initial infrastructure.
        "Day 1" refers to OS and application configurations you apply after you have initially built your 
        infrastructure.

6. What are the use cases of Terraform?

        Heroku App Setup
        Multi-Tier Applications
        Self-Service Clusters
        Software Demos
        Disposable Environments
        Software Defined Networking
        Resource Schedulers
        Multi-Cloud Deployment

      Reference: <a target="_blank" href=https://www.terraform.io/intro/use-cases.html >https://www.terraform.io/intro/use-cases.html</a>

7. What are the advantages of Terraform?

        Platform Agnostic
        State Management
        Operator Confidence

      Reference: <a target="_blank" href=https://learn.hashicorp.com/terraform/getting-started/intro > https://learn.hashicorp.com/terraform/getting-started/intro </a>

8. Where do you describe all the components or your entire datacenter so thatTerraform provision those?

        Configuration files ends with *.tf

9. How can Terraform build infrastructure so efficiently?

        Terraform builds a graph of all your resources, and parallelizes the creation and modification of any
        non-dependent resources. Because of this, Terraform builds infrastructure as efficiently as possible, and
        operators get insight into dependencies in their infrastructure.

10. What is multi-cloud deployment?

        Provisoning your infrastrcutire into multiple cloud providers to increase fault-tolerance of your 
        applications.

11. How multi-cloud deployment is useful?

        By using only a single region or cloud provider, fault tolerance is limited by the availability of that 
        provider.
        Having a multi-cloud deployment allows for more graceful recovery of the loss of a region or entire provider.

12. What is cloud-agnostic in terms of provisioning tools?

        cloud-agnostic and allows a single configuration to be used to manage multiple providers, and to even handle 
        cross-cloud dependencies.

13. Is Terraform cloud-agostic?

        Yes

14. What is the use of terraform being cloud-agnostic?

        It simplifies management and orchestration, helping operators build large-scale multi-cloud infrastructures.

15. What is the Terraform State?

        Every time you run Terraform, it records information about what infrastructure it created in a Terraform
        state file
        By default, when you run Terraform in the folder /some/folder, Terraform creates the file 
        /some/folder/terraform.tfstate
        This file contains a custom JSON format that records a mapping from the Terraform resources in your 
        configuration files to the representation of those resources in the real world.

16. What is the purpose of the Terraform State?

        Mapping to the Real World => Terraform requires some sort of database to map Terraform config to the real
         world because you can not find the same functionality in every cloud provider. You need to have some kind 
         of mechanism to be cloud-agnostic

        Metadata => Terraform must also track metadata such as resource dependencies, pointer to the provider 
         configuration that was most recently used with the resource in situations where multiple aliased providers 
         are present.

        Performance => When running a terraform plan, Terraform must know the current state of resources in order 
         to effectively determine the changes that it needs to make to reach your desired configuration.
         For larger infrastructures, querying every resource is too slow. Many cloud providers do not provide APIs
         to query multiple resources at once, and the round trip time for each resource is hundreds of milliseconds.
         So, Terraform stores a cache of the attribute values for all resources in the state. This is the most 
         optional feature of Terraform state and is done only as a performance improvement.

        Syncing => When two people works on the same file and doing some changes to the infrastructure. Its very 
          important for everyone to be working with the same state so that operations will be applied to the same
          remote objects.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/state/purpose.html>https://www.terraform.io/docs/state/purpose.html</a>

17. What is the name of the terraform state file?

        terraform.tfstate

18. How do you install terraform on different OS?

        // Mac OS
        brew install terraform
        // Windows
        choco install terraform
        
19. How do you manually install terraform?

        step 1: Download the zip fille
        step 2: mv ~/Downloads/terraform /usr/local/bin/terraform

20. Where do you put terraform configurations so that you can configure somebehaviors of Terraform itself?

        The special terraform configuration block type is used to configure some behaviors of Terraform itself, 
        such as requiring a minimum Terraform version to apply your configuration.

        terraform
         {
           # ...
         }

21. Only constants are allowed inside the terraform block. Is this correct?

        Yes

        Within a terraform block, only constant values can be used; arguments may not refer to named objects such
        as resources, input variables, etc, and may not use any of the Terraform language built-in functions. 

22. What are the Providers?

        A provider is a plugin that Terraform uses to translate the API interactions with the service. A provider
        is responsible for understanding API interactions and exposing resources. Because Terraform can interact
        with any API, you can represent almost any infrastructure type as a resource in Terraform.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/configuration/providers.html> https://www.terraform.io/docs/configuration/providers.html</a>

23. How do you configure a Provider?

        provider "google" {
          project = "acme-app"
          region = "us-central1"
        }
        
        The name given in the block header ("google" in this example) is the name of the provider to configure. 
        Terraform associates each resource type with a provider by taking the first word of the resource type name
        (separated by underscores), and so the "google" provider is assumed to be the provider for the resource 
        type name google_compute_instance.

        The body of the block (between { and } ) contains configuration arguments for the provider itself. Most 
        arguments in this section are specified by the provider itself; in this example both project and region
        are specific to the google provider.

24. What are the meta-arguments that are defined by Terraform itself and availablefor all provider blocks?

        version: Constraining the allowed provider versions 
        alias: using the same provider with different configurations for different resources

25. What is Provider initialization and why do we need?

        Each time a new provider is added to configuration -- either explicitly via a provider block or by adding
        a resource from that provider -- Terraform must initialize the provider before it can be used.

        Initialization downloads and installs the provider's plugin so that it can later be executed.

26. How do you initialize any Provider?

        Provider initialization is one of the actions of terraform init. 
        Running this command will download and initialize any providers that are not already initialized.

27. When you run terraform init command, all the providers are installed in thecurrent working directory. Is this true?

        Providers downloaded by terraform init are only installed for the current working directory; other working
        directories can have their own installed provider versions.

        Note that terraform init cannot automatically download providers that are not distributed by HashiCorp.
        
28. How do you constrain the provider version?

        To constrain the provider version as suggested, add a required_providers block inside a terraform block:

        terraform {
          required_providers {
          aws = "~> 1.0"
          }
        }

29. How do you upgrade to the latest acceptable version of the provider?

        terraform init --upgrade
        It upgrade to the latest acceptable version of each provider. This command also upgrades to the latest
        versions of all Terraform modules. 

30. How many ways you can configure provider versions?

        1. With required_providers blocks under terraform block: 

          terraform {
            required_providers {
            aws = "~> 1.0"
            }
          }

        2. Provider version constraints can also be specified using a version argument within a provider block:

          provider {
              version= "1.0"
          }

31. How do you configure Multiple Provider Instances?

          alias

          You can optionally define multiple configurations for the same provider, and select which one to use on
          a per-resource or per-module basis.

32. Why do we need Multiple Provider instances?

        Some of the example scenarios:

          a. multiple regions for a cloud platform
          b. targeting multiple Docker hosts
          c. multiple Consul hosts, etc.

33. How do we define multiple Provider configurations?

        To include multiple configurations for a given provider, include multiple provider blocks with the same 
        provider name, but set the alias meta-argument to an alias name to use for each additional configuration.

        # The default provider configuration
          provider "aws" {
            region = "us-east-1"
          }
          
        # Additional provider configuration for west coast region
          provider "aws" {
            alias = "west"
            region = "us-west-2"
          }

34. How do you select alternate providers?

        By default, resources use a default provider configuration inferred from the first word of the resource 
        type name. For example, a resource of type aws_instance uses the default (un-aliased) aws provider 
        configuration unless otherwise stated.

        resource "aws_instance" "foo" {
          provider = aws.west

          # ...
        }

35. What is the location of the user plugins directory?

        Windows => %APPDATA%\terraform.d\plugins
        Unix based systems => ~/.terraform.d/plugins

36. Third-party plugins should be manually installed. Is that true?

        True

37. The command terraform init cannot install third-party plugins? True or false?

        True

        Install third-party providers by placing their plugin executables in the user plugins directory. The user 
        plugins directory is in one of the following locations, depending on the host operating system.

        Once a plugin is installed, terraform init can initialize it normally. You must run this command from the
        directory where the configuration files are located.

38. What is the naming scheme for provider plugins?

        "terraform-provider-<NAME>_vX.Y.Z"

39. What is the CLI configuration File?

        The CLI configuration file configures per-user settings for CLI behaviors, which apply across all Terraform
        working directories.

        It is named either ".terraformrc" or "terraform.rc" .
        
40. Where is the location of the CLI configuration File?

        On Windows, the file must be named named "terraform.rc" and placed in the relevant user's
        %APPDATA% directory.

        On all other systems, the file must be named ".terraformrc" (note the leading period) and placed directly
        in the home directory of the relevant user.

        The location of the Terraform CLI configuration file can also be specified using the TF_CLI_CONFIG_FILE
        environment variable.

41. What is Provider Plugin Cache?

        By default, terraform init downloads plugins into a subdirectory of the working directory so that each 
        working directory is self-contained. As a consequence, if you have multiple configurations that use the 
        same provider then a separate copy of its plugin will be downloaded for each configuration.

        Given that provider plugins can be quite large (on the order of hundreds of megabytes), this default 
        behavior can be inconvenient for those with slow or metered Internet connections.

        Therefore Terraform optionally allows the use of a local directory as a shared plugin cache, which then
        allows each distinct plugin binary to be downloaded only once.

42. How do you enable Provider Plugin Cache?

        To enable the plugin cache, use the plugin_cache_dir setting in the CLI configuration file.

        plugin_cache_dir = "$HOME/.terraform.d/plugin-cache"

        Alternatively, the TF_PLUGIN_CACHE_DIR environment variable can be used to enable caching or to override
        an existing cache directory within a particular shell session.

43. When you are using plugin cache you end up growing cache directory withdifferent versions. Whose responsibility
    to clean it?

        User

        Terraform will never itself delete a plugin from the plugin cache once it has been placed there. Over time, 
        as plugins are upgraded, the cache directory may grow to contain several unused versions which must be 
        manually deleted.

44. Why do we need to initialize the directory?

        When you create a new configuration - or check out an existing configuration from version control - you
        need to initialize the directory.

        // Example
          provider "aws" {
            profile = "default"
            region = "us-east-1"
          }

          resource "aws_instance" "example" {
            ami = "ami-2757f631"
            instance_type = "t2.micro"
          }

        Initializing a configuration directory downloads and installs providers used in the configuration, which in
        this case is the aws provider. Subsequent commands will use local settings and data during initialization.

45. What is the command to initialize the directory?

        terraform init

46. If different teams are working on the same configuration. How do you make filesto have consistent formatting?

        terraform fmt

        This command automatically updates configurations in the current directory for easy readability and 
        consistency.

47. If different teams are working on the same configuration. How do you make filesto have syntactically valid and 
    internally consistent?

        terraform validate

        This command will check and report errors within modules, attribute names, and value types.

        Validate your configuration. If your configuration is valid, Terraform will return a success message.

48. What is the command to create infrastructure?

        terraform apply

49. What is the command to show the execution plan and not apply?

        terraform plan

50. How do you inspect the current state of the infrastructure applied?

        terraform show
        
        When you applied your configuration, Terraform wrote data into a file called terraform.tfstate. This file
        now contains the IDs and properties of the resources Terraform created so that it can manage or destroy 
        those resources going forward.

51. If your state file is too big and you want to list the resources from your state.What is the command?

        terraform state list

52. What is plug-in based architecture?

        Defining additional features as plugins to your core platform or core application. 
        This provides extensibility, flexibility and isolation

53. What are Provisioners?

        If you need to do some initial setup on your instances, then provisioners let you upload files, run shell 
        scripts, or install and trigger other software like configuration management tools, etc.

54. How do you define provisioners?

        resource "aws_instance" "example" {
          ami = "ami-b374d5a5"
          instance_type = "t2.micro"

          provisioner "local-exec" {
            command = "echo hello > hello.txt"
          }
        }

        Provisioner block within the resource block. Multiple provisioner blocks can be added to define multiple 
        provisioning steps. Terraform supports multiple provisioners 

55. What are the types of provisioners?

        local-exec
        remote-exec

56. What is a local-exec provisioner and when do we use it?

        The local-exec provisioner executing a command locally on your machine running Terraform.
        We use this when we need to do something on our local machine without needing any external URL.

57. What is a remote-exec provisioner and when do we use it?

        Another useful provisioner is remote-exec which invokes a script on a remote resource after it is created.
        This can be used to run a configuration management tool, bootstrap into a cluster, etc.

58. Are provisioners runs only when the resource is created or destroyed?

        Provisioners are only run when a resource is created or destroyed. Provisioners that are run while 
        destroying are Destroy provisioners.
        They are not a replacement for configuration management and changing the software of an already-running
        server, and are instead just meant as a way to bootstrap a server.

59. What do we need to use a remote-exec?

        In order to use a remote-exec provisioner, you must choose an ssh or winrm connection in the form of a
        connection block within the provisioner. 

        Here is an example

          provider "aws" {
            profile = "default"
            region = "us-west-2"
          }

          resource "aws_key_pair" "example" {
            key_name = "examplekey"
            public_key = file("~/.ssh/terraform.pub")
          }

          resource "aws_instance" "example" {
            key_name = aws_key_pair.example.key_name
            ami = "ami-04590e7389a6e577c"
            instance_type = "t2.micro"

            connection {
              type = "ssh"
              user = "ec2-user"
              private_key = file("~/.ssh/terraform")
              host = self.public_ip
              }

            provisioner "remote-exec" {
              inline = [
                "sudo amazon-linux-extras enable nginx1.12",
                "sudo yum -y install nginx",
                "sudo systemctl start nginx"
              ]
            }
          }

60. When terraform mark the resources are tainted?

        If a resource successfully creates but fails during provisioning, Terraform will error and mark the 
        resource as "tainted".

        A resource that is tainted has been physically created, but can not be considered safe to use since 
        provisioning failed.

61. You applied the infrastructure with terraform apply and you have some taintedresources. You run an execution plan now what happens to those tainted resources?

        When you generate your next execution plan, Terraform will not attempt to restart provisioning on the
        same resource because it is not guaranteed to be safe.

        Instead, Terraform will remove any tainted resources and create new resources, attempting to provision
        them again after creation.

62. Terraform also does not automatically roll back and destroy the resource duringthe apply when the failure happens. Why?

        Terraform also does not automatically roll back and destroy the resource during the apply when the failure
        happens, because that would go against the execution plan: the execution plan would have said a resource
        will be created, but does not say it will ever be deleted. If you create an execution plan with a tainted
        resource, however, the plan will clearly state that the resource will be destroyed because it is tainted.

63. How do you manually taint a resource?

        terraform taint resource.id

64. Does the taint command modify the infrastructure?

        terraform taint resource.id

        This command will not modify infrastructure, but does modify the state file in order to mark a resource as
        tainted. Once a resource is marked as tainted, the next plan will show that the resource will be destroyed
        and recreated and the next apply will implement this change.

65. By default, provisioners that fail will also cause the Terraform apply itself to fail.Is this true?

        True

66. By default, provisioners that fail will also cause the Terraform apply itself to fail.How do you change this?

        The 'on_failure' setting can be used to change this. The allowed values are:

        continue: Ignore the error and continue with creation or destruction.

        fial: Raise an error and stop applying (the default behavior). If this is a creation provisioner, taint 
        the resource.

        // Example
          resource "aws_instance" "web" {
            # ...

            provisioner "local-exec" {
              command = "echo The server's IP address is ${self.private_ip}"
              on_failure = "continue"
            }
          }

67. How do you define destroy provisioner and give an example?

        You can define destroy provisioner with the parameter when:

        provisioner "remote-exec" {
          when = "destroy"
          # <...snip...>
        }

68. How do you apply constraints for the provider versions?

        The "required_providers" setting is a map specifying a version constraint for each provider required by
        your configuration.

        terraform {
          required_providers {
          aws = ">= 2.7.0"
          }
        }

69. What should you use to set both a lower and upper bound on versions for eachprovider?

        terraform {
          required_providers {
          aws = "~> 2.7.0"
          }
        }

70. How do you try experimental features?

        In releases where experimental features are available, you can enable them on a per-module basis by setting
        the experiments argument inside a terraform block:

        terraform {
          experiments = [example]
        }

71. When does the terraform does not recommend using provisions?

        Passing data into virtual machines and other compute resources
        Running configuration management software

      References: 

      <a target="_blank" href=https://www.terraform.io/docs/provisioners/#passing-data-into-virtual-machines-and-other-compute-resources>https://www.terraform.io/docs/provisioners/#passing-data-into-virtual-machines-and-other-compute-resources</a>

      <a target="_blank" href=https://www.terraform.io/docs/provisioners/#running-configuration-management-software>https://www.terraform.io/docs/provisioners/#running-configuration-management-software</a>

72. Expressions in provisioner blocks cannot refer to their parent resource by name.Is this true?

        True

        The "self" object represents the provisioner's parent resource, and has all of that resource's attributes.

        For example, use "self.public_ip" to reference an aws_instance 'public_ip' attribute.

73. What does this symbol version = "~> 1.0" mean when defining versions?

        Any version more than 1.0 and less than 2.0.

74. Terraform supports both cloud and on-premises infrastructure platforms. Is this true?

        True

75. Terraform assumes an empty default configuration for any provider that is notexplicitly configured. A provider block can be empty. Is this true?

        True

76. How do you configure the required version of Terraform CLI can be used withyour configuration?

        The required_version setting can be used to constrain which versions of the Terraform CLI can be used with
        your configuration. If the running version of Terraform does not match the constraints specified, Terraform
        will produce an error and exit without taking any further actions.

77. Terraform CLI versions and provider versions are independent of each other. Isthis true?

        True

78. You are configuring aws provider and it is always recommended to hard codeaws credentials in *.tf files. Is this true?

        False

        nightwolf recommends that you never hard-code credentials into "*.tf" configuration files. We are explicitly
        defining the default AWS config profile here to illustrate how Terraform should access sensitive credentials.

        If you leave out your AWS credentials, Terraform will automatically search for saved API credentials 
        (for example, in ~/.aws/credentials ) or IAM instance profile credentials. This is cleaner when ".tf" files 
        are checked into source control or if there is more than one admin user 

79. You are provisioning the infrastructure with the command terraform apply andyou noticed one of the resources failed. How do you remove that resource withoutaffecting the whole infrastructure?

        You can taint the resource ans the next apply will destroy the resource

        terraform taint <resource.id>

---

[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](terraform_interview_question-2.md)

---

<br>
<br>

{!footer.md!}
