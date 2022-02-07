# Flatpanel

This repository contains all files for making a remote-controllable Flatpanel for astrophotography.

A standard 60x60 cm flatpanel is connected to a dimmable driver that is already set to quite a low brightness to begin with.
Using an Arduino Uno that is connected to USB on the host computer, a MOSFET chops the current to the panel so you can set a very low brightness for making flat fields with your telescope. The MOSFET will switch the black return wire between panel and driver.

Included is the scetch for the Arduino.
When connected to the computer, its USB address should be set to be the HIGHEST virtual COM port number on your system.

Then, using a small executable file "SerialSend.exe", originally by Ted Burke. https://github.com/tedburke/SerialSend
I modified it to fit my purpose, source files are included, but you can just use the executable.
You can send the desired brightness value (0-255) to your LED panel. SerialSend does not specify a COM port number, but sends the data to the highest available COM port number.
Usage from the directory where the executable is located: 
'SerialSend.exe B255' 
where the 3 digit number after the B is the desired brightness from 000 to 255, don't type the quotes!

See "ACP-AutoFlatConfig.txt" to find out how to use this with the "acquire auto-flat" function in the ACP Observatory Control software. 
I replaced the original Alnitak commands with those appropriate for use with SerialSend.exe. In this file I also defined the standard brightness for each filter and different binnings.
That way I can shoot series of flats for all of my 7 filters without the need to be there in person.

After building the interface, just test it from the command prompt. You can also use batch files to switch brightness.
