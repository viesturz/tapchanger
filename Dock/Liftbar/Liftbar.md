# Liftbar dock

A motorized crossbar - compatible with Trident and V2.

For up to 3 toolheads (2 docked), a single motor is sufficient. For more, I recommend two motors.

![Details image](/images/liftbar%20-%20details.jpg)

## BOM

XY Idlers:
 - 2x 20mm 5mm shaft
 - 4x heatset inserts
 - 4x 8mm m3 screw
 - existing pulleys

Common:
- Omron d2f endstop switch
- ~4m 6mm GT2 belt (for 350 size)
- m3 bolts, heatset inserts, t-nuts
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

For dual motor:
- 2x nema 17 motor
- 2x 36mm 5mm shaft
- 4x 625 bearing (voron 2 spec)
- 2x 20T GT2 pulley

## Assembly

Work in progress...

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

## Configuration
See toolchanger-lifbar.cfg in Klipper folder.

## Pics

![Gearbox](/images/liftbar-gearbox.jpg)
