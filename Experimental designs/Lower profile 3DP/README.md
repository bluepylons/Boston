![Side view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-gray-3.JPG?raw=true)

This is a prototype 3D-printed case with the following improvements:
* Reduces front height by ~2mm
* Reduces width by ~2mm
* Switches to countersunk screws for the top screws so that they no longer protrude
* Changes side profile a bit so that the top and bottom bezels are more even
* Revised Right-key separator so that it transitions better into Right-half near the arrow keys

This is intended to be backwards compatible with existing 3DP Bostons. The far right and far left bottom screws switch to shorter M3x8 screws. 

![Side view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-navy-front.JPG?raw=true)
![Side view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-navy-rear.JPG?raw=true)

# Upgrade guide (WIP)

## What parts do you need? 
What parts you will need will depend on which PCB version you have (the PCB version is written on the bottom left of the PCB, roughly near the F3 key):

| PCB version       | Right-half needed                            | Can you easily install new key separators ? |
| ----------------- | -------------------------------------------- | ------------------------------------------- |
| V0.6.1J and below | Lower-profile-right-half-with-reset-hole.stp | No                                          |
| V0.7J             | Lower-profile-right-half-with-reset-hole.stp | Yes                                         |
| V0.8J and above   | Lower-profile-right-half.stp                 | Yes                                         |

The left half file (Lower-profile-left-half.stp) is identical for all versions. 

If you have an older V0.6.1J or earlier PCB and your keyboard is already built, you should keep your existing key separators as you will need to desolder all of your switches to install new key separators. Otherwise, with a newer PCB, you can also print the new key separators (Left-key-separator-revised-with-RGBLED.stp and Right-key-separator-revised.stp)

In addition, you will need additional screws:

| Hardware description                                                   | Quantity     | McMaster-Carr P/N       | Notes                                                                                                                                               |
| ---------------------------------------------------------------------- | ------------ | ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| M3x0.5 10mm long countersunk screw ISO 14581 (Torx) or ISO 10642 (hex) | 11           | 92125A130 (hex, silver) | McMaster does not sell stainless 10mm in Torx; [Bel-Metric](https://belmetric.com) SF3X10TXSS (silver) or SF3X10TXBLKSS (black) recommended instead |
| M3x0.5 8mm long button head screw, ISO 7380 (Torx)                     | 2, ideally 4 | 90991A113               | Also available from Bel-Metric as SB3X10TXSS (silver) or SB3X10TXBLKSS (black)                                                                      |

If you cannot salvage the M3 hex nuts from your old case, you will also need 12 new M3 hex nuts:

| Hardware description                | Quantity | McMaster-Carr P/N | Notes                                                                          |
| ----------------------------------- | -------- | ------------      | ------------------------------------------------------------------------------ |
| M3x0.5 DIN 934 hex nut, zinc plated | 12       | 90591A250         | Also available from Bel-Metric as NR3CLZ. Do not use stainless due to galling. |

A complete parts needed bill-of-materials table is below:

| Part description                   | Quantity (if needed) | Type       | Notes                                                                     | 
| ---------------------------------- | -------------------- | ---------- | ------------------------------------------------------------------------- |
| New left half                      | 1                    | 3D printed |                                                                           |
| New right half                     | 1                    | 3D printed | With reset hole if PCB V0.7J or older                                     |
| New left key separator             | 1                    | 3D printed | Only if PCB V0.7J or newer if keyboard is already built                   |
| New right key separator            | 1                    | 3D printed | Only if PCB V0.7J or newer if keyboard is already built                   |
| M3x0.5 10mm long countersunk screw | 11                   | Fasterner  |                                                                           |
| M3x0.5 8mm long button head screw  | 2, but ideally 4     | Fasterner  | 2 is the bare minimum; 4 replaces the other M3x10 screws for consistency  | 
| M3x0.5 hex nut                     | 12                   | Fasterner  | Only if you cannot salvage the hex nuts from your old case                |

## Assembly 

Remove all 11 screws on the top side:
![Top side screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-bottom-panel-install.jpg?raw=true)

Remove all 12 screws from the bottom side:
![Bottom side screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-bottom-panel-install.jpg?raw=true)

Remove the bottom panel, and slide the old halves off. For the right half you will have to pull the front side towards you a bit to get it to slide past the arrow keys. 
![Sliding halves off](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-1.jpg?raw=true)

If you are replacing your key separators, flip the PCB over. Use a Torx T6 bit to remove all 14 of the M2 self-tapping screws, and remove the key separators.
[image]

If you are using your existing key separators, use a pair of flusher cutters or a blade to trim off the overhang off these parts of left-key-separator and right-key-separator until they are flush:
[image]

Insert M3x0.5 hex nuts into each of the 6 hexagonal pockets on the bottom of each half. Gluing these in with super glue is recommended to prevent them from falling out during assembly - you can two drops to the inside corners of the hexagonal pocket.
[image] 

If you are installing new key separators, install the new key separators but leave the screws about a half turn loose:



### If you are using your existing key separators 



