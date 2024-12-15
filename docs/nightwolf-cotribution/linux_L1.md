# Linux Admin Interview Questions and Answers for Freshers and Experienced - Solved 

<br>
  We have prepared a set of questions to help Freshers and Experienced Linux Admins in their preparations for Interview.
  This list includes Google interview questions for Linux (Infrastructure specialist), Amazon interview questions for Linux (Cloud Support Engineer - II) and other reputed firms as well. 
  You will find these questions very helpful in your Linux Admins interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

    	1. What did you learn yesterday/this week?

    	2. Describe the general file system hierarchy of a Linux system.

    	3. What is the name and the UID of the administrator user in Linux/Unix?
	    Hint => 
			name of user is root and uid is 1.

    	4. How to list all files, including hidden ones, in a directory?

    	5. What is the Unix/Linux command to remove a directory and its contents?
	    Hint => 
			rm -rf DIR_NAME

    	6. Which command will show you free/used memory? Does free memory exist on Linux?
		Hint => 
			free -m
	
    	7. How to search for the string "my konfu is the best" in files of a directory recursively?
		Hint =>
			grep -rin "my konfu is the best" DIR_NAME

    	8. How to connect to a remote server or what is SSH?	
		Hint =>
			We can use ssh command to connect to remote server. 
			command : ssh USER@10.0.0.1	

    	9. How to get all environment variables and how can you use them?
		Hint => 
			env command print all the environment variables associated with user.

    	10. I get "command not found" when I run ifconfig -a. What can be wrong?
		Hint =>
			a). Either ifconfig command binary is not present in /usr/sbin/ or /sbin.
			b). Or PATH environment for user variable do not have /usr/sbin/ and /sbin paths.

    	11. What happens if I type TAB-TAB?
	
    	12. What command will show the available disk space on the Unix/Linux system?
		Hint =>
			df -h 

    	13. What commands do you know that can be used to check DNS records?
		Hint =>
			a) nslookup
			b) dig
			c) host

    	14. What Unix/Linux commands will alter a files ownership, files permissions?
		Hint =>
			a) To change file ownership: chown
			b) To change file permissions: chmod

    	15. What does chmod +x FILENAME do?
		Hint =>
			It will provide shell executable permissions for FILENAME to everybody.

    	16. What does the permission 0750 on a file mean?

    	17. What does the permission 0750 on a directory mean?

    	18. How to add a new system user without login permissions?
		Hint =>
			useradd -s /sbin/nologin tony
			OR
			useradd -M tony
			usermod -L tony

    	19. How to add/remove a group from a user?
		Hint =>
			# gpasswd -d user_name group_name

    	20. What is a bash alias?
		Hint =>
			An alias is a (usually short) name that the shell translates into another (usually longer) name or 
			command. Aliases allow you to define new commands by substituting a string for the first token of a
			simple command

    	21. How do you set the mail address of the root/a user?
		Hint =>
			The system administrator can define email aliases in the file /etc/aliases. This file contains lines
			like root: cwd@mailhost.example.com, /root/mailbox; the effect is the same as having 
                        cwd@mailhost.example.com, root/mailbox in ~root/.forward. You may need to run a program 
                        such as newaliases after changing /etc/aliases.

    	22. What does CTRL-c do?
		Hint => 
			It sends the SIGINT signal to the process, which is technically just a request—most processes will honor
			it, but some may ignore it. 

    	23. What does CTRL-d do?
		Hint => 
			Close the bash shell. This sends an EOF (End-of-file) marker to bash, and bash exits.

    	24. What does CTRL-z do?
		Hint =>
			Suspend the current foreground process running in bash. This sends the SIGTSTP signal to the process.
			To return the process to the foreground later, use the fg process_name command.

    	25. What is in /etc/services?
		Hint =>
			/etc/services contains port number mapping with service name.

    	26. How to redirect STDOUT and STDERR in bash? 
		Hint => 
			a) for all output : &> /dev/null
			b) To redirect the standard error (stderr): 2> /dev/null
			c) To redirect the standard output(stdout): 1> /dev/null

 {!inpage-ads.md!}

    	27. What is the difference between UNIX and Linux.

    	28. What is the difference between Telnet and SSH?

    	29. Which difference have between public and private SSH keys?

    	30. Explain the three load averages and what do they indicate. What command can be used to view 
            the load averages?

    	31. Can you name a lower-case letter that is not a valid option for GNU ls?

    	32. What is a Linux kernel module?

    	33. Walk me through the steps in booting into single user mode to troubleshoot a problem.

    	34. Walk me through the steps you'd take to troubleshoot a 404 error on a web application you administer.

    	35. What is ICMP protocol? Why do you need to use?

    	36. What do the following commands do and how would you use them?
                tee
                awk
                tr
                cut
                tac
                curl
                wget
                watch
                head
                tail
                less
                cat
                touch
                sar
                netstat
                tcpdump
                lsof

    	37. What does an & after a command do?

    	38. What does & disown after a command do?

    	39. What is a packet filter and how does it work?

    	40. What is Virtual Memory?

    	41. What is swap and what is it used for?

    	42. What is an A record, an NS record, a PTR record, a CNAME record, an MX record?

    	43. Are there any other RRs and what are they used for?

    	44. What is a Split-Horizon DNS?

    	45. What is the sticky bit?

    	46. What does the immutable bit do to a file?

    	47. What is the difference between hardlinks and symlinks? What happens when you remove the source to 
            a symlink/hardlink?

    	48. What is an inode and what fields are stored in an inode?

    	49. How to force/trigger a file system check on next reboot?

    	50. What is SNMP and what is it used for?

 {!inpage-ads.md!}

    	51. What is a runlevel and how to get the current runlevel?

    	52. What is SSH port forwarding?

    	53. What is the difference between local and remote port forwarding?

    	54. What are the steps to add a user to a system without using useradd/adduser?

    	55. What is MAJOR and MINOR numbers of special files?

    	56. Describe the mknod command and when you would use it.

    	57. Describe a scenario when you get a "filesystem is full" error, but "df" shows there is free space.

    	58. Describe a scenario when deleting a file, but "df" not showing the space being freed.


        59. What is default signal sent by KILL command ?
            Hint =>
                        a). singnal 15 (SIGTERM) is sent by default if you do not specify the signal type.

        60. Different types of file systems?
            Hint =>
                        ext2, ext3, ext4, xfs, vfat etc.

        61. Difference between ext4 and xfs?

        62. When v create user which files are referred?

        63. Differnce between passwd and shadow file?
            Hint =>
                        /etc/passwd contains details abou User like home directory, shell etc.
                        /etc/shadow conatains User password hashes.

        64. What are the contents in passwd file?
            Hint =>
                        root:x:0:0:root:/root:/bin/bash

                       •   login name
                       •   optional encrypted password
                       •   numerical user ID
                       •   numerical group ID
                       •   user name or comment field
                       •   user home directory
                       •   optional user command interpreter

        65. List all users who are not given passwd? with cmd
            Hint =>
                        cat /etc/shadow| awk -F ":" '$2 ~ /[a-z]/ {print $1}'

        66. How to check what processess are running on which port?
            Hint =>
                        Using "netstat" and "ss" command we can relate processes with port.

        67. How to extend partition in lvm? and indepth questions in lvm ?
            Hint =>
                        1. First attach extra storage/disk to server.
                        2. Create a new partition on the disk using "fdisk" or "parted" command.
                        3. Create a new Physical Volume(PV) on that new partition. e.g. "pvcreate /dev/sdb1"
                        4. Exetend existing Volume Group(VG) using new PV. e.g. "vgextend vg_name /dev/sdb1"
                        5. Now extend the LV. e.g . "lvextend -l 100%FREE /dev/mapper/vg_name-lv_name"
                        6. now execute "resize2fs" or "xfs_growfs".

        68. What is tcpwrappers?
            Hint =>
                        tcpwrappers is a host based Network Access Control List, by which we can allow or deny
                        a host or subnetwork IP addresses,

     	69. What function does DNS play on a network?

        70. On which port dns works?
            Hint =>
                        DNS works on port 53.

        71. What is HTTP?

        72. What is an HTTP proxy and how does it work?

        73. Describe briefly how HTTPS works.

        74. What is SMTP? Give the basic scenario of how a mail message is delivered via SMTP.

        75. What is RAID? What is RAID0, RAID1, RAID5, RAID10?

        76. What is a level 0 backup? What is an incremental backup?

---
[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](linux_L2.md)


 {!inpage-ads.md!}

---
<br>
{!footer.md!}
