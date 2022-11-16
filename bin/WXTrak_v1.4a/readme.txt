This .ZIP file contains the files needed to upgrade the firmware of a Byonics device
using a PIC 16F1827 chip to the WXTrak or WXTrak FA v1.4 firmware.  

Note that only devices with the PIC 16F1827 chip will have the Byonics bootloader and 
	be able to be upgraded this way.

ZIP file contents:
	WXTrakConfig v1.4.exe - The Configuration utility
	WXTrak v1.4.t3f - The firmware for the TinyTrak3Plus and similiar devices
	WXTrak FA v1.4.t3f - The firmware for the MT-RTG FA and MT-AIO and other
		similiar devices that contain a transmitter
	readme.txt - This file


Instructions for updating the firmware of a Byonics 16F1827 chip:
 - Obtain a copy of Tera Term Pro
 - Connect the device the the computer serial port with an appropriate cable: 
	MT-AIO programming cable for the MT-AIO or a F-F null modem cable for 
	the MT-RTG FA or TinyTrak3Plus. This is the same cable used to update settings.
 - Start Tera Term Pro, and under Serial Port..., select the connected 
	COM port, 19200 baud, and a transmit delay of 1 msec/char
 - In the terminal program, press and hold the 'b' key
 - Apply power to the device
 - The terminal should display "ø_1" or "_1". If it doesn't, reset power
	to try again, keeping the 'b' key held.
 - Release the 'b' key
 - Press (and release) the 's' key.  Nothing will be changed in the terminal.
 - Choose File, Send File..., check the binary box, and select the 
	desired .t3f file containging the new firmware.
 - During the upload, nothing should be displayed on the terminal
 - After the upload was successful, the teminal should display a '*'. If
	it does not, repeat from the press and hold 'b' step. There 
	may be a few second delay after the Send File dialog closes
	and the '*' appears.
 - Quit Tera Term Pro
 - Cycle power on the device
 - Run the included WXTrakconfig program to set the desired options.  Do not read
	the existing options, as they could be corrupted.

