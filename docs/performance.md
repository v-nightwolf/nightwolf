## System Performance 
* `Definition: `
  System performance is a measure of the amount of useful work done by a System in a time range. 

* `OS/CPU Load: ` The average amount of processes using or waiting for CPU allocation over a period of time.

Usually System Performance issues can be identified by observing slowness in services offered by OS and it mostly happen due to any of the below reasons. 

        - high CPU Usage 
    	- high Memory Usage
    	- high Disk IO Usage
    	- Network Performance Issues
    	- Software Bugs like memory leaks, Kernel bugs etc. 

We will try to break your investigation steps into major bullet points and helps you to find the root causes of the issue. 

## Tools helpful in your investigation: 
![!image](img/TroubleShooting.jpg)

  - <a href="https://linux.die.net/man/1/top" target="_blank">top</a>
  - <a href="https://linux.die.net/man/1/mpstat" target="_blank">mpstat</a>
  - <a href="https://linux.die.net/man/1/sar" target="_blank">sar</a>
  - <a href="https://linux.die.net/man/1/free" target="_blank">free</a>
  - <a href="https://linux.die.net/man/1/strace" target="_blank">strace</a>
  - <a href="https://linux.die.net/man/1/iotop" target="_blank">iotop</a>
  - <a href="https://www.thegeekstuff.com/2011/07/iostat-vmstat-mpstat-examples/" target="_blank">iostat</a>
  - <a href="https://tldp.org/LDP/nag2/x-087-2-iface.netstat.html" target="_blank">netstat</a>
  - <a href="https://www.thegeekstuff.com/2014/11/pidstat-examples/" target="_blank">pidstat</a>
  - <a href="https://www.thegeekstuff.com/2011/07/iostat-vmstat-mpstat-examples/" target="_blank">vmstat</a>
  - <a href="https://www.tcpdump.org/manpages/tcpdump.1.html" target="_blank">tcpdump</a>
  - <a href="http://iptraf.seul.org/about.html" target="_blank">iptraf</a>
  - <a href="https://git.kernel.org/pub/scm/linux/kernel/git/axboe/blktrace.git/tree/README" target="_blank">blktrace</a>
  - <a href="https://www.tecmint.com/10-lsof-command-examples-in-linux/" target="_blank">lsof</a>
  - <a href="https://www.networkworld.com/article/3633889/looking-at-your-linux-systems-network-interface-with-ethtool.html" target="_blank">ethtool</a>

<br>
You can install these tools  very easily using below command:

`      yum install -y  sysstat iptraf tcpdump procps-ng net-tools strace iotop ethtool blktrace       `

<br>

#### You can start your investigation by executing small script, which will gather a lot of system stats for you:
	
	
	bash <(curl -s https://raw.githubusercontent.com/v-nightwolf/nightwolf/main/server_stats.sh)

The output of above script will look like this: 

	############################################

	Server Uptime: 1days 6:43:23

	Load Average: Current 0.26
	Load Average: 15min Average 0.26

	#### Printing CPU stats: ####
	01:15:26 PM  CPU    %usr   %nice    %sys %iowait    %irq   %soft  %steal  %guest  %gnice   %idle
	01:15:26 PM  all    1.47    0.00    0.48    0.02    0.00    0.12    0.00    0.00    0.00   97.91


	###RAM usage###
	Free Ram: 569.93MB
	Used RAM: 3171.23MB

	15% ram left
	RAM ALERT: Low! 

	TOP RAM CONSUMER: /opt/mongodb/mms/jdk/bin/mms-app
	RAM Usage (RSS): 1857.43 MB
	Total Number of RAM Processes: 2
	Total RAM Usage for all /opt/mongodb/mms/jdk/bin/mms-app processes =  2287.56 MB
	61.15% used by /opt/mongodb/mms/jdk/bin/mms-app


	###CPU usage###
	Top Process:  /opt/mongodb/mms/jdk/bin/mms-app
	CPU % for SINGLE Top Process =  4.2
	number of processes this is running: 2
	Total CPU % for /opt/mongodb/mms/jdk/bin/mms-app =  4.8

	############################################

## Perfomance isssues due to high CPU Usage


       As a default, percentages for these individual categories are displayed.  Where two labels are shown below, those for more recent kernel versions are shown first.
           us, user    : time running un-niced user processes
           sy, system  : time running kernel processes
           ni, nice    : time running niced user processes
           id, idle    : time spent in the kernel idle handler
           wa, IO-wait : time waiting for I/O completion
           hi : time spent servicing hardware interrupts
           si : time spent servicing software interrupts
           st : time stolen from this vm by the hypervisor
    

## Performance issues due to high Memory Usage

## Performance issues due to high Disk IO Usage

## Network Performance Issues
