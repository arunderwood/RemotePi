# RemotePi

This projects aims to create a remotely operated weather station, which when possible, should be roughly analogous to a space satellite.  

The core of the station is a Raspberry Pi. 

*The Raspberry Pi aggregates information from all sensors and communicates the information back to a base station via IP on an AX.25 network.
*The Pi is connected to the Baofeng BF-888S radio via a TNCPi TNC.
*Power Management and IO for the Pi is done through a Sleep Pi hat.
	*The Arduino on the Sleepy Pi collects and stored data from the sensors
		*I2C Attached Temp/Humidity Probe
		*Wind Speed/Direction
		*Luminosity
	*The whole rig is powered by a led acid battery.  This battery is charged by a solar panel through a solar charge regulator.
	*The Pi shuts down when it's not transmitting on the radio.
	*The RTC on the Sleepy Pi interrupts the Arduino when it's time to wake the Pi.
	*Upon boot, the Arduino transfers sensor logs for the period to the Pi, which are transmitted via the radio.
	*Solar panel status, battery voltage, and board temperature are also included in the transmitted data.
	*A picture is captured with the Pi camera, which is also transmitted.
	*When it's operations are complete, the Pi shuts down to conserve battery.
	*The Arduino arms the RTC, so it can wake the Pi for it's next scheduled transmission.
