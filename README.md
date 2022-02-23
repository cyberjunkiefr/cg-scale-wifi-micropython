A big thank's to Roel, my friend, he has very goods idea all the times... Big Up Roel!

# cg-scale-wifi-micropython
A scale to measure the centre og gravity for RC planes in MicroPython

# Project:
This is all about the electronics and software (MicroPython) to build a, Centre of gravity scale for RC planes.
The hardware is build around a ESP32 devit (TTGO T8 V1.8), 2 load cells (YZC-133) and 2 24 bits ADC converters (HX711).
The load cells used are 2kg (front) and 3kg (rear) together they support planes upto 4.5KG.
If needed the load cells can be echanged for stronger ones (ex: 2x5kg).
Informartion about the hard ware can be found in /Docs/BOM.pdf

# TTGO T8 V1.8
The devkit has first to be loaded with the MicroPython firmware that can be found here:  
[MicroPython firmware for ESP32](https://micropython.org/download/esp32spiram/)  
After that is done the rest of the files can be loaded with Thonny for micropython:
/lib
/www
boot.py
config.json
main.py
wificonnect.py

![image](https://user-images.githubusercontent.com/11100197/149840198-f2fd8852-3fe5-4466-a2ef-0aa0bef20f5e.png)

In the main.py files you can enter your ssid and password.
The devkit will first try to connect to your network.
If it gets an IP address assigned it will create a webserver on your network.
If it can't connect to your network it will create a Access Point (CGScale) on 192.168.4.1

The webpage that the webserver uses is not made by me. My friend Roel found it here:  
[Guillaumef's html.h file on GitHub](https://github.com/guillaumef/cg-scale-wifi-oled/blob/master/soft/html.h)  
A lot of thanks to Guillamef for his work!  
The webpage was slightly changed for the software.  

All the libraries to make the project work, can be found in the folder /lib.  

The first parts of scale was design by Greg Ory.
[Greg_Ory's scale on thingiverse.com](https://www.thingiverse.com/thing:5145294)  
Many thanks to him !
I've redefine some parts for optimize they, I continu to change they know, check sometimes if you want the last version, I will create a new folder stl for the old files.

For the moment, the baseplate had to be adapted to hold the devkit, batterie and HX711.
The support whith squares holes will be changed by rounds holes, easyier to calibrate and round profiles are less expensive.

The STL files can be found in the /stl/ folder