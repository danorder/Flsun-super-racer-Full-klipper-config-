# NOTES ON THE SKR 1.3 VARIENT. CHANGE THE TMC PINS TO THE KLIPPER REFERENCE CONFIG. ADDITIONALLY REMOVE THE MCU THERMAL SENSOR THE SKR DOESN'T SUPPORT THIS. 
# at some point a 2nd config will be made for the 1.3. 
#https://github.com/fluidd-core/FluiddPI GO HERE FOR WEB UI. YOU CAN USE OCTOPRINT IT HOWEVER IS NOT RECOMMEND BUT DOES WORK IT MAY INDUCE LAG ISSUES. 
#https://www.klipper3d.org/FAQ.html
#https://www.klipper3d.org/Slicers.html
#https://www.klipper3d.org/Installation.html VIEW ME FIRST TO GENERATE THE CURRENT KLIPPER FIRMWARE.BIN MAKE SURE TO RENAME IT. INSTALL WINSCP IF YOU NEED TO TRANSFER FILE TO PC VIA SSH 
#https://winscp.net/eng/docs/introduction REMOTE FILE VIEWER / DOWNLOADER helpful for periodic required firmare flahes after certain klipper updates. !! ALWAYS READ THE POSTED CHANGES BEFORE UPDATING!!
#https://www.klipper3d.org/G-Codes.html?h=firmware+retract#firmware-retraction 
#https://www.klipper3d.org/G-Codes.html COMPATIBLE DEFAULT GCODES. 

#KLIPPER COMMANDS: ENDSTOP_PHASE_CALIBRATE stepper=stepper_(LETTER) REMOVE BRACKETS. PROBE_CALIBRATE DELTA_CALIBRATE (DO THIS AT PRINTING TEMP) SET FANS 40 PERCENT THEN PID_CALIBRATE HEATER=extruder TARGET=245
# SAVE_CONFG , PID_CALIBRATE HEATER=heater_bed TARGET=80, SAVE_CONFIG. your done. adjust slicer / retract accordingly. 
# OR RUN THE CALIBRATE MACRO MAKE SURE THE PROBE IS ON FOR ALL BED RELATED CALIBRATION INCLUDING Z OFFSET. NOTE FOR THE PAPER METHOD USE THE DEFAULTS IN KLIIPPER DOCS FOR #DELTA CALIBRATE / KINEMATICS REGARDING IT. 
# If the calibrate macro is used. run probe_calibrate first (aka zoffset) then run the macro. calibrate may need to be run 2x.
# Initially its safer to set the zoffset in fluidd/mainsaill a bit higher eg .2mmm or so then lower to 0 while printing a flat square or circle. This is a good safety measure to avoid a slight collison. 
