ATTINY 84 Getting Started
=========================

Preferences>Additional Boards Manager URLs
Add
https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json


Sketch>Include Library>Manage Library select attiny

Don't wire to ATtiny yet you need to upload the ArduinoISP sketch just like any
other program. So Tools>Board>ArduinoUno then File>Examples>ArduinoISP and
upload to the board.

Now the Uno is programmed so we can

Tools>Programmer>Arduino as ISP

Tools>Board>ATTIny24/44/84

Tools>Processor>ATtiny84

Wire Up

Pin 1 on ATTINY 84A bottom left if nothch is facing left. Mine has a triangle
also showing pin 1. Pin 2 is next to it pin 8 is opposite pin 7, pin 14
opposite pin 1.

Wire Arduino Uno +5V to ATtiny84 Pin 1 (vcc)
Uno pin 10 to ATtiny pin 4 (reset)
Uno pin 11 to ATtiny pin 7 (MOSI)
Uno pin 12 to ATtiny pin 8 (MISO)
Uno pin 13 to ATtiny pin 9 (SCK)
Uno GND to ATtiny pin 14 (GND)
Uno RESET to 10uF cap then cap to GND

Now load an example like blink and upload. The Uno will send it to the ATtiny.

To run at 8mhz Tools>Clock>8MHz Internal

Tools>Burn Bootloader

Then upload a sketch
