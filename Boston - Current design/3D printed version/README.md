# 3D printed version

These are the files for the 3D printed version. 

![3D-printed, white](https://github.com/bluepylons/Boston/blob/main/graphics/3D-printed-prototype.JPG?raw=true)
![3D-printed,purple](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-top.JPG?raw=true)
![3D-printed,purple,bottom](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-bottom.JPG?raw=true)

The master CAD assembly is Boston-3D-printed-case.stp. The case was done with a mix of Fusion 360 and later Atom3D (after I decided to stop paying for Fusion) - due to the mix of CAD programs used the master file is actually not particularly editable, so I decided to just provide it as a STEP file that can be opened in any CAD program.

If you have access to a large printer (capable of 405mm on one axis), Technofrikus designed an alternative 3D-printed case using the CNC version files. A 4° option is available for that case. The files for that version are [available on Technofrikus' GitHub repo here](https://github.com/Technofrikus/Boston-Case/blob/main/Photos/DSCF7709%201.jpg?raw=true).

# Ordering guide - (draft)

This is how to order the parts to make a 3D-printed Boston.

**Order parts at your own risk. These files are provided as-is, and I am not responsible for any losses, harm, or damage incurred by following this guide, by ordering parts, by using the files provided, by using the resultant parts or assembled keyboard, or from any mistakes or errors in the files, ordering guide, or resultant parts** 

You will need the following:

## What You Will Need (summary):
| Description                                                            | Qty per board | Type                     |
| ---------------------------------------------------------------------- | ------------- | ------------------------ |
| Case Left Half                                                         | 1             | Custom (3D Printed)      |
| Case Right Half                                                        | 1             | Custom (3D Printed)      |
| Left Key Separator                                                     | 1             | Custom (3D Printed)      |
| Right Key Separator                                                    | 1             | Custom (3D Printed)      |
| 3mm LED spacer (for lock LEDs)                                         | 1             | Custom (3D Printed)      |
| (optional) RGB LED spacer (for lock LEDs)                              | 1             | Custom (3D Printed)      |
| (optional) Knob Spacer                                                 | 1             | Custom (3D Printed)      |
| PCB                                                                    | 1             | Custom (PCB)             |
| FR4 Plate                                                              | 1             | Custom (PCB)             |
| FR4 Bottom Panel                                                       | 1             | Custom (PCB)             |
| FR4 rubber feet holders                                                | 2             | Custom (PCB)             |
| (optional) APA106 RGBLED                                               | 1             | Off-the-shelf            |
| Reset Switch (6x6mm 5mm tall tact switch)                              | 1             | Off-the-shelf            |
| 3mm LED for lock LEDs                                                  | 3             | Off-the-shelf            |
| 1KΩ through-hole resistor for lock LEDs                                | 3             | Off-the-shelf            |
| Alps EC11E18244A5 encoder                                              | 1             | Off-the-shelf            |
| M3x0.5 6mm long button head screw                                      | 8             | Off-the-shelf            |
| M3x0.5 10mm long button head screw                                     | 15            | Off-the-shelf            |
| M3x0.5 hex nut                                                         | 12            | Off-the-shelf            | 
| M2 5mm long self-tapping screw                                         | 14            | Off-the-shelf            |
| PEM KF2-M3-ET threaded insert                                          | 11            | Off-the-shelf            |
| 3/8" diameter rubber feet                                              | 4             | Off-the-shelf            | 
| Knob that fits a 6mm D-shaft                                           | 1             | Off-the-shelf            |
| Mill-Max 821-22-002-10-000101 "pogo pins" (or a short piece of wire)   | 1             | Off-the-shelf            |

| Description                                  | Qty per board                                 | 
| -------------------------------------------- | --------------------------------------------- | 
| MX-style switches                            | 119-127 (depending on layout)                 |  
| Stabilizers (PCB mount)                      | 2-8 2u, 0-1 6.25u or 7u (depending on layout) |


# PCB

![PCB V0.7J top](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-top.png)
![PCB V0.7J bottom](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-bottom.png)

For the PCB - you can order an assembled PCB with the surface mount parts soldered on (minus through-hole parts such as the encoder, RGBLED, and reset switch) from a PCB fab such as JLCPCB or Elecrow.

## How to order on JLCPCB

JLCPCB is cheap and fast, but doesn't have the best cosmetic finish, and their SMT assembly is limited to parts [they stock](https://jlcpcb.com/parts). In the community they tend to only be used for prototypes.

To order a PCB from JLCPCB, you will need the Gerber files (which defines the bare PCB), the PCB assembly bill of materials (BOM file, which is a list of parts that are to be soldered to the PCB), and the component placement file (CPL, which defines where those parts go). The files for PCB revision V0.7J are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.7J/Manufacturing%20files). **Order at your own risk. V0.7J has been prototyped and is used in RNDKBD's Round 2 group buy, though the backlight LEDs on V0.7J have not been tested**

First, you want to go to [JLCPCB](https://jlcpcb.com/), and press "Order Now".

![Step 1](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/1-JLCPCB-home.png?raw=true)

Next, you want to upload the Gerber file for the PCB. You may need to manually input the PCB dimensions (394x154mm). 

![Step 2](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/2-add-gerbers.png?raw=true)

Here, you want to change the specifications to the following. PCB Color and Surface Finish needs to be a combo supported for Economic PCB Assembly in 1.6mm thickness - currently (April 30, 2023), this would be Green in any finish, Black in any finish except ENIG, and Blue, Red, and White with HASL-Leaded. 

![Step 3](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/3-JLCPCB-options.png?raw=true)

Next, you want to scroll down and turn on PCB Assembly. Make sure the following options are selected:

![Step 4](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/4-SMT.png?raw=true)

Press Confirm. Next, you want to upload the BOM and CPL files. 

![Step 5](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/5-BOM-CPL.PNG?raw=true)

Make sure that all the components are selected. Any part that says "Inventory shortage" will not be installed, and you will have to substitute a compatible part, wait for the part to come back in stock, or if you're up to the challenge of SMT soldering, order the part separately and solder it on yourself. 

![Step 6](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/6-BOM.PNG?raw=true)

The next page is a confirmation page. Note that the parts placement preview may be inaccurate (JLCPCB engineers will look over this and make any parts orientation corrections, so don't worry too much about this). 

![Step 7](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/7-review.PNG?raw=true)

As the microcontroller is frequently out of stock due to the chip shortage, line number 20 (for designator U701) can be changed for different compatible MCUs (see the "Compatible MCUs" section below for a list of MCUs that will work). You will name to change the Comment field for that line to the name of the microcontroller you want to use, and change the Footprint and LCSC Part Number as appropriate.

## How to order on Elecrow
Elecrow is a full-service PCB assembly shop, and one of the go-tos in the community for custom keyboard PCBs for the actual group buy sales. They can install any part (not just ones they stock) and generally have better quality surface finish, but is much slower (typically 3-4 week turn around time), and costs more (especially in small quantities). 

To order from Elecrow, you will need to email service@elecrow.com with the [Gerber](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/PCB/V0.7J/Manufacturing%20files/Gerbers-Boston-V07J.zip) and [SMT](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/PCB/V0.7J/Manufacturing%20files/Elecrow%20SMT%20files/BostonV07J-Elecrow-files.xlsx) files and request a quote.

On the [SMT file](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/PCB/V0.7J/Manufacturing%20files/Elecrow%20SMT%20files/BostonV07J-Elecrow-files.xlsx), you will need to edit the first tab to specify your quantity, color, and surface finish. Elecrow's available colors and surface finishes are posted on their [PCB ordering page](https://www.elecrow.com/pcb-manufacturing.html)

![Elecrow](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Elecrow-specifications.png?raw=true)

 
Note - the provided Elecrow SMT files includes having them solder on the RGBLED (LED702), but without the spacer, so it will sit about 2mm lower. 

## Compatible MCUs 

Boston uses a 128kb STM32F072CB-series microcontroller, and can accept either the LQFP-48 (STM32F072CxTx) or 48-UFQFPN (STM32F072CxUx ) versions.

Any of the following microcontrollers will work, and support all features. 

**Compatible MCUs**
| Microcontroller     | JLCPCB (LCSC) part number     |
| ------------------- | ----------------------------- |
| STM32F072CBU6       | C92504                        |
| STM32F072CBU7       | Not on JLCPCB                 |
| STM32F072CBU6TR     | C2054107                      |
| STM32F072CBU7TR     | Not on JLCPCB                 |
| STM32F072CBT6       | C81720                        |
| STM32F072CBT6TR     | Not on JLCPCB                 |
| STM32F072CBT7       | C472592                       |
| STM32F072CBU7TR     | Not on JLCPCB                 |

The 64kb versions of the STM32F072 likely work (but has not been tested), but will only able to run base QMK. These do not support Vial (or VIA if VIA support is ever added in the future) as they do not have enough flash to support dynamic keymaps, so are not recommended. 

**Likely compatible, but won't support Vial - not recommended**
| Microcontroller     | JLCPCB (LCSC) part number     |
| ------------------- | ----------------------------- |
| STM32F072C8U6       | C784818                       |
| STM32F072C8U7       | Not on JLCPCB                 |
| STM32F072C8U6TR     | Not on JLCPCB                 |
| STM32F072C8U7TR     | Not on JLCPCB                 |
| STM32F072C8T6       | C80488                        |
| STM32F072C8T6TR     | Not on JLCPCB                 |
| STM32F072C8T7       | Not on JLCPCB                 |
| STM32F072C8U7TR     | Not on JLCPCB                 |

Other versions of the STM32F072 (which have different footprints or pin counts), or other STM32 microcontrollers will not work. 

## Other Interchangeable PCB Parts

This is here for reference in case some parts are out of stock.

**U702 - BOM Line #21**
This is a SOT-223 linear regulator to drop the 5V down to 3.3V.

EDIT November 9 2021 - changed the default to TI TLV1117LV33DCYR - the other LDOs that fit may not be stable with the current output capacitor setup, as the ESR of the 3 ceramic capacitors used right now are potentially too low for stability. This may result in poor regulation or oscillations and potentially expose the MCU to voltages above its maximum rating. 

| Part                                              | JLCPCB (LCSC) part number |
| ----------------------------------------------------- | ------------------------- |
| TI TLV1117LV33DCYR (default)                          | C15578                    |
| Diodes Inc AZ1117IH-3.3TRG1                           | C108495                   |
| ~~Advanced Monolithic Systems AMS1117-3.3 (Default)~~ | ~~C6186~~                 |
| ~~TI TLV1117-33CDCYR~~                                | ~~C91728~~                |

**U705 - BOM Line #23**
This is a 74LVC1T45 level shifter in an SOT23-6 (SOT26) package. 

| Part                                 | JLCPCB (LCSC) part number |
| ------------------------------------ | ------------------------- | 
| TI SN74LVC1T45DBVR        (Default)  | C7843                     |
| TI SN74LVC1T45DBVT                   | C116653                   |
| Diodes Inc 74LVC1T45W6-7             | C168856                   |

## Other PCB components (through-hole)

These parts are through-hole, and will need to be added once the PCB is received.

### RGBLED (LED702) (optional)

The RGBLED is currently used to indicate the active layer in QMK, though is probably otherwise underutilized. If you do not wish to include it (as it is tricky to solder in), you can exclude it, and use the no-RGBLED version of the left key separator, which does not have the hole for the RGBLED.

The RGBLED indicator uses an APA106-F5 through-hole RGBLED. This is resold by Sparkfun (P/N [COM-12986](https://www.sparkfun.com/products/12986)) and Adafruit ( [P/N 1938](https://www.adafruit.com/product/1938))

Note that Worldsemi WS2812D-F5 does not work as the pinout is different. 

This should be soldered with the 3D-printed [RGBLED spacer](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs/RGB-LED-spacer.stl) in between the bottom of the LED and the PCB. You can solder it straight to the board without the spacer, but the LED will sit very, very low.

Remember to orient this correctly when soldering it to the PCB - it will not work if soldered backwards. The flat side of the LED should match with the "flat side" printed on the PCB.

Despite being through-hole, this is also a bit tricky to solder as the pins are quite close and easily bridged. You definitely want to flux the LED pins when soldering this. Also keep desoldering wick handy while soldering this to remove any bridges. Be careful with the heat, as you can melt the 3D-printed spacer. 

### Reset switch 
The reset switch uses a 5mm tall 6x6mm SPST NO through-hole tact switch. This is a generic part widely available from several vendors - I have used Wealth Metal [TC-0103](https://www.taydaelectronics.com/tact-switch-6x6mm-5mm-through-hole-spst-no.html), but TE 1825910-6, E-switch TL1105AF100Q, Omron B3F-1022, C&K PTS645SK50-2 LFS and numerous other parts should work (though it has not been tested). 

Remember to solder this on the bottom of the PCB and not the top.  

### Encoder
The encoder used is Alps EC11E18244A5, the same one used on the Satisfaction75. Other EC11-style encoders may work, but may need changes to various QMK parameters (ENCODER_RESOLUTION in config.h, and possibly reversing ENCODERS_PAD_A and ENCODERS_PAD_B) to work correctly.

### Lock LEDs and resistors
Most standard 3mm LEDs should work, and are available in several different colors. A 1KΩ resistor is a pretty safe resistor size for the LEDs, but depending on the LED forward voltage, current draw, and desired brightness, you may want to adjust this up or down. Standard 1/4W resistors are suitable.

The LEDs need to be soldered through the [3D-printed 3mm LED spacer](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs/3mm-LED-spacer.stl) - this is described in the assembly instructions. 

### Pogo pins for grounding
On PCB version V0.7J, there is a spot provided on the very right side of the PCB (footprint J707) to solder a pair of spring-loaded pogo pins to electrically ground the plate and the screws on the top of the case. This is to prevent static electricity from resetting the microcontroller. The pogo-pins used are Mill-Max 821-22-002-10-000101, available off [Mouser](https://www.mouser.com/ProductDetail/Mill-Max/821-22-002-10-000101?qs=iJx90KzHWBrJs2LQFpB68w%3D%3D&countrycode=US&currencycode=USD), [Digi-key](https://www.digikey.com/en/products/detail/mill-max-manufacturing-corp/821-22-002-10-000101/1146517?s=N4IgTCBcDaIBxgIwFoxmQBg%2BxHNd0RAF0BfIA), and other sources. Other 2-position 2.54mm pitch pogo pins that can support a 3.5mm board-to-board distance can potentially also work.

Alternatively, you can solder a small piece of wire between either of the through-holes on J707 and the corresponding exposed pad on the plate right above it.

# Other FR4 parts
All FR4 parts can be ordered as a bare PCB from a PCB fab such as JLCPCB, Elecrow, or PCBWay, using the Gerber files. A lead-free finish (such as HASL Lead Free or ENIG) is strongly recommended, especially on the bottom panel.

All FR4 parts are 1.6mm thick. 

Note - on JLCPCB, make sure that "Specify A Location" for "Remove Order number" is selected so that the order number doesn't get printed somewhere you don't want. The Gerber files have the requisite "JLCJLCJLCJLC" text on them and placed in an unobstrusive location.

![Remove Order Number](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Remove-Order-Number.png?raw=true) 

 Also, "Paper between PCBs" under "Advanced Options" is strongly recommended- otherwise there's a decent risk of FR4 parts showing up scratched. 
 
![Paper Between PCBs](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Paper-between-PCBs.PNG?raw=true)

## Plate
The universal plate Gerber files are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version/Plate/Plate-soldered-universal-3DP/Manufacturing%20files)).

Note that JLCPCB will usually charge an extra fee on plates - in the past it has been about $15 additional fee for 5 plates, but may have increased. This extra fee will be requested after you have submitted the order, and you will need to pay it for them to actually manufacture your order. 

## Bottom Panel
The bottom panel Gerber files are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version/Bottom/KiCAD%20files/Manufacturing%20files). 

Definitely use a lead-free finish on this, as you will be touching this when carrying the board. All past bottoms have used HASL-Lead-Free for the finish, but there have been occasional quality issues (e.g. small features on the map were not covered in solder, and were bare copper). ENIG will probably work better, but is more expensive, and will be gold-colored instead of silver. 

## Bumpon holders

You need 2 of these per board - they help keep the bumpons in place. 

The bumpon holder Gerber files are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version/Bumpon%20holders/Manufacturing%20files)

# Mechanical Hardware

These are the fasteners and other hardware you will need. Part numbers from [McMaster-Carr](https://www.mcmaster.com/) are provided. I'm not sure if they ship outside the US, so you may need to figure out how to source the parts locally if you are not in the US.

| Description                                                                    | Qty needed per board | McMaster-Carr P/N | Notes                                                              | 
| ------------------------------------------------------------------------------ | -------------------- | ----------------- | ------------------------------------------------------------------ |
| M3x0.5, 6mm long ISO 7380 button head screw, stainless steel, Torx T10 head    | 8                    | 90991A112         | Hex-head would also work, but Torx strips less easily              |
| M3x0.5, 10mm long ISO 7380 button head screw, stainless steel, Torx T10 head   | 15                   | 90991A114         | Hex-head would also work, but Torx strips less easily              |
| M3x0.5 DIN 934 hex nut, zinc plated                                            | 12                   | 90591A250         | Zinc instead of stainless, as stainless-on-stainless risks galling (cold welding) together and getting very,very stuck |
| M2 5mm long Delta PT ® Torx head thread forming screw                          | 14                   | 96817A207         | Other M2 5mm-long self-tapping screws *might* work. There is also a stainless steel version of this screw – McMaster-Carr 96817A842 |
| PEM tin-plated press-fit threaded insert , M3x0.5. PEM P/N KF2-M3-ET           | 11                   | 95117A499         | Also available on [Mouser](https://www.mouser.com/ProductDetail/PEM/KF2-M3-ET?qs=l4Gc20tDgJKPX2YZdDO0uw%3D%3D) for significantly less |
| Rubber feet (3/8” diameter) – 3M Bumpon SJ5003 or equivalent                   | 4                    | 95495K12          |                                                                    | 

# Knobs
The Alps EC11E18244A5 encoder takes a 6mm knob with either a D-shaft or a set screw. This is a common size for guitars and audio equipment. 1/4" knobs can work but may be loose. 1/4" to 6mm adapters available from various sources if you want to use a 1/4" knob. 

The knob needs to be smaller than 23mm in diameter or it will hit the Esc key. 

I personally recommend Kilo International's OEDNI-75-X-7 lineup - these have very grippy knurling and can be easily rotated with one finger. They can be found on Digi-key, Newark, and other electronics parts vendors. If you use that knob, you want to 3D print a [small spacer](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs/Kilo-OEDNI-75-knob-spacer.stl) to place into the shaft hole on the knob, as otherwise the knob can sit too low and bump into the case. 

| Kilo P/N     | Finish              |
| ------------ | ------------------- |
| OEDNI-75-1-7 | Silver, satin gloss |
| OEDNI-75-2-7 | Black, satin gloss  |
| OEDNI-75-3-7 | Silver, matte       |
| OEDNI-75-4-7 | Black, matte        |

# 3D printing
You will need to 3D-print the parts in [the STL folder](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs). (For the left key separator you need to print either the RGBLED or no RGBLED verison, depending on whether you soldered on the RGBLED on the PCB). More detailed instructions on 3D are available in the assembly instructions. The parts are designed to be FDM 3D printed, and can be printed without support material. 

You can outsource the 3D printing to a service like Shapeways, but if you're printing more than a single case this isn't econommical versus just buying a budget 3D printer - a cheap $250 Ender 3 Pro or a Biqu B1 will print the case just fine. Or if you don't want to deal with that, try finding a friend or acquaintance with a 3D printer. Many public libraries also now have 3D printers also that are available for use. 
# Assembly Instructions

Draft assembly instructions are [here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/3D%20printed%20version/Draft%20instructions%20(barebones%20kit).pdf)


