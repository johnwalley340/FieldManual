Okay so gobuster has now become much more compliacted and yet more powerful. Version 3.0 on on are now compiled via the go compiler. ti install this means you will need ot actuall install bot teh compiler and the program itself. This also mean you will need ot play with the path a bit to make sure you can run the program from anywaywhere. 

installing go. First vist the website https://go.dev/doc/install and download the most recent package. 

after you download you want to change dir3ctories to downloads and run the folling command:

	
	 tar -C /home/jwalley/toolbox/scripts/ -xzf go1.17.5.linux-amd64.tar.gz
	 
For later versions than above simply replace the file name for hte latest version. The above command will extract teh go complier into the scripts directory. Next you will need to modify the path to inclide the go binanaries so they can be run from anywhere. 

	export PATH=$PATH:/home/jwalley/toolbox/scripts/go/bin

You should be ready. you can test this with the following command. 

	go version
	
to install go buster you will want to clone the directory into the toolbox scripts folder. 

	cd ~/toolbox/scripts
	git clone https://github.com/OJ/gobuster.git
	
Once downloaded the the gobuster directory is completed you can make the linux binary

	cd ~/toolbox/scripts/gobuster
	make linux

the Binary is now in the build folder. To make sure you can run the command from anywhere you will need to modify the PATH. 

	export PATH=$PATH:/home/jwalley/toolbox/scripts/gobuster/build/gobuster-linux-amd64

you can test the path by typiing gobuster:

	gobuster

Now that the progrm is now install you you should know this isby for my favorite web directory fuzzing app. 

Since a recent update now you have to tell the app you want to look for directories with the dir extension: gobuster dir

-u URL
-w Wordlist
-x extentions such as txt, php, html, etc.
-f to ignore certificate errors

![[Screenshot from 2021-12-19 14-25-03.png]]

You can install gobuster using the apt install manager. 

	sudo apt install gobuster
	
Return to [[README]]
	


