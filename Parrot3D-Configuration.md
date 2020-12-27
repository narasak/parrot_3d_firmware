# Parrot 3D

## Change from [Parrot3D (Develop Main Branch)](https://github.com/narasak/parrot_3d_firmware/tree/develop/main)

### Configuration.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| **============================== <br/> Temperature <br/> ==============================** |||
| #define TEMP_SENSOR_0 67 | #define TEMP_SENSOR_0 5 | 5: is for E3D Thermistor 67: is for SE HT Thermistor |
| #define TEMP_SENSOR_PROBE 1 | #define TEMP_SENSOR_PROBE 0 | Disable probe temp sensor |
| #define DEFAULT_Kp  28.53 | #define DEFAULT_Kp  16.50 | Default Hot End PID (Kp Value) |
| #define DEFAULT_Ki   2.99 | #define DEFAULT_Ki   1.16 | Default Hot End PID (Ki Value) |
| #define DEFAULT_Kd 168.08 | #define DEFAULT_Kd  58.80 | Default Hot End PID (Kd Value) |
| **============================== <br/> Driver <br/> ==============================** |||
| #define DEFAULT_AXIS_STEPS_PER_UNIT { 200, 200, 400, 830 } | #define DEFAULT_AXIS_STEPS_PER_UNIT { 100, 100, 400, 415 } | Default Axis Steps Per Unit For 1.8 and BMG |
| **============================== <br/> BL Touch <br/> ==============================** |||
| #define FIX_MOUNTED_PROBE | //#define FIX_MOUNTED_PROBE | Disable fix mounted probe |
| //#define BLTOUCH | #define BLTOUCH | The BLTouch probe uses a Hall effect sensor and emulates a servo. |
| #define NOZZLE_TO_PROBE_OFFSET { 23, 5, 0 } | #define NOZZLE_TO_PROBE_OFFSET { -24.3, -34.1, -1.95 } | Nozzle-to-Probe offsets |
| #define Z_CLEARANCE_DEPLOY_PROBE    0 | #define Z_CLEARANCE_DEPLOY_PROBE    5 | Z Clearance for Deploy/Stow |
| #define Z_CLEARANCE_MULTI_PROBE     1 | #define Z_CLEARANCE_MULTI_PROBE     2 | Z Clearance between multiple probes |

### Configuration_adv.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| **============================== <br/> Driver <br/> ==============================** |||
| #define X_CURRENT       800 | #define X_CURRENT       500 | Set motor current |
| #define Y_CURRENT       850 | #define Y_CURRENT       600 | Set motor current |
| #define E0_CURRENT      800 | #define E0_CURRENT      550 | Set motor current |
| **============================== <br/> BL Touch <br/> ==============================** |||
| //#define BLTOUCH_DELAY 500 | #define BLTOUCH_DELAY 200 | The probe needs time to recognize the command. |
| //#define BLTOUCH_SET_5V_MODE | #define BLTOUCH_SET_5V_MODE | BLTouch V3.0 or 3.1: Set default mode to 5V mode at Marlin startup. |
| //#define BLTOUCH_HS_MODE | #define BLTOUCH_HS_MODE | Use "HIGH SPEED" mode for probing. |

