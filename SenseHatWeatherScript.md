# Script for displaying current conditiosn on SenseHat's LED matrix

```sh
#!/usr/bin/python
from sense_hat import SenseHat
import time                                                 // import time of current system
import sys                                                  // import sys library

sense = SenseHat()
sense.clear()

    try:
        while True:
            temp = sense.get_temperature()                  // sensehat gets temp
            temp = 1.8 * round(temp, 1) + 32                // round it to one decimal place
            print("Temperature F",temp)         

            humidity = sense.get_humidity()  
            humidity = round(humidity, 1)  
            print("Humidity :",humidity)  

            pressure = sense.get_pressure()
            pressure = round(pressure, 1)
            print("Pressure:",pressure)

            time.sleep(1)                                   // intervals in betweeen the refreshing of data
except KeyboardInterrupt:
      pass
      
sense.show_message("Temperature F" + str(temp) + "Humidity:" + str(humidity) + "Pressure:" + str(pressure), scroll_speed=(0.08), back_colour= [0, 0, 153])              // displays information on the LED matrix


sense.clear                                                 // clears the LED matrix

