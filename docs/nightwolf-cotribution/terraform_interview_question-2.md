# Top 250 Questions and Answers For Terraform Associate Certification - 2
---

 We have consolidated a list of frequently asked questions in Terraform AssociateCertification. Same list consists of frequently asked Terraform interview questions. This will help DevOps Engineers in their preparations for Interview.
  You will find these questions very helpful in your DevOps interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

80. What is command fmt?

        The terraform "fmt" command is used to rewrite Terraform configuration files to a canonical format and 
        style. This command applies a subset of the Terraform language style conventions, along with other minor
        adjustments for readability.

81. What is the recommended approach after upgrading terraform?

        The canonical format may change in minor ways between Terraform versions, so after upgrading Terraform 
        we recommend to proactively run terraform "fmt" on your modules along with any other changes you are 
        making to adopt the new version.

82. What is the command usage?

        terraform fmt [options] [DIR]

83. By default, fmt scans the current directory for configuration files. Is this true?

        True

        By default, "fmt" scans the current directory for configuration files. If the dir argument is provided 
        then it will scan that given directory instead. If dir is a single dash (-) then fmt will read from 
        standard input (STDIN).

84. You are formatting the configuration files and what is the flag you should use tosee the differences?

        terraform fmt -diff

85. You are formatting the configuration files and what is the flag you should use toprocess the subdirectories as well?

        terraform fmt -recursive

86. You are formatting configuration files in a lot of directories and you don’t wantto see the list of file changes. What is the flag that you should use?

        terraform fmt -list=false

87. What is the command taint?

        The terraform "taint" command manually marks a Terraform-managed resource as tainted, forcing it to be
        destroyed and recreated on the next apply.

        This command will not modify infrastructure, but does modify the state file in order to mark a resource
        as tainted. Once a resource is marked as tainted, the next plan will show that the resource will be 
        destroyed and recreated and the next apply will implement this change.

88. What is the "taint" command usage?

        terraform taint [options] address

        The address argument is the address of the resource to mark as tainted. The address is in the resource 
        address syntax.

89. When you are tainting a resource terraform reads the default state fileterraform.tfstate. What is the flag you should use to read from a different path?

        terraform taint -state=path

90. Give an example of tainting a single resource?

        terraform taint aws_security_group.allow_all

        The resource aws_security_group.allow_all in the module root has been marked as tainted.

91. Give an example of tainting a resource within a module?

        terraform taint "module.couchbase.aws_instance.cb_node[9]"

        Resource instance module.couchbase.aws_instance.cb_node[9] has been marked as tainted.

92. What is the command import?

        The terraform import command is used to import existing resources into Terraform.

        Terraform is able to import existing infrastructure. This allows you take resources you have created by
        some other means and bring it under Terraform management.

        This is a great way to slowly transition infrastructure to Terraform, or to be able to be confident that
        you can use Terraform in the future if it potentially doesn't support every feature you need today.

93. What is the command import usage?

        terraform import [options] ADDRESS ID

94. What is the default workspace name?

        default

95. What are workspaces?

        Each Terraform configuration has an associated backend that defines how operations are executed and where
        persistent data such as the Terraform state are stored.

        The persistent data stored in the backend belongs to a workspace. Initially the backend has only one 
        workspace, called "default", and thus there is only one Terraform state associated with that configuration.

        Certain backends support multiple named workspaces, allowing multiple states to be associated with a single
        configuration.

96. What is the command to list the workspaces?

        terraform workspace list

97. What is the command to create a new workspace?

        terraform workspace new <name>

98. What is the command to show the current workspace?

        terraform workspace show

99. What is the command to switch the workspace?

        terraform workspace select <workspace name>

100. What is the command to delete the workspace?

        terraform workspace delete <workspace name>

101. Can you delete the default workspace?

        No. You can't ever delete default workspace

102. You are working on the different workspaces and you want to use a differentnumber of instances based on the workspace. How do you achieve that?

        resource "aws_instance" "example" {
          count = "${terraform.workspace == "default" ? 5 : 1}"
          # ... other arguments
        }

103. You are working on the different workspaces and you want to use tags based onthe workspace. How do you achieve that?

        resource "aws_instance" "example" {
          tags = {
            Name = "web - ${terraform.workspace}"
          }
          # ... other arguments
        }

