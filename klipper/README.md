# Klipper setup

## Overview

TapChanger is primarily a hardware project. The config here is just the setup I'm using.
Which should be a reasonable starting point.

Long term I'm looking to upstream the changes in klipper and Klipper_ToolChanger where reasonable.

## Installing

- I have a custom github repo with toolchanger extensions. Switch the Klipper install to: https://github.com/viesturz/klipper/tree/toolchanger
- use the config as a template for your own config

Optional:

- autodetect active tool copy the toolklippy/tool_probe* files to  ${KLIPPER_PATH}/klippy/
- nozzle [alignment probe](https://github.com/viesturz/NozzleAlign)

## Z offsets
 
 The Tap probe does not offer a true Z home. Instead it relies on build surface as Z=0. On the other hand, the tool changing needs reasonably repeatable Z position.

 So this is a bit more complicated than yor typical setup:

  - Printer Z=0 - is tool independant, all toolchange moves happen in this space.
  - Tool probe trigger Z offset - distance betwen nozzle touching the bed and probe triggering - is tool specific, but nozzle independant. Specified in tool_probe.z_offset.
  - Tool Z offset - is tool and nozzle specific. Specified in tool.offset.

When **homing** the Z=0 is determined from probe probe tigger location - probe trigger offset - tool Z offset.
For Tool 0 that is the same as normal Tap homing. For other tools the extra tool offset is substracted.
Klipper unfortinately assumes that the Z=0 is a fixed distance from the endstop trigger location, so there are some tricks in homing.cfg to adjust this in post.

When **printing**, the Gcode offset is = tool Z offset.

When **changing tools**, Gcode offset = 0.

