# Toolchanger for Voron 2
A toolchanger system For [Voron 2](https://github.com/VoronDesign/Voron-2) based on the [Tap](https://github.com/VoronDesign/Voron-Tap) bed probe.

This is independant effort, not affiliated with the Voron team. Use at your own risk.

## Features
* Drop in compatibe with [Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner) hotends.
* Adaptable from [Tap](https://github.com/VoronDesign/Voron-Tap) with mostly just printed parts.
* Same rigidity and probe accuracy as regular Tap.
* No servos, no wires on the shuttle, recommended to use with a Canbus toolhead board for less wires, but anything goes.
* Uses the Tap sensor to verify successful dropoffs and pickups.

See [Youtube](https://www.youtube.com/playlist?list=PLqU7kX5nUJDRDw5z0NLwJ22OkV6fbjnSW) for some action.

## Design

Toolheads are docked in an extra extrusion at the front of the printer. The toolhead is rested on a dock and as the shuttle moves down toolhead slides off the Tap rail.

Cudos for inspiration to [WP-Daksh](https://github.com/ankurv2k6/wp-daksh-toolchanger) and the Voron India discord.

The Tap probe is almost working as a toolchanger out of the box, the main issue is that a naked linear carriage is prone to loosing balls.
This is solved by pushing in a supporting TPU plug while the shuttle is traveling between the tools.

In a normal Tap setup, the plug would need to come from above the rail and no room for it there. So the MGN9 rail is flipped around - the carriage is on the shuttle side and the rail is on the toolhead side, allowing the plug to sit below the Tap rail in the dock.

# Work site here

This is **work in progress**, nothing has been tested yet. 

Done:
* The main shuttle + Stealthburner mount
* The dock works
* Put on a printer
* Make the distribution board

WIP: 
* Iron out klipper setup.
* Make install script.
* Test, fix, repeat

## Changelog

V0.2: Tools are changin.
 * 20+ toolchanges and countin.
 * Completely new dock, the rest slightly reworked.
 * Initial klipper setup. Tool auto-detection. Tap Z probe works across tools.


V0.1: It fits together.
 * Basic hardware assembly and operation works.
 * Real printing - still to be tested.

![Preview](/images/side.png)

![Preview](/images/distribution_box.png)
