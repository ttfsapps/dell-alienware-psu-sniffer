# Dell/Alienware PSU Sniffer

Allows user to read the ID string supplied by the PSU to the Dell/Alienware notebook pc.

Dell/Alienwares read the ASCII string sent via the center pin of a genuine Dell/Alienware PSU.

The entire string is displayed for inspection and diagnosis.

The sniffer uses Onewire protocol to communicate with the PSU's DS2502 ROM. The sniffer reads and displays the ROM contents.

Tested on Arduino Mega 2560 / Elegoo 2.8" TFT Color Display Shield with dell_psu_spoofer.


## Arduino Mega and Dell PSU Connectors

>|Function|Arduino Mega Pin|Dell/Alienware Plug|
>|:--------------:|:-------------------:|:-------------------:|
>|id|22|center pin|
>|gnd|gnd|outer shell|
>|+19.5 VDC|not used|inner barrel|

## Decoding the Dell PSU ID String

The ID string is 40 characters long and contains wattage, voltage, and current specs for the PSU. 
 
>DELL00ACWWWVVVIIICN0123456789ABCDEA05

>|Field|Value|Units|
>|:-----:|:-----:|:-----:|
>|Header|DEL00AC||
>|Wattage|WWW|Watts|
>|Voltage|VVV|Volts*10|
>|Current|III|Amps*10|
>|Serial No.|CN...A05||

TTFS Apps 2026
