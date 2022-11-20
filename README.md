# Tempature Sensor
This is basic micropython API for the SHT40 temperature sensor which works with micropython.  The adafruit driver was built for 
circuit python and this ensures it works for micropython without other depedencies.  This builds a temperature reader with teh adafruit [SHT40 reader](https://learn.adafruit.com/adafruit-sht40-temperature-humidity-sensor). This is basic setup which provides terminal readout from the sensor.  

## Node MCU Setup With Micropython
This article provides a nice summary of setting up NodeMCU with micropython.  This should work for blank NodeMCU or one with material already.  https://www.embedded-robotics.com/esp8266-micropython/.  

This provides very good setup and I suggest using Thonny app for develompent.  https://www.embedded-robotics.com/esp8266-micropython/

## ???

To start, I am setting up the NodeMCU with fresh micropython.  I am going to use 
[this reference](https://icircuit.net/nodemcu-getting-started-micropython/2406) to to complete the setup. My setup is on Linux, so here is some helpful howtos on setup:

# Parts
* [Adafruit SHT40](https://learn.adafruit.com/adafruit-sht40-temperature-humidity-sensor)

# Example

```python
from sht40_micropython import SHT40

# this is example setup on the nodemcu ESP8266 board
sht40 = SHT40(scl_pin=4, sda_pin=3, freq=config.board_baud_rate)
results = sht40.measure()

print(results)
```

# References
1. [NodeMCU Micropython setup](https://icircuit.net/nodemcu-getting-started-micropython/2406)
2. [Adafruit SHT40 Tutorial](https://learn.adafruit.com/adafruit-sht40-temperature-humidity-sensor)
3. [Micropython setup instructions](https://docs.micropython.org/en/latest/develop/gettingstarted.html)
4. [Instructions for flashing nodemcu](https://www.embedded-robotics.com/esp8266-micropython/)
5. [Micropython downloads for esp8266](https://micropython.org/download/esp8266/)
6. [SHT40 datasheet](https://cdn-learn.adafruit.com/assets/assets/000/099/223/original/Sensirion_Humidity_Sensors_SHT4x_Datasheet.pdf?1612388531)
7. [adafruit circuit python sht40](https://github.com/adafruit/Adafruit_CircuitPython_SHT4x)