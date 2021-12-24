## SMBClient

You can get a list o shares on a box running smb by typing

	smbclient -L //<ip address>

To mount shared drives you can type:

	mount -t cifs <//target IP address/ShareName> <place you want to mount locally>