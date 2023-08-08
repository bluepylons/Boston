# Boston (3D-printed/FR4 version) Assembly Instructions, including 3D printing 

## Draft. work-in-progress (August 7, 2023)

## To do

* Instructions on how to solder per-key LEDs 

# Table of contents

Before You Start
What’s in the box:
Part 1: 3D-printing the case parts
Part 2: Putting Together The Plate and Key Separators
Part 3: Soldering Additional Parts on the PCB
Part 4: installing stabilizers and switches
Part 5 - Case Prep and Assembly
Part 6: Flashing Firmware
Appendix:

# Before You Start 
* Boston is an open-source keyboard project. Follow these assembly instructions at your own risk. 
* Please read the entirety of this guide before you begin. The assembly process for the 3D-printed version of Boston is a bit atypical.
* The 3D printed key separators must be installed onto the plate before the switches are soldered on. If you have the plate and PCB but do not have the 3D printed parts yet - do not solder your switches on yet.  
* Do not use strong chemicals such as acetone to wipe down any part of the case or PCB. This may cause damage. 
* The PCB has an ESD protection chip to provide some protection when it is fully assembled, but cannot protect the keyboard while you are building it. Please observe basic procedures to prevent damage from electrostatic discharge (ESD) while handling the PCB or assembling the keyboard.
    * Wear a properly-grounded ESD wrist strap while you are assembling the board.
    * Touch a grounded metal object before you begin handling the PCB to reduce risk of ESD damage, and touch a  grounded metal object regularly to discharge any ESD buildup. 
    * Avoid wearing clothing (e.g. wool sweaters, socks) that can cause ESD buildup
    * Avoid working on a carpeted surface. 
    * A guide on basic ESD procedures is available [here](https://www.wikihow.com/Ground-Yourself-to-Avoid-Destroying-a-Computer-with-Electrostatic-**Discharge**). 
* Soldering can be hazardous
  * Wear safety glasses while soldering! Hot droplets of flux may fly towards you while you are soldering.
  * The hot tip of a soldering iron can cause serious burns.
  * Use a fume extractor while soldering, or solder in a well-ventilated space. Flux fumes can be hazardous and can cause long-term lung issues. 
* Do not overtighten the screws! This can strip the head or the threads and cause other damage.
  
# What's in the box
* The PCB
* The FR4 fiberglass plate
* The FR4 bottom panel
* 3x 3mm LEDs
* (soldered version only) 3x 1KΩ resistors 
* A rotary encoder. Your vendor may also include a knob.
* 15 M3x10mm screws
* 8 M3x6mm screws 
* 11 M3 PEM KF2-M3-ET threaded inserts
* 12 M3 hex nuts
* 14 M2x5mm self-tapping screws 
* A reset switch (note on some PCBs this is already soldered on, and won’t be included as a result)
* A set of spring loaded pins (note on some PCBs this is already soldered on, and won’t be included as a result)
* (hotswap version only) 10 M2 3.5mm long standoffs
* (hotswap version only) 20 M2x3mm screws 

If you purchased the kit from a vendor, please inform your vendor if any of the above is missing. 

# 3D printed parts
Your vendor might have included these, or you may need to print these yourself. See [Part 0 - 3D printing the case parts](#part-0---3d-printing-the-case-parts) for the list of parts.

# Parts you'll need to assemble the keyboard
* MX-compatible switches. Depending on the layout you choose, you will need between 119 and 127 switches. 
* Keycaps of your choice. Make sure that they support your desired layout. 
* PCB-mount stabilizers (either screw-in or snap-in) of the correct size and quantity for your preferred layout. 
* A USB-C cable 
* A knob. The included encoder has a 6mm diameter D-shaft with a 4.5mm flat. Most knobs meant for 6mm shafts, that either have the flat or use a set screw for mounting, and are smaller than 21mm in diameter, will work.
* (optional) Through-hole LEDs for backlighting. Check that your switches and keycaps support the LEDs you choose - some switches only work with SMD LEDs (which are not supported on this PCB), and others may hit your keycaps. 

# Tools you'll need to assemble the keyboard 
* A T6 Torx screwdriver or key. Make sure it is actually a T6 size!. A smaller bit may fit in the head, but is much more likely to strip the head. 
* A T10 torx screwdriver or key. Likewise, make sure it is actually a T10 size. 
* A pair of metal tweezers, wire, metal keycap puller, or unbent paper clip for testing the PCB 
* (hotswap only) A #1 Philips screwdriver. Make sure it's actually a #1 size. 
* A soldering iron and solder. 
* Super glue 
* A blue threadlocker, such as Loctite 242, 243, or 248, is recommended to prevent screws from loosening over time. 
* If you make mistakes while soldering parts in, you may need a desoldering pump (solder sucker) or desoldering wick to make fixes. 

# (hotswap only) - A note on hotswap switch installation

* Only use switches that have never been soldered. Desoldered switches can damage the hotswap socket.
* Make sure the pins are straight before inserting the switch 
* Support the back side of the hotswap socket when inserting switches. 

[graphic]

# Part 0 - 3D printing the case parts 

You will need to 3D-print the following parts. STL files for 3D printing are available on Github [here]. You will need a 3D printer with a minimum 200mm x 150mm bed x 210mm tall.

* The 3D-printed case, which comes in 4 pieces: the left half, right half , left-key-separator, and right-key-separator:

* The 3D-printed spacer for the lock LEDs

For the left and right case halves, printing with the long side facing up, like so, is recommended.

You may also want to adjust the Z-seam setting to prevent seams from being in highly visible places. Generally, you should try to locate the Z-seam at the bottom of the case, preferably in an inside corner.

For the key separators, the following orientation is recommended, with the rounded edges facing up. 

# Part 1 - Putting Together The Plate and Key Separators 

## 1.1 - Soldering the threaded inserts into the plate

Flip the plate over so that the underside of the plate is facing you. Press in the PEM threaded inserts into the 11 holes on the plate. 

If it’s too hard to push the inserts in, you can use one of the M3x6 screws to pull the insert in, using a T10 Torx screwdriver. Remove the screw when the insert is all the way in.

With the inserts pushed in, double check that they’re on the correct side - they should be on the bottom of the plate, not the top. Also, make sure the inserts are all of the way in and fully seated. Then solder, them in place:

It may take some time for your soldering iron to get the nut and plate hot enough to get the solder to flow well. Also, avoid getting solder on the threads. If you get solder on the threads, try running an M3 screw through to clear solder off the threads. If that doesn’t work, you’ll need an M3 tap to remove the solder from the threads.

# 1.2 - (hotswap version only) - installing the hotswap standoffs

Attach the M2 3.5mm long standoffs onto the bottom of the plate using the M2x3mm screws, onto the following marked holes on the plate:

[Plate-standoff-positions.png]

# Part 2 - Attaching and aligning the key separators

*On PCBs older than V0.7, the key separators cannot be adjusted after the switches are soldered on without desoldering all your switches. Make sure you get this right before soldering anything!* 

Next, grab the 3D-printed left-key-separator and right-key-separator pieces, and the M2x5 self-tapping screws.. These pieces need to attach to the plate before the switches are soldered in.

Attach the key separators to the plate using the M2x5 self-tapping screws, via the small holes located in the plate. Use a T6 Torx screwdriver for this. Make sure the screws go in straight! **Do not tighten these all the way - leave them about a ½ turn loose, since we’ll need to adjust and align these in a little bit.** There are 14 screws that need to be attached in total - 6 on the left separator, and 8 on the right separator. 

With the screws in but not tightened fully, do a test fit against the left and right case halves by sliding the plate into the left and right case halves. Note that you’ll have to slightly spread apart the right case half to get it past the arrow key cluster. 

Attach the plate to the case using M3x10mm screws. Make sure the plate is fully seated against the case.

Adjust the separator pieces so that the gaps between the separators and the case halves (marked in orange) are minimal when the plate is slid into the very end of the case halves. There may be a small gap between the two separators (gap marked in pink) - this is normal. 

Flip the assembly over, and tighten the screws that can be accessed:

Remove the case halves, and tighten up the remaining screws:

Put everything back together and do a final check of the gaps. Make any adjustments as necessary. Again, on PCBs older than V0.7, you can’t fix this once the switches are soldered in!

When everything looks good, remove the case halves again, and make sure all the screws are tight. 

# Part 3 - Testing and Soldering Additional Parts on the PCB

# 3.1 - Testing each key on the PCB 

While PCBs have been tested before being shipped, there is a small possibility of damage from shipping. Testing the PCB before further assembly is recommended - use a tweezer, metal keycap puller, wire, or unbent paperclip to short the switch opening pins, and a program such as [Aquakeytest](https://geekhack.org/index.php?topic=34670.0) or [Vial](https://get.vial.today/)'s built-in matrix tester to ensure that each key works. 

# 3.2 - (soldered version only) - Soldering on the 1KΩ resistors

Grab the 3 1KΩ resistors and solder them into the spots for R200, R201, and R202, on the top side of the PCB. If you’re using your own LEDs and want them brighter or dimmer, you may want to use different resistors than the provided resistors.

# 3.3 - Soldering on the lock LEDs 

Grab the spacer for the LEDs, and run the LEDs legs through it. Place the LEDs and spacers onto the PCB, for spots LED201, LED202, and LED203. Note that the spacer only fits in one way.

Note that LEDs are directional and will not light up if soldered in backwards. The longer leg on an LED is +. Make sure this matches up with the + symbols on the PCBs. 

Once the LEDs are in, solder them in. Make sure that they’re in straight! 

If you haven’t already done so, clip the legs on the resistors and LEDs with a pair of flush cutters.

# 3.4 - Soldering the rotary encoder onto the PCB 

Next, solder on the rotary encoder onto the top left corner of the PCB.

# 3.5 - Soldering on the reset switch 
If your PCB did not come with the reset switch soldered on, solder it onto the bottom side of the PCB near the numpad (if you have PCB V0.7 or older), or to the top side of the PCB to the left right shift (on PCB V0.8 and newer). 

# 3.6 - Soldering on the spring-loaded pins 

If you are using PCB V0.7 or newer, solder on the spring-loaded pins, which are soldered to the top side of the PCB on the right side of the keyboard. This is used to electrically ground the plate and the screws on the top of the case. 

# Part 4 