Wordlists are critical to brute force techniques from cracking zip file to websites directory traversal. I use one main source for wordlists outside of these that are customer to a project. 

Most programs look under /usr/share/wordlists. You can do this but I like mine to stay under toolbox/scripts/wordlsits. 

To install your wordlists you will need to clone a key repository on github. First you will need to change directories to the ~/toolbox/scripts folder and clone the directory

	cd ~/toolbox/scripts
	git clone https://github.com/danielmiessler/SecLists.git

After cloning the directory I also untar the rockyou.txt file

	tar xvf ./SecLists/Passwords/Leaked-Databases/rockyou.txt.tar.gz

Return to [[README]]