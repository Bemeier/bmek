# Hardware for BMEK - Bemeier Ergonomic Keyboard

![BMEK](https://i.imgur.com/ZM27uPo.jpg)

| WARNING: WORK IN PROGRESS! |
| --- |

BMEK is an ergonomic keyboard in the spirit of [Lyn's EM7](https://geekhack.org/index.php?topic=83328.0) and [TGR Alice](https://geekhack.org/index.php?topic=95009.0).
Notable differences are the more [HHKB-like](https://www.hhkeyboard.com/) layout, the mirrored space-bar layout and the 4 extra keys on the left for better symmetry.

## PCB

The current version of the PCB only allows for the HHKB-like layout, as shown above.
Both hot-swap sockets and permanent soldering are supported. Connector is USB-C, and is confirmed to also work with USB-C to USB-C cables.

The PCB design was based on the schematics from the [Goldfish](https://github.com/Dr-Derivative/Goldfish) controller.
PCB source files will be released later.

## BOM 

All Gerber & BOM files needed for ordering at JLCPCB are under `pcb/jlcpcb`. It can be ordered with pick-and-place.
SMD part costs from jlcpcb quotation (ordering 5 PCBs with pick & place).
Only top-mounted LEDs (optional), hot-swap sockets (optional) and USB-C connector need to be ordered separately and soldered by hand.
Ordering 5 boards, the cost comes around to ~12$, including assembly (excluding USB-C connector and other optional parts).

**Part**|**#**|**Part ID**|**Cost**|**Total**
:-----:|:-----:|:-----:|:-----:|:-----:
[ATmega32U4-AU](https://lcsc.com/product-detail/ATMEL-AVR\_ATMEL\_ATMEGA32U4-AU\_ATMEGA32U4-AU\_C44854.html)|1|C44854|$3.30|$3.30
[Oscillator 16MHz 18pF](https://lcsc.com/product-detail/SMD-Crystal-Resonators\_Yangxing-Tech-X322516MLB4SI\_C13738.html)|1|C13738|$0.10|$0.10
[Reset Switch](https://lcsc.com/product-detail/Tactile-Switches\_XKB-Enterprise-TS-1187-B-A-A\_C318884.html)|1|C318884|$0.02|$0.02
[Schottky Diode](https://lcsc.com/product-detail/Schottky-Barrier-Diodes-SBD\_Changjiang-Electronics-Tech-CJ-B5819W\_C8598.html)|1|C8598|$0.04|$0.04
[Switching Diodes](https://lcsc.com/product-detail/Switching-Diode\_1N4148W\_C81598.html)|66|C81598|$0.02|$1.32
[5.1KΩ](https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount\_Uniroyal-Elec-0603WAF5101T5E\_C23186.html)|2|C23186|$0.01|$0.02
[10KΩ](https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount\_Uniroyal-Elec-0603WAF1002T5E\_C25804.html)|2|C25804|$0.01|$0.02
[22Ω](https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount\_Uniroyal-Elec-0603WAF220JT5E\_C23345.html)|2|C23345|$0.01|$0.02
[0.1uF](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT\_100nF-104-10-50V\_C14663.html)|12|C14663|$0.01|$0.12
[4.7uF](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT\_SAMSUNG\_CL10A475KO8NNNC\_4-7uF-475-10-16V\_C19666.html)|1|C19666|$0.39|$0.39
[22pF](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT\_SAMSUNG\_CL10C220JB8NNNC\_22pF-220-5-50V\_C1653.html)|2|C1653|$0.02|$0.04
[1uF](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT\_SAMSUNG\_CL10A105KB8NNNC\_1uF-105-10-50V\_C15849.html)|1|C15849|$0.01|$0.01
[Kailh PCB Sockets](https://kbdfans.com/products/mechanical-keyboard-switches-kailh-pcb-socket)|66|PG151101S11|$0.10|$6.60
[USB-C Receptacle](https://www.digikey.nl/product-detail/en/w-rth-elektronik/632723300011/732-9618-1-ND/5806673?cur=USD&lang=en)|1|632723300011|$4.40|$4.40
[WS2812b](https://lcsc.com/product-detail/Light-Emitting-Diodes-LED_5050-RGBIntegrated-Light-4Pin_C114586.html)|6|C114586|$0.10|$0.60
 | | | | | 
 | | | |**Total:**|**$17.00**

## Firmware

Setup QMK and run `make bemeier/bmek:default`  

Source: [Release](https://github.com/qmk/qmk_firmware/tree/master/keyboards/bemeier/bmek), [Dev](https://github.com/Bemeier/qmk_firmware/tree/bemeier/keyboards/bemeier/bmek)

## Cases

A 2-pieces high profile case with integrated plate mounts (intended for CNC-machining from Polycarbonate & Aluminium) can be found under `cases/highprofile`.
At a later point, SVGs for a lasercut case will be made available under `cases/lasercut`. 

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">BMEK Mechanical Keyboard</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://github.com/Bemeier/bmek" property="cc:attributionName" rel="cc:attributionURL">Jan Kolkmeier</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
