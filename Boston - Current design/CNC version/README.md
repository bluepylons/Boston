# Boston CNC Version

![CNC version](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/DSC_0395_01.JPG?raw=true)

These are the files for the CNC version of Boston. The PCB is in the [PCB](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB) directory however. 

# Ordering Guide for making your own Boston (draft)

This is the ordering guide for the CNC version of Boston. 

**Order parts at your own risk. These files are provided as-is, and I am not responsible for any losses, harm, or damage incurred by following this guide, by ordering parts, by using the files provided, by using the resultant parts or assembled keyboard, or from any mistakes or errors in the files, ordering guide, or resultant parts** 

** This is for the older version that uses a C3 Unified Daughterboard. There is a newer design that uses  the new S1 daughterboard. This version is being prototyped by RNDKBD, and is awaiting confirmation that everything works. See README-S1-DB for the draft guide for that version.**

# What you will need:

### Parts:

# 
| Description                                        | Qty per board | Type                                                   | Variants |
| -------------------------------------------------- | ------------- | ------------------------------------------------------ | -------- |
| Case top                                           | 1             | Custom (CNC machined)                                  |          |
| Case bottom                                        | 1             | Custom (CNC machined)                                  | Yes (3)  |
| Plate                                              | 1             | Custom (PCB, laser cut, waterjet cut, or CNC machined) | Yes (3)  |
| PCB                                                | 1             | Custom (PCB)                                           | Yes (3+) |
| SK6812 Mini-E RGBLED (if using JLCPCB for the PCB) | 1             | Off-the-shelf                                          |          |
| Daughterboard holder PCB                           | 1             | Custom (PCB)                                           |
| LED spacer (for the lock LEDs - 3D printed)        | 1             | Custom (3D-printed)                                    |
| C3 Unified (or compatible) Daughterboard           | 1             | Off-the-shelf or custom                                |
| JST cable (>75mm long)                             | 1             | Off-the-shelf or custom                                |
| M2x0.4 5mm socket head cap screw                   | 4             | Off-the-shelf                                          |
| M3x0.5 5mm socket head cap screw                   | 14            | Off-the-shelf                                          |
| M3x0.5 10mm socket head cap screw                  | 4             | Off-the-shelf                                          |
| M3x0.5 16mm socket head cap screw                  | 4             | Off-the-shelf                                          |
| PEM KF2-M2-ET threaded insert                      | 4             | Off-the-shelf                                          |
| VCC LFC037CTP Light Pipe                           | 1             | Off-the-shelf                                          |
| VCC RTN125 Light Pipe Retainer                     | 1             | Off-the-shelf                                          |
| Alps EC11E18244A5 rotary encoder                   | 1             | Off-the-shelf                                          |
| 6x6mm tact switch, 5mm high                        | 1             | Off-the-shelf                                          |
| Knob suitable for 6mm D-shaft                      | 1             | Off-the-shelf                                          |
| 3mm LED for lock LEDs                              | 3             | Off-the-shelf                                          |
| 1KΩ through-hole resistor for lock LEDs            | 3             | Off-the-shelf                                          |
| 3/4" dia x 3/8" tall rubber dome feet              | 2             | Off-the-shelf                                          |               
| 3/8" dia x 5/32" tall rubber dome feet             | 2             | Off-the-shelf                                          |

| Description                                  | Qty per board                                 | 
| -------------------------------------------- | --------------------------------------------- | 
| MX-style switches                            | 119-127 (depending on layout)                 |  
| Stabilizers (PCB mount)                      | 2-8 2u, 0-1 6.25u or 7u (depending on layout) |

For a standard ANSI build (using the fixed layout plate) you need 121 switches, 6 2u stabilizers, and 1 6.25u stabilizer.

