## Get full shell

### Bash
To create get a full shell on a target you can try a simple bash upgrade like 

	/bin/bash
	
if that doesn't work (which it wont most times)you can try 

	SHELL=/bin/bash script -q /dev/null

### Python

If simple bash/sh command don't work and the system supports python you are in luck. the following command works almost every time:

	python3 -c 'import pty;pty.spawn("/bin/bash");'
	
for python2 you will wan tot use the following command

	python -c 'import pty;pty.spawn("/bin/bash");'
	
If you still do not have a full shell you can try

	export TERM=xterm
	
Return to [[README]]



