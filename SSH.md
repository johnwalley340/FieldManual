## ssh
I know it funny to have something like ssh as an entry BUT there is a good reason for it. ssh can go well beyond the typical remote connection to a system in its native form. 

##### Algorithms

On occasion you may receive an error in ssh stating that no matching key exchange method found. You should get a list of what is offered to change this in ssh do the following:

	ssh -oKexAlgorithms=+<supported agorythem form list>  user@legacyhost
   
##### SOCKS Proxy

ssh -D will create a dynamic port to proxy your ssh traffic.
  
	ssh -d<port> <owned target> will set up a listner once occnected. 

to further investigate netstat -plant will show box listening on the port and will be forwarded to the owned target as a proxy. This can be used in Burp or via commandline via proxy chains

The conf. for proxychains is /etc/proxychains.conf

>Socks 5= ssh
Socks 4= metasploit

Return to [[README]]