104. You want to create a parallel, distinct copy of a set of infrastructure in order totest a set of changes before modifying the main production infrastructure. How doyou achieve that?

        Workspaces

105. What is the command state?

        The terraform state command is used for advanced state management. As your Terraform usage becomes more
        advanced, there are some cases where you may need to modify the Terraform state. Rather than modify the
        state directly, the terraform state commands can be used in many cases instead.

      Reference: <a href=https://www.terraform.io/docs/commands/state/index.html target="_blank">https://www.terraform.io/docs/commands/state/index.html</a>

106. What is the command usage?

        terraform state <subcommand> [options] [args]

107. You are working on terraform files and you want to list all the resources. Whatis the command you should use?

        terraform state list

108. How do you list the resources for the given name?

        terraform state list <resource name>

109. What is the command that shows the attributes of a single resource in the statefile?

        terraform state show 'resource name'

110. How do you do debugging terraform?

        Terraform has detailed logs which can be enabled by setting the "TF_LOG" environment variable to any value.

        This will cause detailed logs to appear on stderr.

        You can set "TF_LOG" to one of the log levels TRACE, DEBUG, INFO, WARN or ERROR to change the verbosity of
        the logs. TRACE is the most verbose and it is the default if TF_LOG is set to something other than a log 
        level name.

        To persist logged output you can set TF_LOG_PATH in order to force the log to always be appended to a
        specific file when logging is enabled. Note that even when TF_LOG_PATH is set, TF_LOG must be set in order
        for any logging to be enabled.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/internals/debugging.html>https://www.terraform.io/docs/internals/debugging.html</a>

111. If terraform crashes where should you see the logs?

        crash.log

        If Terraform ever crashes (a "panic" in the Go runtime), it saves a log file with the debug logs from the
        session as well as the panic message and backtrace to crash.log.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/internals/debugging.html > https://www.terraform.io/docs/internals/debugging.html</a>

112. What is the first thing you should do when the terraform crashes?

        panic message

        The most interesting part of a crash log is the panic message itself and the backtrace immediately following.
        So the first thing to do is to search the file for panic.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/internals/debugging.html> https://www.terraform.io/docs/internals/debugging.html</a>

113. You are building infrastructure for different environments for example testand dev. How do you maintain separate states?

        There are two primary methods to separate state between environments:
          directories
          workspaces

114. What is the difference between directory-separated and workspace-separatedenvironments?

        Directory separated environments rely on duplicate Terraform code, which may be useful if your deployments
        need differ, for example to test infrastructure changes in development. But they can run the risk of
        creating drift between the environments over time.

        Workspace-separated environments use the same Terraform code but have different state files, which is useful
        if you want your environments to stay as similar to each other as possible, for example if you are providing
        development infrastructure to a team that wants to simulate running in production.

115. What is the command to pull the remote state?

        terraform state pull

        This command will download the state from its current location and output the raw format to stdout.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/commands/state/pull.html>https://www.terraform.io/docs/commands/state/pull.html</a>

116. What is the command is used manually to upload a local state file to a remotestate

        terraform state push

        The "terraform state push" command is used to manually upload a local state file to remote state. This 
        command also works with local state.
      Reference: <a target="_blank" href=https://www.terraform.io/docs/commands/state/push.html>https://www.terraform.io/docs/commands/state/push.html</a>

117. The command terraform taint modifies the state file and doesn’t modify theinfrastructure. Is this true?

        True

        This command will not modify infrastructure, but does modify the state file in order to mark a resource as
        tainted. Once a resource is marked as tainted, the next plan will show that the resource will be destroyed
        and recreated and the next apply will implement this change.

118. Your team has decided to use terraform in your company and you have existinginfrastructure. How do you migrate your existing resources to terraform and startusing it?

        You should use terraform import and modify the infrastrcuture in the terraform files and do the terraform 
        workflow (init, plan, apply).

119. When you are working with the workspaces how do you access the currentworkspace in the configuration files?

        ${terraform.workspace}

120. When you are using workspaces where does the Terraform save the state file forthe local state?

        terraform.tfstate.d

        For local state, Terraform stores the workspace states in a directory called "terraform.tfstate.d".

121. When you are using workspaces where does the Terraform save the state file forthe remote state?

        For remote state, the workspaces are stored directly in the configured backend.

