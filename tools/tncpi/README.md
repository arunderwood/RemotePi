## TNCPi Tools

TNCPi is a TNC in the form of a hat which sits on top of the Raspberry Pi.

#### Power
The TNCPi draws it's power from the RPi's 3.3v pin.

#### Communicating with the Pi
The TNCPi can communicate with the RPi over either serial or I2C.  By default it uses serial, however for the purposes of this project we will need to switch it to I2C.
We need to do this because the RPi only has one serial UART, and we need that free so the RPi can flash the Arduino on the SleepyPi hat.

#### Pin out for the radio header
* Pin 1 (the square pad): Receive Audio
* Pin 2: Ground
* Pin 3: TX Audio
* Pin 4: Push to Talk (PTT)

#### Additional Resources
* http://www.tnc-x.com/TNCPi.htm
* http://tarpn.net/t/tncpi/tncpi.html

![TNCPi 2.3 Schematic](http://tarpn.net/t/tncpi/2015_12_02_TARPN_TNCPI_2_3_Schematic.jpg "TNCPi 2.3 Schematic")