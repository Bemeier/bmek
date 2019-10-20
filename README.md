# Hardware for BMEK - Bemeier Ergonomic Keyboard

![BMEK](https://i.imgur.com/ZM27uPo.jpg)

| WARNING: WORK IN PROGRESS! |
| --- |

BMEK is an ergonomic keyboard in the spirit of [Lyn's EM7](https://geekhack.org/index.php?topic=83328.0) and [TGR Alice](https://geekhack.org/index.php?topic=95009.0).
Notable differences are the more [HHKB-like](https://www.hhkeyboard.com/) layout, the mirrored space-bar layout and the 4 extra keys on the left for better symmetry.

## Firmware
Setup QMK and run `make bemeier/bmek:default`
[Release](https://github.com/qmk/qmk_firmware/tree/master/keyboards/bemeier/bmek), [Dev](https://github.com/Bemeier/qmk_firmware/tree/bemeier/keyboards/bemeier/bmek)

## PCB
The current version of the PCB only allows for the HHKB-like layout shown above.
Both hot-swap sockets and permanent soldering are supported. USB-C socket, confirmed to work with USB-C to USB-C cable.

All Gerber & BOM files needed for ordering at JLCPCB are under `pcb/jlcpcb`. It can be ordered with pick-and-place. Only top-mounted LEDs (optional), hot-swap sockets (optional) and USB-C connector need to be ordered separately and soldered by hand.

The PCB design was based on the schematics from the [Goldfish](https://github.com/Dr-Derivative/Goldfish) controller.
PCB source files will be released later.

## BOM 
TODO

LEDs...
[USB-C Connector](https://katalog.we-online.de/en/em/COM_3_1_THR_SMT_TYPE_C_RECEPTACLE_HORIZONTAL)
[Kailh PCB Sockets](https://novelkeys.xyz/products/kailh-pcb-sockets)

## Cases
A 2-pieces high profile case with integrated plate mounts (intended for CNC-machining from Polycarbonate & Aluminium) can be found under `cases/highprofile`.
At a later point, SVGs for a lasercut case will be made available under `cases/lasercut`. 

## License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">BMEK Mechanical Keyboard</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://github.com/Bemeier/bmek" property="cc:attributionName" rel="cc:attributionURL">Jan Kolkmeier</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