122. How do you remove items from the Terraform state?

        terraform state rm 'packet_device.worker' 

        The "terraform state rm" command is used to remove items from the Terraform state. This command can remove
        single resources, single instances of a resource, entire modules, and more.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/commands/state/rm.html>https://www.terraform.io/docs/commands/state/rm.html</a>

123. How do you move the state from one source to another?

        terraform state mv 'module.app' 'module.parent.module.app'

        The "terraform state mv" command is used to move items in a Terraform state. This command can move single
        resources, single instances of a resource, entire modules, and more. This command can also move items to
        a completely different state file, enabling efficient refactoring.

      Reference: <a target="_blank" href=https://www.terraform.io/docs/commands/state/mv.html>https://www.terraform.io/docs/commands/state/mv.html</a>

124. How do you rename a resource in the terraform state file?

        terraform state mv 'packet_device.worker' 'packet_device.helper'

        The above example renames the packet_device resource named worker to helper.

125. Where do you find and explore terraform Modules?

        The Terraform Registry makes it simple to find and use modules.

        The search query will look at module name, provider, and description to match your search terms. On the 
        results page, filters can be used further refine search results.

126. How do you make sure that modules have stability and compatibility?

        By default, only verified modules are shown in search results. By using the filters, you can view 
        unverified modules as well.

127. How do you download any modules?

        You need to add any module in the configuration file like below 

        module "consul" {
          source = "hashicorp/consul/aws"
          version = "0.1.0"
        }

        terraform init command will download and cache any modules referenced by a configuration.

128. What is the syntax for referencing a registry module?

        <NAMESPACE>/<NAME>/<PROVIDER>

        // for example

          module "consul" {
            source = "hashicorp/consul/aws"
            version = "0.1.0"
          }

129. What is the syntax for referencing a private registry module?

        <HOSTNAME>/<NAMESPACE>/<NAME>/<PROVIDER>

        // for example

          module "vpc" {
            source = "app.terraform.io/example_corp/vpc/aws"
            version = "0.9.3"
          }

130. The terraform recommends that all modules must follow semantic versioning.Is this true?

        True

131. What is a Terraform Module?

        A Terraform module is a set of Terraform configuration files in a single directory. Even a simple
        configuration consisting of a single directory with one or more ".tf" files is a module.

132. Why do we use modules for?

        * Organize configuration
        * Encapsulate configuration
        * Re-use configuration
        * Provide consistency and ensure best practices

133. How do you call modules in your configuration?

        Your configuration can use module blocks to call modules in other directories.
        When Terraform encounters a module block, it loads and processes that module's configuration files.

134. How many ways you can load modules?

        Local and remote modules

        Modules can either be loaded from the local filesystem, or a remote source.

        Terraform supports a variety of remote sources, including the Terraform Registry, most version control
        systems, HTTP URLs, and Terraform Cloud or Terraform Enterprise private module registries.

135. What are the best practices for using Modules?

        1. Start writing your configuration with modules in mind. Even for modestly complex Terraform configurations
           managed by a single person, you' willll find the benefits of using modules outweigh the time it takes 
           to use them properly.

        2. Use local modules to organize and encapsulate your code. Even if you are not using or publishing remote
           modules, organizing your configuration in terms of modules from the beginning will significantlty reduce
           the burden of maintaining and updating your configuration as your infrastructure grows in complexity.

        3. Use the public Terraform Registry to find useful modules. This way you can more quickly and confidently
           implement your configuration by relying on the work of others to implement common infrastructure scenarios.

        4. Publish and share modules with your team. Most infrastructure is managed by a team of people, and modules
           are important way that teams can work together to create and maintain infrastructure. As mentioned 
           earlier, you can publish modules either publicly or privately. We will see how to do this in a future
           guide in this series.

136. What are the different source types for calling modules?

        Local paths
        Terraform Registry
        GitHub
        Generic Git, Mercurial repositories
        Bitbucket
        HTTP URLs
        S3 buckets
        GCS buckets

      Reference: <a target="_blank" href=https://www.terraform.io/docs/modules/sources.html>https://www.terraform.io/docs/modules/sources.html</a>

137. What are the arguments you need for using modules in your configuration?

        source and version

        // example
          module "consul" {
            source = "hashicorp/consul/aws"
            version = "0.1.0"
          }

