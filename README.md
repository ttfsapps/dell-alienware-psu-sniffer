# Dell/Alienware PSU Sniffer

Allows the user to read the ID string supplied by the PSU to the Dell/Alienware notebook pc.

Dell/Alienwares read the ASCII string sent via the center pin of a genuine Dell/Alienware PSU and adjust their performance accordingly.Lack of an ID string will result in speed throtling and poor performance. 
The sniffer uses OneWire.h to communicate with and read the PSU's DS2502 ROM, which stores the Dell ID string, using Onewire protocol. The entire string is displayed in ASCII and hex for inspection and diagnosis.

Tested on Arduino Mega 2560 / Elegoo 2.8" TFT Color Display Shield with dell_psu_spoofer.

## Hardware Required
* [Arduino Mega 2560](https://store-usa.arduino.cc/products/arduino-mega-2560-rev3)<br/>
* [Elegoo 2.8" TFT Color Display Shield](https://us.elegoo.com/products/elegoo-2-8-inches-tft-touch-screen)

## Libraries Required
|Library|Function|
|:--------------:|:-------------------:|
|[OneWire.h](https://github.com/PaulStoffregen/OneWire/tree/master)|onewire library| 
|[MCUFRIEND_kbv.h](https://github.com/prenticedavid/MCUFRIEND_kbv)|graphics library| 
|[Adafruit_GFX.h](https://github.com/adafruit/Adafruit-GFX-Library)|required by MCUFRIEND_kbv.h| 
|[TouchScreen.h](https://github.com/adafruit/Adafruit_TouchScreen)|touchscreen handler| 

## Arduino Mega and Dell PSU Connectors

|Function|Arduino Mega Pin|Dell/Alienware Plug|
|:--------------:|:-------------------:|:-------------------:|
|id|22|center pin|
|gnd|gnd|outer shell|
|+19.5 VDC|not used|inner barrel|

## Decoding the Dell PSU ID String

The ID string is 40 characters long and contains wattage, voltage, and current specs for the PSU. 
 
Example: DELL00ACWWWVVVIIICN0123456789ABCDEA05

|Field|Value|Units|
|:-----:|:-----:|:-----:|
|Header|DEL00AC||
|Wattage|WWW|Watts|
|Voltage|VVV|Volts*10|
|Current|III|Amps*10|
|Serial No.|CN...A05||

TTFS Apps 2026
