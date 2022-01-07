# Flatpanel

This repostory contains all files for making a remote-controllable Flatpanel for astrophotography.

A standard 60x60 cm flatpanel is connected to a dimmable driver that is already set to quite a low brightness to begin with.
Using an Arduino Uno that is connected to USB on the host computer, a MOSFET chops the current to the panel so you can set a very low brightness for making flat fields with your telescope.

Included is the scetch for the Arduino.
When connected to the computer, its USB address should be set to the highest virtual COM port number on your system.

Then, using a small executable file "SerialSend.exe" you can send the desired brightness value (0-255) to your LED panel.
