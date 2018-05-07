# Print a message in Python
- Using the LED matrix on the Sensehat you can show messages

# Using 'VIM' you must create a .py (Python) file for your script
- Navigate to your preferred folder before you run the command below:
```sh
$ vim Print_Message.py
```
> After running this command you are presented with a terminal window,
this is where you write your script. In order to insert text you must press
the letter I to enter insert mode. Use the script below:

## Example:
```sh
#!/usr/bin/python                           // makes it executable

from sense_hat import SenseHat              // imports its knowledge
sense = SenseHat()                          // declares sense as SenseHat 
sense.show_message("Well Helllllo there!")  // uses the show_message which is part of SenseHats knowledge
```
- After you enter the script press ESC to leave insert mode and type:

```sh
$ :wq!
```
> This will (W)rite the script to memory and (Q)uit the VIM editor 

Simple enough, right? 