### Tools:
| Description                                                                                      |  Used for                                                           |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| 2.5mm hex key or bit ("Allen key")                                                               | All M3 screws                                                       |
| T6 Torx, #1 Philips, 1.3mm, or 1.5mm hex key or bit                                              | M2x5 screws (depends on what screws you buy) for the daughterboard  |
| Soldering iron and solder                                                                        | For soldering everything                                            |
| Flush cutters                                                                                    | For cutting legs off soldered LEDs and resistors                    |
| Large pliers, locking pliers ("Vise grips"), C-clamp, a vise, or oversized (~7mm dia) M2 washer  | For pressing the PEM threaded inserts into the daughterboard holder | 

# Case

Boston has a two piece case, consisting of the top and the bottom. It does not have a weight (though, if you have mechanical design and CAD skills, it should be pretty easy to add an internal weight to the design). 

There are two versions of the bottom case - the main version and the alternate version. The alternate version was actually what I designed first and prototyped, but it has very sharp edges on the bottom rear (near the rear bumpon) caused by the vertical faces, which are sharp enough to potentially cut into your skin. I changed the vertical faces to 45° beveled faces to eliminate those sharp edges. This version with the beveled 45° faces is the main version. Both versions have been prototyped.

![Case bottom - main versus alternate 2](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/Main-vs-alternate-bottom-2.png?raw=true)

![Case bottom - main versus alternate](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/Main-vs-alternate-bottom.png?raw=true)

## How to contact a machine shop to order the case 

To have the case made, you will need to contact a machine shop with a CNC machine. These are informally referred to as "manus" by the mechanical keyboard community.

