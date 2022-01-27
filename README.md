########################IN BETA AT THE MOMENT ################ JAN 26 2022 
THINGS UPDATED . CALIBRATE BUTTON /MACRO REMOVED TILT. (TILT IS A SEPERATE BUTTOM) IF MESH IS DESIRED JUST CHANGE THE COMMAND TO bed_mesh_calibrate or use g29 and, enable mesh in config. note tilt and mesh cannot be on at the same time. 
acceleraton values 
note on cura enable acc/jerk controls for default marlin like values. do not use, compensate walls , outerwall wipe its generally slow and unessary. MAKE SURE RELATIVE EXTRUSION
IS ENABLED IN PROFILE. not doing so will lead to coordinate issues. 
things that need to be setup /adjusted, filemnt run out sensor / pause macro 

adding additional ez setup / convience macros , pid calibrate button , set babysteps as zoffset for fine tuning will require delta calibrate again to apply values) 
beta ideamaker profiles. 


ATTENTION INITIAL SETUP PROCESS. PROBE_CALIBRATE/ZOFFSET FIRST. RUN DELTA CALIBRATE TO APPLY ANY ZOFFSET RELATED CHANGES IT WONT APPLY OTHERWISE. 2ND RUN DELTA CALIBRATE
ZOFFSET HAS NOW BEEN APPLIED AND EFFECTOR TRAMMED. DO NOT USE BED MESH / TILT UNLESS THIERS A REAL DIMENSIONAL PROBLEM WITH THE BED. This may lead to a false calibration. PEI HOWEVER MAY NEED IT. delta calibrate should get things "trammed" Note ensure bed clips are not warping the bed in some way certain temps may expand the bed to much (the clips cant move with it loosening then lightly tightening may resolve this for x bed temp) eg 100c-80-70c. Note klipper generally runs faster pla in particular is typically 225-245 
depending on desired speed this is relativly standard for this speed range. if things aren't sticking some beds / pla brands need 70c. 
NOT ALL PROBES WORK AS WELL AS OTHERS QC ETC if none of the above works. use paper method found on the klipper website. set values to delta kinemtaic defaults for probe height /
delacalibrate height. otherwise the nozzle will be excessivly high making probe_calibrate a pain. 
ZOFFSET/PROBE CALIBRATE IS EASIEST WITH KLIPPER SCREEN IT AUTOMATES THINGS A BIT MORE VS TERMINAL COMMANDS. PAPER METHOD YOU CAN OPEN USE THE UP AND DOWN JUST DONT HIT START 
THEN HIT ACCEPT AND SAVE_CONFIG. IF YOU HIT START IT MAY LOWER THE NOZZLE INTO THE BED OR IT MAY JUST RESET (I HAVENT TESTED THIS) 

# Flsun-super-racer-Full-klipper-config-NANO SKR 1.3 VERSION COMING SOON (yes this is for stock printers with out mods ) 
  This readme is currently under construction more info will be added over time.

Complete Kllipper based on klipper docs and flsun marlin. routinely updated with the same functionality and higher spec 
 This config is currently compatible with cura after minor klipper specific changes to start gcode under printer settings version 4.12. The 4.10 cura should work by default.
in cura the start gcode is setup to use relative extrusion. this must be enabled in the profile otherwise random movments can and will occure. make sure to change both stock   profiles. This config is setup like a tutorial island the settings must be enabled for it to work. This is to attempt to lessen the learning curve if you can compile marlin. and to ensure that individual machines are setup to their indivial values. every machine is a bit different due to qc and, assembly. 
 
 OTHER HARDWARE / REOMMENDED BUT OPTIONAL.
  HDMI Capacitive Lcd for KLIPPER SCREEN. This grants nearly full acess to a clean ui with most klipper settings / standard printer controls in a modern touch ui  
it should be noted the stock. lcd more then likely will not be added to Klipper by developers anytimee soon (months/years) theres many other more common screens 
stil waiting for support. This is mostly a manufacture issue / semi propriatary software and tfts running their own firmware. if you don't want to use a pc / cell phone don't    wait up. Notes on klipper screen this removes most of the need for fluidd / mainsail other then uploads. IT makes certain features easier such as setting up zoffset / baby stepping. It also has visual bed mesh , wifi selection , and, what you'd expect control wise from a graphical marlin screen in terms of settings / control. 
 
USEFUL LINKS AND RESOURCES / INFO TO BE BECOME FAMILIAR WITH
https://klipperscreen.readthedocs.io/en/latest/ FULL TOUCH UI FOR CAPACITIVE HDMI TFT OR RESSISTIVE. TFT I USED / STL https://www.thingiverse.com/thing:2798667
https://www.klipper3d.org/Installation.html The offical manual 
https://www.klipper3d.org/Rotation_Distance.html?h=extr Extruder calibration docs 
Manual input shaper https://www.klipper3d.org/Resonance_Compensation.html?h=input
https://docs.fluidd.xyz Fluid web ui a premade raspberry pi image with everything require is also here. 
https://docs.mainsail.xyz/update/klipper Main sail web ui (more current / active updates at this time. ) either ui / image is entirely a matter of preference. 
https://github.com/th33xitus/KIAUH Kiauh installer script useful to have to update or some times fix certain problems via reinstall 
https://www.balena.io/etcher/ belena etcher a tool used to either clone or install images to sdcard for the raspberry pi. this can be very useful for multiple printers. the sdcard can simply be cloned and, config changed 
https://winscp.net/eng/index.php a gui ssh client to edit files on the raspberry pi. 

 WHATS NEW 
Bed mesh works on this copy provided the probe is with in range / tilt option) bed mesh recommended for diagnostic purposes eg finding bad areas on the bed / calibration issues. 
delta shouldn't need this at all for glass. 0.06 -.1mm is fine. inital layer height should be a bit obove these by default. eg 0.2-0.3 
Correct values for stealth chop. note their are only 2 options hybrid will loose torque and cause layer skips and excessive noise as seen on other configs. 
Pressure advance (klippers equivalent to linear advance ) 
Thermal runaway is enabled by default in klipper. the configs for it must be added to make changes. default internal values should be fine. if its triggering more then likely Wrong pid or somthing is loose on the hotend or bed. it will only go of if it has reason to. 
1/128 stepping 
High torque / tuned tmc drivers 
Fluidd or Mainsail web ui 

WHAT NOT TO DO 
 Once everything is installed, due to printers offsets being different it is suggested  to raise the z offset in fluidd or mainsail 1 or 2mm to then lower it incrimentally on a test print.This is a good safety measure  to ensure the measured value were correct. It is also recommended to test the probe via probing into a hand to ensure its working with the other hand on the power if it doesnt stop for whatever reason. 
 Do not enable listed features in slicer that are known to be incompatible. those can be found on the klipper slicer docs on the website listed. 
 Do not assume square corner velocity is the same as jerk its not the same. klipper runs on different motion software similar to junction deviation usually 5-7 on the sr is good and high acceelration. there are exceptions to this eg low accelleration  higher square corner for smaller prints with lower acceleration. 

GENERAL DISCLAIMER use at your own risk I am not responsible for any resulting damages or miss use. All setting are setup to be in spec to the orginal marlin 1.3 firmware or close due to firmware differences. The speed is however setup to be faster and resolution is 3x higher then  marlin on the steppers. In general it is a bit more quiet.

If you like the work and, want to buy me a coffee https://www.paypal.com/paypalme/danorder 


