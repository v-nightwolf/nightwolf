## MySql Tuner

Below script can help you in tunning your MYSQL database for best performance. Please note that do not blindly trust what this script says. Always think before you impliment the recommendations.  
 
	wget https://raw.github.com/major/MySQLTuner-perl/master/mysqltuner.pl; chmod +x mysqltuner.pl; ./mysqltuner.pl

The output of this script will look like:

	
	[root@linux~]# ./mysqltuner.pl
 
	 >>  MySQLTuner 1.4.0 - Major Hayden <major@mhtx.net>
	 >>  Bug reports, feature requests, and downloads at http://mysqltuner.com/
	 >>  Run with '--help' for additional options and output filtering
	[OK] Currently running supported MySQL version 5.1.73
	[OK] Operating on 64-bit architecture
	 
	-------- Storage Engine Statistics -------------------------------------------
	[--] Status: +CSV +InnoDB +MRG_MYISAM
	[!!] InnoDB is enabled but isn't being used
	[OK] Total fragmented tables: 0
 	
	-------- Security Recommendations  -------------------------------------------
	[!!] User '@bash-test' has no password set.
	[!!] User '@localhost' has no password set.
 	
	-------- Performance Metrics -------------------------------------------------
	[--] Up for: 44m 11s (13 q [0.005 qps], 7 conn, TX: 16K, RX: 662)
	[--] Reads / Writes: 100% / 0%
	[--] Total buffers: 34.0M global + 2.7M per thread (1000 max threads)
	[!!] Maximum possible memory usage: 2.7G (280% of installed RAM)
	[OK] Slow queries: 0% (0/13)
	[OK] Highest usage of available connections: 0% (1/1000)
	[OK] Key buffer size / total MyISAM indexes: 8.0M/90.0K
	[!!] Query cache is disabled
	[OK] Temporary tables created on disk: 0% (0 on disk / 3 total)
	[!!] Thread cache is disabled
	[OK] Table cache hit rate: 53% (8 open / 15 opened)
	[OK] Open file limit used: 0% (16/5K)
	[OK] Table locks acquired immediately: 100% (18 immediate / 18 locks)
	 
	-------- Recommendations -----------------------------------------------------
	General recommendations:
	    Add skip-innodb to MySQL configuration to disable InnoDB
	    MySQL started within last 24 hours - recommendations may be inaccurate
	    Reduce your overall MySQL memory footprint for system stability
	    Enable the slow query log to troubleshoot bad queries
	    Set thread_cache_size to 4 as a starting value
	Variables to adjust:
	  *** MySQL's maximum memory usage is dangerously high ***
	  *** Add RAM before increasing MySQL buffer variables ***
	    query_cache_size (>= 8M)
	    thread_cache_size (start at 4)