138. How do you set input variables for the modules?

        The configuration that calls a module is responsible for setting its input values, which are passed as
        arguments in the module block. Aside from source and version , most of the arguments to a module block
        will set variable values.

        On the Terraform registry page for the AWS VPC module, you will see an Inputs tab that describes all of
        the input variables that module supports.

        For example, we have defined a lot of input variables for the modules such as ads, cidr,name, etc.

        provider "aws" {
          region = "us-west-2"
        }

        module "vpc" {
          source = "terraform-aws-modules/vpc/aws"
          version = "2.21.0"

          name = var.vpc_name
          cidr = var.vpc_cidr

          azs = var.vpc_azs
          private_subnets = var.vpc_private_subnets
          public_subnets = var.vpc_public_subnets
          enable_nat_gateway = var.vpc_enable_nat_gateway
          tags = var.vpc_tags
        }

        module "ec2_instances" {
          source = "terraform-aws-modules/ec2-instance/aws"
          version = "2.12.0"
          name = "my-ec2-cluster"
          instance_count = 2
          ami = "ami-0c5204531f799e0c6"
          instance_type = "t2.micro"
          vpc_security_group_ids = [module.vpc.default_security_group_id]
          subnet_id = module.vpc.public_subnets[0]
          tags = {
            Terraform = "true"
            Environment = "dev"
          }
        }


139. How do you access output variables from the modules?

        You can access them by referring module.<MODULE NAME>.<OUTPUT NAME>

140. Where do you put output variables in the configuration?

        Module outputs are usually either passed to other parts of your configuration, or defined as outputs in
        your root module. You will see both uses in this guide.

        Inside your configuration's directory, outputs.tf will need to contain:

        output "vpc_public_subnets" {
          description = "IDs of the VPC's public subnets"
          value = module.vpc.public_subnets
        }

        output "ec2_instance_public_ips" {
          description = "Public IP addresses of EC2 instances"
          value = module.ec2_instances.public_ip
        }

141. How do you pass input variables in the configuration?

        You can define variables.tf in the root folder

        variable "vpc_name"
        {
          description = "Name of VPC"
          type = string
          default = "example-vpc"
        }

        Then you can access these varibles in the configuration like this

        module "vpc" {
          source = "terraform-aws-modules/vpc/aws"
          version = "2.21.0"

          name = var.vpc_name
          cidr = var.vpc_cidr

          azs = var.vpc_azs
          private_subnets = var.vpc_private_subnets
          public_subnets = var.vpc_public_subnets
          enable_nat_gateway = var.vpc_enable_nat_gateway
          tags = var.vpc_tags
        }

142. What is the child module?

        A module that is called by another configuration is sometimes referred to as a "child module" of that
        configuration.

143. When you use local modules you don’t have to do the command init or get everytime there is a change in the local module. why?

        When installing a local module, Terraform will instead refer directly to the source directory. Because
        of this, Terraform will automatically notice changes to local modules without having to re-run terraform
        init or terraform get.

144. When you use remote modules what should you do if there is a change in themodule?

        When installing a remote module, Terraform will download it into the ".terraform" directory in your
        configuration's root directory. You should initialize with terraform init.

145. A simple configuration consisting of a single directory with one or more .tf filesis a module. Is this true?

        True

146. When using a new module for the first time, you must run either terraforminit or terraform get to install the module. Is this true?

        True

147. When installing the modules and where does the terraform save these modules?

        .terraform/modules

        // Example
        
        .terraform/modules
          ├── ec2_instances
          │    └── terraform-aws-modules-terraform-aws-ec2-instance-ed6dcd9
          ├── modules.json
          └── vpc
               └── terraform-aws-modules-terraform-aws-vpc-2417f60

148. What is the required argument for the module?

        source

        All modules require a source argument, which is a meta-argument defined by Terraform CLI. Its value is
        either the path to a local directory of the module's configuration files, or a remote module source that
        Terraform should download and use. This value must be a literal string with no template sequences; arbitrary
        expressions are not allowed. For more information on possible values for this argument, see Module Sources.

149. What are the other optional meta-arguments along with the source whendefining modules

        version - (Optional) A version constraint string that specifies which versions of the referenced module are
                  acceptable. The newest version matching the constraint will be used. version is supported only
                  for modules retrieved from module registries.

        providers - (Optional) A map whose keys are provider configuration names that are expected by child module
                  and whose values are corresponding provider names in the calling module. This allows provider
                  configurations to be passed explicitly to child modules. If not specified, the child module
                  inherits all of the default (un-aliased) provider configurations from the calling module.

