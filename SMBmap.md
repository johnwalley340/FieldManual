## SMBMap
This is great for seeing permissions!

Note this will attempt to create a file on the remote system. You may not be able to delete this file and will leave a fingerprint of your attack. Only use this if you can clean up behind yourself or if you don't mind getting caught. (Pentesting)

Usage:

	smbmap -u <user> -p <password or hash> -H <host IP>