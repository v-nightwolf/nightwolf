## OS Networking Interview Questions
`General questions about basic Networking + OS Networking + Troubleshooting.
`	

 {!inpage-ads.md!}

	1.  How to check if you are receiving connection timeouts when trying to connect to a server. 

	2.  In what condition you will receive connection refused. Hint: 1. if packets are rejected using 
	    firewall/iptables action "REJECT" 2. If service is not responding or is down. 

	3.  what will you do/check if customer calls and tells you that there is packet drop when he is trying 
	    to access a remote server.

	4.  How will you troubleshoot packet drops?

	5.  What is TCP re-transmissions ?

	6.  What if there are no Packet drops/loss and high TCP re-transmissions on server. How will this impact 
	    server/services ?

	7.  What tools can be used to check bandwidth usage between  2 servers/devices.  

	8.  When you poweron a laptop, how does it receives IP every time. Explain the process. 

	9.  What if dhcp lease is over, will IP/connection drop from server. 

	10. What is APIPA. In what case Server gets APIPA ip? Hint: When server is configured to receive IP from DHCP 
	    and there is no DHCP in that network. 

	11. What happens in backend why you type google.com in browser and hit enter. 

	12. Explain recursive and Iterative DNS queries. 

	13. What can be the reason for receiving Request time outs when trying to resolve rackspace.com.

	14. What are HOPs in network. 
	    In a packet-switching network, a hop is the trip a data packet takes from one router or intermediate point 
	    to another in the network. On the Internet (or a network that uses TCP/IP), the number of hops a packet has 
	    taken toward its destination (called the "hop count") is kept in the packet header. A packet with an exceedingly 
	    large hop count is discarded.

	15. what is Apache 500 status code (Internel server error) and how to troubleshoot the 500 status code issue. 
	
	16. DNS working flow? What happens when we hit www.google.com in browser? 
	
	17. What is recursive and iterative query? 

	18. What are the dns records? Explain each and every record? 
	
	19.  What is difference between below 3 domains 
		www.google.com 
		Google.com 
		www.google.com. 

	20. What is the DORA process ? 

{!horizontal-ads.md!}
	
	21. TCP 3 way handshaking and 4 way termination? 
	
	22. SSL/TLS 4 way hand shaking? 
	
	23. How to check TCP buffer size in Linux system? 
	
	24. How to check packet drops in Linux? 
	
	25. Explain the OSI model and working of each and every layer. 
	
	26. Difference between TCP and UDP protocol. 
	
	27. Why we have only 13 DNS server in the world? 
	
	28. A customer complains of website slowness, what will be your troubleshooting approach in network prospective? 
	
	29. Difference between Router and switch ? 
	
	30. What configuration happens on switch and router? 
	
	31. What happens when you open a website in browser? 
	
	32. How does a client gets connected to Wifi? or What happens in the backend when client connects to wifi? 

	33. Remove session layer from the picture and now consider running traceroute on 2 CMD terminals. How does
	    the request differ on both CMD terminals? 
	
	34. Can sequence number be duplicate in TCP/IP? 
	 
	35. How many traceroute hops will be there when you run traceroute from server A to Server B 
		Server A --> Switch A --> Router R1 --> Router R2 --> Switch B --> Server B 
	
	36. Please explain a recent issue that you experienced in your environment and your learning associated with it. 

{!horizontal-ads.md!}

##Questions from Github
A lot more Questions from <a href="https://github.com/v-nightwolf/nightwolf-cotribution/blob/main/network.md" target="_blank">nightwolf-cotribution github repo</a>


     1. What is localhost and why would ping localhost fail?

     2. What is the similarity between "ping" & "traceroute" ? How is traceroute able to find the hops.

     3. What is the command used to show all open ports and/or socket connections on a machine?

     4. Is 300.168.0.123 a valid IPv4 address?

     5. Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?

     6. What is a VLAN?

     7. What is ARP and what is it used for?

     8. What is the difference between TCP and UDP?

     9. What is the purpose of a default gateway?

    10. What is command used to show the routing table on a Linux box?

    11. A TCP connection on a network can be uniquely defined by 4 things. What are those things?

    12. When a client running a web browser connects to a web server, what is the source port and what is the 
        destination port of the connection?

    13. How do you add an IPv6 address to a specific interface?

    14. You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping 
        to the v6 address gives you the response sendmsg: operation not permitted. What could be wrong?

    15. What is SNAT and when should it be used?

    16. Explain how could you ssh login into a Linux system that DROPs all new incoming packets using a SSH tunnel.

    17. How do you stop a DDoS attack?

    18. How can you see content of an ip packet?

    19. What is IPoAC (RFC 1149)?

    20. What will happen when you bind port 0?

    21. Customer changes an A record in their DNS control panel but calls us because they're still seeing the old version 
        of their web site. How would you troubleshoot? 

    22. I type "ping nightwolf.in" at a command-line. What things does the Linux OS do to turn "nightwolf.in" into an IP address? 
        Hints =>
        a). /etc/hosts - used in name resolution whenever the files source is being defined in the hosts database 
        b). nameserver – IP (IPv4 or IPv6) of the server that will resolve the queries 
        c). /etc/resolv.conf - used by the libresolv library that's used by the libnss_dns library, this is when the 
        source used is DNS. 

    23. Can you still SSH to a Linux server if its default gateway is set incorrectly? How? 
        Hints =>  
        a). You can SSH in, but only from another device in the same subnet, or in a network to which the "broken" 
            server has a static route defined. 
        b).some static route is there which can route to destination network.

    24. Two servers behind the same firewall are able to communicate by their private IPs, but not via FQDN. 
        What might be causing this, and what can be done to fix it?
        Hints =>
        a). The FQDNs are resolving to public IPs, and public IPs are unrouteable within the private network behind 
            the firewall.
        b). Edit /etc/hosts on the all servers behind the firewall to override DNS to point to private IP.
        c). The "best" fix would be to enable DNS doctoring/translation at the firewall.

{!horizontal-ads.md!}

    25. What are the pros/cons of Load Balancer Health checks?
       
    26. What is persistence (ie: sticky sessions), and what are the pros and cons of it?
        Hint =>
        Persistence: If source X went to node Y within the past Z minutes, bypass all balancing algorithms and
        send directly to node Y again.

        Pros:
        • Avoids the breakage of per-node session information (ie: /var/lib/php/session files). Shopping
          carts, active logins, etc.
        Cons:
        • In general, persistence can lead to some imbalance of active sessions between nodes. If a node
          is temporarily unavailable (ie: rebooted), all active sessions become persistent to the remaining
          node(s).
        • With LeastConnections, this means the recovering node takes all new sessions, and is potentially 
          overloaded until sessions equalize.
        • With RoundRobin, this means the recovering node has significantly fewer sessions than the others 
          for quite a while.
        • If one connection is causing a large load, that load is not balanced - persistence keeps it all on
          one node. 

---
<br>
{!footer.md!}
