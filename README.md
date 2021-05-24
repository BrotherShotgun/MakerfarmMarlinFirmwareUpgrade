# MakerfarmMarlinFirmwareUpgrade
Upgrading Makerfarm Prusa i3v RAMPS Marlin Firmware

Makerfarm (R.I.P.) printers originally came with instructions locking you into oooooold versions of Marlin and Slic3r

In 2017 I underwent the process of making the necessary leaps to get mine upgraded to what was then the current release - 1.1.5

I'm starting to go back through my files to remember and repeat the process -- and sharing this time

This is a Work In Progress
This is a Work In Progress
This is a Work In Progress
This is a Work In Progress
This is a Work In Progress
This is a Work In Progress
This is a Work In Progress

The main thing I remember is that the whole structure of the .h files was different between the versions
I had to hunt a lot of stuff down and do a lot of file comparisons
I also upgraded to the full graphical LCD at the time
The only real issue I had was with leveling, which turned out to be not realizing I had to enable the second Z-axis stepper





From Colin's Original Instructions:

Installing RAMPS firmware for i3v printers
1. First we will install the driver for your Printer, after you download the RAMPS/RUMBA driver above unzip the file then run “RRD_RUMBA_TAURINO_DriverSetup.exe”
2. If you haven’t already downloaded the arduino software goto www.arduino.cc, click on “Download”, then click on “Previous Releases” then Download Arduino 1.0.6 (Don’t get a newer version, get 1.0.6) that matches your Operating System. For this set of instructions we are going to use the Windows version, but other operating systems should be similar. After Downloading the Arduino 1.0.6 software go ahead and install it.
3. Open the Arduino software, Click on the Tools tab, then board and select “Arduino Mega 2560 or Mega ADK”. Then select Tools tab and serial port, take note of the com ports that are listed, since you haven’t plugged in your printer yet these ports are not your Printer.
4. Now we are ready to plug the usb cable into our Printer, then plug it directly into your PC (Do not plug into a USB Hub), at this point the driver will install and it will be setup on a Com port, to check open the Arduino software again, Click on the Tools tab then Serial Port, you should now see a new com port, this is your printers Com Port, go ahead and click on that com port under the Serial Port section of the Tools tab.
5. Next Unzip the Firmware zip you downloaded earlier, then in the arduino software, click File, then Open, browse to the firmware folder you just unzipped, open the “Marlin_RAMPS_EPCOS_i3.ino”
6. If you have an E3D Hot End we need to modify the thermistor for the hot end, select the Configuration.h tab and scroll down till you see: “#define TEMP_SENSOR_0 6”, change this to: “#define TEMP_SENSOR_0 5”
7. Now that we have our firmware loaded, printer plugged in via USB cable directly into the PC, “Arduino Mega 2560 or Mega ADK” selected in the Tools, Board menu and we have our printer’s Com port selected in the Tools, Serial Port menu all we need to do is click on Sketch then Verify/Compile, if you do not get any errors and see “Done Compiling” at the bottom then click File, then Upload. You will see “Compiling Sketch” then the lights will start to flash when you see “Uploading”, when it finishes you will see “Done Uploading”

