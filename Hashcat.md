Hashcat install requires additional files including Cuda drivers to support GPU support. To install run the following commands. 

	sudo apt install -y ocl-icd-libopencl1 nvidia-driver nvidia-cuda-toolkit
	nvidia-smi
	sudo hashcat -I` or `sudo hashcat --benchmark` for benchmarks

Once installed there is a basic format to cracking passwords. here is an example:

	hashcat -m 500 example500.hash /usr/share/wordlists/sqlmap.txt
	
you can see the format by simply typing hashcat --help

For more information this is a pretty good site: https://linuxhint.com/hashcat-tutorial/

Return to [[-README]]