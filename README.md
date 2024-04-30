## Adafruit USB Host BFF for QT Py or Xiao with MAX3421E PCB

<a href="http://www.adafruit.com/products/5956"><img src="assets/5956.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit USB Host BFF for QT Py or Xiao with MAX3421E. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5956

### Description

Is your QT Py all alone, lacking a friend to travel the wide world with? When you were a kid, you may have learned about the "buddy" system. Well, this product is kind of like that! It is a board that will watch your QT Py's back and add a USB Host port.

That means that your tiny microcontroller project can have a keyboard, mouse, or disk drive plugged into it, opening up a huge ecosystem of common off-the-shelf devices that you can now integrate. The Adafruit USB Host BFF makes it easy to add USB Host support, especially now that TinyUSB supports it in the Arduino library as a 'native' interface for host support. 

This BFF uses the MAX3421E - a tried and true USB Host chip. It uses SPI plus an IRQ pin to send data to just about any USB device. Note that because the chip is older and you're limited to the SPI port speed, you won't get blazing 480Mbps high-speed data transfer. But for basic HID interfacing or even reading/writing to a Mass Storage device, it does work quite well. There's a famous USB Host Library that can be used, and its specialty is AVR support, but it also seems to support nRF52 and ESP32.

We personally recommend using the TinyUSB Arduino library - however, the trade-off is that the chip must have TinyUSB support already, which means it's great for RP2040, ESP32-S2 or S3, nRF52840, SAMD21/51 chips. Make sure your desired QT Py mainboard is supported between the two libraries before purchasing! 

To keep the BFF very compact, we use a micro-B USB "OTG" connector - a full sized USB Type A wouldn't fit! You'll need to use a basic OTG adapter (such as those sold for use with the Pi Zero) to convert to type A. Unlike our USB Host 'Wing we don't include a 5V power booster, so you will need to power the QT Py + BFF over USB or in some other way provide 5V on the 5V power line. However, to make it easier to power-cycle the peripheral, we have wired up a P-FET for switching the 5V host power on and off, you can either short the pin to A0 or you can use the MAX3421E's GPIO pin.

We include some header that you can solder to your QT Py. You can also pick up an Itsy Bitsy short female header kit to make it removable but compact; you'll need to trim the headers to 7 pins long.

Remember, you need driver support for the MAX3421E (see above for chips that are known to work). Unless you're using a generic mouse, keyboard, CDC serial, or USB mass storage device, you will also need a USB driver that knows how to talk to the device—and writing a driver is non-trivial.

QT Py or Xiao is not included!

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
