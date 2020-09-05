# V3 of the PCB

This is the PCB as it will be shipped in the group buy. It comes in both a solder and hotswap version. 
I've ordered a test batch from JLCPCB with these files and I'll update the readme here to confirm that it works as expected.
Either way, *order these files at your own risk*.
And most importantly, always critically review the parts placement (oftentimes the previewer on the JLCPCB website is broken, so ask for a review of the parts placement per mail!)

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
There are two versions exported, one with the crosshatched pattern on the back (shown below) and one without (shown above).
The crosshatch pattern increases the gerber filesize significantly, which made the JLCPCB gerber viewer choke completely to the point that I couldn't go through the order process properly.

![Crosshatch Back Image](https://i.imgur.com/kUrYCUo.png)

## Ordering on JLCPCB
These are the basic steps for ordering V3 PCBs from JLCPCB. Please note a couple important things: 
- If you do not pay/have them install the SMD components, you will have to order those and install them manually
- Regardless of choosing to have them install SMD components, they do not support installing the USB C port (required), LEDs (optional), or hotswap sockets (required for building hotswap PCB). These will need to be acquired and installed manually.
- Grab the latest version of the necessary files (pretty much everything in `pcb/v3` folder)
- This is DIY. You will have to solder _at least_ the USB C port. You will also have to source this (and other optional parts) yourself.
- Read through, and understand, these steps AND everything detailed on this page before continuing. Make sure you understand **and** accept all risks you are taking. This guide is to help those with questions who have never used JLPCB before. It's relevancy may change as files change OR jlcpcb's services or site change.

1. Go to [JLCPCB](http://www.jlcpcb.com).
2. Find the '2  Layers' graphic and click 'Quote Now'.
3. On the new page, click the 'Add your gerber file' button.
4. Find an select your desired file within `pcb/v3` folder (don't unzip). It will take a while to upload the file. Go grab a snack and give it some time. Good things come to those who wait.
5. After the file has finished uploading (it'll say completed and the loading bar gone), you'll likely have to manually enter the Dimensions: 115mm x 354mm. Everything else should be entered correctly.
6. If you **DO NOT** want to have jlcpcb do SMT assembly, SKIP TO STEP 10. 
7. For SMT Assembly, you'll want to select the toggle towards the bottom (SMT Assembly). If you see an error, it's likely because you skipped the step about entering dimensions above. If that wasn't it, review the error and address it. Also select the following options:
   1. 'Assemble bottom side' - needs to be selected
   2. 'SMY QTY' - set to your desired quantity
   3. 'Tooling holes' - select 'Added by JLCPCB'
   4. Once all is set, click 'Confirm' button (not the 'Next' button) It will redirect you to create an account or sign in - once done, you should be redirect back to the order page. You'll need to click 'Confirm' again.
8. You should now be on a page for uploading a 'BOM' and 'CPL' file. These files are also in the `pcb/v3` folder. Upload the correct file to it's correlating upload button. ('Add BOM File' and 'Add CPL File') and click 'Next'. Files:
   1. V3_BOM_JLC
   2. V3_CPL_JLC
9.  It should auto-find all necessary parts. You will see one item `HRO-TYPE-C-31-M-12` that says 'No part selected'. This is the USB C port which has to be acquired and installed manually. Click 'Next'.
10. If everything looks good (make sure you entered dimensions from step 5), you should be ready to 'SAVE TO CART' and continue to check out. If you didn't create an account earlier, you're going to be asked to do so before being able to checkout. 
11. Don't forget to source the USB C port you will need. You're going to need enough to cover all the PCBs you're ordering (or as many as you want to build). `HRO-TYPE-C-31-M-12` should be easily found online from multiple vendors.

### Checking DFM
Since the preview for the parts placement often fails on the JLCPCB website, it is good to check it after the JLC engineers have processed it.
To do this, click on the "DFM Analysis" on the order page, it will show something like this:

![DFM Analysis Screenshot](https://i.imgur.com/NEGX5gh.png)

Make sure that the orientation of the parts (as denoted by the red dots and the +/-) looks like this (both for hotswap and solder, click the image for a high resolution image):

[![Correct component placement](https://i.imgur.com/kTeKakSl.png)](https://i.imgur.com/kTeKakS.png)

Again, the DFM Analysis will only be made available after the engineers have processed it (can take up to 24h). The actual pick and place process only starts after the PCB is manufacuterd, so you have some time to check this for errors. I usually just send them a mail to hold on the Pick'n'Place until I got a chance to verify the DFM.
