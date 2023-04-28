# Setup & troubleshooting

## Mounting

Mount toolhead X rail. Mine is sitting 20cm below the top, which is pretty close to the ceiling. 

Mount the docks on the rail. Do not tighten, will adjust them later.
Adjust the back screws so that the pivot is not loose anymore.

Install the toolheads in the docks, except #0, that is mounted on the shuttle.

## Software config

See the Klipper folder for my config. This is still evolving so you will need to know how to manually install. If you don't the rest is probably too advanced anyway.

Before proceeding further, you should have all the toolheads configured, endstop offsets setup, toolhead offsets setup. Essentially able to print with each toolhead independantly.

Tool 0 will have offset 0 and the rest of the tools will have some offsets.

See [NozzleAlign](https://github.com/viesturz/NozzleAlign) on my offsets tool. Or anything else out there.

## Dock align

Each dock needs alignment coordinates in the tools.cfg. 
To get them, home with your tool0 - and remove it from the shuttle and place it back into the dock, leaving shuttle with the plug installed.

Now for each tool, position the shuttle so that the empty carriage is exactly below the tool rail.
With X and Y aligned and Z so that there is no gap and also no overlap with tool rail. 

The rail should be ever so sligthly over it's normal position, it tends to move back during mounting. A good guess is it covering the entire carriage opening. You will be able to adjust it later with the screws.

![Preview](/images/AlignmentPosition.jpg)

Write down the coordinates, this is your **park* position for the tool.


Test dock alignment by moving Z up ~20mm. The toolhead should slide into the shuttle without too much judder. At this point you want to tighthen the dock screws.

## Testing

** Be prepared to drop some balls** The first try will likely fail, make sure you can collect any balls flying off the printer. Closing printer doors is a good idea. Removing the flex plate is a good idea - makes the bed less bouncy.

Start with tool 0 mounted and issue the commands to mount next tool. The unmounting usually is fine, any alignment problems will pop up in the mounting process when the shuttle starts moving up. 

**Keep your hand on the toolhead** to help it along if it gets stuck. The most frequent problem is that the toolhead is too far back. Adjust the back screws to compensate.

