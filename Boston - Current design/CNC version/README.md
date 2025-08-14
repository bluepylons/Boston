# Boston CNC Version

![CNC version](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/DSC_0395_01.JPG?raw=true)

These are the files for the CNC version of Boston. The PCB is in the [PCB](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB) directory however. 

# Ordering Guide for making your own Boston (draft)

This is the ordering guide for the CNC version of Boston.  

**Order parts at your own risk. These files are provided as-is, and I am not responsible for any losses, harm, or damage incurred by following this guide, by ordering parts, by using the files provided, by using the resultant parts or assembled keyboard, or from any mistakes or errors in the files, ordering guide, or resultant parts. Even components that have been prototyped may still contain errors. ** 

**This is for the S1 daughterboard version. The older variant uses the C3 Unified Daughterboard; see README-C3-DB.md for that version**

# What you will need:

### Parts:

## Parts needed for all variants
| Description                                        | Qty per board | Type                                               | Notes                                                                                                                   |
| -------------------------------------------------- | ------------- | ---------------------------------------------------| ----------------------------------------------------------------------------------------------------------------------- |
| Case top                                           | 1             | Custom (CNC machined)                              |                                                                                                                         |
| Case bottom                                        | 1             | Custom (CNC machined)                              |                                                                                                                         |
| Plate                                              | 1             | Custom (PCB, laser cut, waterjet, or CNC machined) | Several variants                                                                                                        |
| PCB                                                | 1             | Custom (PCB)                                       | Several variants                                                                                                        | 
| LED spacer (for the lock LEDs)                     | 1             | Custom (3D-printed)                                | Different from the one for the 3DP Boston                                                                               |
| S1 Unified (or compatible) Daughterboard           | 1             | Off-the-shelf or custom                            | Later S-series (e.g. S1.1) should work                                                                                  |
| S1 Unified Daughterboard cable (>75mm long)        | 1             | Off-the-shelf or custom                            | Make sure the [pinout is correct](https://unified-daughterboard.github.io/#/info-consumer?id=buying-replacement-cables) |
| 3mm LEDs for lock LEDs                             | 3             | Off-the-shelf                                      | Pick a color you like!                                                                                                  |
| Alps EC11E18244A5 rotary encoder                   | 1             | Off-the-shelf                                      | Other rotary encoders may work, but may need firmware tweaks                                                            |
| Knob suitable for 6mm D-shaft                      | 1             | Off-the-shelf                                      |                                                                                                                         |
| M3x0.5 10mm socket head cap screw                  | 4             | Off-the-shelf                                      |                                                                                                                         |
| M3x0.5 16mm socket head cap screw                  | 4             | Off-the-shelf                                      |                                                                                                                         |
| M3x0.5 5mm socket head cap screw                   | 12            | Off-the-shelf                                      |                                                                                                                         |        
| 3/4" dia x 3/8" tall rubber dome feet              | 2             | Off-the-shelf                                      |                                                                                                                         |               
| 3/8" dia x 5/32" tall rubber dome feet             | 2             | Off-the-shelf                                      |                                                                                                                         |
| VCC LFC037CTP Light Pipe                           | 1             | Off-the-shelf                                      |                                                                                                                         |
| VCC RTN125 Light Pipe Retainer                     | 1             | Off-the-shelf                                      |                                                                                                                         |

| Description                                  | Qty per board                                 | 
| -------------------------------------------- | --------------------------------------------- | 
| MX-style switches                            | 119-127 (depending on layout)                 |  
| Stabilizers (PCB mount)                      | 2-8 2u, 0-1 6.25u or 7u (depending on layout) |

For a standard ANSI build (using the fixed layout plate) you need 121 switches, 6 2u stabilizers, and 1 6.25u stabilizer. 

## Additional parts needed only for the soldered PCB variant 

| Description                                        | Qty per board | Type                                                   |
| -------------------------------------------------- | ------------- | ------------------------------------------------------ |
| 1KΩ 1/4W through-hole resistor for lock LEDs       | 3             | Off-the-shelf                                          |

## Additional parts recommended for the hotswap variant 

| Description                                            | Qty per board | Type          | Notes                                                                                                                                               |
| ------------------------------------------------------ | ------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| M2x0.4 3.5mm threaded standoff for hotswap boards      | 10            | Off-the-shelf | Available as a [13-pack from KBDfans](https://kbdfans.com/products/kbdfans-m2-3-countersunk-flat-head-screw-kit)                                    |
| M2x0.4 3mm Philips-head pan head screws                | 10-20         | Off-the-shelf | The KBDfans kit comes with 13 of them, but you will need another 7 if you aren't countersinking the plate                                           |
| M2x0.4 3mmm flat head screw                            | 0-10          | Off-the-shelf | Only needed if you're countersinking the plate, and the KBDfans kit comes with enough, so you shouldn't need to buy these if buying the KBDfans kit |

These are recommended for the hotswap variant for holding the plate and PCB together, though you might be fine just relying on the switches to hold the plate and PCB together.

## Additional parts needed only if ordering the PCB through JLCPCB

| Description                                        | Qty per board | Type                                               |
| -------------------------------------------------- | ------------- | -------------------------------------------------- |
| 6x6mm tact switch, through-hole, 5mm high          | 1             | Off-the-shelf                                      |

## Tools needed 
| Description                                                                                      |  Used for                                                           |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| 2.5mm hex key or bit ("Allen key")                                                               | All M3 screws                                                       |
| Soldering iron and solder                                                                        | For soldering everything                                            |
| Flush cutters                                                                                    | For cutting legs off soldered LEDs and resistors                    |

## Additional tools recommended for the hotswap variant only
| Description                                                                                      |  Used for                                                           |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| Philips #1 screwdriver                                                                           | The optional M2 screws that attach the plate to the PCB             |
| Switch puller                                                                                    | Removing switches                                                   |

# Case

Boston has a two piece case, consisting of the top and the bottom. It does not have a weight (though, if you have mechanical design and CAD skills, it should be pretty easy to add an internal weight to the design). 

## How to contact a machine shop to order the case 

To have the case made, you will need to contact a machine shop with a CNC machine. These are informally referred to as "manus" by the mechanical keyboard community.

[Dadesin](https://dadesin.en.alibaba.com/) is a popular high-quality Chinese one, though expensive. I used [SuNPe](https://sunpe.com/) (also in China) for my prototypes, though the quality was middling. A friend ran a small private group buy through [Gaojie](https://www.gj-prototype.com) and had good results. There are numerous other ones. You can also reach out to a local CNC machine shop.  Note that usually there is a tradeoff between cost and quality, with cheaper shops often being lower quality or sloppier with their machining (and more prone to mistakes, like forgetting to machine features or forgetting to tap holes). 

You will need to send a "Request for Quote" email to them with the following files:

* 3D files - you will need the 3D .STEP files for the [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/STEP/Boston-top.stp), and the [bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/STEP/Boston-bottom-S1-UDB.stp)
* The mechanical drawings, which include the tapping instructions for the tapped (threaded) holes. [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-top.pdf), [Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-S1-UDB.pdf)
* If you want a raw as-machined finish with visible tool marks, or want to anodize directly over the tool marks, you may want to include the milling instructions for more pleasing tool marks. [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-top-AS-MACHINED-milling-instructions.png), [Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-AS-MACHINED-milling-instructions.png) If you are going for a bead-blasted finish, you do not need to include these. These are PNG images with picture illustrations, as many machine shops are overseas and do not speak English well. 
* In the body of the email, you want to specify the quantity, material, and the surface finish, as well as that you want these parts to be made by CNC machining. Materials and surface finish are discussed more in depth in the next sections.

You will also need to specify a material and a finish, a color for the finish (if you are anodizing, e-coating, painting, powder coating, or Cerakoting), as well as the quantity you want to order. Here is an example email reaching out to a manufacturer for a quote:

![Example email to manufacturer](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/example-email.PNG?raw=true)

The manufacturer will get back to you with a quote. If you wish to proceed with the quote, let them know that you wish to proceed, and they will send you instructions for payment (often via Paypal or bank transfer) and ask for a shipping address. 

With a Chinese shop, expect to pay $300-$700 for a single case machined out of aluminum (and about $60-$150 for shipping - note that some machine shops inflate their shipping costs). Expect higher for a US or EU shop. The price each usually goes down if you order more (even 3-5 units can lower the price significantly for each board over ordering just 1). 


## Material

Most custom keyboards are made out of aluminum. There are several different aluminum alloys that are commonly used:

* **6061** - this is a general purpose aluminum alloy and the most common aluminum alloy used for CNC-machined parts. It's a jack of all trades, with decent strength, anodizing finish quality, machinability, and corrosion resistance compared to other aluminum alloys, as well as other desirable properties for some non-keyboard applications (e.g. weldability). Due to its ubiquity and ease of machining it will likely be the cheapest aluminum alloy to make your keyboard out of. All of the prototypes of Boston used 6061. 

* **6063** - Also known as "architectural aluminum", this tends to anodize a bit nicer than 6061, but is half the strength of 6061 and somewhat softer. This means the keyboard will dent more easily, threads will strip more easily (though Boston uses larger M3 threads that are harder to strip than the smaller M2 threads found on many keyboards), and if you have a raw finish, the aluminum will scratch more easily.

* **5052** - I honestly don't know why this gets used in keyboards, as it's mostly used in industry for bent sheet metal (as it bends well without cracking, unlike 6061) and for welding. It's weaker than 6061, but stronger than 6063.

* **7075** - 7075 is a significantly stronger and harder alloy than 6061, and somewhat more expensive, but doesn't anodize as well (it can anodize, but the colors are more limited and the finish won't be as good). If you're looking to keep a raw aluminum finish, 7075 will  be a bit harder to scratch (though it will still scratch quite easily). It will also be harder to dent, and the threads will be more resistant to stripping. However, in raw form it is less corrosion resistant than 6061. 

Other commonly used materials for keyboards - you can use the same files to CNC machine a case out of these materials.
* Polycarbonate
* POM (also known as acetal, and under various proprietary names such as Delrin®). You mostly likely will only be able to obtain this in white or black.
* Brass - brass is expensive and heavy, but machines very well. Note that common brass alloys use for machining (such as brass 360 alloy) have a substantial lead content, and you probably want to specify a coating to avoid lead exposure from handling the keyboard.

There are also more exotic materials, such as stainless steel, titanium, various nickel alloys, copper alloys, and so on that you could hypothetically make a Boston keyboard with using the same files. These are generally much more difficult to machine, and will be very expensive. 

## Surface finish 

In addition to the material, you want to pick a surface finish. There are two parts to this - the texture, and the coating. The vast majority of custom keyboards use a fine bead blasted texture with a Type II anodization coating, which can be dyed different colors. 

### Textures:
* **As-machined** - this is the finish straight out of the CNC, with tool marks, scratches, and all. The appearance of the tool marks and roughness may vary significantly depending on the machine shop's choice of tool, tool path, and feeds and speeds. Using a fly cutter or large face mill and a fine finishing pass can result in *very* shiny finishes. Not common in keyboards, though it's shown up on some Keycults. All of the prototypes of the CNC Boston used an as-machined finish. You can anodize over the tool marks directly, though this is also uncommon. Note that some machine shops occasionally will deburr sharp edges with scour pads, sandpaper, or a wirebrush, which may remove some of the tool marks. If you want the tool marks preserved, you need to tell them to not deburr with those tools. The as-machined milling instructions specify to not use those tools. 
* **Bead Blasted** - this involves blasting the keyboard with fine glass beads for an even matte finish. Most metal keyboards are bead blasted, as well as almost all aluminum consumer electronics (iPhones, Macbooks, etc.). This is almost always paired with a Type II anodize (though you need to specify the anodization separately). Note that there are different roughnesses available, ranging from coarse to fine. I'm not familiar with the specifications for these, but you probably want to specify a "fine" or "very fine" roughness, or specify a specific size. The [Bakeneko60](https://github.com/kkatano/bakeneko-60) specifies a #150 bead blast finish.  
* **Brushed** - this involves using a wirebrush or flapper wheel to impart horizontal streaks across your parts. Not common in keyboards, though you occasionally see it in other consumer electronics. Again, there are different roughnesses available. 
* **Tumbled** - this uses a large tumbling machine and tumbling media (ranging from to plastic  beads to corn cob and walnut husks) to apply an even finish to the part. Again, different roughnesses are available. I'm not aware of any keyboards that use this and am unfamiliar with the textures you can achieve with this, but you can ask if your machine shop can do it. 
* **Polished** - this involves buffing out the case using either a polishing wheel or a tumbling process. I'm not very familiar with this, but you can ask your machine shop.

### Coatings:
* **Anodized** - almost all aluminum on consumer electronics (including custom keyboards) are anodized, usually over a fine bead-blasted finish. Anodizing generates a protective layer of aluminum oxide on the outside of the part, which is much harder than the underlying raw aluminum. This significantly improves the scratch resistance, and also protects the aluminum from corrosion. This layer of aluminum oxide can be clear (showing the underlying silver aluminum), or be dyed a wide range of different colors ([except for white](https://www.bluebuddhaboutique.com/blog/2011/09/no-white-anodized-aluminum/)). However, if you're going for a shiny as-machined or polished finish, it can dull the aluminum a bit. There are a couple of types of anodizing, but Type II (cosmetic anodizing) is the most common, and what you probably want as it is inexpensive, and available in a wide variety of colors. Type III (Hard Anodizing) is occasionally done but uncommon in consumer electronics - Type III generates a much thicker layer of aluminum oxide than Type II, resulting in a dark gray, black, or bronze-brown color. This results in very good wear and scratch resistance, but costs more, can interfere with threaded holes, and is generally unnecessary for keyboards. Note that many machine shops outsource their anodizing, though some (e.g. Dadesin) anodize in-house. If you want to read up more on anodizing, [this](https://omwcorp.com/understanding-and-specifying-anodizing-2/) is a good document to go over (thanks to Croktopus for finding the document). 
* **Raw aluminum** - this means not using any coating whatsoever and leaving the bare metal exposed. Note that raw aluminum is easily scratched (and will most likely arrive from the machine shop with scratches from shipping and handling), so this is a fairly uncommon finish. It may also discolor from corrosion. However, paired with an as-machined or polished finish texture, it can be extremely shiny and reflective. All of my prototypes had a raw finish.   
* **E-coat**, **paint**, **powder coat**, or **Cerakote** - I am not familiar with ordering these finishes, but they show up on keyboards from time to time, and are available in a wide variety of colors. Your machine shop might not be able to handle these, and you may need to find a third party painter, powder coater, or Cerakote applicator. 

**Note that any coating that adds appreciable (>0.03mm) thickness (such as Type III hard anodizing, powder coat, e-coat, paint, and Cerakote) will require the threaded holes and the RGBLED hole to be masked off. Standard (Type II) anodizing is usually thin enough that interference isn't an issue and masking holes should not be needed. 

![RGBLED hole that needs to be masked ](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/RGBLED-hole-masking.png?raw=true)

# Plate

Boston has a traditional top mount plate. 

There are several variants of the plate, and different plates for the hotswap and soldered plates. 

## Plate Variants 

### Hotswap ANSI

![KLE of the hotswap ANSI layout](https://github.com/bluepylons/Boston/blob/main/graphics/boston-hotswap-ANSI-KLE.png?raw=true) 

The hotswap ANSI plate supports all the layouts supported on the hotswap ANSI PCB ([V0.8.2DHA](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8.2DHA)). It also has holes for the 3.5mm standoffs between the PCB and plate, to hold the assembly together when there are no switches installed. 

Note that the hotswap layout reverses the 2.75u and 2.25u split space layout compared to the soldered layout (this was necessary to accommodate those layouts with hotswap sockets). This is reflected in the hotswap plate. The hotswap plate can be used with the soldered PCB if you are not using split space though. 

If you are getting the plate CNC machined, there is a version of the hotswap ANSI plate with countersunk holes for the standoffs if you want to use countersunk screws for a flush finish. Send the [countersinking instructions](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Plate/Hotswap-ANSI/Hotswap-ANSI-plate-countersunk-countersinking-instructions.pdf) to the manufacturer along with the [3D .STEP file](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Plate/Hotswap-ANSI/Hotswap-ANSI-plate-countersunk.stp). Some laser cutting services also offer countersinking, like [Sendcutsend](https://sendcutsend.com/services/countersinking/). 

All of the files for the hotswap ANSI plate are [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Plate/Hotswap-ANSI). 

### Hotswap ISO
![KLE of the hotswap ISO layout](https://github.com/bluepylons/Boston/blob/main/graphics/boston-hotswap-ISO-KLE.png?raw=true) 

The hotswap ISO plate supports all the layouts supported on the hotswap ISO PCB [V0.8.2DHI](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8.2DHI). **Note neither this plate nor the hotswap ISO PCB have been prototyped or tested.**

Note that the hotswap layout reverses the 2.75u and 2.25u split space layout compared to the soldered layout (this was necessary to accommodate those layouts with hotswap sockets). This is reflected in the hotswap plate. The hotswap plate can be used with the soldered PCB if you are not using split space though. 

### Soldered plate (universal layout)

The soldered universal layout plate supports all the [layouts supported](https://github.com/bluepylons/Boston/blob/main/graphics/bostonKLE.png?raw=true) on the soldered PCB ([V0.8D](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8D))

All of the files for the soldered universal layout plate are [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Plate/Soldered-universal).

### Soldered plate (ANSI fixed layout) 

This accommodates only the [standard ANSI layout](https://github.com/bluepylons/Boston/blob/main/graphics/bostonKLE-ANSI-fixed-layout-plate-support.PNG?raw=true) (with a non-stepped Caps Lock key). This results in easier asseembly and an easier-to-clean plate  over the universal plate.

All of the files for the solderedfixed layout plate are [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Plate/Soldered-ANSI-fixed-layout).

## Getting the plate manufactured 

There are a couple of ways to get the plate manufactured. The plate should be made out of 1.4-1.6mm material (which is the official Cherry spec for having the switches click in properly).

### Laser cutting
Virtually all metals (aluminum, brass, steel, titanium, etc.) can be cut using a powerful laser, as well as certain plastics (POM and PP). This will usually be the most cost-effective option for a metal, POM, or PP plate. To get a plate cut, you want to use the DXF (.dxf) file. Units are in mm.

[Sendcutsend](https://sendcutsend.com/) in the US and [Laserboost](https://www.laserboost.com/) in the EU are popular laser cutting services. Many Chinese CNC machine shops, including popular keyboard manufactuerers like Gaojie and Dadesin also offer laser cutting if you want them to make your plate for you as well. 

For the hotswap plate, some laser-cutting services offer countersinking. They may either offer it through their web interface, or you may have to manually request it. Attach the countersinking instructions for the respective plate file. 

#### Waterjet cutting
This is rarely used for keyboard plates as it's not as cost effective as laser-cutting, but is also an option as well if you have access to one. This supports more materials than laser cutting. This uses the same DXF (.dxf) file.

### CNC machining
CNC machining is preferred for some materials like polycarbonate and carbon fiber, which cannot be laser cut. You can ask the same manufacturer as the case to CNC machine the plate for you. 

If you are looking to have the plate CNC machined, you want to use the STEP (.stp or .step) file. Again, the units are in mm. 

### As a printed circuit board (FR4 and aluminum only)

If you are looking to have the plate made out of FR4 or aluminum PCB material, you want to use the .zip Gerber files. This will have to be ordered as a PCB, and can be uploaded to any PCB supplier (JLCPCB, Elecrow, PCBway, AllPCB, etc.). Note that some PCB manufacturers (e.g. JLCPCB) charge an additional fee for plates due to the amount of machining required. Choose 1.6mm for the PCB thickness. 

Note - on JLCPCB, make sure that "Specify A Location" for "Remove Order number" is selected so that the order number doesn't get printed somewhere you don't want. The Gerber files have the requisite "JLCJLCJLCJLC" text on them and placed in an unobstrusive location.

![Remove Order Number](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Remove-Order-Number.png?raw=true) 

 Also, "Paper between PCBs" under "Advanced Options" is strongly recommended- otherwise there's a decent risk of FR4 parts showing up scratched. 
 
![Paper Between PCBs](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Paper-between-PCBs.PNG?raw=true)

# PCBs

You can order an assembled PCB (minus switches, LEDs, and rotary encoder) from a PCB fab such as JLCPCB or Elecrow.

Note that **the CNC version of Boston does not use the same PCBs as the 3D printed version** due to the daughterboard, though they use the samae firmware as the key matrix is identical. All PCB variants with a -D suffix ("D" for "daughterboard) are for the CNC variant.

## Hotswap ANSI PCB 
The current hotswap ANSI PCB is [V0.8.2DHA](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8.2DHA)

## Hotswap ISO PCB 
The current hotswap ANSI PCB is [V0.8.2DHI](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8.2DHI). **Note this PCB has not been prototyped or tested**

## Soldered PCB
The current soldered PCB is [V0.8D](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.8D)

## Ordering on JLCPCB 
[JLCPCB](https://jlcpcb.com/) is cheap and fast, but doesn't have the best cosmetic finish, and their SMT assembly is limited to parts [they stock](https://jlcpcb.com/parts) (though they recently announced "Global Parts Sourcing"). In the community they tend to only be used for prototypes.

To order a PCB from JLCPCB, you will need the Gerber files (which defines the bare PCB), the SMT bill of materials (BOM file, which is a list of parts that are to be soldered to the PCB), and the component placement file (CPL, which defines where those parts go). These files are available under the "Manufacturing Files" folder of the PCB (**NOTE - some PCB versions do not yet have their JLCPCB files ready yet **)

First, you want to go to [JLCPCB](https://jlcpcb.com/), and press "Order Now".

![Step 1](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/1-JLCPCB-home.png?raw=true)

Next, you want to upload the Gerber file for the PCB. You may need to manually input the PCB dimensions (393.5x147mm). 

![Step 2](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/2-add-gerbers.png?raw=true)

Here, you want to change the specifications to the following. 

![Step 3](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/3a-JLCPCB-options-standard.png?raw=true)

Next, you want to scroll down and turn on PCB Assembly. Make sure the following options are selected. 

![Step 4](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/4a-SMT-standard.png?raw=true)

Press Confirm. Next, you want to upload the BOM and CPL files. 

![Step 5](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/5-BOM-CPL.PNG?raw=true)

Make sure that all the components are selected. Any part that says "Inventory shortage" will not be installed, and you will have to substitute a compatible part, wait for the part to come back in stock, or if you're up to the challenge of SMT soldering, order the part separately and solder it on yourself. 

![Step 6](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/6-BOM-CNC.PNG?raw=true)

The next page is a confirmation page. Note that the parts placement preview may be inaccurate (JLCPCB engineers will look over this and make any parts orientation corrections, so don't worry too much about this). 

![Step 7](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/7-checkout-CNC.PNG?raw=true)

As the microcontroller is frequently out of stock due to the chip shortage, line number 16 (for designator U701) can be changed for different compatible MCUs (see the "Compatible MCUs" section below for a list of MCUs that will work). At different times some microcontroller variants may be cheaper than the others (for example, on August 29, 2022, the STM32F072CBT6 is $4.50 and the STM32F072CBU6 is $9.52, whereas during other times -CBU6 has been significantly cheaper than the -CBT6). In the BOM and CPL spreadsheet you will need to change the Comment field for that line to the name of the microcontroller you want to use, and change the Footprint and LCSC Part Number as appropriate. The line for the microcontroller is highlighted in yellow in the BOM and CPL files.

### Compatible MCUs 

Boston uses a 128kb STM32F072CB-series microcontroller, and can accept either the LQFP-48 (STM32F072CxTx) or 48-UFQFPN (STM32F072CxUx ) versions. This is Line #19 on the JLCPCB BOM files. Due to fluctuations in price some variants may be cheaper over time. 

Any of the following microcontrollers will work, and support all features. 

**Compatible MCUs - JLCPCB BOM Line #19**
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

### Other Interchangeable Parts On The PCB 

This is here for reference in case some parts are out of stock.

**U702 - JLCPCB BOM Line #17**
This is a SOT-223 linear regulator to drop the 5V down to 3.3V. Since ceramic capacitors are used the output, and some linear regulators are unstable with ceramic capacitors as their ESR is too low, the linear regulator needs to be explicitly compatible with low-ESR output capacitors.

| Part                                                  | JLCPCB (LCSC) part number |
| ----------------------------------------------------- | ------------------------- |
| Diodes Inc AZ1117IH-3.3TRG1 (default)                 | C108495                   |
| TI TLV1117LV33DCYR                                    | C15578                    |

**U705 - JLCPCB BOM Line #18**
This is a 74LVC1T45 level shifter in an SOT23-6 (SOT26) package. 

| Part                                 | JLCPCB (LCSC) part number |
| ------------------------------------ | ------------------------- | 
| TI SN74LVC1T45DBVR        (Default)  | C7843                     |
| TI SN74LVC1T45DBVT                   | C116653                   |
| Diodes Inc 74LVC1T45W6-7             | C168856                   |

## Ordering on Elecrow

Elecrow is a full-service PCB assembly shop, and one of the go-tos in the community for custom keyboard PCBs for the actual group buy sales. They can install any part (not just ones they stock) and generally have better quality surface finish, but is much slower (typically 3-4 week turn around time), and costs more (especially in small quantities). 

To order from Elecrow, you will need to email service@elecrow.com with the Gerber files and the files from the "Elecrow SMT files" folder for your respective PCB. They will get back to you with a quote.

On the spreadsheet (.xlsx) file, you will need to edit the first tab to specify your quantity, color, and surface finish. Elecrow's available colors and surface finishes are posted on their [PCB ordering page](https://www.elecrow.com/pcb-manufacturing.html)

![Elecrow](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/Elecrow-specifications-CNC.png?raw=true)

## Through Hole parts on the Main PCB

### Reset Switch
For JLCPCB, you will need to solder on the through-hole parts for the PCB yourself. Elecrow will solder this on for you, so this isn't necessary for Elecrow. 

The reset switch (next to the Right Shift key) uses a 5mm tall 6x6mm SPST NO through-hole tact switch. This is widely available from several vendors - I have used Wealth Metal [TC-0103](https://www.taydaelectronics.com/tact-switch-6x6mm-5mm-through-hole-spst-no.html), but TE 1825910-6, E-switch TL1105AF100Q, Omron B3F-1022, C&K PTS645SK50-2 LFS and numerous other parts should work (though it has not been tested). 

This is soldered onto the top side of the PCB next toe the Right Shift key, and is accessible through the plate when the Right Shift keycap is removed.

### Encoder
The encoder used is [Alps EC11E18244A5](https://octopart.com/ec11e18244a5-alps-757484?r=sp), the same one used on the Satisfaction75. Other EC11-style encoders may work, but may need changes to various QMK parameters (ENCODER_RESOLUTION in config.h, and possibly reversing ENCODERS_PAD_A and ENCODERS_PAD_B) to work correctly.

[LCSC](https://lcsc.com/product-detail/Rotary-Encoders_ALPSALPINE-EC11E18244A5_C255515.html) is the cheapest source of these encoders if you are running a group buy. They are run by the same parent company as JLCPCB, though unfortunately they cannot combine shipping. 

### LED spacer
For the lock LEDs, you will need to 3D print a [small spacer](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Case/STL%20(3D%20print)). Units are in mm.  You can use an online printing service like [Shapeways](https://www.shapeways.com/) or [Craftcloud](https://craftcloud3d.com/), find a friend with a 3D printer, or purchase your own 3D printer to print this with. Your local library may have a 3D printer that may be available to use. The machine shop you use for the case may also offer 3D printing services. The spacer is designed to be printed using FDM printing, but other printing methods (SLA, SLS) probably also work. On my prototype I printed this out of PLA on a cheap $250 Ender 3 printer, with 0.2mm layer height.

Note that this spacer is different from the one on the 3D-printed version of Boston.

### Lock LEDs and resistors
Most standard 3mm LEDs should work, and are available in several different colors. 

If you are using the soldered PCB, you will need through-hole resistors for the lock LEDs. A 1KΩ resistor is a pretty safe resistor size for the LEDs, but depending on the LED forward voltage, current draw, and desired brightness, you may want to adjust this up or down. Standard 1/4W resistors are suitable.

Be aware that LEDs only work in one direction - the longer leg on LEDs is positive (+) - match this to the + markings on the PCB. 

These need to be soldered through the LED spacer discussed above. 

# Hardware

## Screws 

You will need the following screws for all variants. Part numbers for [McMaster-Carr](https://www.mcmaster.com) are provided, though you can easily find fasteners off other sources. McMaster also may not ship outside the United States.

| Description                                                           | Qty per board | McMaster-Carr P/N    | Note                                                                                                                                          | 
| --------------------------------------------------------------------- | ------------- | -------------------- |---------------------------------------------------------------------------------------------------------------------------------------------- |
| M3x0.5, 5mm long ISO 4762 socket head cap screw, stainless steel      | 12            | 91292A110 100-pack)  | Available from numerous other suppliers. Used to attach the plate to the case top, and to attach the daughterboard  to the case bottom.        |
| M3x0.5, 10mm long ISO 4762 socket head cap screw, stainless steel     | 4             | 91292A113 (100-pack) | Available from numerous other suppliers. Used for the front 4 case screws attaching the case top to the case bottom.                          |
| M3x0.5, 16mm long ISO 4762 socket head cap screw, stainless steel     | 4             | 91292A115 (100-pack) | Available from numerous other suppliers. Used for the front 4 case screws attaching the case top to the case bottom.                          |

## Additional screws for the hotswap variant 
If you are putting together a hotswap board, standoffs to hold the PCB and plate together are strongly recommended, though you might be fine just relying on the switches to hold the plate and PCB together. The only known regular source of these is from KBDfans, unless you get them custom made with a standoff manufacturer.

| Description                                            | Qty per board                                | Link or Part Number                                                                            | Notes                                               |
| -----------------------------------------------------  | -------------------------------------------- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| M2x0.4 3.5mm standoffs                                 | 10                                           | [KBDfans](https://kbdfans.com/products/kbdfans-m2-3-countersunk-flat-head-screw-kit) (13-pack) | KBDfans kit comes with other screws                 |  
| M2x0.4 3mm long DIN 7985 pan head screw                | 10 (countersunk plate) or 20 (regular plate) | McMaster-Carr 95836A103 (100-pack)                                                             | Above KBDfans kit comes with 13 of them             |
| M2x0.4 3mm long DIN 965 flat-head screw                | 10 (countersunk plate) or 0 (regular plate)  | McMaster-Carr 92010A784 (100-pack)                                                             | Above KBDfans kit comes with 13 of them             |

If you are countersinking your hotswap plate, you should only need to buy a single 13-pack of the KBDfans standoff kit as it comes with all the required screws. If you are not countersinking the plate, you will need to buy some additional M2x0.4 3mm long pan head screws.

## Rubber feet 
Boston uses standard circular, dome-shaped rubber feet. The smaller feet go in the front while the larger feet go in the back. These are available in a few colors.

| Description                         | Qty per board | McMaster-Carr P/N | Other Compatible parts                                                                                    | 
| ----------------------------------  | ------------- | ----------------- | --------------------------------------------------------------------------------------------------------- |
| 3/4" dia x 3/8" tall rubber feet    | 2             | 95495K73          | 3M SJ5017 (black, gray, or white), 3M SJ5317 (clear)                                                      |
| 3/8" dia x 5/32" tall rubber feet   | 2             | 95495K39          | 3M SJ5406 (white), 3M SJ5306 (clear), Essentra RBS-12BK (black), Essentra RBS-12 (clear)                  |


## Light Pipe
Boston uses a clear light pipe to transmit the RGBLED indicator light next to the knob. These use the following parts, which are available off numerous electronics distributors (Digi-key, Mouser, Newark, etc.). Links are provided to Octopart, which compiles all the websites you can buy the parts from (such as Digi-key, Mouser, Newark, and so on).

| Description                                                                             | Qty per board |  Notes     | 
| --------------------------------------------------------------------------------------- | ------------- | ---------- |
| [VCC LFC037CTP Light Pipe](https://octopart.com/lfc037ctp-vcc-54190594?r=sp)            | 1             |            |
| [VCC RTN125 Light Pipe Retainer](https://octopart.com/rtn125-vcc-54190599?r=sp)         | 1             |            |

The light pipe goes through the hole next to the knob. The retainer (which is a smaller rubber ring) is stuck on via the back to prevent the light pipe from falling off. If you so desire, you could also glue the light pipe in.

## Knobs
The Alps EC11E18244A5 rotary encoder used for the knob takes a 6mm knob with either a D-shaft or a set screw. This is a common size for guitars and audio equipment. 1/4" knobs can work but may be loose. 1/4" to 6mm adapters available from various sources if you want to use a 1/4" knob. 

The knob needs to be smaller than 23mm in diameter or it will hit the Esc key. 

I personally recommend Kilo International's OEDNI-75-X-7 lineup - these have very grippy knurling and can be easily rotated with one finger. They can be found on Digi-key, Newark, and other electronics parts vendors. If you use that knob, you want to 3D print a [small spacer](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/3D%20printed%20version/STLs/Kilo-OEDNI-75-knob-spacer.stl) to place into the shaft hole on the knob, as otherwise the knob can sit too low and bump into the case. 

| Kilo P/N     | Finish              |
| ------------ | ------------------- |
| OEDNI-75-1-7 | Silver, satin gloss |
| OEDNI-75-2-7 | Black, satin gloss  |
| OEDNI-75-3-7 | Silver, matte       |
| OEDNI-75-4-7 | Black, matte        |

## Daughterboard

The CNC version of Boston now uses the [S-series Unified Daughterboard](https://unified-daughterboard.github.io/#/db-spec-s), and is meant for use with PCB revisions V0.8 and newer. Various vendors sell this daughterboard, such as [Cannonkeys](https://cannonkeys.com/products/unified-s1-daughterboard-and-molex-cable) and [RNDKBD](https://rndkbd.com/products/unified-daughterboard?variant=42772031242474). You can also find manufacturing files for it on their website. 

Note that older PCBs (V0.6.1D and older) were meant to be used with the the older C3 Daughterboard, which as a different connector (a JST SM connector instead of a Molex PicoEZmate connector). You may need to find or make an adapter cable if you are using a V0.6.1D or older PCB with a case meant for the S1 Daughterboard. Cannonkeys includes a Molex to JST adapter cable with their Unified S1 daughterboard.

### Unified Daughterboard Cable

To connect the daughterboard and the main PCB, you will need a Molex PicoEZmate cable with [the correct pinout](https://unified-daughterboard.github.io/#/info-consumer?id=pinout) for Unified Daughterboards and that is at least 75mm long. The cables sold by keyboard vendors that come with their daughterboards should be the correct ones.

**Note that the PicoEZmate cables that Molex sells (part numbers 36920-04xx) do not have the correct pinout for use with Unified Daughterboards, and may damage your PCB**

If you need to make a cable, the Unified Daughterboard Project [suggests](https://unified-daughterboard.github.io/#/info-vendor?id=prototype-cables) buying pre-crimped wires and cable housings and making your own cables with the correct pinouts. You will need the following to make a cable; this will result in a long 300mm cable. Simply insert the pre-crimped wire ends into the connector housing until it clicks. 

| Molex P/N  | Qty needed | Description             | Link | 
| ---------- | ---------- | ----------------------- | ---- |
| 079758101  | 4          | Pre-crimped wire        | [Octopart](https://octopart.com/search?q=0797581010&currency=USD&specs=0) |
| 0781720004 | 2          | 4-pin connector housing | [Octopart](https://octopart.com/search?q=0781720004&currency=USD&specs=0) |

# Build instructions

Build instructions are currently [a work in progress](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Assembly-guide.md).
