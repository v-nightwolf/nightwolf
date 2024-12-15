# Ansible Interview Questions 

<br>
  We have prepared a set of frequently asked  Ansible questions to help Freshers and Experienced Admins in their preparations for Interview.

  You will find these questions very helpful in your Linux/Ansible/DevOps Admins interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.
 {!inpage-ads.md!}
---

1. What is Ansible architecture ?

2. How a normal yaml file is different from Ansible playbook ?

3. What is Ansible playbook, define all terms in playbook ?

4. What is handlers and notifiers ?

5. What are resgisters ?

6. What are various modules you have used in Ansible ?

7. How to used when condition and loops in Ansible ?

8. Write a playbook to start a service, stop a service and check the health check of service.

9. What are Ansible adhoc commands ?

10. What are roles and tell where you will keep the diffrenet files in diffrenet folders ?

11. What is Ansible vault and how you store the secret files ?

12. How the SSH connectivity takes place between two server in Ansible ?

13. What is different between Puppet and Ansible ?

14. How can I set the PATH or any other environment variable for a task or entire play ?

        Setting environment variables can be done with the environment keyword. It can be used at the task or other
        levels in the play.


15. How do I handle different machines needing different user accounts or ports to log in with ?

        Setting inventory variables in the inventory file is the easiest way.

        For instance, suppose these hosts have different usernames and ports:

        [webservers]
        test.nightwolf.in  ansible_port=5000   ansible_user=nightwolf
        foo.nightwolf.in   ansible_port=5001   ansible_user=bar


16. How do I get ansible to reuse connections, enable Kerberized SSH, or have Ansible pay attention to my local SSH config file ?

        Switch your default connection type in the configuration file to ssh, or use -c ssh to use Native OpenSSH
        for connections instead of the python paramiko library. In Ansible 1.2.1 and later, ssh will be used by
        default if OpenSSH is new enough to support ControlPersist as an option.

        Paramiko is great for starting out, but the OpenSSH type offers many advanced options. You will want to run
        Ansible from a machine new enough to support ControlPersist, if you are using this connection type. You can
        still manage older clients. If you are using RHEL 6, CentOS 6, SLES 10 or SLES 11 the version of OpenSSH is
        still a bit old, so consider managing from a Fedora or openSUSE client even though you are managing older
        nodes, or just use paramiko.

17. How do I get Ansible to notice a dead target in a timely manner ?

        You can add -o ServerAliveInterval=NumberOfSeconds in ssh_args from ansible.cfg. Without this option, SSH
        and therefore Ansible will wait until the TCP connection times out. Another solution is to add
        ServerAliveInterval into your global SSH configuration. A good value for ServerAliveInterval is up to you
        to decide; keep in mind that ServerAliveCountMax=3 is the SSH default so any value you set will be tripled
        before terminating the SSH session.

18. How do I see a list of all of the ansible_ variables ?

        Ansible by default gathers “facts” about the machines under management, and these facts can be accessed in
        playbooks and in templates. To see a list of all of the facts that are available about a machine, you can
        run the setup module as an ad hoc action:

        ansible -m setup hostname

        This will print out a dictionary of all of the facts that are available for that particular host. You might
        want to pipe the output to a pager.This does NOT include inventory variables or internal ‘magic’ variables.

19. How do I see all the inventory variables defined for my host? 

        By running the following command, you can see inventory variables for a host:

        ansible-inventory --list --yaml

20. How do I see all the variables specific to my host ?

        To see all host specific variables, which might include facts and other sources:

        ansible -m debug -a "var=hostvars['hostname']" localhost

        Unless you are using a fact cache, you normally need to use a play that gathers facts first, for facts
        included in the task above.

 
21. How do I loop over a list of hosts in a group, inside of a template ?

22. How do I access a variable name programmatically ?

        An example may come up where we need to get the ipv4 address of an arbitrary interface, where the interface
        to be used may be supplied via a role parameter or other input. Variable names can be built by adding
        strings together using “~”, like so:

          {{ hostvars[inventory_hostname]['ansible_' ~ which_interface]['ipv4']['address'] }}

        The trick about going through hostvars is necessary because it’s a dictionary of the entire namespace of
        variables. inventory_hostname is a magic variable that indicates the current host you are looping over in
        the host loop.

        In the example above, if your interface names have dashes, you must replace them with underscores:

          {{ hostvars[inventory_hostname]['ansible_' ~ which_interface | replace('_', '-') ]['ipv4']['address'] }}

23. How do I access shell environment variables ? 

        On controller machine : Access existing variables from controller use the env lookup plugin. For example,
        to access the value of the HOME environment variable on the management machine:

          ---
          # ...
            vars:
               local_home: "{{ lookup('env','HOME') }}"

        On target machines : Environment variables are available via facts in the ansible_env variable:

            {{ ansible_env.HOME }}

24. How do I generate encrypted passwords for the user module ?

        Ansible ad hoc command is the easiest option:

          ansible all -i localhost, -m debug -a "msg={{ 'mypassword' | password_hash('sha512', 'mysecretsalt') }}"

        The mkpasswd utility that is available on most Linux systems is also a great option:

          mkpasswd --method=sha-512

25. How do I get the original ansible_host when I delegate a task ?

        As the documentation states, connection variables are taken from the delegate_to host so ansible_host is
        overwritten, but you can still access the original via hostvars:

          original_host: "{{ hostvars[inventory_hostname]['ansible_host'] }}"

        This works for all overridden connection variables, like ansible_user, ansible_port, and so on.


<br>
<br>
<br>
---
<br>
{!footer.md!}