150. What is the Core Terraform workflow?

        The core Terraform workflow has three steps:

        1. Write - Author infrastructure as code.
        2. Plan - Preview changes before applying.
        3. Apply - Provision reproducible infrastructure.

151. What is the workflow when you work as an Individual Practitioner?

        Please check the below URL for detailed workflow: 
      <a target="_blank" href=https://www.terraform.io/intro/core-workflow#working-as-an-individual-practitioner>https://www.terraform.io/intro/core-workflow#working-as-an-individual-practitioner</a>

152. What is the workflow when you work as a team?

        Please check the below URL for detailed workflow:
      <a target="_blank" href=https://www.terraform.io/intro/core-workflow#working-as-a-team>https://www.terraform.io/intro/core-workflow#working-as-a-team</a>

153. What is the workflow when you work as a large organization?

        Please check the below URL for detailed workflow:
      <a target="_blank" href=https://www.terraform.io/intro/core-workflow#the-core-workflow-enhanced-by-terraform-cloud>https://www.terraform.io/intro/core-workflow#the-core-workflow-enhanced-by-terraform-cloud</a>

154. What is the command init?

        The "terraform init" command is used to initialize a working directory containing Terraform configuration
        files. This is the first command that should be run after writing a new Terraform configuration or cloning
        an existing one from version control. It is safe to run this command multiple times.

155. You recently joined a team and you cloned a terraform configuration files fromthe version control system. What is the first command you should use?

        terraform init

        This command performs several different initialization steps in order to prepare a working directory for use.

        This command is always safe to run multiple times, to bring the working directory up to date with changes in
        the configuration. Though subsequent runs may give errors, this command will never delete your existing
        configuration or state. If no arguments are given, the configuration in the current working directory is 
        initialized. It is recommended to run Terraform with the current working directory set to the root directory
        of the configuration, and omit the DIR argument.

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/init.html>https://www.terraform.io/docs/commands/init.html</a>

156. What is the flag you should use to upgrade modules and plugins a part of theirrespective installation steps?

        upgrade
        terraform init -upgrade

157. When you are doing initialization with terraform init, you want to skipbackend initialization. What should you do?

        terraform init -backend=false

158. When you are doing initialization with terraform init, you want to skip childmodule installation. What should you do?

        terraform init -get=false

159. When you are doing initialization where do all the plugins stored?

        On Unix Based operationg systems : ~/.terraform.d/plugins
        on Windows : %APPDATA%\terraform.d\plugins

160. When you are doing initialization with terraform init, you want to skip plugininstallation. What should you do?

        terraform init -get-plugins=false

        Skips plugin installation. Terraform will use plugins installed in the user plugins directory, and any
        plugins already installed for the current working directory. If the installed plugins aren't sufficient
        for the configuration, init fails.

161. What does the command terraform validate does?

        The "terraform validate" command validates the configuration files in a directory, referring only to the
        configuration and not accessing any remote services such as remote state, provider APIs, etc.

        Validate runs checks that verify whether a configuration is syntactically valid and internally consistent,
        regardless of any provided variables or existing state.

        It is thus primarily useful for general verification of reusable modules, including correctness of 
        attribute names and value types.

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/validate.html>https://www.terraform.io/docs/commands/validate.html</a>

162. What does the command plan do?

        The "terraform plan" command is used to create an execution plan. Terraform performs a refresh, unless
        explicitly disabled, and then determines what actions are necessary to achieve the desired state specified
        in the configuration files.

163. What does the command apply do?

        The "terraform apply" command is used to apply the changes required to reach the desired state of the
        configuration, or the pre-determined set of actions generated by a terraform plan execution plan.

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/apply.html >https://www.terraform.io/docs/commands/apply.html</a>

164. You are applying the infrastructure with the command apply and you don’twant to do interactive approval. Which flag should you use?

        terraform apply -auto-approve

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/apply.html>https://www.terraform.io/docs/commands/apply.html</a>

165. What does the command destroy do?

        The "terraform destroy" command is used to destroy the Terraform-managed infrastructure.

166. How do you preview the behavior of the command terraform destroy?

        terraform plan -destroy

