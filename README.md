# Boston Keyboard 

![3D-printed/FR4 version](https://github.com/bluepylons/Boston/raw/main/graphics/3D-printed-prototype.JPG)
![CNC version](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/DSC_0317.JPG?raw=true)

## Introduction 
Boston is a compact battleship with a complement of 18 programmable keys, in a footprint 2u narrower than a full-size, and only about 1.5u wider than a 96%. There is a 3D printed version and a CNC aluminum version. Hotswap PCBs for both are in development. All are open source. 

The immediate inspiration for Boston was the DriftMechanics [Austin](https://github.com/Gondolindrim/Austin), as well as the [7-row Thinkpad keyboards](https://cdn.mos.cms.futurecdn.net/ZgDSnno6WfhXMf8u8fsBv7-970-80.jpg) found on Thinkpads of the T420 generation and older. The general idea was to make a narrower full-size that retained both the 2u numpad "0" and traditional 2x3 Ins/Del/Home/End/PgUp/PgDn nav block, by expanding vertically. 

The name is a pun off Austin, since the layout is derived from it. I also grew up around the city of Boston and still live in the area. 

## Supported layouts

Soldered PCB:
![Boston layouts](https://github.com/bluepylons/Boston/raw/main/graphics/bostonKLE.png)

ANSI hotswap PCB: (note the split space 2.75u and 2.25u keys are flipped around compared to the soldered version - this was necessary to split both split space and standard 6.25u space on the same PCB with hotswap sockets)
![Boston ANSI hotswap layouts](https://github.com/bluepylons/Boston/raw/main/graphics/boston-hotswap-ANSI-KLE.png)

ISO hotswap PCB: TBD

Click [this link](http://www.keyboard-layout-editor.com/#/gists/75e63e00e1acc52cdb8eeda7f8ac4ba6) for the KLE file for the soldered PCBs.

Click [this link](http://www.keyboard-layout-editor.com/##@@_x:1.5%3B&=P1&=P2&=P3&=P4&_x:0.25%3B&=P5&=P6&=P7&=P8&_x:0.25%3B&=P9&=P10&=P11&=P12&_x:0.25%3B&=P13&=P14&=P15&_x:0.25%3B&=Insert&=Home&=PgUp%3B&@=Esc&_x:0.5%3B&=F1&=F2&=F3&=F4&_x:0.25%3B&=F5&=F6&=F7&=F8&_x:0.25%3B&=F9&=F10&=F11&=F12&_x:0.25%3B&=Print%0A%0A%0A%0A%0A%0AScreen&=Scroll%0A%0A%0A%0A%0A%0ALock&=Pause%0A%0A%0A%0A%0A%0ABreak&_x:0.25%3B&=Delete&=End&=PgDn%3B&@_y:0.5%3B&=~%0A%60&=!%0A1&=%2F@%0A2&=%23%0A3&=$%0A4&=%25%0A5&=%5E%0A6&=%2F&%0A7&=*%0A8&=(%0A9&=)%0A0&=%2F_%0A-&=+%0A%2F=&_c=%239a67ea&w:2%3B&=Backspace&_x:0.25&c=%23cccccc%3B&=P16&_x:0.25%3B&=Num%20Lock&=%2F%2F&=*&=-%3B&@_w:1.5%3B&=Tab&=Q&=W&=E&=R&=T&=Y&=U&=I&=O&=P&=%7B%0A%5B&=%7D%0A%5D&_w:1.5%3B&=%7C%0A%5C&_x:0.25%3B&=P17&_x:0.25%3B&=7%0AHome&=8%0A%E2%86%91&=9%0APgUp&_c=%23ff9800&h:2%3B&=+&_x:0.75%3B&=-%3B&@_c=%23cccccc&w:1.75%3B&=Caps%20Lock&=A&=S&=D&=F&=G&=H&=J&=K&=L&=%2F:%0A%2F%3B&=%22%0A'&_w:2.25%3B&=Enter&_x:0.25%3B&=P18&_x:0.25%3B&=4%0A%E2%86%90&=5&=6%0A%E2%86%92&_x:1.75&c=%23ff9800%3B&=+%3B&@_c=%23cccccc&w:2.25%3B&=Shift&=Z&=X&=C&=V&=B&=N&=M&=%3C%0A,&=%3E%0A.&=%3F%0A%2F%2F&_t=%23ff0000&w:1.75%3B&=Shift&_x:2.5&t=%23000000%3B&=1%0AEnd&=2%0A%E2%86%93&=3%0APgDn&_h:2%3B&=Enter%3B&@_y:-0.75&x:14.25%3B&=%E2%86%91%3B&@_y:-0.25&w:1.25%3B&=Ctrl&_w:1.25%3B&=Win&_w:1.25%3B&=Alt&_c=%2333b5e5&t=%23757575%0A%23ffffff&w:6.25%3B&=%0A6.25u&_c=%23cccccc&t=%23000000%3B&=Alt&=Menu&=Ctrl&_x:3.5&c=%23ffc107&w:2%3B&=0%0AIns&_c=%23cccccc%3B&=.%0ADel%3B&@_y:-0.75&x:13.25%3B&=%E2%86%90&=%E2%86%93&=%E2%86%92%3B&@_x:3.75&c=%2333b5e5&t=%23757575%0A%23ffffff&w:2.75%3B&=%0A2.75u&_t=%23ff0000&w:1.25%3B&=%0A1.25u&_t=%23757575%0A%23ffffff&w:2.25%3B&=%0A2.25u%3B&@_y:-0.75&x:12.75&c=%239a67ea&t=%23ff0000%3B&=Back&=Del&_x:1.75&c=%23ffc107%3B&=0&=00) for the KLE file for the ANSI hotswap PCB. 

## Features:
* 121-keys in standard ANSI configuration
* Alps EC11E rotary encoder above the Escape key 
* Full-size numpad with 2u "0" key
* Traditional 2x3 Ins/Del/Home/End/PgUp/PgDn navblock 
* Uses keys found in GMK base kits (except for the programmable keys)
* RGBLED layer-status indicator light 
* ISO enter key, ISO left shift, split backspace, split numpad 0, split space, and WKL bottom row support 
* Optional through-hole LED backlight (dimmable as a single block only) - soldered version only. This hasn't been tested in the newer PCBs but probably still work. 
* USB-C
* STM32F072 controller running QMK. Circuitry is derived from the Austin. 
* Uses Gondolindrim/Acheron's [single-button reset circuit](http://acheronproject.com/images/reset_article/reset2_tighter.svg)
* QMK and Vial support 
* Approximately 6.5° typing angle 

### 3D Printed Version:
* Printable on cheap hobby printers - 200mm x 150mm (X/Y) x 210mm (Z) bed size needed to print all the case parts (doable on a Bambu P1S or X1C, Ender 3, Biqu B1, Prusa i3, etc.) 
* Bottom panel with [artwork of Boston's maze-like street network](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-bottom.JPG).
* Technically top mount, though an unusual implementation (screws come in from the top of the case and screw into threaded inserts on the plate - load path is identical to top mount)
* Designed around an FR4 plate with soldered-in threaded inserts 

### CNC Version:
* 2-piece CNC machined case (no weight)
* Traditional top mount 
* Uses a Unified S1 daughterboard (older versions use the C3 daughterboard)
* Low USB-C port parallel to desk 

## Current Errata

For all PCB versions - if you use the 1u numpad + and = key options instead of 2u numpad +, the 1u + and 1u = keys are swapped in firmware and on the PCB compared to the KLE (physically pressing the upper 1u key actuates the lower 1u key in firmware and vice-versa). For now, just swap the key assignments in Vial and you should be good. I may fix this eventually in the QMK and Vial files but it's a low priority for me.

## Status
Due to [complications around electromagnetic compatibility testing regulations](https://www.keebtalk.com/t/your-custom-keyboard-is-probably-illegal-a-long-post-on-radio-interference-testing-regulations-and-keyboards/16104), and my current personal circumstances, I decided to open-source the files for the project rather than running a group buy or sale. You can use the files to make one for yourself, as long as you comply with the CERN OHL-W license. 3rd-party group buys or sales are permitted under the license (I will not be directly involved in any 3rd party sales). [RNDKBD](https://rndkbd.com/) currently sells the 3D printed version as an in-stock item (printed to order in a variety of different colors). There has also been at least one small 3rd-party private buy for the CNC version.

Note that under the terms of the CERN OHL-W license, if you modify the design or make derivative works from the design, you are required to open-source them under a compatible license. 

Current status:

Cases:

**3D printed version** - prototyped and working. 

**CNC version** - prototyped and working. 

PCB:

**V0.8 series** - PCB has been prototyped and tested by Andy of RNDKBD.

**V0.7J** (3DP version) - prototyped and working (except optional backlight LED feature has not been tested)

**V0.6.1D** (CNC version) - prototyped and working (except optional backlight LED feature has not been tested).

## Ordering Guide

A draft ordering guide for the 3D printed version is available on the README under [the folder for the 3D printed version](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version). 

A draft ordering guide for the CNC version is available on the README under [the folder for the CNC version](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version). Assembly instructions for the CNC version are still being worked on.

## PCB Renders 

Renders done with [tracespace.io](https://tracespace.io/).

V0.8J (integrated USB-C port and ESD protection - used on the 3D printed version):
![PCB V0.8J top](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-top.png)
![PCB V0.8J bottom](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-bottom.png)

V0.8D (Molex Pico-EZmate connector for use with UDB S1 and C4 daughterboards):
![PCB V0.8D top](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-V08D-top.png)
![PCB V0.8D bottom](https://github.com/bluepylons/Boston/raw/main/graphics/PCB-V08D-bottom.png)

## Firmware
All PCBs from V0.4 onward (including V0.5.2, V0.6.1D, V0.6.1J, V0.7J, and the V0.8 line, both hotswap and soldered) have the same key matrix and therefore use the same firmware. However, the RGBLED on the CNC variant PCBs (the -D variants) has its red and green channels reversed compared to the 3DP version PCBs (-J variants) (as unfortunately the SK6812 mini-E RGBLED used on V0.6.1D and the APA106 RGBLED used on the others have different orders for the red, green, and blue channels). 

The compiled QMK firmware .bin file is [here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/boston_default.bin). Source files are on the [QMK repo](https://github.com/qmk/qmk_firmware/tree/master/keyboards/boston). 

The compiled [Vial](https://get.vial.today/) firmware .bin file is [here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/boston_vial.bin). Source files are on the [Vial-QMK repo](https://github.com/vial-kb/vial-qmk/tree/vial/keyboards/boston). The current Vial build uses Vial V0.6. This is the recommended firmware. 

Firmware can be flashed using QMK Toolbox or DFU. On PCB versions V0.6 and newer, you need to long press the reset button (for several seconds) to access the DFU bootloader to allow for flashing - a short press only resets the MCU. 

## Copyright Notice
The PCB files and hardware designs are released under the [CERN OHL-W](https://ohwr.org/cern_ohl_w_v2.txt) license. The QMK/Vial firmware is released under [GNU GPL V3](https://www.gnu.org/licenses/gpl-3.0.en.html). I am considering changing the PCB file and hardware design license to [Acheron OHL](http://acheronproject.com/AOHL14/) in the future.

The map artwork for the bottom panel on the 3D printed version, in \Boston - Current design\3D printed version\Bottom, was created using OpenStreetMap data, © OpenStreetMap contributors, under OpenStreetMap's [conditions](https://www.openstreetmap.org/copyright). The resulting KiCAD footprint and PCB files for the bottom FR4 panel containing the artwork is specifically released under the [Open Data Commons Open Database License](https://opendatacommons.org/licenses/odbl/) rather than CERN OHL-W.

The rubber feet, screws, nuts, and threaded inserts in the STEP files were remodelled from scratch, as most 3D models available online do not permit redistribution. 

## Libraries
This project uses the Acheron Project's [Alexandria Library](https://github.com/AcheronProject/AcheronLibrary). A few custom footprints are used:
* Boston-PCB-custom-footprints contains custom footprints for V0.7J (currently just a 4.4mm hole)
* Boston-3DP-plate-library contains custom footprints for the 3D-printed version's FR4 plate.
* Boston-plate-custom-footprints contains custom footprints for the CNC version's FR4 plate 

The KiCAD files are done using KiCAD V7.

 The KiCAD files use project-specific paths to the Acheron Library. To set this up - in KiCAD, open Preferences > Configure Paths. Add a new entry, with ALEXANDRIA for the name, and for the path, the directory where the AcheronLibrary folder resides in.

## Derivatives
Technofrikus designed an alternative 3D-printed case derived from the files of the CNC version, and also designed a case with a 4° typing angle. The files for those are [available on Technofrikus' GitHub](https://github.com/Technofrikus/Boston-Case).
![Technofrikus' 3D-printed version](https://github.com/Technofrikus/Boston-Case/blob/main/Photos/DSCF7709%201.jpg?raw=true)

DatGameh designed a 0.5° version of the 3D printed case, using parts for the 3DP version. The files are [available on DatGameh's Github](https://github.com/DatGameh/Pretty-Flat-Boston-Case). 


## Acknowledgements

Many thanks to:
* The [Acheron Project](http://acheronproject.com/) - the KiCAD library and the source files for the Austin have been invaluable for designing this board.
* The designers of the Austin (Driftingbunnies, PheonixStarr and Gondolindrim). The layout, schematics, and firmware were derived from that board.
* Gondolindrim, for assistance and feedback with the PCB design, as for running the Acheron project.
* KiCAD, for being an awesome free open-source PCB design tool.
* [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/), where I designed the layout. 
* [Swill's plate generator](http://builder.swillkb.com/) and [Ai03's plate generator](https://kbplate.ai03.com/), which I used for making the plate.
* [Maperitive](http://maperitive.net/) and [OpenStreetMap](https://www.openstreetmap.org/#map=4/38.01/-95.84), which was used to generate the map artwork on the bottom of the 3D-printed/FR4 case. 


