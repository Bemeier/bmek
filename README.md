# Hardware for BMEK - Bemeier Ergonomic Keyboard

![First Alu Prototype](https://i.imgur.com/g2n1SY1.jpg)

BMEK is an ergonomic keyboard in the spirit of [Lyn's EM7](https://geekhack.org/index.php?topic=83328.0) and [TGR Alice](https://geekhack.org/index.php?topic=95009.0).
Notable differences are the [HHKB-like](https://www.hhkeyboard.com/) layout and the and the more symmetric looks due to the space bars and left key cluster arrangement.

- [Geekhack Thread](https://geekhack.org/index.php?topic=103032.0)
- [Discord Server](https://discord.gg/BFZNmtM)
- [More Pictures 1](https://imgur.com/a/tHlaMWA)
- [More Pictures 2](https://imgur.com/a/MdbbHqe)

## UPDATES & GROUPBUY COMING!

Before you jump in and start making your own case, consider checking out the [Progress Thread](https://geekhack.org/index.php?topic=103032.0), and join the [Discord Server](https://discord.gg/BFZNmtM). There will also be a small group-buy for aluminum cases, plates and PCBs ([Interest Check](https://geekhack.org/index.php?topic=107203.0)). In the course of this group buy there will also be some changes made to the design that have not (all) been pushed to this repository yet, so you might want to wait for these to land before building your own.

## Layout

The main key layout (besides the extra 4 key-cluster on the left) is almost exactly the [Layout of the HHKB](https://deskthority.net/wiki/HHKB_Professional2). The only changes are in the bottom row:

- The 1.5u modifiers are replaced by 1.25u modifiers
- The single spacebar is replaced by two smaller ones

### Layout with PCB V2 + V2.1

These versions of the PCB only support the fixed layout as described above. Note that you'll need 2x2.75 spacebars. Most GMK (spacebar) kits only come with one, but you can always use a 2.75u or 2.25 shift key or spacebar and live with a little gap :)

### Layout with PCB V3

The upcomming V3 of the PCB will support a 2u backspace option, as well as 2.25u/2.75u layout options for the spacebars (the new version of the case comes with a "blocker" to fill in the gap that is created when using the 2.25u spacebar) and an option to use full or split rshift.

## Firmware

Setup QMK and run `make bemeier/bmek:default`

Alternatively you can download and flash the precompiled firmware from the [Releases](https://github.com/Bemeier/bmek/releases) section. Firmware Source: [TODO: Release](https://github.com/qmk/qmk_firmware/tree/master/keyboards/bemeier/bmek), [Dev](https://github.com/Bemeier/qmk_firmware/tree/bemeier/keyboards/bemeier/bmek)

## PCB

### V2 & V2.1

With this version, both hot-swap sockets and permanent soldering are supported. Connector is USB-C, and is confirmed to also work with USB-C to USB-C cables.

The PCB design was based on the schematics from the [Goldfish](https://github.com/Dr-Derivative/Goldfish) controller.

All Gerber & BOM files needed for ordering at JLCPCB are under [pcb](https://github.com/Bemeier/bmek/tree/master/pcb).
It can be ordered with pick-and-place assembly. Only top-mounted LEDs (optional), hot-swap sockets (optional) and USB-C connector need to be ordered separately and soldered by hand.

![PCBv2 top](https://i.imgur.com/iHjo18j.jpg)
![PCBv2 bottom](https://i.imgur.com/7royTzh.jpg)

### Differences between PCB v2 and v2.1

PCB v2.1 adds some changes to fit the new plate-based design. Namely cutouts to access the scews that mount the plate to the top-case. Note that these are not strictly required to build the new case, but it is a bit more convenient (in case you want to swap out your plate+switch+pcb assembly without desoldering everything).

### V3

Version 3 of the PCB comes in either hotswap or solder version, not in a combined version. It includes the extra cutouts for the plate screws from v2.1. It further comes with these changes compared to v2.x:

- Layout option backspace: 2u Backspace and 2x 1u hhkb-like
- Layout options bottom row: Each of the 2.75u spacebarss can be replaced with a 2.25u spacebar for better keyset compatibility.
- ESD protection circuity
- Switched to the popular, cheaper and easier to hand-solder HRO-TYPE-C-31-M-12 USB-C receptacle
- Made completely from scratch in KiCad (project will be released as soon as design is verified)

## Cases

### Integrated Case

3D models for a 2-piece high profile case with integrated plate mounts (intended for CNC-machining from polycarbonate or aluminium) are under [cases/old_integrated_plate_case](https://github.com/Bemeier/bmek/tree/master/cases/old_integrated_plate_case).

![BMEK](https://i.imgur.com/3rHByZJ.jpg)
![Case Assembled](https://i.imgur.com/5wR5hRO.jpg)

### Top-mounted plate Case

A top-mounted version of the original case is being designed under [cases/top_mount](https://github.com/Bemeier/bmek/tree/master/cases/top_mount). This is the case I would recommend building - especially if you want to 3D print parts, I'd suggest to print top and bottom case, but get the plate cut/machined from metal (as this is the part where the tolerances are most important.

![Top Mounted 1](https://i.imgur.com/kyHzoL8.png)
![Top Mounted 2](https://i.imgur.com/Dd6fttt.jpg)
![Top Mounted 3](https://i.imgur.com/lirDxdv.jpg)

### Lasercut Case

Lasercut Case material Acrylic. made by [tahutech](https://github.com/TahuTech)

![Lasercutcase](https://github.com/TahuTech/bmek/blob/master/cases/Lasercut/Photo/case1.jpg)
![Lasercutcase](https://github.com/TahuTech/bmek/blob/master/cases/Lasercut/Photo/case.jpg)

## Disclaimer & Contributing

Obviously you will be building the PCB or case at your own risk, but feel free to reach out if you need help or want to contribute. Check out the [geekhack thread](https://geekhack.org/index.php?topic=103032.0), [Discord Server](https://discord.gg/BFZNmtM), or use the issue system on this repository.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">BMEK Mechanical Keyboard</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://github.com/Bemeier/bmek" property="cc:attributionName" rel="cc:attributionURL">Jan Kolkmeier</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
