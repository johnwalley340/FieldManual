## Disk Manupilation

##### List Block Devices (drives)
You can use the lsblk command to list all drives on teh system. This is simular to the olf fdisk -l but i like the output a lot better.

	sudo lsblk

##### Copy and Convert
Beelieve it or not DD stands for copy and convert. Its called dd because cc is already in use by C compiler. dd can be used to write an image to a disk take a back up or iso.

if = imput file / disk
of = output file / disk
status = progress will show progress of a write process

to create a backup or dd/iso image:

	sudo dd if=/dev/<drive> of=<filename.iso/.dd> ststus=progress
	
to wrant an image / backup to a drive

	sudo dd if=<filename.iso/.dd of=/dev/<drive> status=progress
	
You can alslo use dd to completly erase a disk. 

	sudo dd if=/dev/zero of=/dev/<disk> bs=512 count=32

## Format Disk
fdisk can be used to format a disk 

	sudo fdisk /dev/<disk>

follow instrustions when prompted.

## Make File System

mkfs will allow you to create many types of file systems. to see all of the option you can type the mkfs. and TAB and your options will appear. 

For FAT32 you can use 

		sudo mkfs.vfat -F32 /dev/sdb1


##### Disk Usage
du  "Disk Usage" will find the approximate file space fro files and directories. 

	du -hs \<filename> = name will return the size value.

![[Pasted image 20211219132908.png]]

##### Disk Free
df -hs = file system sizes

![[Pasted image 20211219132758.png]]


Return to [[README]]