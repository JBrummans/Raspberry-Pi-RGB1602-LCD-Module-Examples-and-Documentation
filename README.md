# Raspberry Pi RGB1602 LCD Module Examples and Documentation

Examples and Documentation for the RGB1602 LCD display by SeeedStudio

Seeed Studio product page: <https://www.seeedstudio.com/Raspberry-Pi-RGB1602-LCD-Module.html>

Product pages links to this wiki: https://wiki.52pi.com/index.php/52Pi-BPi_LCD_1602_Module_SKU:EP-0045 

Basically useless... Only provides a single example written in C which doesnt compile due to missing libraries.

For the example to work, follow instructions however install wiringPi from here: http://wiringpi.com/download-and-install/ instead of the git repo as the link in the example is broken. 

Also when compiling the example, instead of: 
`sudo gcc mylcd1602.c /home/pi/wiringPi/devLib/lcd.o -lwiringPi -o mylcd1602`
Use:
` sudo gcc mylcd1602.c -lwiringPi -lwiringPiDev -o mylcd1602`
The compile command given was missing the `-lwiringPiDev` library required.

When Googling random snippets from the C example on the product's wiki, I found this:
<http://wiki.banana-pi.org/BPI_LCD_1602_display_module>
Which is an identically designed RGB1602 display but actually has some info regarding the design. Might be useful as it gives more information about the pin out of the GPIO.
