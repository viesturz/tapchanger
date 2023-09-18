# Tapchanger

A nozzle Z probe + toolchanger for Voron 2.

![Preview](/Images/hotend-shuttle.jpg)

## Features
* Drop in compatibe with [Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) hotends.
* Adaptable from [Tap](https://github.com/VoronDesign/Voron-Tap) with mostly just printed parts.
* Same rigidity and probe accuracy as regular Tap.
* Mostly staying within the same external printer dimensions.
* No servos, no wires on the shuttle, recommended to use with a Canbus toolhead board for less wires, but anything goes.
* Uses the Tap sensor to verify successful dropoffs and pickups.

# How does this work?

It's essentially an oversized linear rail, that supports only ~4 mm of travel. The steel rail is replaced by bearing riding on rods.

In addition it's a kinematic mount, meaning that it's self aligning and there is no play even if the parts are not aligned precisely.

![Preview](/Images/explain1.png)
![Preview](/Images/explain2.png)

# Build guide

Check the [BOM](./Bom.md).

[Print](./Print%20Guide.md) the parts.

Assembly instructions coming...

Configure [Klipper](./klipper/README.md).

# Community

Improvement ideas - bugs, pull requests welcome. Find me on [Voron Toolchangers Discord](https://discord.gg/xmDWrYGwVJ), or file bugs here.

See Tapchanger [youtube channel](https://www.youtube.com/playlist?list=PLqU7kX5nUJDRDw5z0NLwJ22OkV6fbjnSW).

# Credits

- Basic models from [Voron Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) and [Voron 0](https://github.com/VoronDesign/Voron-0).
- Mini SB Orbiter cowling form [mozartlovescats](https://www.printables.com/model/366337-voron-02-orbiter-20-trianglelab-chc-mini-stealthbu).
- Mini SB LGX lite cowling form [MC](https://www.printables.com/model/395933-voron-02-mini-stealthburner-remix-for-lgx-light-ex/files).

# Revision history:

## V2.1 - Rods fixes.

Various fixes to refine the rods version. Ready for general testing.

## V2 - Rods version added.

A new experimental version using 3mm rods. See -rods files. Shuttle and mount plates changed, the rest is same.

![Preview](/Images/rods-photo.jpg)

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
