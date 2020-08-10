# V3 of the PCB

This is the PCB as it will be shipped in the group buy. It comes in both a solder and hotswap version. 
I've ordered a test batch from JLCPCB with the files from this commit: https://github.com/Bemeier/bmek/commit/85931f795956d60f2ae7042b2607ad3a0f845139 
I'll update the readme here to confirm that it works as expected.
Either way, *order these files at your own risk*. And most importantly, always critically review the parts placement (oftentimes the previewer on the JLCPCB website is broken, so ask for a review of the parts placement per mail!)

## Improvements over V2/2.1

- Separate design for hotswap and solder versions (to avoid the [potential interference issue](https://www.youtube.com/watch?v=Bh93sXRh4x4&vl=en) with the previously south facing  option when using hotswap sockets)
- Layout options:
  - backspace: 2u Backspace and 2x 1u hhkb-like
  - bottom row: The 2.75u spacebar can be replaced with a 2.25u spacebar for better keyset compatibility.
  - Split left shift option (ISO style)
  - 2.75u right shift option (besides the default split right shift)
- ESD protection circuity
- Switched to the popular, cheaper and easier to hand-solder [HRO-TYPE-C-31-M-12](https://lcsc.com/product-detail/USB-Type-C_Korean-Hroparts-Elec-TYPE-C-31-M-12_C165948.html) USB-C receptacle

## Kicad Project
For this version, I've also released the Kicad projects (see ../kicad/projects).

## Hotswap Version
![Hotswap Version Image](https://i.imgur.com/3CGNeox.png)

## Solder Version
![Solder Version Image](https://i.imgur.com/DP67VNZ.png)

## Crosshatch Back:
The .zip's exported here have the crosshatch pattern on the back copper layer removed (shown in the images above), as it increased the filesize significantly, which made the JLCPCB gerber viewer choke completely.
If you want to order it with the crosshatch pattern (it's purely cosmetic, see image below), you can open the Kicad project and generate the gerbers yourself.

![Crosshatch Back Image](https://i.imgur.com/kUrYCUo.png)
