# Assembly guide for S1 DB variants (work in progress) 

# Before You Start 
* Please read the entirety of this guide before you begin.
* Do not use strong chemicals such as acetone to wipe down the PCB. This may cause damage.
* Observe basic ESD (Electrostatic Discharge) handling procedures while assembling the keyboard to avoid permanent damage to the PCB. All ESD protection is provided by the daughterboard, and the PCB does not have ESD protection while not connected to the daughterboard. 
	* Wear a properly-grounded ESD wrist strap while you are assembling the board.
	* Touch a grounded metal object before you begin handling the PCB to reduce risk of ESD damage, and touch a grounded metal object regularly to discharge any ESD buildup.
	* Avoid wearing clothing (e.g. wool sweaters, socks) that can cause ESD buildup
	* Avoid working on a carpeted surface.
	* A very basic guide to ESD procedures is available [here](https://www.wikihow.com/Ground-Yourself-to-Avoid-Destroying-a-Computer-with-Electrostatic-Discharge). 
* Soldering can be hazardous.
	* Wear safety glasses while soldering - hot droplets of flux may fly towards you while you are soldering.
	* The hot tip of a soldering iron can cause serious burns
	* Use a fume extractor while soldering, or soder in a well-ventilated space. Flux fumes can be hazardous and can cause long-term long issues
	* Lead-free solder is strongly recommended. If you are using leaded solder, take measures to avoid lead contamination. According to the [US Centers for Disease Control](https://www.cdc.gov/niosh/topics/lead/safe.html), "washing skin with standard soap and water is not enough to remove lead residues", and you may need to use special lead removal wipes such as D-lead®, or wear gloves while handling leaded solder. 
* Do not overtighten screws - this can strip the screw head or the screw threads, and cause other damage. 

# The parts you'll need 

[picture of the parts]

Acquiring parts is covered by the [ordering guide](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/README.md)

## Parts you'll need to assemble the keyboard.
* MX-compatible switches. If you are using the fixed-layout plate, you will need 121 switches. For the universal plate, you will need between 119 and 127 switcehs depending on the layout you choose.
* Keycaps of your choice. Make sure that they support your desired layout.
* PCB-mount stabilizers of the correct size and quantity for your preferred layout. PCB
screw-in stabilizers are recommended, but PCB snap-in will work. For the fixed-layout plate you will need 6 2u stabilizers and 1 6.25u stabilizer.
* A USB-C cable
* A knob. The included encoder has a 6mm diameter D-shaft with a 4.5mm flat. Most knobs meant for 6mm shafts, that either have the flat or use a set screw for mounting, and are smaller than 21mm in diameter, will work.
* (optional - also warning that the backlight feature has not been tested on the V0.6 PCBs) Through-hole LEDs for backlighting. Check that your switches and keycaps support the LEDs you choose - some switches only work with SMD LEDs (which are not supported on this PCB), and others may hit your keycaps.
 

# Tools you'll need
| Description                                                                                                  |  Used for                                                           |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| 2.5mm hex key or bit ("Allen key")                                                                           | All M3 screws                                                       |
| Soldering iron and solder                                                                                    | For soldering everything                                            |
| Flush cutters                                                                                                | For cutting legs off soldered LEDs and resistors                    |
| Tweezer, metal keycap puller, wire, or unbent paperclip                                                      | Testing the PCB without switches                                    |

# Part 1 - Preparing the PCB 

## 1.1 - Basic ESD and safety precautions 
As the PCB lacks ESD protection when the daughterboard is not connected, observe basic ESD protection procedures. Otherwise, you risk damaging the PCB. 

* Wear a properly grounded metal ESD strap when handling the PCB and when assembling the keyboard 
* Avoid wearing clothing (such as thick wool sweaters or socks) or working on surfaces (e.g. carpet) that are prone to generating static electricity. 
* Touch a grounded metal object before handling the PCB, and regularly while you are working. Common grounded metal objects include metal appliances that are plugged in with a 3-prong plug, computers  that are plugged in with a 3-prong plug, any exposed metal on cables that protrude out of said computers (e.g. USB cables), and metal sinks and faucets. Doorknobs are not grounded and are not a good place to discharge static. 

For soldering, wear eye protection while soldering, and make sure that your space is well ventilated to avoid breathing in flux fumes. 

## 1.2 - Soldering on the reset switch. 

Solder the reset switch onto the top side of the PCB, next to Right Shift. Depending on where you obtained the PCB, this might already be soldered on for you.

[picture of the reset switch soldered on]

## 1.3 - Installing software for flashing the firmware

If you ordered the PCB directly from a PCB fab, it likely won't have the firmware installed on it. 

To flash the firmware, you'll have to install a few pieces of software.

If you are on Windows, you'll want to install drivers. This can be done with a tool called [Zadig](https://zadig.akeo.ie/). 

a.) Install and open Zadig:
![Zadig Step 1](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Zadig-1.PNG?raw=true)

b.) Select "List All Devices" in the Options Menu :
![Zadig Step 2](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Zadig-2.PNG?raw=true)

c.) Select "STM32 Bootloader" in the dropdown menu:
![Zadig Step 3](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Zadig-3.PNG?raw=true)

d.) Select WinUSB here:
![Zadig Step 4](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Zadig-4.PNG?raw=true)

e.) Click the Replace Driver button. This will install the driver. 

f.) After Zadig is installed, install [QMK Toolbox](https://github.com/qmk/qmk_toolbox). Download links are at the bottom of the page.

g.) Download the .bin Vial firmware file [here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/boston_vial.bin) 
 
## 1.4 - Flashing the Firmware 

a.) Connect the USB-C daughterboard to the PCB using the JST cable. Remove any metal or other conductive objects from the vicinity to reduce the risk of the PCB getting shorted, and be careful to avoid letting the daughterboard touch the PCB (as that can also cause a short circuit). 

