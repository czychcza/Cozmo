# Cozmo - Collecting Cubes and Self Docking on Charger
This program enables Cozmo to drive off its charger, collect its cubes by placing them near it and then climbing back onto its charger when it is done. Cozmo will directly try to climb back onto its charger if its battery is low and will ignore its cubes. No further help or markers are required. It is possible that Cozmo does not find a cube or its charger, so it will ask for help if needed. It will either say "Cube?" or "Charge?" dependending on what it is looking for. Just place the required object or Cozmo in a position where Cozmo can keep working and let it finish its job! If finding any cube takes too long, Cozmo will give up and go back to its charger. 

You can basically launch the whole procedure from any state. It means you can play a few games with the app and then switch to sdk mode and run the script. Just make sure the setting is not too different from what is described in the following section.

> **Note**: Use the updated version of the controller (v2) for stacked cubes!

## Optimal Setup When Starting
Cozmo should be on its charger when starting (but it will work otherwise too). The cubes can now be stacked (2 or 3!) or rolled and should be located somewhere in front of the charger. 

This video demonstrates how things work: 

https://youtu.be/xfAxPHdetH0

The video is sped up 4 times and there is therefore no sound. 

## Error Detection
Different strategies were implemented to detect if Cozmo is succeeding in its task or if a problem occured while running the program. This task is not easy and is prone to errors, that can occur at different levels. The error handling is based on timeouts and unexpected 
positions of the robot as well as action failures to determine if the current process has to be aborted/restarted or not. 

## Improvements (TODO)
- ~~Support already stacked or rolled cubes when cleaning up.~~ -> **Solved with *self_docking_v2***
- Stack cubes as a pyramid instead of current configuration. 
- ~~Detect if backup_onto_charger() has succeeded (not possible?).~~ -> **Solved**
- Speed up some processes. 
