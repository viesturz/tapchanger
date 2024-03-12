# Tapchanger-Rods Xol-Toolhead (Experimental)
by [MikeYankeeOscarBeta](https://github.com/MikeYankeeOscarBeta/tapchanger) (VoronDesign Discord: #MikeyMike V2.5796, Voron Toolchangers Discord: MikeyMike - Github: [MikeYankeeOscarBeta](https://github.com/MikeYankeeOscarBeta/tapchanger))

### This is EXPERIMENTAL If you have issues, please post them on the tapchanger discord ASAP!

## Description
Tapchanger parts compatible with Xol-Toolhead (Experimental)

Based on Tapchanger StealthBurner Parts.

For crossbar (horizontal 2020 aluminium extrusion in front of printer) only!

Designed to be compatible with all Xol-Toolhead versions as of 2024-01-19.
(However only Revo Voron and Rapido 2 UHF has been tested)

#### NB! Tapchanger-Rods Xol-Toolhead dock has it's own docking tool-path. Remember to change to 'rods_xol' in your toolhead config.
In case you don't already have it from the tapchanger example config toolchanger.cfg , here's the docking tool-path:
```
params_rods_xol_path: [{'y':59, 'z':17.5},{'y':5, 'z':17.5},{'y':5, 'z':0.2},{'y':0.5, 'z':0.1},{'z':0, 'y':0, 'f':0.5},{'z':-5, 'y':0},{'z':-6, 'y':3},{'z':-8, 'y':7},{'z':-10, 'y':16}]
```

#### NB! only compatible with tapchanger rods version as of 2024-01-19

Example:
```
[tool T0]
tool_number: 0
extruder: extruder
params_type = 'rods_xol'
fan: multi_fan T0_partfan
gcode_x_offset: 0
gcode_y_offset: 0
gcode_z_offset: 0
```

## BOM:
| Part                        | Amount    | Description                                                      |
|-----------------------------|-----------|------------------------------------------------------------------|
| 6x3 magnets                 | 4         | N35 to N52 (N52 recommended)                                     |
| springsteel plate           | 1         | max 10mm wide, max 1mm thick, with M4 hole (I used blades from a [feeler gauge](https://www.biltema.no/en-no/car---mc/car-tools/engine-tools/spark-plug-tools/feeler-gauge-mminches-2000028588) ) |
| M4 screw                    | 1         | Maximum 6.3mm wide screw head                                    |
| M3x14mm BHCS or SHCS screw  | 2         | Any M3 screw will work                                           |
| M3 T-slot nut               | 2         | Any M3 2020 T-Slot Nut will work (recommend springnuts)    |


## Assembly
- Print
    - dock
    - maglock faceplate
    - tapchanger-rods xol-base
    - tapchanger-rods shuttle (if you haven't already)
- Push and glue in magnets
- Insert springsteel plate into slot in the Dock
- Cut and bend springsteel plate to fit your toolhead
- (optional) apply/mold silicone to the springsteel plate
- Fix the springsteel plate in place with the m4 screw
- Screw it onto the 2020 aluminium extrusion

