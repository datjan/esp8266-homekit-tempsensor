# esp8266-homekit-tempsensor
This is a native HomeKit temperature sensor with D1 mini ESP8266 and DS18B20 sensor in celsius.

## Hardware
The following hardware is required:
```
- D1 mini (ESP8266)
- Temperature sensor (DS18B20)
```

Connection:
D1 mini -> DS18B20
```
5V -> VCC (red)
GND -> GND (black)
D4 -> DQ (yellow)
```
![alt text](https://github.com/datjan/esp8266-homekit-tempsensor/blob/main/Schema.png?raw=true)

## Development
This sketch is for following development environment
```
Arduino
```

Following libraries are required
```
https://github.com/datjan/Arduino-HomeKit-ESP8266 (fork from Mixiaoxiao/Arduino-HomeKit-ESP8266:master)
https://www.arduinolibraries.info/libraries/one-wire
https://www.arduinolibraries.info/libraries/dallas-temperature
```

## Setup
Setup my_accessory.c:
```
.password = "123-55-222". // Homekit Code
```

Setup wifi_info.h
```
const char *ssid = "xxx"; // SETUP Wlan ssid
const char *password = "xxx"; // SETUP Wlan password
```

## Upload to device
Following files needs to be uploaded to the ESP8266 (D1 mini)
```
esp8266-homekit-tempsensor.ino
my_accessory.c
wifi_info.h
```

## Add device to Homekit
The device can be added to homekit like every other homekit device.
