## SUID
SUID bits can be dangerous, some binaries such as passwd need to be run with elevated privileges (as its resetting your password on the system), however other custom files could that have the SUID bit can lead to all sorts of issues.

To search the a system for these type of files run the following: 

	find / -perm -u=s -type f 2>/dev/null
	
See the [[Find]] section for more information on find