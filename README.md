# TapChanger for Voron
A toolchanger system For [Voron 2](https://github.com/VoronDesign/Voron-2) based on the [Tap](https://github.com/VoronDesign/Voron-Tap) bed probe.

This is independant effort, not developed by the Voron team.

## Features
* Drop in compatibe with [Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) hotends.
* Adaptable from [Tap](https://github.com/VoronDesign/Voron-Tap) with mostly just printed parts.
* Same rigidity and probe accuracy as regular Tap.
* No servos, no wires on the shuttle, recommended to use with a Canbus toolhead board for less wires, but anything goes.
* Uses the Tap sensor to verify successful dropoffs and pickups.


## Design

Toolheads are docked in an extra extrusion at the front of the printer. The toolhead is rested on a dock and as the shuttle moves down toolhead slides off the Tap rail.

Cudos for inspiration to [WP-Daksh](https://github.com/ankurv2k6/wp-daksh-toolchanger) and the Voron India discord.

The Tap probe is almost working as a toolchanger out of the box, the main issue is that a naked linear carriage is prone to loosing balls.
This is solved by pushing in a supporting plastic plug while the shuttle is traveling between the tools.

In a normal Tap setup, the plug would need to come from above the rail and no room for it there. So the MGN9 rail is flipped around with the carriage on the shuttle side and the rail is on the toolhead side, allowing the plug to sit below the Tap rail in the dock.

## BOM

Shuttle:
 * 8x M3 5mm slotted pan head screws for the [shuttle assembly](assembly.md), look [like this](https://accu-components.com/us/pan-head-screws/7119-SFP-M3-5-A4).
 * 2x M3x6 steel countersunk screws, same ones as in Tap kit.
 * 2x 5x2mm round magnets for the carriage plug. Or mod for 6x3.
 
Toolhead:
 * A Tap kit + a Stealthburner toolhead of your choice
 * 2x 5x2 round magnet
 * 2x M3x12 screws with thread dremeled off for the last 3 mm

Dock:
 * 2x m3x8 steel screws - need to be magnetic
 * 2x m3x6 countersunk steel scews - need to be magnetic
 * 2x m3x16, 1x m3x12, 1x m3x10, 2x heatset insert
 * Some 1mm silicone sheet, can reuse cooking gloves or bakery cups

# Work site here

This is **work in progress**, nothing has been tested yet.

Done:
* The main shuttle + Stealthburner mount
* The dock works

WIP: 
* Test, test, test


![Preview](/images/side.png)
