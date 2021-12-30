Okay so gobuster has now become much more compliacted and yet more powerful. Version 3.0 on on are now compiled via the go compiler. ti install this means you will need ot actuall install bot teh compiler and the program itself. This also mean you will need ot play with the path a bit to make sure you can run the program from anywaywhere. 


To install go buster you will want to clone the directory into the toolbox scripts folder. 

	cd ~/toolbox/scripts
	git clone https://github.com/OJ/gobuster.git
	
Once downloaded the the gobuster directory is completed you can make the linux binary. Important: You have to have Go installed

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

	
Return to [[README]]
	


