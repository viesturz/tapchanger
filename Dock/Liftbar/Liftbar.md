# Liftbar dock

A motorized crossbar - compatible with Trident and V2.

For up to 3 toolheads (2 docked), a single motor is sufficient. For more, I recommend two motors.

![Details image](/images/liftbar%20-%20details.jpg)

## BOM
2020 Extrusion:
 -  279mm long for 250mm build
 -  329mm long for 300mm build
 -  379mm long for 350mm build

XY Idlers:
 - 2x 20mm 5mm shaft
 - 4x heatset inserts
 - 4x 8mm m3 screw
 - existing pulleys

Common:
- Omron d2f endstop switch
- ~4m 6mm GT2 belt (for 350 size)
- m3 bolts, heatset inserts, nuts
- 8x 8mm m4 bolts, t-nuts
- 8x F623RS flanged bearings (voron 0 spec)

Voron 2.4:
- 2x MGN9H rails, same length as your Z rails

Voron Trident: 
- 2x  MGN9H rails, 210mm+

For Single motor:
- nema 17 motor
- 36mm 5mm shaft
- 2x 625 bearing (voron 2 spec)
- 20T GT2 idler
- 20T GT2 pulley
- 2x 5x1mm washers

For dual motor:
- 2x nema 17 motor
- 2x 36mm 5mm shaft
- 4x 625 bearing (voron 2 spec)
- 2x 20T GT2 pulley
- 4x 5x1mm washers

## Assembly

* Assemble and replace the the XY idlers
* Install the Top idlers
* Install the linear rails, make sure they clear the XY idlers
* Install endstop
* Assemble and connect the gearboxes
* Assemble the gantry
* Install the belt
* Adjust the belt so that the gantry is ~horizontal
* Tension the belt
* Test the lifbar movement


Work in progress...

### Gearbox

The assembly sequence is a bit tricky.

* First mount the gears - small on the stepper axis and large on the pulley. Use the grubscrews in reverse to tighten the large gear. The small gear is just friction fit.
* Then install the m3 screws for the motor, do not mount the motor yet.
* Then press fit in the rear bearing, this needs quite some force, use a rod or hex wrench through the front hole to push it in.
* Install the Left side M4 screw, but *not* the right one.
* Install the big gear, this is a bit tricky:
  * Push in the shaft through the bearing from back, have it extend 1mm inside.
  * Place the washer on the shaft
  * Push the gear assembly down from above, it's a right fit, but should go in without much force.
  * Push the shaft all the way through
  * Add the second washer and bearing.
* Install the motor, test if the gears mesh smoothly
* Install the remaing 2 M4 screws.

Cross cut vs Trident leadscrew:

![Gearbox 0](/images/gearbox-cross-section.png)

Top down, test fitting the Motor, remove the motor to install the large gear.
![Gearbox 1](/images/gearbox-top.jpg)

Finished, ready to be mounted:

![Gearbox 1](/images/gearbox-coros.jpg)

### Docks
![Gearbox](/images/liftbar-dock.jpg)

## Configuration
See toolchanger-lifbar.cfg in Klipper folder.

