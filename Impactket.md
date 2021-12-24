Sectretsdump is used to get the hash from the SAM / SYSTEM files on widows based systems. This is a post exploit local exploit that can be used get the users and password after downloading the sam and system files to your local computer. 

impacket has several tools which should already be installed on your kali machine. 

Usage:

	secretsdump.py -sam SAM -system SYSTEM local

To install you will need to go to the git hub site and clone the directory form tehere you will need to install all f the packages. 

	cd ~/toolbox/scripts
	git clone https://github.com/SecureAuthCorp/impacket.git
	cd impactket
	pip install -r requirements.txt
	python3 -m pip install .
	
For lots of information on everything in impactket you can visit https://www.secureauth.com/labs/open-source-tools/impacket/ 

Return to [[README]]
	
	
	