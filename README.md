# Minimal Black Pill (STM32F4xx) BOB for grblHAL 
Single layer breakout board for the popular Black Pill (*NOT Blue Pill*). Features 4 axes, 5V outputs, optoisolated inputs.

Firmware: [grblHAL](https://github.com/terjeio/grblHAL)

The goal of this project was to replace a classical Grbl setup on an Arduino Uno/Nano, with minimal effort and minimal features (which is enough for most honny machines anyway).
All inputs are mapped to one side of the board, all outputs (except spindle PWM) are on the other. 
This allows for a very clean single sided design and is very suitable milling, UV exposing or even toner transfer methods.
The only critical requirements for manufacturing - minimal separation between traces is 0.2mm.

## Feb 2021 Initial release
  * 4 Axis outputs
  * 10 5V buffered outputs (XYZA step/dir outputs, single source-multiple buffered outputs enable, spindle PWM and enable, mist, flood)  
  * 8 Opto-isolated inputs (mapped to XYZ limits, probe, halt, pause, start, safety door)
  * External supply connectors. Can be powered by USB, external 5V or external 12V-24V (depending on the Vreg). 
  * All I/O done on 3.5mm pitch connectors.
![Top view](https://github.com/avizienis/Minimal-Black-Pill--STM32F4xx-BOB-for-grblHAL/blob/main/Images/Mini%20BP%20BOB%20PCB%20top.png?raw=true)
![Bottom view](https://github.com/avizienis/Minimal-Black-Pill--STM32F4xx-BOB-for-grblHAL/blob/main/Images/Mini%20BP%20BOB%20PCB%20bottom.png?raw=true)
![Assembled](https://github.com/avizienis/Minimal-Black-Pill--STM32F4xx-BOB-for-grblHAL/blob/main/Images/Assembled.jpg?raw=true)
![Control box](https://github.com/avizienis/Minimal-Black-Pill--STM32F4xx-BOB-for-grblHAL/blob/main/Images/Controller%20box.jpg?raw=true)

## Notes

### Vreg can be a simple 7805 or as in my implementation (also see images folder) - a tiny DC-DC converter. The latter happily accepts up to 24V input.
![DC-DC converter](https://github.com/avizienis/Minimal-Black-Pill--STM32F4xx-BOB-for-grblHAL/blob/main/Images/buck_converter.jpg?raw=true)

### This is only tested on genuine [WeAct Black Pill V3](https://github.com/WeActTC/MiniF4-STM32F4x1).
Other/older versions of the board can have slightly different mappings.
Also I've read that blocking USB power diodes are not present on some older variants of the board.
If so, when using external supply microcontroller's 5V lines should not be connected to the main board.

