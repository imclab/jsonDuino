# jsonDuino - An internet connected Arduino with a RESTful JSON Interface

jsonDuino is firmware for your Arduino that exposes its IO values as JSON. Also provided
are some data logging clients (that log to Thingspeak and Pachube) as well as jQuery
based user interfaces for viewing and controlling the Arduino.

## Service Interface (Draft)

### Read Pins (GET)
- http://yourhost/json --> returns JSON
- http://yourhost      --> returns HTML
- http://yourhost/form --> HTML form

*Below usages are to dos...*

- http://yourhost/0    --> returns JSON of digital pin value
- http://yourhost/a0   --> returns JSON value of analog pin value

### Write Pins (POST) 
- http://yourhost/0  --> POST json value to set the digital pin
- http://yourhost/a0 --> POST json value to set the analog pin

#### JSON for POSTing
- `{"value":"500"}`    --> analog value/ digital PWM value
- `{"value":"HIGH"}`   --> digital value

## Dependencies
- Webduino Library
  - https://github.com/sirleech/Webduino

## Hardware You Can Use
- Arduino + Ethernet Shield
- Etherten

## Sources and Attribution
- http://code.google.com/p/webduino/ (original Webserver library)
- http://jasongullickson.posterous.com/restduino-arduino-hacking-for-the-rest-of-us (inspiration for RESTful interface)
