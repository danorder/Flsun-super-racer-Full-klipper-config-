SUPER REACER PROFILES WITH PRINTER EMULATION. for super slicer stable version Version 2.3.57

Disclaimer these are still just generic profiles tuning flow / retraction is a requirement every machine and, filament brand is different etc. 

once installed if coming from another slicer assume flow is a bit off. slicers calculate things differently in some cases. 

step 1 calibrate flow first with the usual 2 wall cube method 
step 2 calibrate retraction z hop should be off as this will generate strings on its own throwing off results. 
Most profiles have generic temps they may or may not need adjustment. The sr should be min 220 pla 60-70 bed or less depending on glass pei or build stickers. reminder 
klipper generally runs faster and, more constant temps are often higher. and most roles of pla are sold for ender3s 190 will usually just lead to overtime damage or not
work at all. eg 500 ender acc vs sr 3700 acc default or stock marlin 2600. note some brands will extrude at really low temps their is always a exception to the rule etc. 
Id suggest with any brand preheat the nozzle and, feed in some filament by hand to see if its unreasonably hard to extrude. eg you can't push it at all imagine whats is
happening to the extruder for hours. 

For installation i would suggest first making a snapshot / back up of the original profiles if already using super slicer. in some cases it is possible for somthing to go
wrong and corrupt profiles etc. always make backups for things you care about. 

Note profiles are custom / ported however if you add x machine through the wizard it will still have its own original settings and, be incompatible with the sr. although this 
would still work if one owns that particular machine as well like normal. 

Note on the macros they both set firmware limits for emulated profiles. On labeled sr profiles they will also be able to override speed at anytime during print. or before 
personally i will hit cartesian macro from tft or fluidd/ mainsail if i need to go some where thus slowing the print down to "safer" speeds unattended. 
Firmware retraction is required since this allows for different machines / profiles to be used without using their default retraction values" under filament custom gcode
different retract lenghs / speeds can be set for each filament if desired. 

Other general notes.
Most profiles are simply ported and, will be using the safest defaults for X machine. Typically min layer time seconds will be set to 20 undre the filament cooling tab
this will will most small prints on the slow side. lowering this will increase general speed. eg the stock sr uses a default of 4 seconds. 
on some profiles the travel acceleration may be another point of interest. some are set 1500 acc however this can be increased in most cases without breaking the profile. 
notably some filaments are known to have issues with more then 1500 travel and, may lead to tearing or delayed extrusion on travel / restart moves. 

