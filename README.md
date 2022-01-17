# cg-scale-wifi-micropython
A scale to measure the centre og gravity for RC planes in MicroPython 

# Project:
This is all about the electronics and software (MicroPython) to build a, Centre of gravity scale for RC planes.
The hard ware is build around a ESP32 devit (TTGO T8 V1.8), 2 load cells (YZC-133) and 2 24 bits ADC converters (HX711).
The load cells used are 2kg (front) and 3kg (rear) together they support planes upto 4.5KG.
If needed the load cells can be echanged for stronger ones (ex: 2x5kg).
Informartion about the hard ware can be found in Docs/BOM.pdf

# TTGO T8 V1.8
The devkit has first to be loaded with the MicroPython firmware that can be found here: 
https://micropython.org/download/esp32spiram/
After that is done the rest of the files can be loaded with Thonny for micropython:
/lib
/www
boot.py
config.json
main.py
wificonnect.py

In the main.py files you can enter your ssid and password.
The devkit will first try to connect to your network.
If it gets an IP address assigned it will create a webserver on your network.
If it can't connect to your network it will create a Access Point (CGScale) on 192.168.4.1

The webpage that the webserver uses is not made by me. I found it here: 
https://github.com/guillaumef/cg-scale-wifi-oled/blob/master/soft/html.h
A lot of thanks to Guillamef for his work!
The webpage was slightly changed for my software.

All the librariesto make the project work, can be found in the folder /lib.

The enclosure to put in all the hardware and finalize the scale can be found here:
https://www.thingiverse.com/thing:5145294
Many thanks to Greg Ory!
The baseplate had to be adapted to hold the devkit, batterie and HX711.
The STL files can be found in the /stl folder

