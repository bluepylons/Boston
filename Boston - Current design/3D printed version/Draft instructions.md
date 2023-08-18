# Boston (3D-printed/FR4 version) Assembly Instructions, including 3D printing 

## Draft. work-in-progress, incomplete (August 7, 2023)

## To Do

* Instructions on how to solder per-key LEDs 

# Table of Contents

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
  
# What You Should Have:
* The PCB:
[image needed of PCB]
* The FR4 fiberglass plate: 
![FR4 fiberglass plate](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-FR4-plate.jpg?raw=true)
* The FR4 bottom panel:
![FR4 bottom panel](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-FR4-bottom.jpg?raw=true)
* 3x 3mm LEDs:
![3mm LEDs](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-3mm-LEDs.jpg?raw=true)
* (soldered version only) 3x 1KΩ resistors:
![1K resistors](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-1K-resistors.jpg?raw=true)
* A rotary encoder. Your vendor may also include a knob.
![Encoder](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-encoder.jpg?raw=true)
* 15 M3x10mm screws:
![M3x10mm screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-M3x10-screws.jpg?raw=true)
* 8 M3x6mm screws:
![M3x6mm screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-M3x6-screws.jpg?raw=true)
* 11 M3 PEM KF2-M3-ET threaded inserts:
![PEM KF2-M3-ET threaded inserts](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-PEM-KF2-M3-ET.jpg?raw=true)
* 12 M3 hex nuts:
![M3 hex nuts](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-M3-hex-nut.jpg?raw=true)
* 14 M2x5mm self-tapping screws:
![M2x5mm self-tapping screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-M2x5-self-tapping-screws.jpg?raw=true)
* A reset switch (note on some PCBs this is already soldered on, and won’t be included as a result):
![Reset switch](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-reset-switch.jpg?raw=true)
* (soldered version only) A set of spring loaded pins (note on some PCBs this is already soldered on, and won’t be included as a result. You can also substitute this with a short piece of wire):
[image needed of spring loaded pins]
* (hotswap version only) 10 M2 3.5mm long standoffs:
[image needed of 3.5mm long standoffs]
* (hotswap version only) 20 M2x3mm screws: 
[image needed of M2x3mm screws]

If you purchased the kit from a vendor, please inform your vendor if any of the above is missing. 

