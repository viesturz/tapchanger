# Tapchanger

A nozzle Z probe + toolchanger for Voron 2.

![Preview](/images/rods-photo.jpg)

## Features
* Drop in compatibe with [Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) hotends.
* Supports Mini Stealthburner for more compact footprint - can fit 6 hotends in 350 frame.
* Adaptable from [Tap](https://github.com/VoronDesign/Voron-Tap) with mostly just printed parts.
* Same [rigidity](https://youtu.be/mGRXtK9F408) and probe accuracy as regular Tap.
* Mostly staying within the same external printer dimensions.
* No servos, no wires on the shuttle, recommended to use with a Canbus toolhead board for less wires, but anything goes.
* Uses the Tap sensor to verify successful dropoffs and pickups.

# Build guide

I would recommend to install a working single hotend printer first:

* Check the [BOM](/Tapchanger/BOM.md).
* [Print](./Print%20Guide.md) the parts.
* [Assemble](/Tapchanger/Assembly.md) it.

Multiple tools setup:

* You will need a umbilical system supporting multiple hotends, I am [using this](https://github.com/viesturz/Voron2Toolbox)
* Install [docks](/Dock/Dock.md).
* Configure [Klipper](./Klipper/README.md).
* Calibrate the offsets. I'm using [this](https://github.com/viesturz/NozzleAlign).

# Community

Improvement ideas - bugs, pull requests welcome. Find me on [Voron Toolchangers Discord](https://discord.gg/xmDWrYGwVJ), or file bugs here.

See Tapchanger [youtube channel](https://www.youtube.com/playlist?list=PLqU7kX5nUJDRDw5z0NLwJ22OkV6fbjnSW).

# Credits

- Basic models from [Voron Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) and [Voron 0](https://github.com/VoronDesign/Voron-0).
- Mini SB Orbiter cowling form [mozartlovescats](https://www.printables.com/model/366337-voron-02-orbiter-20-trianglelab-chc-mini-stealthbu).
- Mini SB LGX lite cowling form [MC](https://www.printables.com/model/395933-voron-02-mini-stealthburner-remix-for-lgx-light-ex/files).
- Dragon Burner from [chirpy2605](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner).

# How does this work?

It's essentially an oversized linear rail, that supports only ~4 mm of travel. The steel rail is replaced by bearing riding on rods.

In addition, it's a kinematic mount, meaning that it's self aligning and there is no play even if the parts are not aligned precisely.

![Preview](/images/explain1.png)
![Preview](/images/explain2.png)

# Revision history:

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
