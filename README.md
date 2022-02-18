GENERAL NOTICE 
note on cura enable acc/jerk controls for default marlin like values. do not use, compensate walls , outerwall wipe its generally slow and unessary. MAKE SURE RELATIVE EXTRUSION
IS ENABLED IN PROFILE. not doing so will lead to coordinate issues. 
things that need to be setup /adjusted, filemnt run out sensor / pause macro 

REMAINING FEATURES TO DO pause, filament runout , skr 1.3 config , 

CALIBRATION PROCEDURE 1 probe_calibrate. remove probe test z down cold nozzle use paper accept save_config. 2 calibrate macro. 3 run pid macros. 
note on mesh it should only be used to deal with damged beds or diagnostics. using it to compensate for off delta calibrates does work but, the con is the nozzle will be lifting but remain angled = poor finish / possibly stringing releated issues. 

# Flsun-super-racer klipper based on oem spec / functionality  (yes this is for stock printers with out mods ) 

Routinely updated with the similar functioanlity to oem marlin. spec upgraded in areas 
 This config is currently compatible with cura after minor klipper specific changes to start gcode under printer settings version 4.12. The 4.10 cura should work by default.
in cura the start gcode is setup to use relative extrusion. this must be enabled in the profile otherwise random movments can and will occure. make sure to change both stock   profiles. This config is setup like a tutorial island the settings must be enabled for it to work. This is to attempt to lessen the learning curve if you can compile marlin. and to ensure that individual machines are setup to their indivial values. every machine is a bit different due to qc and, assembly. 
 
 OTHER HARDWARE / REOMMENDED BUT OPTIONAL.
  HDMI Capacitive Lcd for KLIPPER SCREEN. This grants nearly full acess to a clean ui with most klipper settings / standard printer controls in a modern touch ui  
it should be noted the stock. lcd more then likely will not be added to Klipper by developers anytimee soon (months/years) theres many other more common screens 
stil waiting for support. This is mostly a manufacture issue / semi propriatary software and tfts running their own firmware. if you don't want to use a pc / cell phone don't    wait up. Notes on klipper screen this removes most of the need for fluidd / mainsail other then uploads. IT makes certain features easier such as setting up zoffset / baby stepping. It also has visual bed mesh , wifi selection , and, what you'd expect control wise from a graphical marlin screen in terms of settings / control. 
 


WHAT NOT TO DO 
 Once everything is installed, due to printers offsets being different it is suggested  to raise the z offset in fluidd or mainsail 1 or 2mm to then lower it incrimentally on a test print.This is a good safety measure  to ensure the measured value were correct. It is also recommended to test the probe via probing into a hand to ensure its working with the other hand on the power if it doesnt stop for whatever reason. 
 Do not enable listed features in slicer that are known to be incompatible. those can be found on the klipper slicer docs on the website listed. 
 Do not assume square corner velocity is the same as jerk its not the same. klipper runs on different motion software similar to junction deviation usually 5-7 on the sr is good and high acceelration. there are exceptions to this eg low accelleration  higher square corner for smaller prints with lower acceleration. 

GENERAL DISCLAIMER use at your own risk I am not responsible for any resulting damages or miss use. All setting are setup to be in spec to the orginal marlin 1.3 firmware or close due to firmware differences. The speed is however setup to be faster and resolution is 3x higher then  marlin on the steppers. In general it is a bit more quiet.

If you like the work and, want to buy me a coffee https://www.paypal.com/paypalme/danorder 


