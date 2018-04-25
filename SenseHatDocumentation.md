# Final Project
#### SenseHat Environmental Gauge
##### Items needed
-	SenseHat
-	Raspberry Pi 
-	Text Editor (for Python)
-	Computer 
-	Internet Access

>Using a SenseHat board, attached to an Raspberry Pi 3,  I will code a Python program that will make use of built in gyroscope, accelerometer, magnetometer, temperature, and barometric pressure gauges displaying its readings on the 8x8 LED light grid located atop the board. The readings will be displayed >in a marquee manner, refreshing its content every minute until a keyboard command is executed, killing the program. 

## Getting Started
```sh
$ sudo apt-get install sense-hat
```

## Post SenseHat installation
>SenseHat has an API that shows how to call, and display information gathered from the SenseHat. 
I will be using a small Python script, that will run at startup, to display the environmental conditions. 

## Python 
>Using references from the SenseHat API to call and display information
### EXAMPLE 
```sh
sense = SenseHat()
temp = sense.get_temperature()
		temp = round(temp, 1)
		logger.log(“Temperature C”, temp)
```
>The script above is an example of Python and the SenseHat API working together to grab and display (log) 
information collected by the SenseHat board.

# REMINDER 
- All scripts must start with this:
```sh
#!/usr/bin/python
```
- And include:
```sh
from sense_hat import SenseHat 
```
- The latter imports all of SenseHat's knowledge 
### Logging information collected via INITIAL STATE

## What is INITIAL STATE?
>A data storage/analytics site for IoT (Internet of Things) devices
- The data is uploaded directly to the website via preauthorized keys that you receive after completion
- The data is then displayed in bar graphs
