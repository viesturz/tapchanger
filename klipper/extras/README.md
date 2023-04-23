# Extra Klipper extensions

## Tool probe endstop

Allows to create a virtual Z endstop from a multitude of Tap probes.

### GCode commands
* All the normal *[probe]* commands.
* **SET_ACTIVE_TOOL_PROBE T=99** - manually change the active endstop to the specified tool
* **DETECT_ACTIVE_TOOL_PROBE** - query all endstops look for single not-triggered and set that as the active one.

### Config
```
# Define tool probe endstop will be used
[tool_probe_endstop]

# For each tool, define same as normal probe
[tool_probe t0]
pin: !e0:gpio25
tool: 0
z_offset: -1.35


# Use virutal endstop for your Z axis
[stepper_z]
...
endstop_pin: probe:z_virtual_endstop
...

```

## Tool alignment calibration

TODO