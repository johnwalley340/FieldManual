# Custom Ubuntu Build
I used to like Kali and the desktop but Ubuntu is so much more compliant than Kali and many more program function properly. You can download at : 
https://ubuntu.com/download/desktop

## Update and Upgrade
let make sure the system is all up to date before we do anything else. Don't forget to reboot after the upgrade just in case you downloaded a new kernel.

	sudo apt update && apt upgrade
	sudo reboot

## Obsidian

I have been a long term believer in Zim and I like it but crossing platforms has been difficult. I wanted something I could use daily for all note taking not just for my filed manual. I think Obsidian is the answer. It works on GitHb wiki, normal markdown and atom. Having the normal markdown language is a huge win and the linking is a plus for sure. 

To install obsidian you will need to go to the website located at https://obsidian.md/ and download the right version for the OS. Obsidian works on all platforms which was another plus for and the main reason for choosing to move away from zim. 

For Linux snap is the best way to install. after the download is compete use the following command pointed to the downloaded snap file.

	sudo snap install --dangerous obsidian_0.7.3_amd64.snap


## Chrome
Download chrome: https://www.google.com/chrome/ and install

	sudo apt install ~/Downloads/google-chrome-stable_current_amd64.deb 

## Lastpass
Add last pass extensions to Firefox

## Foxy Pro
Add the Foxy Pro to Firefox 
Set up options for Burp Suit
* Name: BURP
* Address: 127.0.0.1
* Port: 8080


## VIM
install vim

	sudo apt install vim

## ZSH
I wasn't an early adopter of zsh but i grew to love it as i worked more and more with git. Now I love it and there are so many themes that you can install any flavor you like. To install you can use the apt install manager.

	sudo apt install zsh
	chsh -s $(which zsh) 

Reboot, open a terminal and complete the zsh setup
install OhMyZSH 

	sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Set up preferances if you wan tto change the theme

	vim .zshrc

Change the shell dark blue to cyan

	eval $(dircolors -p | sed -e 's/DIR 01;34/DIR 01;36/' | dircolors /dev/stdin)
	
## Terminal
Change coloring by right clicking inside the terminal and selecting preferences → coloring
>Background: \#0A0D0E
>Test: \#7DA1AF

## tmux
It took some time to get used to tmux. Once i did it became a game changer. one of the hardest things about tmux was learning the shortcuts and making sure mouse support was on. to install tmux you can use the the apt install manager. 

	sudo apt install tmux

Once tmux is installed to add mouse support use the control +b and use the :setw -g mouse on

	CTRL+b :setw -g mouse on
	
I've gone back and forth on if i like vi mode or not. I have mixed feelings on this. currently i like the vi search options. to add this option you can use the CTRL+b to enter input mode and set mode-keys to vi. See below for the command.  

	CTRL+b : setw -g mode-keys vi

A full list of shortcuts can be found here: https://gist.github.com/MohamedAlaa/2961058. Below is a list of the common ones I use

