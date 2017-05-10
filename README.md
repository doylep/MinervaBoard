Minerva Board
=============
Raspberry Pi sheild with built-in Arduino for ease of connection to puzzle room props.

Board Outline
-------------
This board connects a Raspberry Pi base (either the normal Pi or the Pi Zero) to an ATMega328. The board exposes all of the GPIO outputs of the ATMega328 and the the majority of the GPIO outputs of the Raspberry Pi. In addition, the board offers several sockets to enhance the GPIO outputs to provide higher power or match 5V output.

The board is designed to operate from a regulated 5V power supply and interface (almost) exclusively with 5V inputs and outputs.

Known Issues
------------
This board is in active development, and there are several suspected issues with this design:
- Although the UART communication circuit between the Raspberry Pi and the ATMega328 is based on documented examples with the TXS0102, this circuit between has not been tested.
- The board doesn't offer any power breakouts for supplying power to additional accessories from the same power supply. Although not necessary, this would further reduce the need for additional wiring and circuits.

License
-------
Released under the Creative Commons Attributuion Share-Alike 4.0 License  
https://creativecommons.org/licenses/by-sa/4.0/

This design is based on the Arduino Pro. Although some circuits are the same, the majority of the board has been redesigned to create a shield for the Raspberry Pi.  

Original Arduino Mini Design by Team Arduino  
Arduino Pro Mini Design by Spark Fun Electronics  
Minerva Board Design by Decode Detroit  

Documentation Outline
---------------------
- ATMega328 input/outputs D6-D13 can be connected directly to the pins or routed through a Darlington array for high current output. In addition, these intput/outputs can be set up in a button circuit which allows them to simultaneously read the status of the button turn on a light or other indicator.
- ATMega328 input/outputs D0-D5 and A4-A5 can be connected directly to the pins or routed through a Darlington array for high current output.
- ATMega328 input/outputs A0-A5 are exposed directly to pins for analoq reading or low current GPIO.
- Raspberry Pi input/outputs Pi7-8, Pi12, Pi16, Pi20, and Pi24-26 can be connected directly to the pins, routed through a Darlington array for high current output, or routed through a level shifter for 5V input or output. The propogation direction of the level shifter is set by Pi23.
- Raspberry Pi input/outputs Pi4-5, Pi9-11, Pi17, Pi22, and Pi27 can be connected directly to the pins, routed through a Darlington array for high current output, or routed through a level shifter for 5V input or output. The propogation direction of the level shifter is set by Pi6.
- Raspberry Pi input/outputs Pi2-3 are exposed directly to the pins for 3V input and output.
- The audio output is currently implemented as a direct connection to the Adafruit MAX98357 breakout board. This allows the board to be soldered using a simple soldering iron; future versions may implement the MAX98357 connections directly.

Further documentation is forthcoming.
