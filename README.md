# Hardware for BMEK - Bemeier Ergonomic Keyboard

![BMEK](https://i.imgur.com/3rHByZJ.jpg)


BMEK is an ergonomic keyboard in the spirit of [Lyn's EM7](https://geekhack.org/index.php?topic=83328.0) and [TGR Alice](https://geekhack.org/index.php?topic=95009.0).
Notable differences are the more [HHKB-like](https://www.hhkeyboard.com/) layout and the and the more symmetric looks due to the space bars and left key cluster arrangement.

[Geekhack Thread](https://geekhack.org/index.php?topic=103032.0), [More Pictures 1](https://imgur.com/a/tHlaMWA), [More Pictures 2](https://imgur.com/a/MdbbHqe), 

## Layout

In the current version, only a HHKB-style layout ([KLE](http://www.keyboard-layout-editor.com/#/gists/ae301a4ba7e58ec17bfcf9b79da94a00)) is supported - no iso enter, no 2u spacebar for now.
Also note that you'll need 2x2.75 spacebars. Most GMK (spacebar) kits only come with one, but you can always use a shift key, or use a 2.25u spacebar and live with a little gap :)

## Firmware

Setup QMK and run `make bemeier/bmek:default`  

Source: [TODO: Release](https://github.com/qmk/qmk_firmware/tree/master/keyboards/bemeier/bmek), [Dev](https://github.com/Bemeier/qmk_firmware/tree/bemeier/keyboards/bemeier/bmek)

## PCB

Both hot-swap sockets and permanent soldering are supported. Connector is USB-C, and is confirmed to also work with USB-C to USB-C cables.

The PCB design was based on the schematics from the [Goldfish](https://github.com/Dr-Derivative/Goldfish) controller.

All Gerber & BOM files needed for ordering at JLCPCB are under [pcb/jlcpcb](https://github.com/Bemeier/bmek/tree/master/pcb/jlcpcb).
It can be ordered with pick-and-place assembly. SMD part costs from jlcpcb quotation (ordering 5 PCBs with pick & place).
Only top-mounted LEDs (optional), hot-swap sockets (optional) and USB-C connector need to be ordered separately and soldered by hand.
When ordering 5 boards (MOQ), the cost comes out to ~12$ per board, including assembly, but excluding USB-C connector and LEDs.

Fully working PCBv2:

![PCBv2 top](https://i.imgur.com/iHjo18j.jpg)
![PCBv2 bottom](https://i.imgur.com/7royTzh.jpg)

### BOM

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

## Cases

3D models for a 2-piece high profile case with integrated plate mounts (intended for CNC-machining from polycarbonate & aluminium) are under [cases/highprofile](https://github.com/Bemeier/bmek/tree/master/cases/highprofile).
I'll also eventually release the entire Fusion360 project at a later point, as well as lasercut plate and case files ([cases/lasercut](https://github.com/Bemeier/bmek/tree/master/cases/lasercut)).

![Case Assembled](https://i.imgur.com/5wR5hRO.jpg)

## Contributing

Check out the [geekhack thread](https://geekhack.org/index.php?topic=103032.0), or use the issue system on this repository.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">BMEK Mechanical Keyboard</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://github.com/Bemeier/bmek" property="cc:attributionName" rel="cc:attributionURL">Jan Kolkmeier</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
