# Script for logging of conditions collected by SenseHat

```sh
#!/usr/bin/python

from sense_hat import SenseHat  
import time                     // imports the time of the current system
import sys                      // imports the sys library
from ISStreamer.Streamer import Streamer    //this streams the data to InitalSlate

sense = SenseHat()
logger = Streamer(bucket_name=SenseHat Data for Wooding, access_key= "")
sense.clear()

try:
    while True:
            temp = sense.get_temperature()
            temp = 1.8 * round(temp, 1) + 32
            logger.log("Temperature F",temp)
            
            humidity = sense.get_humidity()
            humidity = round(humidity, 1)
            logger.log("Humididty: ",humidity)
            
            pressure = sense.get_pressure()
            pressure = round(pressure, 1)
            logger.log("pressure: ",pressure)
        
        time.sleep(1)                   // intervals between the displaying of current readings
except KeyboardInterrupt:
    pass
    
sense.clear                             // clears the LED matrix

