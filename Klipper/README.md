# This is temporary document

Use for a thermistor of SliceEngineering only.

## Step 1
### Calibrating the BLTouch Probe
* PROBE_CALIBRATE
* TESTZ Z=-xx

Keep lowering until the paper meets resistance when you try to move it
* ACCEPT
* SAVE_CONFIG

## Step 2
### Perform Mesh Bed Leveling
* BED_MESH_CALIBRATE
* BED_MESH_PROFILE SAVE=name
* SAVE_CONFIG

## Step 3
### Auto Z Adjust
* Z_TILT_ADJUST

## Step 5
### PID Tuning for Extruder
Turn the fan on at 40% of speed
* M106 S40
* PID_CALIBRATE HEATER=extruder TARGET=240
* SAVE_CONFIG

### PID Tuning for Heated Bed
* PID_CALIBRATE HEATER=heater_bed TARGET=60
* SAVE_CONFIG

