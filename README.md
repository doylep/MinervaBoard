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
- The power supply traces (in particular, the 5V line) is too thin to provide the necessary power for all four Darlington Arrays to operate at full capacity (2A for the arrays, 1A for the Raspberry Pi, and 1A for the ATMega328 and OpAmp).
- The communication circuit between the Raspberry Pi and the ATMega328 has not been tested. Although the circuit uses an example circuit from the PCA9306, this example circuit is for an I2C bus, not the UART communication between the two devices.
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
- Raspberry Pi input/outputs Pi12, Pi16-18, Pi20, and Pi23-25 can be connected directly to the pins, routed through a Darlington array for high current output, or routed through a level shifter for 5V input or output. The propogation direction of the level shifter is set by Pi18.
- Raspberry Pi input/outputs Pi5-6, Pi9-11, Pi13, Pi19, and Pi26 can be connected directly to the pins, routed through a Darlington array for high current output, or routed through a level shifter for 5V input or output. The propogation direction of the level shifter is set by Pi21.
- Raspberry Pi input/outputs Pi2-4, Pi17, Pi22, and Pi27 are exposed directly to the pins for 3V input and output.

Further documentation is forthcoming.
