# Minimal Black Pill (STM32F4xx) BOB for grblHAL 
Single layer breakout board for the popular Black Pill. Features 4 axes, 5V outputs, optoisolated inputs.
Firmware: [grblHAL](https://github.com/terjeio/grblHAL)
The goal of this project was to replace a classical Grbl setup on an Arduino Uno/Nano, with minimal effort.
All inputs are mapped to one side of the board, all outputs (except spindle PWM) are on the other. 
This allows for a very clean single sided design and is very suitable milling, UV exposing or even toner transfer methods.
The only critical requirements for manufacturing - minimal separation between traces is 0.2mm.

## Feb 2021 Initial release
  * 4 Axis outputs
  * 10 5V buffered outputs (XYZA step/dir outputs, single source-multiple buffered outputs enable, spindle PWM and enable, mist, flood)  
  * 8 Opto-isolated inputs (mapped to XYZ limits, probe, halt, pause, start, safety door)
  * External supply connectors. Can be powered by USB, external 5V or external 12V-24V (depending on the Vreg). 
  * All I/O done on 3.5mm pitch connectors.
![T4.1 BreakuoutBoard](https://github.com/phil-barrett/grbl-teensy-4/blob/master/RA159231_DxO_2048.jpg "V2.09 Unkit PCB")

