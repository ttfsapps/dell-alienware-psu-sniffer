Onewire Sniffer for Dell PSU's

Displays Dell ID sring in hex and ASCII

Tested on Arduino Mega 2560 with Elegoo 2.8" TFT Color Display Shield and Dell_PSU_Spoofer

Version 0.0   initial release 

Version 0.1   serial port only enabled for debug - reliability

Dell Power Adapter PCB Header Pins and Barrel Connector

  P1 inner barrel: +19.5 VDC

  P2 center pin: id 

  P3 outer shell: gnd

Sniffer and Dell PSU Spoofer Pins

  Sniffer                 Spoofer

  ATmega Pin              ATTiny85 Pin

  22  --------------->    <-------- PB2 onewire

  GND --------------->    <-------- GND

  not used ----------X    <-------- 19.5 VDC

TTFS Apps 2026
