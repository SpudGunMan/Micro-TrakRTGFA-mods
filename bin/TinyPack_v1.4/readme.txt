This .ZIP file contains the files needed to upgrade and configure the 
Byonics TinyPack Firmware (www.byonics.com)

Note that there are 2 versions of the firmware.  The FA version is for
hardware with a built in frequency agile transmitter.  A working Byonics 
PIC 16F1827 is required for this update.

TinyPack v1.4.t3f - This is the firmware for TinyTrak3 based 
   hardware with a PIC 16F1827 chip and WITHOUT a Micro-Trak transmitter. 
   (TinyTrak3Plus, WXTrak, TinyPack, etc)

TinyPack FA v1.4.t3f - This is the firmware for a TinyTrak3 based 
   hardware with a PIC 16F1827 chip and WITH a Micro-Trak transmitter. 
   (Micro-Trak RTG FA, Micro-Trak AIO, Micro-Fox 15, etc)

TinyPackConfig v1.4.exe - This is the config program for both v1.4 firmwares.

Firmware updates in v1.4
 - First firmware release of TinyPack / TinyPack FA for the PIC 16F1827 chips

Instructions for updating the TinyPack firmware:
 - Obtain a copy of Tera Term Pro
 - Connect the TinyTrak3/Micro-Trak the the computer serial port with a 
	programming cable. (TT USB, F-F Null modem or AIO style)
 - Start Tera Term Pro, and under Serial Port..., select the connected 
	COM port, 19200 baud, and a transmit delay of 1 msec/char
 - In the terminal program, press and hold the 'b' key
 - Apply power to the TinyTrak3/Micro-Trak
 - The terminal should display "ø_1" or "_1". If it doesn't, reset power
	to try again, keeping the 'b' key held.
 - Release the 'b' key
 - Press (and release) the 's' key.  Nothing will be changed in the terminal.
 - Choose File, Send File..., check the binary box, and select the 
	applicable .t3f file
 - During the upload, nothing should be displayed on the terminal
 - After the upload was successful, the teminal should display a '*'. If
	it does not, repeat from the press and hold 'b' step. There 
	may be an up to 30 second delay after the Send File dialog closes
	and the '*' appears.
 - Quit Tera Term Pro
 - Cycle power on the TinyPack
 - Run the TinyPack config program to set the desired options. (Do not 
	read current settings first, they may be bad)
 