# Tapchanger

A nozzle Z probe + toolchanger for Voron 2.

## Features
* Off the shelf voron parts, except for bearings.
* Uses [Dragon Burner](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner) toolhead - can fit 6 hotends in 350 frame. [Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) and MiniStealthburner 
are an option but limited support. (Experimental version of the [Rapid Burner](https://github.com/chirpy2605/voron/tree/main/V0/Rapid_Burner) is in the works by @Marshalldog) (Experimental version for the [Xol-Toolhead](https://github.com/Armchair-Engineering/Xol-Toolhead) is in the works)
* Uses [OptoTap](https://www.google.com/search?q=optotap) probe sensor for nozzle Z probing.
* Same [rigidity](https://youtu.be/mGRXtK9F408) and probe accuracy as Tap.
* Same external printer dimensions, except for top hat.
* No servos, no wires on the shuttle, recommended to use with a Canbus toolhead board for less wires, but anything goes.

![Shuttle](/images/shuttle-pomo.jpg)
![Printer](/images/printer.jpg) 

# Build guide

I would recommend to get a single hotend working first:

* Check the [BOM](/Tapchanger/BOM.md).
* [Print](./Print%20Guide.md) the parts.
* [Assemble](/Tapchanger/Assembly.md) it.

Multiple tools setup:
* Install [Umbilical](/Umbilical/Umbilical.md).
* Install [Docks](/Dock/Dock.md)
* Add a [TopHat](/TopHat/TopHat.md)
* Configure [Klipper](/Klipper/README.md)
* Calibrate the offsets. I'm using [this](https://github.com/viesturz/NozzleAlign)

# Community

Improvement ideas - bugs, pull requests welcome. Find me on [Voron Toolchangers Discord](https://discord.gg/xmDWrYGwVJ), or file bugs here.

See Tapchanger [youtube channel](https://www.youtube.com/playlist?list=PLqU7kX5nUJDRDw5z0NLwJ22OkV6fbjnSW).

# Credits

- Basic models from [Voron Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) and [Voron 0](https://github.com/VoronDesign/Voron-0).
- Mini SB Orbiter cowling form [mozartlovescats](https://www.printables.com/model/366337-voron-02-orbiter-20-trianglelab-chc-mini-stealthbu).
- Mini SB LGX lite cowling form [MC](https://www.printables.com/model/395933-voron-02-mini-stealthburner-remix-for-lgx-light-ex/files).
- Dragon Burner from [chirpy2605](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner).
- HGX gears extruder derived from [nhchiu's ProtoXtruder](https://github.com/nhchiu/VoronMods/tree/main/Extruders/ProtoXtruder)

# How does this work?

It's essentially an oversized linear rail, that supports only ~4 mm of travel. The steel rail is replaced by bearings riding on rods.

In addition, it's a kinematic mount, meaning that it's self aligning and there is no play even if the parts are not aligned precisely.

![Preview](/images/explain1.png)
![Shuttle](/images/Animation.gif)

# Revision history:

## V4.2
Small tweaks across the board:
* Dragon toolhead mount plate 1mm thicker - no interferance with fans and 8mm tensioning screws do not stick out
* Fix shuttle mounting plate misalignment, thanks [vikwin](https://github.com/vikwin) for spotting
* Alternative version for the PFTE tube holder at the side
* Dock for RapidBurner
* Extras
  * Better ventilated EBB36 shield 
  * Improved strain relief for HGX + DragonBurner
  * More Stepper gear distance adjustability for HGX + DragonBurner.

Dragon burner toolhead exploded view: 

![Exploded](/images/toolhead_exploded.png)

## V4.1
HGX gears + Dragon + EBB36 [optimized toolhead](/Tapchanger/STL/Toolheads/DragonBurner/HGX%20Gears/):

* 17 mm shorter filament path
* 17 grams lighter than stock, only 2 screws
* Integrated harness strain relief
* Integrated EBB36 mount & shield
* Bambu & Revo adapters only for now
* There will be some supports to remove.

![HGX gears toolhead](/images/hgx_toolhead.jpg)

## V4.0
[Liftbar dock](/Dock/Liftbar/Liftbar.md)

![Liftbar](/images/liftbar.jpg)

Other minor DragonBurner changes:
* More clearance around the hookon slot.
* More room around the cooling fans, to avoid cracking the cowling when tightening the bottom screws.
* More sturdy dock.

## V3.2
Introduces support for the Experimental Rapid Burner Toolhead by @Marshalldog.

## V3.1
End of year update, lots of small printability, clearance, etc updates. 
This is a stable version.

* Migrated to Dragon V8 hotend.
* More clearance around the OptoTap sensor.
* Tuning of the tension screw angles to minimize the docking resistance.
* More clearance for big block hotends.
* Hook-on dock is now the recommended for DragonBurner.

## V3.0

Further improvements to DragonBurner toolhead and dock.
The screw head locking mechanism is back.
Configuration updated, with better dock pathing.

The Dragon Burner toolhead is now the default. Let me know if you would like to see backports.

## V2.9

Improved DragonBurner toolhead and dock, adding bottom mounting screws for better stability.
Needs the modified cowling now.

## V2.8

# Added Tophat and Ubmilical, it's now a Printer!

![Printer](/images/printer.jpg) 

## V2.5

* Added top mounted dock. see updated Dock folder.
* Slight tweaks square rods mounting plate for easier fit.

![Preview](/images/Dock-Top-Inside.jpg)

## V2.3 - Nozzle pads upgraded to springsteel ones, no more melting.

![Pads](/images/pad.jpg)

## V2.2 - Square rods version added.

Option to use square rods for better contact surface for the bearings.  Shares the shuttle and bearings with rods.

There are now total of 3 versions:
 - Plates - bigger bearings, more work to make the plates and assemble. The rolling surface is not great. Very rigid.
 - Rods - smaller bearings, easiest to assemble, but more flex.
 - Square rods - middle ground between plates and rods, the rigidity testing was done with this.

![Versions](/images/versions.jpg)

## V2.1 - Rods fixes.

Various fixes to refine the rods version. Ready for general testing.

## V2 - Rods version added.

A new experimental version using 3mm rods. See -rods files. Shuttle and mount plates changed, the rest is same.

![Preview](/images/rods-photo.jpg)

- Easier to assemble
- Tension adjustment screws easily available
- Runs smoother
- Using smaller 3x8x3 bearings - saves 5 grams and even more rigid.
- Even load distribution between the bearings by adjusting the angles to 26 and 64 degrees.

## V1.1 - Verified and cleaned up.

- Minor model tweaks for better fit and printability.


## V1 - This should work

- Redesigned and optimized - not compatible with V0
- Significanly more rigid
- Supports both Mini and full size Stealthburner

## V0 - Initial drop
 
 - It can print and looks reasonably rigid
 - ~10 Tool chnages so far
 - Initial dock, that looks okay for the job
