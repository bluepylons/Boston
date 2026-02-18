![Side view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP/3DP-LP-gray-3.JPG?raw=true)

This is a prototype 3D-printed case with the following improvements:
* Reduces front height by ~2mm
* Reduces width by ~2mm
* Switches to countersunk screws for the top screws so that they no longer protrude
* Changes side profile a bit so that the top and bottom bezels are more even
* Revised Right-key separator so that it transitions better into Right-half near the arrow keys

This is intended to be backwards compatible with existing 3DP Bostons, though some of the fasteners change.

![Front view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP/3DP-LP-navy-front.JPG?raw=true)
![Rear view](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP/3DP-LP-navy-rear.JPG?raw=true)
![Right key separator](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP/right-key-separator-arrow-keys.JPG?raw=true)

# Upgrade guide (draft)

## What parts will I need? 
What parts you will need will depend on which PCB version you have (the PCB version is written on the bottom left of the PCB, roughly near the F3 key):

| PCB version       | Right-half needed                            | Can you easily install new key separators ? |
| ----------------- | -------------------------------------------- | ------------------------------------------- |
| V0.6.1J and below | Lower-profile-right-half-with-reset-hole.stp | No                                          |
| V0.7J             | Lower-profile-right-half-with-reset-hole.stp | Yes                                         |
| V0.8J and above   | Lower-profile-right-half.stp                 | Yes                                         |

The left half file (Lower-profile-left-half.stp) is identical for all versions. 

If you have an older V0.6.1J or earlier PCB and your keyboard is already built, you should keep your existing key separators as you will need to desolder all of your switches to install new key separators. Otherwise, with a newer PCB, you can also print and install the new key separators (Left-key-separator-revised-with-RGBLED.stp and Right-key-separator-revised.stp)

In addition, you will need additional screws:

