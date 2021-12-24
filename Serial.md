You can connect to a serial port like cisco or tenable.core via usb by using screen and set serial. to get a list of serial tty ports you can run the following command:

	sudo setserial -g /dev/ttyUSB*

You can leverage the screen command to connect to a serial tty:

	screen /dev/ttyUSB0 115200

See [[Screen]] for more info

Return to [[README]]
