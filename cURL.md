cURL is a text based web browser. This is a favorite go to and I use it on a daily basis for so many purposes from testing HTTP and HTTPS connectivity to downloading malicious code to a target. 

There are a few tips a tricks. First man pages are pretty good for this program. Use them.

the -k flag allows you to bypass any certificate errors

	curl -k https://target.system

If you ever get a 403 forbidden page you can try to bypass this by adding "X-Client-IP" header with the vlaue of "127.0.0.1"

	curl -l https://target.system -H "X-Client-IP: 127.0.0.1"

To install cURL you can use the apt install manager.

	sudo apt install curl
	
Return to [[README]]cURL is a text based web browser. This is a favorite go to and I use it on a daily basis for so many purposes from testing HTTP and HTTPS connectivity to downloading malicious code to a target. 

There are a few tips a tricks. First man pages are pretty good for this program. Use them.

the -k flag allows you to bypass any certificate errors

	curl -k https://target.system

If you ever get a 403 forbidden page you can try to bypass this by adding "X-Client-IP" header with the value of "127.0.0.1"

	curl -l https://target.system -H "X-Client-IP: 127.0.0.1"

To install cURL you can use the apt install manager.

	sudo apt install curl
	
Return to [[README]]