| Hardware description                                                   | Quantity     | McMaster-Carr P/N       | Notes                                                                                                                                               |
| ---------------------------------------------------------------------- | ------------ | ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| M3x0.5 10mm long countersunk screw ISO 14581 (Torx) or ISO 10642 (hex) | 11           | 92125A130 (hex, silver) | McMaster does not sell stainless 10mm in Torx; [Bel-Metric](https://belmetric.com) SF3X10TXSS (silver) or SF3X10TXBLKSS (black) recommended instead |
| M3x0.5 8mm long button head screw, ISO 7380 (Torx)                     | 2, ideally 4 | 90991A113               | Also available from Bel-Metric as SB3X8TXSS (silver) or SB3X8TXBLKSS (black)                                                                      |

If you cannot salvage the M3 hex nuts from your old case, you will also need 12 new M3 hex nuts:

| Hardware description                | Quantity | McMaster-Carr P/N | Notes                                                                               |
| ----------------------------------- | -------- | ------------      | ----------------------------------------------------------------------------------- |
| M3x0.5 DIN 934 hex nut, zinc plated | 12       | 90591A250         | Also available from Bel-Metric as NR3CLZ. Do not use stainless due to galling risk. |

A summary bill-of-materials table is below:

| Part description                   | Quantity (if needed) | Type       | Notes                                                                     | 
| ---------------------------------- | -------------------- | ---------- | ------------------------------------------------------------------------- |
| New left half                      | 1                    | 3D printed |                                                                           |
| New right half                     | 1                    | 3D printed | Use "-with-reset-hole" variant if PCB V0.7J or older                      |
| New left key separator             | 1                    | 3D printed | If keyboard is already built, only use if PCB is V0.7J or newer           |
| New right key separator            | 1                    | 3D printed | If keyboard is already built, only use if PCB is V0.7J or newer           |
| M3x0.5 10mm long countersunk screw | 11                   | Fastener   |                                                                           |
| M3x0.5 8mm long button head screw  | 2, but ideally 4     | Fastener   | 2 is the bare minimum; 4 replaces the other M3x10 screws for consistency  | 
| M3x0.5 hex nut                     | 12                   | Fastener   | Only if you cannot salvage the hex nuts from your old case                |

## Assembly 

Remove all 11 screws on the top side:
![Top side screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-3.jpg?raw=true)

Remove all 12 screws from the bottom side:
![Bottom side screws](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-bottom-panel-install.jpg?raw=true)

Remove the bottom panel, and slide the old halves off. For the right half you will have to pull the front side towards you a bit to get it to slide past the arrow keys. 
![Sliding halves off](https://github.com/bluepylons/Boston/blob/main/graphics/Assembly-guide-3DP/Case-half-install-1.jpg?raw=true)

Insert M3x0.5 hex nuts into each of the 6 hexagonal pockets on the bottom of each of the new case halves. Gluing these in with super glue is recommended to prevent them from falling out during assembly - you can two drops to the inside corners of the hexagonal pocket.
![Suergluing](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/supergluing-hex-pocket.JPG?raw=true)
![Hex nut in pocket](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/hex-nut-pocket.JPG?raw=true)


### If you are installing new key separators:
If you are replacing your key separators, first remove the knob from the rotary encoder.

Flip the PCB over. Get a Torx T6 bit (a magnetic one is strongly recommended), and use it to remove all 14 of the M2 self-tapping screws (circled in orange below), and remove the old key separators:
![Remove these screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/PCB-underside-labelled.JPG?raw=true)
![Removing screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/unscrewing-key-separators.JPG?raw=true)
![Key separators removed](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/key-separators-removed.JPG?raw=true)

Install the new key separators (install the left one first), using the 14 M2 self-tapping screws, but leave the screws about a half turn too loose.
![Key separators installed](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/new-key-separators-installed.JPG?raw=true)

Temporarily install the new left and right case halves using a few M3x10 countersunk screws to screw it to the plate. For the right case half, you will have to bend the front portion slightly to get it to slide past the arrow keys.
![Key separators installed](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/halves-temporarily-installed.JPG?raw=true)

Adjust the separator pieces so that the gaps between the separators and the case halves are minimized when the plate is slid into the very end of the case halves. 
![Key separators gaps](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/halves-temporarily-installed-with-arrows.JPG?raw=true)

Flip the assembly over, and fully tighten the screws that are accessible. Remember to not overtighten the screws or you may strip the 3D-printed plastic.
![Key separators installed](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/screwing-in-key-separators.JPG?raw=true)

Remove the left and right case halves, and fully tighten the remaining screws on the key separators.

### If you are re-using your existing key separators
Do a test fit with the left and right case halves. You may need to trim off this lip between the F-row and main block on the left and right key separators with a pair of flush cutters, though only do this if the fit between this and the case halves is poor. You will ***not*** need to trim the similar lip near the knob.
![Lip](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/lip.JPG?raw=true)
![Lip removal](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/lip-removal.JPG?raw=true)


## Assembly continued

Slide on the left and right case halves. For the right case half, you will have to bend the front portion slightly to get it to slide past the arrow keys.
![Case halves slid on](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/case-halves-no-screws.JPG?raw=true)

Install the 11 M3x10 countersunk screws into the top, though leave them about a half turn loose.
![Screwing in top screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/screwing-in-top-screws.JPG?raw=true)

Install the bottom panel and rubber feet holders. Use M3x6mm long screws on the middle 8 screw holes, and M3x8mm long screws on the 4 corners screw holes. (if necessary, the 2 rear corner screws can be M3 10mm, but the front 2 corner screws must be M3x8mm long). 
![Labelled bottom screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/labelled-bottom-screws.JPG?raw=true)
![Screwing in bottom screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/screwing-in-bottom-screws.JPG?raw=true)

Place the keyboard on a rigid, flat surface. Push down gently on the middle of the keyboard while using your other hand to fully tighten the screws; this is to help make sure the keyboard is built flat and will not wobble:
![Fully tightening top screws](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/pressing-down-while-tightening.JPG?raw=true)

Flip the keyboard over, and fully tighten all the screws on the bottom.

Reinstall the knob. You are done!
![Done!](![Lip removal](https://github.com/bluepylons/Boston/blob/main/graphics/3DP-LP-specific-assembly/built-with-knob.JPG?raw=true)
