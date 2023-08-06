STARTING 2022 12-12 KLIPPER UPDATES REQUIRE THE UPDATED START GCODE OTHERWISE THIS WILL LEAD TO G3 /G2 ERRORS 

Printer.cfg is now divided between 2 files. both are required to run and go in the usual spot. This was done to "declutter" by moving most things not requiring adjustments.  Must have printer.cfg and, emulator_other_features.cfg. Do not copy and, paste this can lead to formating errors for wheatever Reason. 



**Initial Calibration Order of Events**

1. First, put on the probe, then run `Probe_calibrate` from the vanilla Klipper screen. This is found under the zcalibrate button and named "probe." The printer will lower and probe. Once complete, pull off the probe. Then, using Klipper screen buttons, jog down using the paper test to get the appropriate gap. Note: Klipper accounts for hot nozzles and applies a small correction. Do not run it hot. Also, make sure it is clean; a fleck of filament will add an amount of height. **IMPORTANT**: FIRST HIT ACCEPT ON KLIPPER SCREEN. It should then ask to save_config. Don't save config without hitting accept first; otherwise, values will not be saved.

2. Put the probe back on. Preheat the bed to whatever material temp you're using. Hit the calibrate macro. The printer will run an automated calibration: `endstop calibrate` then reboot, then `delta_calibrate` then reboot, and finally, it will run `bed_mesh`. Do not remove the probe until it's finished. Ensure the probe is well-seated, and wires won't entangle, etc.

3. The calibrate macro will leave the nozzle babystepped 0.6 mm high to avoid scrapes/human error on `probe_calibrate`. Simply gradually lower this for the first print to set the final height. Afterward, for good measure, `save_config`. Double-check the babystep values load on boot; this will take several seconds.

4. The printer is mostly ready. `PID` bed and `PID` hotend should also be run for final calibration.
