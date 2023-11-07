# PCBs

These are the PCB files. All PCBs so far have been manufactured at JLCPCB, so I include the JLCPCB SMT BOM and placement files (except for the V0.8-series, which are getting prototyped with Elecrow thanks to RNDKBD). Elecrow files are also provided for V0.6.1D and V0.7J. 

The PCBs are compatible only with MX-format switches and PCB-mount stabilizers. Washers should not be necessary for screw-in stabilizers.

These files require  KiCAD V7 to open. These files use the [Alexandria (Acheron) library](https://github.com/AcheronProject/AlexandriaLibrary) from Gondolindrim's [Acheron Project](https://acheronproject.com/). To configure that library correctly in KiCAD, you will need to go to Preferences > Configure Paths, and add "ALEXANDRIA" to the Name column and the location of the Alexandria library folder in Path column. 

The 3D-printed version uses the -J series PCBs, which have a USB port and ESD protection built-in. The CNC version (and Technofrikus's 3D-printed version) uses the -D series PCBs, which are for use with an external daughterboard.
V0.8 is the next version that's currently being worked on. On the daughterboard version, this switches over to a 4-pin Molex Pico-EZmate for use the newer S1 daughterboard. 

# Changelog

## Current PCBs

### CNC version PCBs
| Version   | Type     | Daughterboard connector               | Supported layouts | Design status                 | Elecrow Files Status          | JLCPCB Files Status                                             |
| --------- | -------- | ------------------------------------- | ----------------- | ----------------------------- | ----------------------        | --------------------------------------------------------------- |
| V0.6.1D   | Soldered | JST SH (for UDB C3 and earlier)       | All               | Done and prototyped           | Done, not prototyped          | Done and prototyped (no RGBLED), not prototyped (RGBLED)        | 
| V0.8D     | Soldered | Molex Pico-EZmate (for UDB S1 and C4) | All               | Done and prototyped by RNDKBD | Done and prototyped by RNDKBD | Done, not prototyped                                            | 
| V0.8.2DHA | Hotswap  | Molex Pico-EZmate (for UDB S1 and C4) | ANSI              | Done and prototyped by RNDKBD | Done and prototyped by RNDKBD | Done, not prototyped                                            | 
| V0.8.2DHI | Hotswap  | Molex Pico-EZmate (for UDB S1 and C4) | ISO               | Initial draft done            | Done, not prototyped          | Not yet started                                                 | 

### 3DP version PCBs
| Version   | Type     | Supported layouts | Reset button location | Design status                 | Elecrow Files Status          | JLCPCB Files Status  |
| --------- | -------- | ----------------- | --------------------- | ----------------------------- | ----------------------        | -------------------- |
| V0.7J     | Soldered | All               | Bottom                | Done and prototyped           | Done and prototyped           | Done and prototyped  | 
| V0.8J     | Soldered | All               | Top                   | Done and prototyped by RNDKBD | Done and prototyped by RNDKBD | Not yet started      | 
| V0.8.2JHA | Hotswap  | ANSI              | Top                   | Done and prototyped by RNDKBD | Done and prototyped by RNDKBD | Not yet started      | 
| V0.8.2JHI | Hotswap  | ISO               | Top                   | Not yet started               | Not yet started               | Not yet started      | 

### J-variant (integrated USB port, JLCPCB SMT-assemblable, used on the 3D-printed version)

* V0.8J - March 28, 2023. Soldered PCB. The reset button has been moved to the top side of the board, underneath the right shift key (just like on the CNC version). Design is done and is awaiting prototyping. 

* V0.8.2JHA - May 19, 2023. ANSI hotswap variant for the 3D printed version. This does not support backlight LEDs. Flipped the spacebar stab footprints so that the stab wire no longer hits the plate. Fixed some minor silkscreen issues.

### D-variant (uses a daughterboard, used on the CNC version, and Technofrikus' 3D printed version)

* V0.8D - March 19, 2023. Soldered PCB. Adds a clamping diode to slightly improve ESD protection over V0.6.1D. Switches to the Molex Pico-EZmate connector for compatibility with the new [Unified S1 Daughterboard](https://unified-daughterboard.github.io/#/db-spec-s) and [C4 daughterboard](https://unified-daughterboard.github.io/#/db-spec-c). Added reverse polarity protection as Molex Pico-EZmate cables often have the wrong pinout for use with Unified Daughterboards and can cause PCB damage.  Design done; awaiting prototyping. 

* V0.8.2DHA - May 19, 2023. ANSI hotswap variant for the CNC version. Has a Molex Pico-EZmate connector for use with the Unified S1 or C4 daughterboards. Flipped the spacebar stab footprints so that the stab wire no longer hits the plate like on V0.8.1DHA

* V0.8.2DHI - June 4, 2023. ISO hotswap variant. Not yet prototyped. 

## Works in Progress

### J-variant (integrated USB port, used on the 3D-printed version)

* V0.8.2JHI - ISO hotswap variant of V0.8.2JHA. Design not yet started.

## Previous PCBs

### J-variant (integrated USB port, JLCPCB SMT-assemblable, used on the 3D-printed version)

* V0.8.1JHA - April 5, 2023. ANSI hotswap variant of V0.8J. This does not support backlight LEDs. Fixed an issue on V0.8JHA where there was a spot of exposed solder mask underneath F11 tht can cause +3.3V to short to ground easily.
***Note - this has an error where the spacebar stabilizers also are upside down relative to the plate and the stab wire will hit the plate and cause noise, though everything still works and you can file small notches into the stab cutouts to get rid of the noise***

* V0.8JHA - March 27, 2023 ANSI hotswap variant of V0.8J. To make routing the hotswap sockets easier I eliminated the optional through-hole backlight LEDs (as they're not useful on a hotswap board anyways). Will have to be split up into ANSI and ISO versions. Initial draft of the design done; still need to error check. Design is done and is awaiting prototyping. 
***Note - this has an error where there is a piece of exposed solder mask underneath F11 that can cause +3.3V to short to ground easily. This is fixed in V0.8.1JHA. The spacebar stabilizers also are upside down relative to the plate and the stab wire will hit the plate and cause noise, though everything still works and you can file small notches into the plate to get rid of the noise***

* V0.7J - May 16, 2022.  This added access holes to the PCB to allow access to the screws that hold the key separators on the 3D printed version. On V0.6.1J and earlier these screw heads are not accessible, and means that the key separators cannot be removed or adjusted after the PCB is soldered. Some components had to be moved around to achieve that. V0.7J also added a place to solder on pogo pins (or a piece of wire) for grounding the plate and top side screws on the 3D-printed case. This is prototyped and working. RNDKBD used this version for Round 2 of their group buy. 

* V0.6.1J - November 28, 2021. This removed a couple of loops on the backlight LEDs near the numpad, and added some more ground vias for EMI purposes. Prototyped and working (though backlight LEDs have not been tested). RNDKBD used this PCB for Round 1 of their group buy.  

* V0.6J - October 15, 2021 - this version is designed to have all SMT parts be assemblable on JLCPCB. To achieve this, the 5V->3.3V conversion is done by a linear regulator rather than a switching regulator, and the LEDs are powered off 5V instead of 3.3V originally. Other changes include using Gondolindrim's improved STM32 reset circuit, and implementing EMI best-practices such as ground plane stitching and ground plane vias in case it needs to pass FCC/CE EMI testing. This has a return loop on the upper right numpad backlight LEDs, though it is unclear if this is an issue (especially if the backlight is not used), as this version was never prototyped.

* V0.5.2 - October 6, 2020 - Removed a loop in the ground plane (which did not seem to affect functionality), and made some minor changes to the silkscreen. Increased thermal clearances around the RGBLED to make it easier to solder. Minor silkscreen fixes. Tested and working. People who bought Round 0 barebones kits received this PCB.  JLCPCB at the time was not able to solder on connectors, and was out of stock of STM32F072 microcontrollers, so those parts are not included on the manufacturing files and were soldere on by hand. JLCPCB also did not carry the fuse, the AP63203WU-7 buck controller, or the buck controller inductor, so those parts are not included in the manufacturing files for JLCPCB SMT, and were soldered on by hand. 

* V0.5.1 - September 23, 2020 - this fixed the routing errors in V0.5, and slightly improved the silkscreen graphics. The grounding screw hole is now connected to ground via a ferrite bead. Tested and working. Beta testers received fixed V0.5 and V0.5.1 boards.

* V0.5 - September 16, 2020 - added split space and WKL support, a grounding pad for the CNC case, changed silkscreen somewhat, and changed the microcontroller footprint to be able to take both LQFP-48 and UFQFPN48 due to shortages of LQFP48 STM32F072's. This had several routing errors and requires some fixes for all features to work.

* V0.4 - August 11, 2020 - a complete redesign. Placed everything on a single PCB, with a centered USB-C port. The F-key clusters are moved slightly closer to the main alpha keys. Switched to SMD diodes. Designed for both a 3D-printed/FR4 case, and a CNC metal case. Working. 

* V0.3 and earlier - these used a two-PCB design, with microcontroller, USB port, and associated components on the daughterboard, and a completely through-hole main PCB. Used with the earliest prototypes. Not compatible with the published case designs. The firmware is largely similar, though the matrix is different.

### D-variant (uses a daughterboard, used on the CNC version, and Technofrikus' 3D printed version)

* V0.8.1DHA - April 5, 2023. ANSI hotswap variant of V0.8J. This does not support backlight LEDs. Fixed an issue on V0.8DHA where there was a spot of exposed solder mask underneath F11 tht can cause +3.3V to short to ground easily.
***Note - this has an error where the spacebar stabilizers also are upside down relative to the plate and the stab wire will hit the plate and cause noise, though everything still works and you can file small notches into the stab cutouts to get rid of the noise***

* V0.8DHA - March 28, 2023. ANSI hotswap variant. Adds hotswap sockets. Switches to the Molex Pico-EZmate connector for compatibility with the new [Unified S1 Daughterboard](https://unified-daughterboard.github.io/#/db-spec-s) and [C4 daughterboard](https://unified-daughterboard.github.io/#/db-spec-c). Added reverse polarity protection as Molex Pico-EZmate cables often have the wrong pinout for use with Unified Daughterboards and can cause PCB damage. Also has some changes to the diodes to try to slightly improve ESD protection over V0.6.1D. To make routing the hotswap sockets easier I eliminated the optional through-hole backlight LEDs (as they're not useful on a hotswap board anyways). Design done; awaiting prototyping. ***Note - this has an error where there is a piece of exposed solder mask underneath F11 that can cause +3.3V to short to ground easily. This is fixed in V0.8.1DHA. The spacebar stabilizers also are upside down relative to the plate and the stab wire will hit the plate and cause noise, though everything still works and you can file small notches into the plate to get rid of the noise***

Note that V0.7D was skipped to line up the versioning between the J- and D- variants.

* V0.6.1D - February 5, 2022. Has a JST connector for use with the C3 Unified Daughterboard. Fixed the incorrect silkscreen on the RGBLED (LED702), which had the arrow on pin 1 instead of pin 3. This was done by switching to Acheron's LED footprint instead of using KiCAD's default footprint. There is a very slight difference in the ground fill around LED702 (which is due to the Acheron footprint not having a keepout zone for ground fills, so I added one manually to keep the PCB as identical as posible to V0.6D). Prototyped and working (though backlight LEDs have not been tested) 

* V0.6D - January 5, 2022. This is meant for the redesigned CNC version of Boston, and is meant to be used with a daughterboard (using the standard 4-pin JST connector). All ESD protection has been moved off to the daughterboard, moves the reset button to the top side of the PCB near Right Shift, and uses a reverse-mount RGBLED (meant to be used with a light pipe on the case) instead of a through-hole one. Otherwise very similar to V0.6.1J, and can run identical firmware as the matrix is identical. The silkscreen on the RGBLED (LED702) was incorrect (the arrow was on pin 1 instead of pin 3). Otherwise working. 