b.) Connect the daughterboard to your computer. The PCB and daughterboard will receive power, and will be vulnerable to short circuits, so continue to be careful. 

c.) Open QMK Toolbox. 

d.) Hold down the reset button for at least 5 seconds, and then release it. In QMK Toolbox, "STM32 DFU device connected" should appear in yellow.
![QMK Toolbox Step 1](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/QMK-Toolbox-1.PNG?raw=true)

e.) Press "Open" in QMK Toolbox and navigate to the location of your .bin firmware file. 
![QMK Toolbox Step 2](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/QMK-Toolbox-2.PNG?raw=true)


f.) Press the Flash button. Do not disconnect the keyboard until it is done flashing, or you may permanently brick your keyboard. 
![QMK Toolbox Step 3](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/QMK-Toolbox-3.PNG?raw=true)


## 1.5 - Testing your PCB 

Use a tweezer, metal keycap puller, wire, or unbent paperclip to short the switch opening pins, and a program such as [Aquakeytest](https://geekhack.org/index.php?topic=34670.0) to ensure that each key works. 

Disconnect the daughterboard from the PCB once you're done.

## 1.6 - Soldering on the lock LEDs and resistors 

If you have a soldered PCB, solder on the 3 1KΩ resistors onto the positions for R200, R201, and R202. 1KΩ is a comfortable value, but if you want your LEDs brighter or dimmer you may wish to use different resistors. Resistors are not directional and will work soldered in either direction. The hotswap PCB has these pre-soldered on so you will not need to solder on the resistors.

![Resistors](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Resistors.JPG?raw=true)

Next up, we want to do the lock LEDs (on both the hotswap and soldered PCBs). Note that LEDs are directional and will not light up if soldered in backwards. The longer leg on an LED is +. Make sure this matches up with the + symbols on the PCBs.
![LED-legs-labelled](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/LED-legs-labelled.JPG?raw=true)

Solder the lock LEDs through the LED spacer as shown - the LED spacer only fits on one way. 
![LEDs in spacer](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/LED-in-spacer.JPG?raw=true)
![LEDs soldered on](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/LEDS-installed.JPG?raw=true)


## 1.7 - Soldering on the rotary encoder 

Solder on the rotary encoder on the upper left of the PCB. Make sure you solder this to the top side of the PCB. 

# Part 2 - Preparing the case 

## 2.1 - Installing the rubber feet 
Peel the backing paper off the rubber feet and stick them in the circular pockets on the bottom of the case. 

[image] 

## 2.2 - Installing the RGBLED light pipe 

a.) Press the light pipe into the hole meant for the light pipe on the upper left of the case top. 
![Light pipe installation](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Light-pipe-installation.JPG?raw=true)

b.) Flip the case top over. Slip the rubber light pipe retainer onto the back of the light pipe, and move it down so that it prevents the light pipe from falling out. If you want, you can glue the RGBLED light pipe and retainer, using hot glue, epoxy, or another adhesive. 
![Light pipe retainer installation](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Light-pipe-retainer-installation.JPG?raw=true)

![Light pipe retainer installed](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Light-pipe-retainer-installed.JPG?raw=true)

# Part 3 - Installing the Daughterboard 

a.) Plug the daughterboard cable into the daughterboard. 
[image]

b.) Using 2 M3x5 screws, screw the daugherboard into the bottom case. 
[image] 

# Part 4 - Switches and stabilizers 

## 4.1 - Installing your stabilizers

If you want to lube or otherwise tune your stabilizers, do so before installing them. It is much harder to make any changes after they're installed, and stabilizers cannot be installed or removed after the switches are installed or soldered in. You will need to remove or desolder most or all of your switches in order to remove the stabilizers once your keyboard is assembled.

Install all stabilizers according to the instructions from their manufacturer. Insulation washers are not necessary. 

After installing your stabilizers, briefly test them. To do this, take the plate, a switch, and the appropriate keycap for the stabilizer you want to test, and install them over the PCB (without soldering the switch in). Make sure the key feels okay - that it’s not binding, or failing to go all the way to the bottom, or failing to return, for instance. Do this for all your stabilizers to make sure that they’ve been installed properly.

## 4.2 - Installing and soldering your switches

If you want to modify or tune your switches (e.g. by lubing, changing springs, etc.), do so before installing them. 

Install the switches into the plate and solder them, like you would when building any other custom keyboard.

If you are using the universal plate, test your bottom row with keycaps before proceeding, as it is easy to make mistakes here. Install keycaps on the bottom row to make sure that it's correct before soldering. 

Solder all your switches.

# Part 5 - Everything comes together

## 5.1 - Installing the plate and PCB assembly

Screw the plate to the top case using the M3 x 5mm screws. 
![Screwing in the plate](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Screwing-in-plate.JPG?raw=true)


## 5.2 - Connecting the daughterboard

With the top case and PCB near the bottom case (avoid accidentally tugging on the daughterboard cable as this can damage the cable or rip the connector off the daughterboard or PCB) - connect the daughterboard cable to the main PCB. 

[image] 

## 5.3 - Screwing everything together

Again, being careful to avoid tugging on the daughterboard cable - set the case top onto the case bottom. Flip everything over. Place M3x10 screws on the front four screw holes, and M3x16 screws on the rear four screw holes. Tighten those screws to screw the top and bottom cases together. 
![Screwing case together](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-CNC/Screwing-case-together.JPG?raw=true)

## 5.4 - Installing your knob and keycaps. 

Next, flip the keyboard back over and install your keycaps and knob. 

Some knobs slip on, and some use a set screw which you must line up with the flat part the D-shaft . You may need a spacer with some knobs. 

You are done!