> CTRL + B then c = Create New Window
> CTRL + B then ,= Name Window
> CTRL + B then % = Split Window (creating two panes) vertically
> CTRL + B then "" = Split Window (creating two panes) horizontally
> CTRL + B then z = Zoom into a single panel. This is helpful when you need to scroll with your mouse wheel. 
> CTRL + B then \[ = Enter copy mode. I mainly use this for searching files.
> In copy mode \ to start a search down

## SSH
believe it or not i have found that when installing a base image for Ubuntu ssh is not installed. If you run into this you can install it via the apt install manager. 

	sudo apt install ssh

## SSH-Keygen
	$ ssh-keygen -t ed25519 -C "me@johnwalley.com"
I like to name my ssh key to something I know. I also often will share a master key for all of my personal boxes. once it is created I will keep it for about a year then replace it for all access. I put this key in a safe place and always protect it with a password. 

To upload the key to other machines you can simply use the ssh-copy command. 

	ssh-copy-id -i </link to .pub file> user@ipaddress
	
## Git
Go to https://github.com/settings/keys and either upload the new key for this computer or copy your private key over to you new computer and put in the home ~/.ssh folder. 

	install git
	sudo apt install git

Set up global configurations

	git config --global user.email "<email@address.com>"
	git config --global user.name "<MyName>"

To sync local to GitHub use the following commands in sequence. 
Add all files in folder

	git add .

Commit all changes and add change notes

	git commit -m

when you are ready to upload to the remote repository. note the branch for the Field Manual is master. sometime this is main instead of master. zsh will identify your current branch.

![[Pasted image 20211219103726.png]]

	git push origin master

## Vim
Install vim. This may already be installed but it is good to check. 

	sudo apt install vim

## NMAP
NMAP is the most powerful tool available when it come to red team and pen testing. To install NMAP you can use apt install

	sudo apt install nmap

## cURL

cURL is by far the best tool for testing web connectivity but it also allows for website calls and downloads from command line. its basically a text based web browser. To install cURL on Linux you can utilize the apt install manager.

	sudo apt install curl

More on cURL can be found here [[cURL]]

## Metasploit-Framework
This is a stand alone version and updates apart from the OS unlike on Kali. The command below is correct wit the spacing do not change it to install Metasploit. Copy the whole section below and paste. The command below may change from time to time. you can see the install string here: https://github.com/rapid7/metasploit-framework/wiki/Nightly-Installers 

	curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
	chmod 755 msfinstall && \
	./msfinstall

Run msfconsole as sudo the first time. this will allow the system to properly build out the back end database. 

	sudo msfconsole
	
Once the database is up and running exit the msfconsole and update. 

	sudo msfupdate to update

More information on Metasploit: [[Metasploit]]

## 7zip
7 zip is a file archive tool but it provides so much more like the ability to view virtual drives. To install 7zip you can utilize the apt install manager. 

	sudo apt install p7zip-full p7zip-rar
	
For more on 7zip: [[7zip]]

## Flameshot
Flameshot is by far my favorite screen capture tool and i wish it was available on mac and windows. Greenshot is a close competitor for flameshot but I don't care for the lines and arrows in greenshot and like the clean lines in flameshot. I love this for documentation. To install flameshot you can use the apt install manager. 

	sudo apt install flameshot

Once installed you will need to set up some environmental setting to make it more user friendly. 

>Go to setting in Ubuntu and keyboard shortcuts
>Go to "Save a screenshot to pictures and Disable by clicking then backspace.
>Scroll to the bottom and add a new shortcut
>Name Flameshot
>Link /usr.bin/flameshot gui
>Link it to the print screen button

## UFW
UFW is a simplified way of controlling iptables firewall. UFW should already be installed. If it isn't you can install it with the apt install manager. 

	sudo apt install ufw
	
Now you can enable the firewall

	sudo ufw enable

Once installed I like to DROP ICMP traffic. This is optional as it can make troubleshooting difficult if you want to remote into your laptop from another device. 

To edit the default policies you will need to edit the before.rules file. 

	sudo vim /etc/ufw/before.rules

Change the following line from ACCEPT to DROP

>\#ok icmp codes for INPUT
>-A ufw-before-input -p icmp --icmp-type destination-unreachable -j DROP
>-A ufw-before-input -p icmp --icmp-type time-exceeded -j DROP
>-A ufw-before-input -p icmp --icmp-type parameter-problem -j DROP
>-A ufw-before-input -p icmp --icmp-type echo-request -j DROP

Reload your firewall to ensure the new rules are in place. 

	sudo ufw reload

## Python3
Python 2 is finally gone for the most part. It was such a pain to cross between 2 and 3. i haven'tT been having many issues and I think most systems are on Python3. For Python to fully function you will need to install Pyathon3 plus all of the needed libraries. You can utilize the apt install manager for this action. 

	sudo apt install python3 python3-pip python3-xlrd
	
I also like to install all of the pyTenable modules. if you want to do this you can add these with the pip installer.

	pip install pytenable

## Setserial
Setserial is a tool that will allow you to turn a Linux terminal into a serial screen and map to your tty output. You can use the apt install manager to install setserial.

	sudo apt install setserial

To list all serial ports you can use the following command:

	sudo setserial -g /dev/ttyS[0123]

to display USB serial ports you can use the following command:

	sudo setseral -g /dev/ttyUSB[01]

## Screen
Screen has many uses from holding session open even if the connection if severed to allowing tty connection. Before tmux I used screen for everything. I still use it pretty heavily for my servers. to install screen you can use the apt install manager. 

	sudo apt install screen

A few commands to know:

>CTRL+A D = detach from screen
CTRL+A k = Kill window / session
CTRL+A c = Create new window
CTRL+A S = Split term horizontally
CTRL+A CTRL+A = toggle between windows

Screen not only helps with things like running programs and scripts when disconnected from the tty it can also be used for serial connections via a console cable and plays well with setserial. 

For example to connect to Tenable.ot device over USB to serial I can check the USB serial assignment with set serial and then use screen to connect as 1115200 baud. 

	sudo screen /dev/ttyUSB0 115200

## fping
I used to write my own IP scanners then i learned about fping. This little tool and amazing. I love it. If i want to run a ping sweep it will do it all. You can install fping with the apt install manager. 

	sudo apt install fping

There are tons of options but the primary use is for scanning full subnets. you can do this by using the -ag flag and the subnet with the cider notation. fping will show errors so i typically sent the to /dev/null. An example is below:

	fping -ag 192.179.0.0/24 2> /dev/null

More on [[Fping]]

## Wordlists
lets not forget all the wordlsits you could ever want. This will be used with many many tools and it good to know where to get this and where they should reside on your computer. Most programs look under /usr/share/wordlists. You can do this but I like mine to stay under toolbox/scripts/wordlsits. 

to install you will need to clone a few lists off of github

change directories to the ~/toolbox/scripts folder and clone the directory

	cd ~/toolbox/scripts
	git clone https://github.com/danielmiessler/SecLists.git

After cloning the directory I also untar the rockyou.txt file

	tar xvf ./SecLists/Passwords/Leaked-Databases/rockyou.txt.tar.gz
	
More on Wordlists here: [[Wordlists]]

## GoBuster
This is by far my favorite web directory enumeration tool. You can install via the apt install manager.

	sudo apt install gobuster
	
For more on Gobuster [[GoBuster]]

## MySQL
I don't install the full MySQL server. I only install the client. You will seldom need more than the client and adding server introduces risk. You can install the MySQL clients  via the apt install manager using the following command:

	sudo apt install mysql-client

For more on MySQL: [[MySQL]]

## gnome-tweak-tool
Okay now the the fluffy stuff. lets make it so we can play with login screens, backgrounds and such. the gnome-tweak-tool will allow you to change these options. You can install this with the apt install manager.

	sudo apt install gnome-tweak-tool

Once installed open tweaks in the app selection window and go to appearance. Change the setting to yaru dark.

## Discord
I use this to chat, share screen, and troubleshoot when it isn't in a professional setting. You can install Discord using the snap installer:

	snap install Discord

## Function Keys working
This section only apples to my personal MSI laptop. There are some function keys that will not work without updating grub. editing the /etc/default/gfrb file and replacing the the line GRUB_CMDLINE_LINUX_DEFAULT="quiet splash" with GRUB_CMDLINE_LINUX_DEFAULT="acpi_osi=! acpi_osi='Windows 2009' quiet splash" will fix the functions key issue. 

>GRUB_CMDLINE_LINUX_DEFAULT="acpi_osi=! acpi_osi='Windows 2009' quiet splash"

**Important:**
Make sure you don't leave any lingering ' marks this will break your apt upgrade process and drive you nuts.

Return to [[-README]]





