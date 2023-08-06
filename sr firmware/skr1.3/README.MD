THIS IS A `BETA` UNTESTED PORT INTENDED FOR USE WITH "STOCK OUT OF BOX  SPEEDERPADS"  

IF USING VANILLA ENABLE M205 
Not required but highely suggest to at a minimum have VANILLA KLIPPER SCREEN. stock does not have Probe_calibrate commands. it uses babystep leaving it unable to set the probes offset. this will require the use of conole
commands. Found on the Klipper website. (testz)  Note vanilla klippper screen probe_calibrate is found under the zcalibrate button the option is named "probe"  further note if using kliper screen probe_calibrate or delta_calibrate keep in mind it will not leave the nozzle high like the `calibrate macro`  always reset babystep in mainsail if using probe_calibrate. 


`skr1.3` config instructions/notes

0. inital calibration order of events

1. first put on the probe then run Probe_calibrate from vanilla Klipperscreen. this is found under zcalibrate button and named "probe" 
printer will lower and probe once complete pull off probe then , using klipper screens buttons jog down using the paper test to get the appropriate gap. 
note: kliper accounts for hot nozzles and, applies a small correction do not run it hot. also make sure it is clean a fleck of filament will add an amount of height. 
IMPORTANT FIRST HIT ACCEPT ON KLIPPER SCREEN.  It should then ask to save_config. don't save config without hitting accept first. otherwise values will not be saved. 

2. Put `probe` back on. `preheat bed` to whatever material temp your using. hit the `calibrate macro`. printer will run a automated calibration.  endstop calibrate then reboot. then delta_calibrate then reboot, then Finnally it will run bed_mesh. do not remove the probe until its finsihed.  Ensure probe is well seated / wires wont entangle etc.

3. `calibrate macro` will leave the nozzle  `babbystepped` 0.6 mmm high to avoid scrapes / human error on prob_calibrate. Simply gradually lower this for the first print to set the final height. afterwards for good measure 
save_config. double check the `babystep`  values load on boot this will take several seconds

3. printer is mostly ready pid bed and pid hotend should also be run for final calibration. 
