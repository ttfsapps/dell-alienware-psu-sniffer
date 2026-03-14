# Onewire Sniffer for Dell PSU's

Displays Dell ID sring in hex and ASCII

Tested on Arduino Mega 2560 with Elegoo 2.8" TFT Color Display Shield and Dell_PSU_Spoofer

Version 0.0   initial release 

Version 0.1   serial port only enabled for debug - reliability

## Dell Power Adapter Barrel Connector and dell_psu_spoofer.kicad_pcb pin numbers

>|PCB Header J2 Pin No.|Dell/Alienware PSU Plug|
>|:-----:|:-----:|
>|P1|inner barrel: +19.5 VDC|
>|P2|center pin: id|
>|P3|outer shell: gnd|

## Sniffer and Dell PSU Spoofer Pins

>|Sniffer|Spoofer|
>|:--------------:|:-------------------:|
>|**ATmega Pin**|**Dell/Alienware Plug**|   
>|22|center pin: id|
>|gnd|outer shell: gnd|
>|not used|inner barrel: +19.5 VDC|

TTFS Apps 2026
