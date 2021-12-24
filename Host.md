Host is used for a few thing but the biggest advantage is the nameserver capabilities. 

	host -t ns <domainname>
	host -l will list for zone tranfers.

Too look information about a domain you can use:

	host -t nc <domain name>

The -t is the type mx would be for mail servers
A host without a type will return the ip address

Return to [[README]]