# 3D-Printed Parts
Your vendor might have included these, or you may need to print these yourself. See [Part 0 - 3D printing the case parts](#part-0---3d-printing-the-case-parts) for information on how to print these parts.

* The left and right case halves:
![3D printed case halves](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-case-halves.JPG?raw=true)

* The left key separator:
![3D printed left key separator](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-3DP-Left-key-separator.png?raw=true)

* The right key separator:
![3D printed right key separator](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-3DP-Right-key-separator.png?raw=true)

* The 3D-printed spacer for the lock LEDs:
![3D printed lock LED spacer](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Parts-3DP-lock-LED-spacer.png?raw=true)

# Parts You'll Need to Assemble the Keyboard
* MX-compatible switches. Depending on the layout you choose, you will need between 119 and 127 switches. 
* Keycaps of your choice. Make sure that they support your desired layout. 
* PCB-mount stabilizers (either screw-in or snap-in) of the correct size and quantity for your preferred layout. 
* A USB-C cable 
* A knob. The included encoder has a 6mm diameter D-shaft with a 4.5mm flat. Most knobs meant for 6mm shafts, that either have the flat or use a set screw for mounting, and are smaller than 21mm in diameter, will work.
* (optional) Through-hole LEDs for backlighting. Check that your switches and keycaps support the LEDs you choose - some switches only work with SMD LEDs (which are not supported on this PCB), and others may hit your keycaps. 

# Tools You'll Need to Assemble the Keyboard 
* A T6 Torx screwdriver or key. Make sure it is actually a T6 size!. A smaller bit may fit in the head, but is much more likely to strip the head. 
* A T10 torx screwdriver or key. Likewise, make sure it is actually a T10 size. 
* A pair of metal tweezers, wire, metal keycap puller, or unbent paper clip for testing the PCB 
* (hotswap only) A #1 Philips screwdriver. Make sure it's actually a #1 size. 
* A soldering iron and solder. 
* Super glue 
* A blue threadlocker, such as Loctite 242, 243, or 248, is recommended to prevent screws from loosening over time. 
* If you make mistakes while soldering parts in, you may need a desoldering pump (solder sucker) or desoldering wick to make fixes. 

# (Hotswap Only) - A Note on Hotswap Switch Installation

* Only use switches that have never been soldered. Desoldered switches can damage the hotswap socket.
* Make sure the pins are straight before inserting the switch 
* Support the back side of the hotswap socket when inserting switches. 

[image needed on how to support hotswap switches - similar to Novelkey's [diagram](https://cdn.shopify.com/s/files/1/3099/8088/files/Group_686_2x_cd694deb-8455-4dc1-82ed-5332ea2de4f6.png?v=1634837791) on [their instruction guides](https://novelkeys.com/pages/howto)]

# Part 0 - 3D Printing the Case Parts 

You will need to 3D-print the parts listed in [# 3D printed parts](#-3D-printed-parts). STL files for 3D printing are available on Github [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs). You will need a 3D printer with a minimum 200mm x 150mm bed x 210mm tall.

For the left and right case halves, printing with the long side facing up, like so, is recommended.
![Case halve orientation](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/3D-printing-orientation.png?raw=true)

You may also want to adjust the Z-seam setting to prevent seams from being in highly visible places. Generally, you should try to locate the Z-seam at the bottom of the case, preferably in an inside corner.

For the key separators, the following orientation is recommended, with the rounded edges facing up: 
![Key separators orientation](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/3D-printing-key-separators.png?raw=true)

# Part 1 - Putting Together The Plate and Key Separators 

## 1.1 - Soldering the Threaded Inserts into the Plate

Flip the plate over so that the underside of the plate is facing you. Press in the PEM threaded inserts into the 11 holes on the plate. 

![Pushing PEM nuts in](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-inserting-threaded-inserts.jpg?raw=true)

If it’s too hard to push the inserts in, you can use one of the M3x6 screws to pull the insert in, using a T10 Torx screwdriver. Remove the screw when the insert is all the way in.

![Pulling PEM nuts in](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-pulling-in-threaded-inserts.jpg?raw=true)
![Pulled in PEM nuts](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-screwed-in-threaded-insert.jpg?raw=true)

With the inserts pushed in, double check that they’re on the correct side - they should be on the bottom of the plate, not the top. Also, make sure the inserts are all of the way in and fully seated. Then, solder them in place:
![Soldered in PEM nuts](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-soldered-threaded-insert.jpg?raw=true)

It may take some time for your soldering iron to get the nut and plate hot enough to get the solder to flow well. Also, avoid getting solder on the threads. If you get solder on the threads, try running an M3 screw through to clear solder off the threads. If that doesn’t work, you’ll need an M3 tap to remove the solder from the threads.

# 1.2 - (Hotswap Version Only) - Installing the Hotswap Standoffs

Attach the M2 3.5mm long standoffs onto the bottom of the plate using the M2x3mm screws, onto the following marked holes on the plate:

![Soldered in PEM nuts](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-standoff-positions.png?raw=true)

[image needed of plate with screwed in standoffs]

# Part 2 - Attaching and Aligning the Key Separators

*On PCBs older than V0.7, the key separators cannot be adjusted after the switches are soldered on without desoldering all your switches. Make sure you get this right before soldering anything!* 

Next, grab the 3D-printed left-key-separator and right-key-separator pieces, and the M2x5 self-tapping screws. These pieces need to attach to the plate before the switches are soldered in.

![Key separators](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separator-parts.png?raw=true)

Attach the key separators to the plate using the M2x5 self-tapping screws, via the small holes located in the plate. Use a T6 Torx screwdriver for this. Make sure the screws go in straight! **Do not tighten these all the way - leave them about a ½ turn loose, since we’ll need to adjust and align these in a little bit.** There are 14 screws that need to be attached in total - 6 on the left separator, and 8 on the right separator. 

![Key separators](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-assembly-1.jpg?raw=true)

![Key separators](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-assembly-2.jpg?raw=true)

![Key separators](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-assembly-3.jpg?raw=true)

With the screws in but not tightened fully, do a test fit against the left and right case halves by sliding the plate into the left and right case halves. Note that you’ll have to slightly spread apart the right case half to get it past the arrow key cluster. 

![Key separators test fit](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-test-fit.jpg?raw=true)

Attach the plate to the case using M3x10mm screws. Make sure the plate is fully seated against the case.

![Key separators test fit](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-test-fit-2.jpg?raw=true)

Adjust the separator pieces so that the gaps between the separators and the case halves (marked in orange) are minimal when the plate is slid into the very end of the case halves. There may be a small gap between the two separators (gap marked in pink) - this is normal. 

![Plate key separators gap](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-gap.png?raw=true)

Flip the assembly over, and tighten the screws that can be accessed:

![Plate key separators assembly 4](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-assembly-4.jpg?raw=true)

Remove the case halves, and tighten up the remaining screws:
![Plate key separators assembly 5](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Plate-key-separators-assembly-5.jpg?raw=true)

Put everything back together and do a final check of the gaps. Make any adjustments as necessary. Again, on PCBs older than V0.7, you can’t fix this once the switches are soldered in!

When everything looks good, remove the case halves again, and make sure all the screws are tight. 

# Part 3 - Testing and Soldering Additional Parts on the PCB

# 3.1 - Testing Each Key on the PCB 

Testing the PCB before further assembly is recommended - use a tweezer, metal keycap puller, wire, or unbent paperclip to short the switch opening pins, and a program such as [Aquakeytest](https://geekhack.org/index.php?topic=34670.0) or [Vial](https://get.vial.today/)'s built-in matrix tester to ensure that each key works. 

![PCB testing with tweezers](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-testing-tweezer.jpg?raw=true)

# 3.2 - (Soldered Version Only) - Soldering on the 1KΩ Resistors

Grab the 3 1KΩ resistors and solder them into the spots for R200, R201, and R202, on the top side of the PCB. If you’re using your own LEDs and want them brighter or dimmer, you may want to use different resistors than the provided resistors.

![PCB 1K resistors](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-1K-resistors.jpg?raw=true)

# 3.3 - Soldering on the Lock LEDs 

Grab the spacer for the LEDs, and run the LEDs legs through it. Place the LEDs and spacers onto the PCB, for spots LED201, LED202, and LED203. Note that the spacer only fits in one way.

![PCB lock LEDs](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-lock-LEDs.jpg?raw=true)

Note that LEDs are directional and will not light up if soldered in backwards. The longer leg on an LED is +. Make sure this matches up with the + symbols on the PCBs. 

![LED polarity](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-lock-LEDs.jpg?raw=true)

Once the LEDs are in, solder them in. Make sure that they’re in straight! 

![PCB lock LEDs](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-lock-LEDs-done.jpg?raw=true)

If you haven’t already done so, clip the legs on the resistors and LEDs with a pair of flush cutters.

# 3.4 - Soldering the Rotary Encoder 

Next, solder on the rotary encoder onto the top left corner of the PCB.

![Rotary encoder](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-encoder.jpg?raw=true)

# 3.5 - Soldering on the Reset Switch 
If your PCB did not come with the reset switch soldered on, solder it onto the bottom side of the PCB near the numpad (if you have PCB V0.7 or older), or to the top side of the PCB to the left right shift (on PCB V0.8 and newer). 

![Reset switch](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-reset-switch.jpg?raw=true)

# 3.6 - Soldering on the Spring-Loaded Pins 

If you are using PCB V0.7 or newer, solder on the spring-loaded pins, which are soldered to the top side of the PCB on the right side of the keyboard. This is used to electrically ground the plate and the screws on the top of the case so that static shocks do not reset the keyboard microcontroller. If you do not have the spring loaded pins, you can solder a small wire to where the spring loaded pin goes and solder the other end of the wire to the corresponding area on the plate. 

![Spring loaded pins 1](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-spring-loaded-pin-1.jpg?raw=true)
![Spring loaded pins 2](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/PCB-spring-loaded-pin-2.png?raw=true)

# Part 4 - Installing Stabilizers and Switches

# 4.1 - Deciding Your Layout

Boston supports the following layout on the soldered PCB:
![Soldered PCB supported layouts](https://github.com/bluepylons/Boston/blob/main/graphics/bostonKLE.png?raw=true)

The following layouts are supported on the hotswap ANSI PCB:
![ANSI HS PCB supported layouts](https://github.com/bluepylons/Boston/blob/main/graphics/boston-hotswap-ANSI-KLE.png?raw=true)

Decide what layout you want (for example, do you want ANSI Enter, or ISO Enter?), and determine where you’ll need to install stabilizers. Any keys 2 units wide or longer (for example, a standard backspace key) will need stabilizers. Also, make sure you have the keycaps for the layout you want.

## Modding Your Switches and Stabilizers 
If you want to mod or tune your switches or stabilizers (e.g. lubing them, or changing the springs in them), do so before installing them. It is much harder to make any changes after they’re installed. On soldered keyboards, stabilizers cannot be installed or removed after switches are soldered in, without desoldering most or all of your switches.

# 4.2 - Installing the Stabilizers 

Boston takes PCB-mount stabilizers, either screw-in or clip in style. These are available from several manufacturers (e.g. GMK, TX, Cherry, C3, Durock, Zeal, and others make PCB mount-stabilizers).

Install all the stabilizers according to the instructions from their manufacturer.

![Stabilizers](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Stabilizers.jpg?raw=true)

# 4.3 - (Hotswap Version Only) - Attaching the PCB to the Plate 

Screw the PCB onto the plate via the 10 standoffs on the plate that were previously attached in Step 1.2. 

[image needed]

# 4.4 - Testing Your Stabilizers 

It’s strongly recommended to test your stabilizers before proceeding, as any fixes to your stabilizers after soldering the switches will likely require removing or desoldering all the switches and removing the plate from the PCB. Test them now, as if there's something wrong with them it will be much more work to fix them later.

To do this, take a switch and an appropriate keycap for the stabilizer you want to test. If you're on the soldered version, you will also need to grab the plate now. 

Install the switch onto the plate and PCB. On the hotswap version, remember  to support the hotswap socket from the back side while inserting the switch, and that the switch pins are straight before inserting it in. On the soldered version - you do not need to solder the switch in yet - just make sure it fits into the PCB. 

![Stabilizer testing 1](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Stabilizer-testing-1.jpg?raw=true)

Install the keycap onto the switch. Make sure the key feels okay - that it’s not binding, or failing to go all the way to the bottom, or failing to return, for instance. Do this for all your stabilizers to make sure that they’ve been installed properly. 

![Stabilizer testing 2](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Stabilizer-testing-2.jpg?raw=true)

# 4.5 - Installing Your Bottom Row 

On the soldered version - we’ll start installing and soldering switches on the bottom row as this is the most likely place that mistakes are made, since the soldered version of Boston supports several different bottom row layouts, and it's easy to accidentally put a switch in the wrong place. You can also start here on the hotswap version, though due to the more restricted bottom row layout you're much less likely to make mistakes here.

Both the plate and PCB on the soldered version are marked with where to put the switches in for your desired bottom row positions. The arrows point at the center of the switch. Install switches into the desired positions on the bottom row. Make sure that the switches are fully seated into the plate. 

After installing the switches into the plate, and before soldering the switches, install keycaps on your bottom row to ensure that everything is in the correct place. Make any fixes as necessary. 

![Bottom row testing](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Bottom-row-test.jpg?raw=true)

If everything looks correct, solder the switches in.

# 4.6 - Install the Rest of the Switches

Solder or install the rest of your switches.

# Part 5 - Case Prep and Assembly

# Part 5.1 - Installing the M3 Hex Nuts into the Case

Take the left and right case halves from earlier, and the M3 hex nuts. Push the hex nuts into the 6 hex-shaped pockets on the bottom of each case half. If it’s difficult to push them in, you can use an M3x6 screw to pull the nuts in. If the nuts fit in loosely and fall out easily, glue them in with super glue or hot glue.

![Pushing M3 nuts into case](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-pushing-nut-in.jpg?raw=true)

# Part 5.2 - Installing the Case Halves 

Take the left and right case halves and slide them onto the plate, and screw them into the plate using M3x10 screws. **Do not tighten these down all the way - leave them about 1 turn loose, as we need to align them later.** For the right case half, you’ll have to spread the case apart slightly to get it past the arrow key cluster.

![Case half install 1](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-1.jpg?raw=true)
![Case half install 2](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-2.jpg?raw=true)
![Case half install 3](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-3.jpg?raw=true)

# Part 5.3 - Installing the Bottom Panel and Rubber Feet 

Flip everything over, and install the bottom panel. With PCB V0.7 and older, you need to place the bottom panel in the orientation shown (if you get it backwards, the reset switch will not be accessible). On PCB revision V0.8 or older, you can install the bottom panel in either orientation as the reset button has moved to the top side.

Install M3x6 screws in the middle 8 holes to secure the bottom panel. Avoid pushing down on the screwdriver as this can cause the hex nut on the other side to push out and fall out (and you’ll have to take the case back apart to retrieve it and reinstall it). Again, don’t tighten these in all the way, but leave them about a turn loose.

![Case bottom panel install](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-bottom-panel-install.jpg?raw=true)

Take the FR4 rubber feet holders and install them on the ends using M3x10 screws. Again, avoid pushing down on the screwdriver. Tighten these screws in all the way. 

![FR4 bottom feet holder install](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-FR4-rubber-feet-holder-install.jpg?raw=true)

Once the rubber feet holders are installed, peel the rubber feet off from the backing sheet and stick them onto the four corners.

![Rubber feet install](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-rubber-feet-install-1.jpg?raw=true)
![Rubber feet install](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-rubber-feet-install-2.jpg?raw=true)

# Part 5.4 - Leveling the Keyboard 

Next, take the keyboard and place it right-side up over a flat, level surface. Take your palm or forearm, and push the keyboard down against your flat, level surface, and tighten all the exterior case screws. This is to make sure the case and feet are flat and do not wobble. 

![Leveling](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Leveling.jpg?raw=true)

Once this is done, press down on the corners of the keyboard and make sure the keyboard doesn’t wobble or see-saw. If it still does, make adjustments as necessary. There may be a slight misalignment between the left and right case halves after this adjustment - this is normal, as unfortunately 3D printing is a relatively imprecise process. If there is unresolvable wobble or misalignment, you may need to adjust the frame alignment on your 3D printer and reprint the parts.

After all this, install the knob and keycaps. Plug the keyboard into a computer and check that it works (it may take a couple of seconds for the keyboard to initialize). You’re done!

![You are done!](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Keyboard-done.jpg?raw=true)

# Appendix 1 - Flashing Firmware

# Appendix 2 - Default Firmware Key Assignments

The knob is set for volume. Press the knob for mute. 