167. What are implicit and explicit dependencies?

        Implicit dependency: By studying the resource attributes used in interpolation expressions, Terraform can
          automatically infer when one resource depends on another. Terraform uses this dependency information to
          determine the correct order in which to create the different resources. Implicit dependencies via
          interpolation expressions are the primary way to inform Terraform about these relationships, and should
          be used whenever possible.

        Explicit dependency: Sometimes there are dependencies between resources that are not visible to Terraform.
          The depends_on argument is accepted by any resource and accepts a list of resources to create explicit
          dependencies for.

168. Give an example of implicit dependency?

        In the example below, the reference to aws_instance.example.id creates an implicit dependency on the 
        aws_instance named example.

        provider "aws" {
          profile = "default"
          region = "us-east-1"
        }

        resource "aws_instance" "example" {
          ami = "ami-b374d5a5"
          instance_type = "t2.micro"
        }

        resource "aws_eip" "ip" {
          vpc = true
          instance = aws_instance.example.id
        }

169. Give an example of explicit dependency?

        In the example below, an application we will run on our EC2 instance expects to use a specific Amazon S3
        bucket, but that dependency is configured inside the application code and thus not visible to Terraform.
        In that case, we can use depends_on to explicitly declare the dependency.

        resource "aws_s3_bucket" "example" {
            bucket = "some_bucket"
            acl = "private"
        }

        resource "aws_instance" "example" {
            ami = "ami-2757f631"
            instance_type = "t2.micro"
            depends_on = [aws_s3_bucket.example]
        }

170. How do you save the execution plan?

        terraform plan -out=tfplan
      
        you can use that file with apply:

        terraform apply tfplan

171. You have started writing terraform configuration and you are using somesample configuration as a basis. How do you copy the example configuration intoyour working directory?

        terraform init -from-module=MODULE-SOURCE

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/init.html#copy-a-source-module>https://www.terraform.io/docs/commands/init.html#copy-a-source-module</a>

172. What is the flag you should use with the terraform plan to get detailed on theexit codes?

        terraform plan -detailed-exitcode

        Return a detailed exit code when the command exits. When provided, this argument changes the exit codes and
        their meanings to provide more granular information about what the resulting plan contains:

          * 0 = Succeeded with empty diff (no changes)
          * 1 = Error
          * 2 = Succeeded with non-empty diff (changes present)

173. How do you target only specific resources when you run a terraform plan?

        -target=resource  - A Resource Address to target. This flag can be used multiple times.

174. How do you update the state prior to checking differences when you run aterraform plan?

        terraform plan -refresh=true

175. The behavior of any terraform destroy command can be previewed at any timewith an equivalent terraform plan -destroy command. Is this true?

        True

176. You have the following file and created two resources docker_image anddocker_container with the command terraform apply and you go to the terminaland delete the container with the command docker rm. You come back to yourconfiguration and run the command again. Does terraform recreates the resource?

        resource "docker_image" "nginx" {
          name = "nginx:latest"
          keep_locally = false
        }

        resource "docker_container" "nginx" {
          image = docker_image.nginx.latest
          name = "nginxtutorial"
          ports {
            internal = 80
            external = 8080
          }
          upload {
            source = "${abspath(path.root)}/files/index.html"
            file = "/usr/share/nginx/html/index.html"
          }
        }

        Yes. Terrsform creates the resource again since the execution plan says two resources and the terraform
        always maintains the desired state.

177. You created a VM instance on AWS cloud provider with the terraformconfiguration and you log in AWS console and removed the instance. What does thenext apply do?

        It creates the instance again.

178. You have the following file and created two resources docker_image anddocker_container with the command terraform plan and you go to the terminal anddelete the container with the command docker rm. You come back to yourconfiguration and run the command again. What is the output of the commandplan?

        resource "docker_image" "nginx" {
          name = "nginx:latest"
          keep_locally = false
        }

        resource "docker_container" "nginx" {
          image = docker_image.nginx.latest
          name = "nginxtutorial"
          ports {
            internal = 80
            external = 8080
          }

          upload {
            source = "${abspath(path.root)}/files/index.html"
            file = "/usr/share/nginx/html/index.html"
          }
        }

        Terraform will perform the following actions:

          # docker_container.nginx will be created
          Plan: 1 to add, 0 to change, 0 to destroy.

---

[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](terraform_interview_question-3.md)

---
<br>
<br>
{!footer.md!}
