UPDDATE: THIS REPO IS DEPECIATTING IN FAVOR OF A MERGE / V3 ALL IN ONE FIRMWARE. FOR SR / V400 "OFFICIAL KLIPPER and, OFFICIAL SUPPORTED DEVICES. Currently btt pad7, bttpi , Raspberry PI " or, devices with "Official projects installed" 



# Flsun-super-racer klipper based on oem spec / functionality  (STOCK ) 
#Default. QQS And Q5 BETA ADDED CREDITS - Johnny-f Fletman converting things over. 
Support group / updates link https://www.facebook.com/groups/1502404840209556


Routinely updated with the similar functioanlity to oem marlin. spec upgraded in areas 
 This config is currently compatible with cura after minor klipper specific changes to start gcode under printer settings version 4.12. The 4.10 cura should work by 
in cura the start gcode is setup to use relative extrusion. this must be enabled in the profile otherwise random movments can and will occure. make sure to change both stock   profiles. This config is setup like a tutorial island the settings must be enabled for it to work. This is to attempt to lessen the learning curve if you can compile marlin. and to ensure that individual machines are setup to their indivial values. every machine is a bit different due to qc and, assembly. 


OTHER HARDWARE / REOMMENDED BUT OPTIONAL.
  HDMI Capacitive Lcd for KLIPPER SCREEN. This grants nearly full acess to a clean ui with most klipper settings / standard printer controls in a modern touch ui  
it should be noted the stock. lcd more then likely will not be added to Klipper by developers anytimee soon (months/years) theres many other more common screens 
stil waiting for support. This is mostly a manufacture issue / semi propriatary software and tfts running their own firmware. if you don't want to use a pc / cell phone don't    wait up. Notes on klipper screen this removes most of the need for fluidd / mainsail other then uploads. IT makes certain features easier such as setting up zoffset / baby stepping. It also has visual bed mesh , wifi selection , and, what you'd expect control wise from a graphical marlin screen in terms of settings / control. 
 
WHAT NOT TO DO 
 Once everything is installed, due to printers offsets being different it is suggested  to raise the z offset in fluidd or mainsail 1 or 2mm to then lower it incrimentally on a test print.This is a good safety measure  to ensure the measured value were correct. It is also recommended to test the probe via probing into a hand to ensure its working with the other hand on the power if it doesnt stop for whatever reason. 
 Do not enable listed features in slicer that are known to be incompatible. those can be found on the klipper slicer docs on the website listed. 
 Do not assume square corner velocity is the same as jerk its not the same. klipper runs on different motion software similar to junction deviation usually 5-7 on the sr is good and high acceelration. there are exceptions to this eg low accelleration  higher square corner for smaller prints with lower acceleration.
use a bed mesh to solve underlying problems. A mesh should be used to deal with poor topography eg pitted / damaged glass or , uneven pei. delta calibrate should be able to tram the effector to the bed. while a mesh may resolve some issues however at a cost. The nozzle will remain crooked and fail to iron lines cleenly leading to cosmetic issues. 
mesh will simply raise the z to compensate for height / depth variance without correcting the nozzle /effector angle. 

GENERAL DISCLAIMER use at your own risk I am not responsible for any resulting damages or miss use. All setting are setup to be in spec to the orginal marlin 1.3 firmware or close due to firmware differences. The speed is however setup to be faster and resolution is 3x higher then  marlin on the steppers. In general it is a bit more quiet.

If you like the work and, want to buy me a coffee https://www.paypal.com/paypalme/danorder 


