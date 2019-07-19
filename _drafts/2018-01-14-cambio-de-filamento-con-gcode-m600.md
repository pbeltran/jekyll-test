--- layout: post title: Cambio de filamento con gcode M600 date:
'2018-01-14T12:41:00.000+01:00' author: Pablo Beltrán-Pellicer tags:
modified\_time: '2018-01-14T12:41:32.901+01:00' --- M600 E0.7 L0 X0 Y0
Z10  
  
E. retracción antes de mover al punto de cambio  
L retracción en el punto de cambio  
Z es incremental  
  
Ponerlo en el gcode a mano, justo cuando sube para empezar la capa nueva
(en al que queremos que cambie de color)  
;LAYER:8  
G0 X34.318 Y237.268 **Z1.9**  
M600 E0.7 L0 X0 Y0 Z10  
  
Para esto, en el marlin 1.1.8 hay que habilitar por compilación  
configuration\_Adv.h  
  
  
  
  
/\*\*  
 \* Advanced Pause  
 \* Experimental feature for filament change support and for parking the
nozzle when paused.  
 \* Adds the GCode M600 for initiating filament change.  
 \* If PARK\_HEAD\_ON\_PAUSE enabled, adds the GCode M125 to pause
printing and park the nozzle.  
 \*  
 \* Requires an LCD display.  
 \* Requires NOZZLE\_PARK\_FEATURE.  
 \* This feature is required for the default FILAMENT\_RUNOUT\_SCRIPT.  
 \*/  
\#define ADVANCED\_PAUSE\_FEATURE  
\#if ENABLED(ADVANCED\_PAUSE\_FEATURE)  
  \#define PAUSE\_PARK\_RETRACT\_FEEDRATE 40      // Initial retract
feedrate in mm/s  
  \#define PAUSE\_PARK\_RETRACT\_LENGTH 2         // Initial retract in
mm  
                                              // It is a short retract
used immediately after print interrupt before move to filament exchange
position  
  \#define FILAMENT\_CHANGE\_UNLOAD\_FEEDRATE 10  // Unload filament
feedrate in mm/s - filament unloading can be fast  
  \#define FILAMENT\_CHANGE\_UNLOAD\_LENGTH 0   // Unload filament
length from hotend in mm  
                                              // Longer length for
bowden printers to unload filament from whole bowden tube,  
                                              // shorter length for
printers without bowden to unload filament from extruder only,  
                                              // 0 to disable unloading
for manual unloading  
  \#define FILAMENT\_CHANGE\_LOAD\_FEEDRATE 6     // Load filament
feedrate in mm/s - filament loading into the bowden tube can be fast  
  \#define FILAMENT\_CHANGE\_LOAD\_LENGTH 0       // Load filament
length over hotend in mm  
                                              // Longer length for
bowden printers to fast load filament into whole bowden tube over the
hotend,  
                                              // Short or zero length
for printers without bowden where loading is not used  
  \#define ADVANCED\_PAUSE\_EXTRUDE\_FEEDRATE 3   // Extrude filament
feedrate in mm/s - must be slower than load feedrate  
  \#define ADVANCED\_PAUSE\_EXTRUDE\_LENGTH 0    // Extrude filament
length in mm after filament is loaded over the hotend,  
                                              // 0 to disable for manual
extrusion  
                                              // Filament can be
extruded repeatedly from the filament exchange menu to fill the
hotend,  
                                              // or until outcoming
filament color is not clear for filament color change  
  \#define PAUSE\_PARK\_NOZZLE\_TIMEOUT 240        // Turn off nozzle if
user doesn't change filament within this time limit in seconds  
  \#define FILAMENT\_CHANGE\_NUMBER\_OF\_ALERT\_BEEPS 2 // Number of
alert beeps before printer goes quiet  
  \#define PAUSE\_PARK\_NO\_STEPPER\_TIMEOUT       // Enable to have
stepper motors hold position during filament change  
                                              // even if it takes longer
than DEFAULT\_STEPPER\_DEACTIVE\_TIME.  
  //\#define PARK\_HEAD\_ON\_PAUSE                // Go to filament
change position on pause, return to print position on resume  
  //\#define HOME\_BEFORE\_FILAMENT\_CHANGE       // Ensure homing has
been completed prior to parking for filament change  
\#endif
