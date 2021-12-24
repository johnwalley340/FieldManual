 I used to write script for doing a ping sweep across a network segment. However I recently found a program called fping. This took away the need for a script. To ping a full network segment sue the following:

	fping -a -r 0 -g 10.1.0.0/24 2> /dev/null
	
Return to [[README]]

