# Klipper setup

## Overview

TapChanger is primarily a hardware project. The config here is just the setup I'm using.
Which should be a reasonable starting point.

I'm working to upstream the changes in klipper where reasonable.

## Installing

- Install [toolchanger extension](https://github.com/viesturz/klipper-toolchanger/).
- Use the [config examples](https://github.com/viesturz/klipper-toolchanger/tree/main/examples) to setup your Klipper config.

## Prusa slicer config

I'm using the following custom Gcode.

**Start Gcode** - all must be a single line
```
PRINT_START  TOOL_TEMP={first_layer_temperature[initial_tool]} {if is_extruder_used[0]}T0_TEMP={first_layer_temperature[0]}{endif} {if is_extruder_used[1]}T1_TEMP={first_layer_temperature[1]}{endif} {if is_extruder_used[2]}T2_TEMP={first_layer_temperature[2]}{endif} {if is_extruder_used[3]}T3_TEMP={first_layer_temperature[3]}{endif} {if is_extruder_used[4]}T4_TEMP={first_layer_temperature[4]}{endif} {if is_extruder_used[5]}T5_TEMP={first_layer_temperature[5]}{endif}  BED_TEMP=[first_layer_bed_temperature] TOOL=[initial_tool]
```

**Tool change Gcode**
```
M104 S{temperature[next_extruder]} T[next_extruder] ; set new tool temperature so it can start heating while changing
```

## Optional - Z homing with any toolhead.

The included config has a rather elaborate setup that allows Z homing with any toolhaed. This avoids the need to ensure that toolhead 0 is mounted before homing.

The tool changing needs reasonably repeatable gantry Z position, since Tap homes to nozzle possition, it will be different for each toolhead.

So this is a bit more complicated than yor typical setup:

  - Printer Z=0 - is tool independant, all toolchange moves happen in this space.
  - Tool probe trigger Z offset - distance betwen nozzle touching the bed and probe triggering - is tool specific, but nozzle independant. Specified in tool_probe.z_offset.
  - Tool Z offset - is tool and nozzle specific. Specified in tool.offset.

When **homing** the Z=0 is determined from probe tigger location - probe trigger offset - tool Z offset.
For Tool 0 that is the same as normal Tap homing. For other tools the extra tool offset is substracted.
Klipper unfortinately assumes that the Z=0 is a fixed distance from the endstop trigger location, so there are some tricks in homing.cfg to adjust this in post.

When **printing**, the Gcode offset is = tool Z offset.

When **changing tools**, Gcode offset = 0.
