# smi-opensesame

How to set up the SMI RED in P103i to use opensesame as the stimulus program running on a separate PC.

## What does this repo do?

Change a baked-in default in OpenSesame's SMI library from "expects a single IP address" to "expects 2 IP addresses". 

The source code lives at:
    esdalmaijer/PyGaze/blob/master/pygaze/\_eyetracker/libsmi.py

The path to installed libsmi.py is "site-packages/pygaze/\_eyetracker/libsmi.py"

Where are my changes?
  - 2-PC setup:         see # connect to iViewX      c. line 210 (also in the \_\_init__ args c. line 127)
  - Write an .idf file: see # output file properties c. line 167

## What settings are needed in the \*.osexp?

Psychopy backend (?)

## Display settings for OpenSesame use

The laptop needs to be set up as follows: right click on the desktop and choose "Screen resolution". From "screen resolution" choose "display on 1 only" - this means that the laptop is constrained to show things only on its own inbuilt screen.

The stimulus PC needs to be set up as follows: right click on the desktop and choose "Screen resolution". From "screen resolution" choose "display on 1 only" - this constrains the stimulus PC to show things only on its screen 1 which is the SMI  screen to which the stimulus PC must be attached using the (blue) VGA connection.

## Display settings for Experiment Center use

The laptop needs to be set to "extend this display" and "use 2 as primary". That puts the taskbar on the SMI screen (screen 2). In Experiment Center, use the toggle at the bottom of the interface to select display 2. That puts the calibration stimuli and the experiment stimuli on the SMI screen (screen 2). 

(An alternative, that would be more compatible with the required setup for opensesame, would be to "use 1 as primary" putting the taskbar on the laptop screen, and set Experiment Center to use display 2, putting all stimuli on the SMI display.)
