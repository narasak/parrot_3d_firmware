# This is temporary document

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
### PID Tuning
* PID_CALIBRATE HEATER=extruder TARGET=240

