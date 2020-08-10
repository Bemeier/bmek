# Ordering v2 at JLCPCB

- **Use at your own risk.**
- This is outdated and doesn't fit the new case well due to the missing access cutouts for the plate screws. Consider making V3 instead!
- But if you must, go to [jlcpcb.com](https://jlcpcb.com) and get a quotation. Use the .zip for uploading gerber files. For assembly, use BOM_LED.csv and CPL_LED.csv.


![PCB](https://i.imgur.com/Gihmnn3.png)
![PCBv2 top](https://i.imgur.com/iHjo18j.jpg)
![PCBv2 bottom](https://i.imgur.com/7royTzh.jpg)

### BOM V2 & V2.1

**Part Detail**|**Unit Price**|**Quantity**
-----|-----|-----
Tactile Switches SPST 5.10mm x 5.10mm 0.40mm 50mA @ 12VDC SMD C318884|€0.07|1
ATMEL & AVR QFP-44\_10x10x08P C44854|€3.26|1
Multilayer Ceramic Capacitors MLCC - SMD/SMT 22pF 50V 0603 C1653|€0.01|2
Chip Resistor - Surface Mount 10KOhms ±1% 1/10W 0603 C25804|€0.00|2
Chip Resistor - Surface Mount 470Ohms ±1% 1/10W 0603 C23179|€0.02|1
Multilayer Ceramic Capacitors MLCC - SMD/SMT 100nF 50V 0603 C14663|€0.00|12
Multilayer Ceramic Capacitors MLCC - SMD/SMT 1uF 50V 0603 C15849|€0.04|1
Schottky Barrier Diodes (SBD) SOD-123 C8598|€0.14|1
Multilayer Ceramic Capacitors MLCC - SMD/SMT 4.7uF 16V 0603 C19666|€0.06|1
Switching Diode 75V 150mA 1.25V @ 150mA 4ns SOD-123 C81598|€0.01|66
Chip Resistor - Surface Mount 22Ohms ±1% 1/10W 0603 C23345|€0.01|2
SMD Crystal Resonators 16MHz ±10ppm SMD-3225\_4P C13738|€0.38|1
Chip Resistor - Surface Mount 5.1KOhms ±1% 1/10W 0603 C23186|€0.00|2
Light Emitting Diodes (LED) -WS2812B-B C114586|€0.10|6
USB-C Receptacle - 632723300011|€4.00|1


## Changelog

### PCBv2.zip (tested and works!)
- Improve decoupling capacitor positioning
- Moved atmega closer to USB port
- Added hot-swap sockets
- Top layer footprints for 6x optional WS2812b 

### PCBv1.zip
- First version
