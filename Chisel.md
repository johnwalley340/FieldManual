## Chisel
Chisel is a fast TCP/UDP tunnel, transported over HTTP, secured via SSH. Single executable including both client and server. Written in Go (golang). Chisel is mainly useful for passing through firewalls, though it can also be used to provide a secure endpoint into your network.

Thisis create ofr bypassing both hostbased and network firewalls. this allows you to create a reverse shell for instance over port 80 tunneling ssh. 

![[Pasted image 20211229111046.png]]

Install works though a go compiler. to install you have to run as root not sudo

	sudo bash
	go get -v github.com/jpillora/chisel
	
Return to [[README]]
	
