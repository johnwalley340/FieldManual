Guestmount allows you to mount a remote SMB drive to a remote target. this makes it easy to traverse the file structure on a remote computer. Guestmoiunt is a part of the libguestfs-tool package. To connect to a guest file system use the following command: 

	guestmount --add <filename> -i inspector --ro -v <mountpoint>


Guestmount should be installed by default but you may find your system does't not have it. If this is the case you can install guestmount via the apt install manager. 

	sudo apt install libguestfs-tools


Return to [[README]]