[Dadesin](https://dadesin.en.alibaba.com/) is a popular high-quality Chinese one, though expensive and somewhat backed up right now. I used [SuNPe](https://sunpe.com/) (also in China) for my prototypes, though the quality was middling. A friend ran a small private group buy through [Gaojie](https://www.gj-prototype.com) and had good results. There are numerous other ones. You can also reach out to a local CNC machine shop.  Note that usually there is a tradeoff between cost and quality, with cheaper shops often being lower quality or sloppier with their machining (and more prone to mistakes, like forgetting to machine features or forgetting to tap holes). 

You will need to send a "Request for Quote" email to them with the following files:

* 3D files - you will need the .STEP files for the [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/STEP/Boston-top.stp), and either the [Main Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/STEP/Boston-bottom-C3-DB.stp) or the [Alternate Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/STEP/Boston-bottom-C3-DB-alternate%20(sharp%20edges).stp). 
* The mechanical drawings, which include the tapping instructions for the tapped (threaded) holes. [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-top.pdf), [Main Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-C3-DB.pdf), [Alternate Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-C3-DB-alternate.pdf)
* If you want a raw as-machined finish with visible tool marks, or want to anodize directly over the tool marks, you may want to include the milling instructions for more pleasing tool marks. [Top](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-top-AS-MACHINED-milling-instructions.png), [Main Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-AS-MACHINED-milling-instructions.png), [Alternate Bottom](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Case/Manufacturing%20drawings/Boston-bottom-alternate-AS-MACHINED-milling-instructions.png). If you are going for a bead-blasted finish, you do not need to include these. These are PNG images with picture illustrations, as many machine shops are overseas and do not speak English well. 
* In the body of the email, you want to specify the quantity, material, and the surface finish, as well as that you want these parts to be made by CNC machining. Materials and surface finish are discussed more in depth in the next sections.

You will also need to specify a material and a finish, a color for the finish (if you are anodizing, e-coating, painting, powder coating, or Cerakoting), as well as the quantity you want to order. Here is an example email reaching out to a manufacturer for a quote:

![Example email to manufacturer](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/example-email.PNG?raw=true)

The manufacturer will get back to you with a quote. If you wish to proceed with the quote, let them know that you wish to proceed, and they will send you instructions for payment (often via Paypal or bank transfer) and ask for a shipping address. 

With a Chinese shop, expect to pay $300-$600 for a single case machined out of aluminum (and about $60-$150 for shipping - note that some machine shops inflate their shipping costs). Expect higher for a US or EU shop. The price each usually goes down if you order more (even 3-5 units can lower the price significantly for each board over ordering just 1). 


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
* **Anodized** - almost all aluminum on consumer electronics (including custom keyboards) are anodized, usually over a fine bead-blasted finish. Anodizing generates a protective layer of aluminum oxide on the outside of the part, which is much harder than the underlying raw aluminum. This significantly improves the scratch resistance, and also protects the aluminum from corrosion. This layer of aluminum oxide can be clear (showing the underlying silver aluminum), or be dyed a wide range of different colors ([except for white](https://www.bluebuddhaboutique.com/blog/2011/09/no-white-anodized-aluminum/)). However, if you're going for a shiny as-machiend or polished finish, it does dull the aluminum a bit. There are a couple of types of anodizing, but Type II (cosmetic anodizing) is the most common, and what you probably want as it is inexpensive, and available in a wide variety of colors. Type III (Hard Anodizing) is occasionally done but uncommon in consumer electronics - Type III generates a much thicker layer of aluminum oxide than Type II, resulting in a dark gray, black, or bronze-brown color. This results in very good wear and scratch resistance, but costs more, can interfere with threaded holes, and is generally unnecessary for keyboards. Note that many machine shops outsource their anodizing, though some (e.g. Dadesin) anodize in-house. If you want to read up more on anodizing, [this](http://www.omwcorp.com/wp-content/uploads/2018/02/Understanding-and-Specifying-Anodizing-1.pdf) is a good document to go over (thanks to Croktopus for finding the document). 
* **Raw aluminum** - this means not using any coating whatsoever and leaving the bare metal exposed. Note that raw aluminum is easily scratched (and will most likely arrive from the machine shop with scratches from shipping and handling), so this is a fairly uncommon finish. It may also discolor from corrosion. However, paired with an as-machined or polished finish texture, it can be extremely shiny and reflective. All of my prototypes had a raw finish.   
* **E-coat**, **paint**, **powder coat**, or **Cerakote** - I am not familiar with ordering these finishes, but they show up on keyboards from time to time. 

**Note that any coating that adds appreciable (>0.03mm) thickness (such as Type III hard anodizing, powder coat, e-coat, paint, and Cerakote) will require the threaded holes and the RGBLED hole to be masked off. Standard (Type II) anodizing is usually thin enough that interference isn't an issue and masking holes should not be needed. 

![RGBLED hole that needs to be masked ](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/RGBLED-hole-masking.png?raw=true)

# Plate

Boston has a top mount plate. There are two versions of the plate - a fixed layout version that accommodates only the standard ANSI layout (with a non-stepped Caps Lock key), and a universal layout that should accommodate any of the layouts (split space, ISO, etc.) that the PCB supports. Both plates have been prototyped. 

The plate should be made out of 1.4-1.6mm material (which is the official Cherry spec for having the switches click in properly). 

**Fixed plate**:
![Fixed Layout Plate](https://github.com/bluepylons/Boston/raw/main/graphics/CNC/Fixed-plate.PNG)
![KLE of the fixed layout](https://github.com/bluepylons/Boston/raw/main/graphics/bostonKLE-fixed-layout-plate-support.PNG)


**Universal plate**:
![Universal Layout Plate](https://github.com/bluepylons/Boston/raw/main/graphics/CNC/Universal-plate.PNG)
![KLE of the universal layout](https://github.com/bluepylons/Boston/raw/main/graphics/bostonKLE.png)

The plate files are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Plate). 

If you are looking to have a plate laser cut or water jet (via a service such as [Sendcutsend](https://sendcutsend.com/) in the US, [Laserboost](https://www.laserboost.com/) in the EU, or elsewhere), you want to use the DXF files (.dxf). The units are in mm. You can upload it to their website. Many Chinese CNC machine shops have laser cutters, and can also make your plate in addition to your case if you send them the files. Make that sure the thickness of the material you choose is between 1.4mm and 1.6mm. 
* Virtually all metals (aluminum, brass, steel, titanium etc ). can be laser cut. 
* Some plastics (such as POM) laser cut well. 

If you are looking to have the plate CNC machined, you want to use the STEP (.stp) file. Again, the units are in mm. CNC machining is necessary for some materials like polycarbonate and carbon fiber. 

If you are looking to have the plate made out of FR4 or aluminum PCB material, you want to use the .zip Gerber files. This will have to be ordered as a PCB, and can be uploaded to any PCB supplier (JLCPCB, Elecrow, PCBway, AllPCB, etc.). Note that some PCB manufacturers (e.g. JLCPCB) charge an additional fee for plates due to the amount of milling required compared to a typical PCB. Choose 1.6mm for the PCB thickness. 

Note - on JLCPCB, make sure that "Specify A Location" for "Remove Order number" is selected so that the order number doesn't get printed somewhere you don't want. The Gerber files have the requisite "JLCJLCJLCJLC" text on them and placed in an unobstrusive location.

![Remove Order Number](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Remove-Order-Number.png?raw=true) 

 Also, "Paper between PCBs" under "Advanced Options" is strongly recommended- otherwise there's a decent risk of FR4 parts showing up scratched. 
 
![Paper Between PCBs](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Paper-between-PCBs.PNG?raw=true)

# Hardware

## Screws 

You will need the following screws. Part numbers for [McMaster-Carr](https://www.mcmaster.com) are provided, though you can easily find fasteners off other sources. McMaster also may not ship outside the United States.

| Description                                                           | Qty per board | McMaster-Carr P/N | Notes                                                                                                                                                                | 
| --------------------------------------------------------------------- | ------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| M3x0.5, 5mm long ISO 4762 socket head cap screw, stainless steel      | 14            | 91292A110         | Available from numerous other suppliers. Used to attach the plate to the case top, and to attach the daughterboard holder to the case bottom.                        |
| M3x0.5, 10mm long ISO 4762 socket head cap screw, stainless steel     | 4             | 91292A113         | Available from numerous other suppliers. Used for the front 4 case screws attaching the case top to the case bottom.                                                 |
| M3x0.5, 16mm long ISO 4762 socket head cap screw, stainless steel     | 4             | 91292A115         | Available from numerous other suppliers. Used for the front 4 case screws attaching the case top to the case bottom.                                                 |
| M2x0.4, 5mm long ISO 7045 button head screw, Torx T6, stainless steel | 4             | 90362A136         | Other M2 screw types (e.g. ISO 7380 button head) or driver types (e.g. Philips #2) would also work ok. Used to attach the daugterhboard to the daughterboard holder. |

## PEM nuts (threaded inserts)

The daughterboard holder uses PEM KF2-M2-ET tin-plated threaded inserts, which are pressed in and soldered onto the holes the daughterboard holder. You will need 4 of these. They're available off [Mouser](https://www.mouser.com/ProductDetail/PEM/KF2-M2-ET?qs=l4Gc20tDgJIwDb1wwu7XpQ%3D%3D), [McMaster-Carr](https://www.mcmaster.com/95117A477/), and elsewhere. 

You can press these in with large pliers (though this tends to scratch the other side of the PCB), with Vise-grip style locking pliers, a C-clamp, or with a vise. A hammer might work but you risk damaging the threads. You also may also be able to pull the insert into the hole using an M2 screw and an over-sized M2 washer (e.g. McMaster-Carr 91116A240), though this likely only works with a Torx M2 screw (as the hex and Philips head versions strip too easily). 

## Rubber feet 
Boston uses standard circular, dome-shaped rubber feet. These are available in several colors. 

| Description                         | Qty per board | McMaster-Carr P/N | Other Compatible parts                                                                                    | 
| ----------------------------------  | ------------- | ----------------- | --------------------------------------------------------------------------------------------------------- |
| 3/4" dia x 3/8" tall rubber feet    | 2             | 95495K73          | 3M SJ5017 (black, gray, or white), 3M SJ5317 (clear)                                                      |
| 3/8" dia x 5/32" tall rubber feet   | 2             | 95495K39          | 3M SJ5406 (white), 3M SJ5306 (clear), Essentra RBS-12BK (black), Essentra RBS-12 (clear)                  |


## Light Pipe
Boston uses a clear light pipe to transmit the RGBLED indicator light next to the knob. These use the following parts, which are available off numerous electronics distributors (Digi-key, Mouser, Newark, etc.). 

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

# PCBs

# Main PCB
The CNC version of Boston uses the [V0.6.1D PCB](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.6.1D) (D for Daughterboard) - this **not the same PCB as the 3D printed version** due to the daughterboard, though they use the same firmware as the matrix is identical.

For the PCB - you can order an assembled PCB (minus through-hole parts such as the encoder, RGBLED, and reset switch) from a PCB fab such as JLCPCB or Elecrow.

## Ordering on JLCPCB
[JLCPCB](https://jlcpcb.com/) is cheap and fast, but doesn't have the best cosmetic finish, and their SMT assembly is limited to parts [they stock](https://jlcpcb.com/parts) (though they recently announced "Global Parts Sourcing"). In the community they tend to only be used for prototypes.

To order a PCB from JLCPCB, you will need the Gerber files (which defines the bare PCB), the SMT bill of materials (BOM file, which is a list of parts that are to be soldered to the PCB), and the component placement file (CPL, which defines where those parts go). The files for PCB revision V0.6.1D are available [here](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.6.1D/Manufacturing%20files). 

**Note that JLCPCB does not offer the SK6812 Mini-E RGBLED used for LED702 for Economic PCB Assembly**, and you will have to solder order this elsewhere and solder it on manually yourself. Adafruit sells it as the [Neopixel Reverse mount](https://www.adafruit.com/product/4960), and it is also available off [Digi-key](https://www.digikey.com/en/products/detail/adafruit-industries-llc/4960/14302512) (but oddly enough, not Mouser). Line up the notch on the LED with the notch marking on the PCB when you are soldering it.

First, you want to go to [JLCPCB](https://jlcpcb.com/), and press "Order Now".

![Step 1](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/1-JLCPCB-home.png?raw=true)

Next, you want to upload the Gerber file for the PCB. You may need to manually input the PCB dimensions (393.5x147mm). 

![Step 2](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/2-add-gerbers.png?raw=true)

Here, you want to change the specifications to the following. PCB Color and Surface Finish needs to be a combo supported for Economic PCB Assembly in 1.6mm thickness - currently (April 30, 2023), this would be Green in any finish, Black in any finish except ENIG, and Blue, Red, and White with HASL-Leaded. 

![Step 3](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/3-JLCPCB-options-CNC.png?raw=true)

Next, you want to scroll down and turn on PCB Assembly. Make sure the following options are selected:

![Step 4](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/4-SMT.png?raw=true)

Press Confirm. Next, you want to upload the BOM and CPL files. 

![Step 5](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/5-BOM-CPL.PNG?raw=true)

Make sure that all the components are selected. Any part that says "Inventory shortage" will not be installed, and you will have to substitute a compatible part, wait for the part to come back in stock, or if you're up to the challenge of SMT soldering, order the part separately and solder it on yourself. 

![Step 6](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/6-BOM-CNC.PNG?raw=true)

The next page is a confirmation page. Note that the parts placement preview may be inaccurate (JLCPCB engineers will look over this and make any parts orientation corrections, so don't worry too much about this). 

![Step 7](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/7-checkout-CNC.PNG?raw=true)

As the microcontroller is frequently out of stock due to the chip shortage, line number 16 (for designator U701) can be changed for different compatible MCUs (see the "Compatible MCUs" section below for a list of MCUs that will work). At different times some microcontroller variants may be cheaper than the others (for example, on August 29, 2022, the STM32F072CBT6 is $4.50 and the STM32F072CBU6 is $9.52, whereas during other times -CBU6 has been significantly cheaper than the -CBT6). You will need to change the Comment field for that line to the name of the microcontroller you want to use, and change the Footprint and LCSC Part Number as appropriate.

### Compatible MCUs 

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

### Other Interchangeable Parts On The PCB 

This is here for reference in case some parts are out of stock.

**U702 - BOM Line #17**
This is a SOT-223 linear regulator to drop the 5V down to 3.3V. Since ceramic capacitors are used the output, and some linear regulators are unstable with ceramic capacitors as their ESR is too low, the linear regulator needs to be explicitly compatible with low-ESR output capacitors.

| Part                                              | JLCPCB (LCSC) part number |
| ----------------------------------------------------- | ------------------------- |
| Diodes Inc AZ1117IH-3.3TRG1 (default)                 | C108495                   |
| TI TLV1117LV33DCYR                                    | C15578                    |

**U705 - BOM Line #18**
This is a 74LVC1T45 level shifter in an SOT23-6 (SOT26) package. 

| Part                                 | JLCPCB (LCSC) part number |
| ------------------------------------ | ------------------------- | 
| TI SN74LVC1T45DBVR        (Default)  | C7843                     |
| TI SN74LVC1T45DBVT                   | C116653                   |
| Diodes Inc 74LVC1T45W6-7             | C168856                   |

## Ordering on Elecrow

Elecrow is a full-service PCB assembly shop, and one of the go-tos in the community for custom keyboard PCBs for the actual group buy sales. They can install any part (not just ones they stock) and generally have better quality surface finish, but is much slower (typically 3-4 week turn around time), and costs more (especially in small quantities). 

To order from Elecrow, you will need to email service@elecrow.com with the [Gerber](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/PCB/V0.6.1D/Manufacturing%20files/Gerbers-V06-1D.zip) and [SMT](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.6.1D/Manufacturing%20files/Elecrow%20SMT%20files) files and request a quote. **Note - the Elecrow files have not been tested**

On the [SMT file](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/PCB/V0.6.1D/Manufacturing%20files/Elecrow%20SMT%20files), you will need to edit the first tab to specify your quantity, color, and surface finish. Elecrow's available colors and surface finishes are posted on their [PCB ordering page](https://www.elecrow.com/pcb-manufacturing.html)

![Elecrow](https://github.com/bluepylons/Boston/blob/main/graphics/CNC%20ordering%20guide/Elecrow-specifications-CNC.png?raw=true)

Elecrow will install the RGBLED (LED702), unlike JLCPCB, so you do not need to buy it separately and solder it on yourself. 

## Through Hole parts on the Main PCB
For both Elecrow and JLCPCB, you will need to solder on the through-hole parts for the PCB yourself. 

### Reset Switch

The reset switch (next to the Right Shift key) uses a 5mm tall 6x6mm SPST NO through-hole tact switch. This is widely available from several vendors - I have used Wealth Metal [TC-0103](https://www.taydaelectronics.com/tact-switch-6x6mm-5mm-through-hole-spst-no.html), but TE 1825910-6, E-switch TL1105AF100Q, Omron B3F-1022, C&K PTS645SK50-2 LFS and numerous other parts should work (though it has not been tested). 

This is soldered onto the top side of the PCB, and is accessible through the plate when the Right Shift keycap is removed.

### Encoder
The encoder used is [Alps EC11E18244A5](https://octopart.com/ec11e18244a5-alps-757484?r=sp), the same one used on the Satisfaction75. Other EC11-style encoders may work, but may need changes to various QMK parameters (ENCODER_RESOLUTION in config.h, and possibly reversing ENCODERS_PAD_A and ENCODERS_PAD_B) to work correctly.

[LCSC](https://lcsc.com/product-detail/Rotary-Encoders_ALPSALPINE-EC11E18244A5_C255515.html) is the cheapest source of these encoders if you are running a group buy. They are run by the same parent company as JLCPCB, though unfortunately they cannot combine shipping. 

### LED spacer
For the lock LEDs, you will need to 3D print a [small spacer](https://github.com/bluepylons/Boston/tree/main/Boston%20-%20Current%20design/CNC%20version/Case/STL%20(3D%20print)). Units are in mm.  You can use an online printing service like [Shapeways](https://www.shapeways.com/) or [Craftcloud](https://craftcloud3d.com/), find a friend with a 3D printer, or purchase your own 3D printer to print this with. Your local library may have a 3D printer that may be available to use. The machine shop you use for the case may also offer 3D printing services. The spacer is designed to be printed using FDM printing, but other printing methods (SLA, SLS) probably also work. On my prototype I printed this out of PLA on a cheap $250 Ender 3 printer, with 0.2mm layer height.

### Lock LEDs and resistors
Most standard 3mm LEDs should work, and are available in several different colors. A 1KΩ resistor is a pretty safe resistor size for the LEDs, but depending on the LED forward voltage, current draw, and desired brightness, you may want to adjust this up or down. Standard 1/4W resistors are suitable.

Be aware that LEDs only work in one direction - the longer leg on LEDs is positive (+) - match this to the + markings on the PCB. 

These need to be soldered through the LED spacer discussed above. 

## Daughterboard
Like many other custom keyboards that use a daughterboard, the CNC version of Boston uses the [C3 Unified Daughterboard](https://github.com/ai03-2725/Unified-Daughterboard), . Files for that are available on their GitHub repo. Note the C3 PCB is too small for JLCPCB's SMT assembly service, unless you panelize it. 

Several vendors also sell the C3 Daughterboard (e.g. [Cannonkeys](https://cannonkeys.com/products/unified-daughterboard-and-jst-cable), [Charue Designs](https://charue-design.com/products/unified-daughterboard-and-jst-cable), [Senseless Clay](https://senselessclay.com/products/usb-type-c-daughterboard), and others). 

### JST Cable 
To connect the daughterboard and the main PCB, you will need a 4-pin JST-SH capable that matches the [specifications laid out on ai03's C3 daughterboard GitHub repo](https://github.com/ai03-2725/Unified-Daughterboard/tree/master/Design%20Resources/C3). Sparkfun's Qwiic and Adafruit's Stemm QT cables (which are available in several lengths) match the specifications and work just fine. A minimum length of 75mm is recommended - both [Adafruit](https://www.adafruit.com/product/4210) and [Sparkfun](https://www.sparkfun.com/products/14427) offer 100mm long cables (and are also sold on Digi-key and Mouser). Some sellers of C3 Daughterboards (such as Cannonkeys) also include a cable with their daughterboards. 

## Daughterboard holder

![Daughterboard Holder](https://github.com/bluepylons/Boston/blob/main/graphics/CNC/daughterboard-holder.JPG?raw=true)

To mount the daughterboard low on the board, the daughterboard is screwed onto a daughterboard holder that then mounts onto the case bottom. This allows the daughterboard to be held upside down, which allows for it to be mounted much lower. 

The daughterboard holder is a bare PCB that can be ordered from JLCPCB, Elecrow, PCBway, or another PCB manufacturing service using the Gerber files available [here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Daughterboard%20holder/Daughterboard-holder-gerbers.zip).  It does not need any SMT assembly. 

The daughterboard holder is 1.6mm thick. 

Note - on JLCPCB, make sure that "Specify A Location" for "Remove Order number" is selected so that the order number doesn't get printed somewhere you don't want. The Gerber files have the requisite "JLCJLCJLCJLC" text on them and placed in an unobstrusive location.

![Remove Order Number](https://github.com/bluepylons/Boston/blob/main/graphics/Ordering%20guide/Remove-Order-Number.png?raw=true) 

Four PEM KF2-M2-ET threaded inserts are pressed in and soldered into the holes on the daughterboard holder. Four M2x5 screws are then used to screw the daughterboard in, and the assembly is screwed into the case bottom using M3x5 screws. 

# Build instructions

[See here](https://github.com/bluepylons/Boston/blob/main/Boston%20-%20Current%20design/CNC%20version/Assembly-guide.md). The text is complete, though some photographes still need to be taken.
