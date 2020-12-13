# Parrot 3D

## Change from Marlin

### Configuration.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| //#define SERIAL_PORT_2 -1 | #define SERIAL_PORT_2 -1 | Enabled Serial Port |
| #define MOTHERBOARD BOARD_RAMPS_14_EFB | #define MOTHERBOARD BOARD_BTT_SKR_V1_4_TURBO | Define Board For SKR 1.4 : #define MOTHERBOARD BOARD_BTT_SKR_V1_4 |
| //#define CUSTOM_MACHINE_NAME "3D Printer | #define CUSTOM_MACHINE_NAME "Parrot 3D" | Change Printer Name |
| #define TEMP_SENSOR_0 1 | #define TEMP_SENSOR_0 5 | 5: is for E3D Thermistor 67: is for SE HT Thermistor |
| #define TEMP_SENSOR_BED 0 | #define TEMP_SENSOR_BED 1 | Enabled Heat Bed Temp Sensor |
| #define TEMP_SENSOR_PROBE 0 | #define TEMP_SENSOR_PROBE 1 | Enable P.I.N.D.A. 2 Temp Sensor |
| #define TEMP_RESIDENCY_TIME 10 | #define TEMP_RESIDENCY_TIME 2 | |
| #define TEMP_WINDOW 1 | #define TEMP_WINDOW 3 | |
| #define TEMP_HYSTERESIS 3 | #define TEMP_HYSTERESIS 2 | |
| #define TEMP_BED_RESIDENCY_TIME 10 | #define TEMP_BED_RESIDENCY_TIME 2 | |
| #define TEMP_BED_WINDOW 1 | #define TEMP_BED_WINDOW 3 | |
| #define TEMP_BED_HYSTERESIS 3 | #define TEMP_BED_HYSTERESIS 2 | |
| #define HEATER_0_MAXTEMP 275 | #define HEATER_0_MAXTEMP 310 | Maximum Hot End Temp up to 310 C |
| #define BED_MAXTEMP 150 | #define BED_MAXTEMP 135 | Maximum Heated Bed Temp up to 135 C |
| #define DEFAULT_Kp  22.20 | #define DEFAULT_Kp  16.50 | Default Hot End PID (Kp Value) |
| #define DEFAULT_Ki   1.08 | #define DEFAULT_Ki   1.16 | Default Hot End PID (Ki Value) |
| #define DEFAULT_Kd 114.00 | #define DEFAULT_Kd  58.80 | Default Hot End PID (Kd Value) |
| //#define PIDTEMPBED | #define PIDTEMPBED | Enabled PID for Heated Bed |
| #define DEFAULT_bedKp 10.00 | #define DEFAULT_bedKp 28.13 | Default Heated Bed PID (Kp Value) |
| #define DEFAULT_bedKi .023 | #define DEFAULT_bedKi 2.09 | Default Heated Bed PID (Ki Value) |
| #define DEFAULT_bedKd 305.4 | #define DEFAULT_bedKd 483.07 | Default Heated Bed PID (Kd Value) |
| #define EXTRUDE_MINTEMP 170 | #define EXTRUDE_MINTEMP 180 | Prevent extrusion if the temperature is below 180 C |
| #define Z_MIN_ENDSTOP_INVERTING false | #define Z_MIN_ENDSTOP_INVERTING true | Invert Z Move Direction |
| #define Z_MIN_PROBE_ENDSTOP_INVERTING false | #define Z_MIN_PROBE_ENDSTOP_INVERTING tue | Invert Z Probe Direction |
| //#define X_DRIVER_TYPE  A4988 | #define X_DRIVER_TYPE  TMC2209 | Select Stepper Driver for X-Axis |
| //#define Y_DRIVER_TYPE  A4988 | #define Y_DRIVER_TYPE  TMC2209 | Select Stepper Driver for Y-Axis |
| //#define Z_DRIVER_TYPE  A4988 | #define Z_DRIVER_TYPE  TMC2209 | Select Stepper Driver for Z-Axis |
| //#define Z2_DRIVER_TYPE A4988 | #define Z2_DRIVER_TYPE TMC2209 | Select Stepper Driver for Z2-Axis |
| //#define E0_DRIVER_TYPE A4988 | #define E0_DRIVER_TYPE TMC2209 | Select Stepper Driver for Extruder |
| #define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 4000, 500 } | #define DEFAULT_AXIS_STEPS_PER_UNIT   { 400, 400, 400, 1660 } | Default Axis Steps Per Unit For 1.8 and BMG |
| #define DEFAULT_MAX_FEEDRATE          { 300, 300, 5, 25 } | #define DEFAULT_MAX_FEEDRATE          {200, 200, 12, 120} | Default Max Feed Rate |
| #define DEFAULT_MAX_ACCELERATION      { 3000, 3000, 100, 10000 } | #define DEFAULT_MAX_ACCELERATION      {2000, 2000, 200, 5000} | Default Max Acceleration change |
| #define DEFAULT_ACCELERATION          3000 | #define DEFAULT_ACCELERATION          1250 | X, Y, Z and E acceleration for printing moves |
| #define DEFAULT_RETRACT_ACCELERATION  3000 | #define DEFAULT_RETRACT_ACCELERATION  1250 | E acceleration for retracts |
| #define DEFAULT_TRAVEL_ACCELERATION   3000 | #define DEFAULT_TRAVEL_ACCELERATION   1250 | X, Y, Z acceleration for travel (non printing) moves |
| ~~//#define CLASSIC_JERK | #define CLASSIC_JERK | Enabled Default Jerk limits |
| ~~#define DEFAULT_XJERK 10.0~~ | ~~#define DEFAULT_XJERK 6.0~~ | ~~Default Jerk limits (mm/s)~~ |
| ~~#define DEFAULT_YJERK 10.0~~ | ~~#define DEFAULT_YJERK 6.0~~ | ~~Default Jerk limits (mm/s)~~ |
| ~~#define DEFAULT_ZJERK  0.3~~ | ~~#define DEFAULT_ZJERK  0.3~~ | ~~Default Jerk limits (mm/s)~~ |
| #define DEFAULT_EJERK    5.0 | #define DEFAULT_EJERK    4.5 | Set Jerk limit on Extruder |
| ~~//#define S_CURVE_ACCELERATION~~ | ~~#define S_CURVE_ACCELERATION~~ | ~~Enabled S-Curve Acceleration Feature~~ |
| #define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN | //#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN | Disabled Z-MIN pin end stop |
| //#define USE_PROBE_FOR_Z_HOMING | #define USE_PROBE_FOR_Z_HOMING | Force the use of the probe for Z-axis homing |
| //#define FIX_MOUNTED_PROBE | #define FIX_MOUNTED_PROBE | Enabled P.I.N.D.A 2 Probe |
| #define NOZZLE_TO_PROBE_OFFSET { 10, 10, 0 } | #define NOZZLE_TO_PROBE_OFFSET { 23, 5, 0 } | Set Nozzle-to-Probe offsets for BMG |
| #define XY_PROBE_SPEED (133*60) | #define XY_PROBE_SPEED (180*60) | Config X and Y Travel speed for probes |
| #define Z_PROBE_SPEED_FAST HOMING_FEEDRATE_Z | #define Z_PROBE_SPEED_FAST (HOMING_FEEDRATE_Z * 4) | |
| //#define MULTIPLE_PROBING 2 | #define MULTIPLE_PROBING 3 | Improved results by probing 3 times |
| #define Z_CLEARANCE_DEPLOY_PROBE   10 | #define Z_CLEARANCE_DEPLOY_PROBE    0 | Z Clearance for Deploy/Stow |
| #define Z_CLEARANCE_BETWEEN_PROBES  5 | #define Z_CLEARANCE_BETWEEN_PROBES  2 | Z Clearance between probe points |
| #define Z_CLEARANCE_MULTI_PROBE     5 | #define Z_CLEARANCE_MULTI_PROBE     1 | // Z Clearance between multiple probes |
| #define Z_PROBE_LOW_POINT          -2 | #define Z_PROBE_LOW_POINT          -4 | Farthest distance below the trigger-point to go before stopping |
| //#define Z_MIN_PROBE_REPEATABILITY_TEST | #define Z_MIN_PROBE_REPEATABILITY_TEST | Enable repeatability test to test probe accuracy |
| //#define PROBING_HEATERS_OFF | #define PROBING_HEATERS_OFF | Turn heaters off when probing |
| #define INVERT_X_DIR false | #define INVERT_X_DIR false | Invert the stepper direction on X-Axis |
| #define INVERT_Y_DIR true | #define INVERT_Y_DIR false | Invert the stepper direction on Y-Axis |
| #define INVERT_Z_DIR false | #define INVERT_Z_DIR true | Invert the stepper direction on Y-Axis |
| #define INVERT_E1_DIR false | #define INVERT_E1_DIR true | Invert the stepper direction on Extruder |
| #define X_BED_SIZE 200 | #define X_BED_SIZE 250 | Config Bed Size of X-Axis |
| #define Y_BED_SIZE 200 | #define Y_BED_SIZE 210 | Config Bed Size of Y-Axis |
| #define Y_MIN_POS 0 | #define Y_MIN_POS -4 | Config Y-Axis min position |
| #define Z_MIN_POS 0 | #define Z_MIN_POS 0.15 | Config Z-Axis min position |
| #define X_MAX_POS X_BED_SIZE | #define X_MAX_POS 255 | Config X-Axis max position |
| #define Y_MAX_POS Y_BED_SIZE | #define Y_MAX_POS 212.5 | Config Y-Axis max position |
| #define Z_MAX_POS 200 | #define Z_MAX_POS 210 | Config Z-Axis max position |
| //#define FILAMENT_RUNOUT_SENSOR | #define FILAMENT_RUNOUT_SENSOR | Enabled Filament Run-Out Sensor |
| #define FIL_RUNOUT_STATE     LOW | #define FIL_RUNOUT_STATE     HIGH | Pin state indicating that filament is NOT present |
| //#define FILAMENT_RUNOUT_DISTANCE_MM 25 | #define FILAMENT_RUNOUT_DISTANCE_MM 2 | After a runout is detected |
| //#define AUTO_BED_LEVELING_BILINEAR | #define AUTO_BED_LEVELING_BILINEAR | Enabled Auto Bed Leveling |
| //#define RESTORE_LEVELING_AFTER_G28 | #define RESTORE_LEVELING_AFTER_G28 | Enabled restore leveling after G28 Command |
| //#define MANUAL_X_HOME_POS 0 | #define MANUAL_X_HOME_POS 0 | Enabled manual home position for X-Axis |
| //#define MANUAL_Y_HOME_POS 0 | #define MANUAL_Y_HOME_POS -2.2 | Enabled manual home position for Y-Axis |
| //#define MANUAL_Z_HOME_POS 0 | #define MANUAL_Z_HOME_POS 0.2 | Enabled manual home position for Z-Axis |
| //#define Z_SAFE_HOMING | #define Z_SAFE_HOMING | Enabled avoid homing with a Z probe outside the bed area |
| //#define EEPROM_SETTINGS  | #define EEPROM_SETTINGS | Persistent storage with M500 and M501 |
| //#define EEPROM_AUTO_INIT | #define EEPROM_AUTO_INIT | Init EEPROM automatically on any errors |
| //#define NOZZLE_PARK_FEATURE | #define NOZZLE_PARK_FEATURE | Park the nozzle at the given XYZ position on idle or G27 |
| //#define PRINTCOUNTER | #define PRINTCOUNTER | Track statistical data |
| //#define SDSUPPORT | #define SDSUPPORT | SD Card on display support |
| //#define SD_CHECK_AND_RETRY | #define SD_CHECK_AND_RETRY | Checks and retries on the SD communication |
| //#define ENCODER_PULSES_PER_STEP 4 | #define ENCODER_PULSES_PER_STEP 4 | |
| //#define ENCODER_STEPS_PER_MENU_ITEM 1 | #define ENCODER_STEPS_PER_MENU_ITEM 1 | |
| //#define INDIVIDUAL_AXIS_HOMING_MENU | #define INDIVIDUAL_AXIS_HOMING_MENU | Add individual axis homing items (Home X, Home Y, and Home Z) to the LCD menu |
| //#define REPRAP_DISCOUNT_SMART_CONTROLLER | #define REPRAP_DISCOUNT_SMART_CONTROLLER | Use Prusa Display |
| //#define NEOPIXEL_LED | #define NEOPIXEL_LED | Enabled NEOPIXEL LED Support |
| #define NEOPIXEL_TYPE   NEO_GRBW | #define NEOPIXEL_TYPE   NEO_GRB | Support NEOPIXEL WS2812/WS2812B with RGB |
| #define NEOPIXEL_PIN     4 | #define NEOPIXEL_PIN     P1_24 | Config PIN for plug NEOPIXEL |
| //#define NEOPIXEL_STARTUP_TEST | #define NEOPIXEL_STARTUP_TEST | Test NEOPIXEL on Startup |

### Configuration_adv.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| #define THERMAL_PROTECTION_PERIOD 40 | #define THERMAL_PROTECTION_PERIOD 60 | Thermal Protection provides additional protection to your printer from damage |
| #define THERMAL_PROTECTION_HYSTERESIS 4 | #define THERMAL_PROTECTION_HYSTERESIS 10 | |
| //#define ADAPTIVE_FAN_SLOWING | #define ADAPTIVE_FAN_SLOWING | Slow part cooling fan if temperature drops |
| #define WATCH_TEMP_PERIOD 20  | #define WATCH_TEMP_PERIOD 40 | |
| #define THERMAL_PROTECTION_BED_PERIOD        20 |  #define THERMAL_PROTECTION_BED_PERIOD        60 | Thermal Protection parameters for the bed are just as above for hotends |
| #define THERMAL_PROTECTION_BED_HYSTERESIS     2 | #define THERMAL_PROTECTION_BED_HYSTERESIS      8 | |
| //#define HOTEND_IDLE_TIMEOUT | #define HOTEND_IDLE_TIMEOUT | Enabled Hotend Timeout |
| //#define FAN_MIN_PWM 50 | #define FAN_MIN_PWM 80 | PWM Fan Scaling form 0-255 |
| #define E0_AUTO_FAN_PIN -1 | #define E0_AUTO_FAN_PIN FAN1_PIN | Config Fan Pin for Extruder |
| #define NUM_Z_STEPPER_DRIVERS 1 | #define NUM_Z_STEPPER_DRIVERS 2 | Config 2 Z-Axis Stepper |
| //#define SENSORLESS_BACKOFF_MM  { 2, 2 } | #define SENSORLESS_BACKOFF_MM  { 2, 2 } | (mm) Backoff from endstops before sensorless homing |
| #define HOMING_BUMP_MM      { 5, 5, 2 } | #define HOMING_BUMP_MM      { 0, 0, 2 } | (mm) Backoff from endstops after first bump |
| #define HOMING_BUMP_DIVISOR { 2, 2, 4 } | #define HOMING_BUMP_DIVISOR { 0, 0, 0 } | e-Bump Speed Divisor (Divides the Homing Feedrate) |
| //#define HOMING_BACKOFF_POST_MM { 2, 2, 2 } | #define HOMING_BACKOFF_POST_MM { 2, 2, 0 } | (mm) Backoff from endstops after homing |
| //#define Z_STEPPER_AUTO_ALIGN | #define Z_STEPPER_AUTO_ALIGN | Enabled Z-Axis stepper auto alignment |
| //#define Z_STEPPER_ALIGN_XY { {  10, 190 }, { 100,  10 }, { 190, 190 } } | #define Z_STEPPER_ALIGN_XY { {  40, 90 }, { 230,  90 } } | Configuration position for align 2 Z-Axis Stepper |
| #define DISABLE_INACTIVE_Z true | #define DISABLE_INACTIVE_Z false | the nozzle could fall onto your printed part! |
| //#define ADAPTIVE_STEP_SMOOTHING | #define ADAPTIVE_STEP_SMOOTHING | Adaptive Step Smoothing increases the resolution of multi-axis moves |
| //#define PROBE_OFFSET_WIZARD | #define PROBE_OFFSET_WIZARD | Add Probe Z Offset calibration to the Z Probe Offsets menu |
| //#define LCD_INFO_MENU | #define LCD_INFO_MENU | Display Info Menu on Display |
| //#define LED_CONTROL_MENU | #define LED_CONTROL_MENU | Display LEC Control Menu on Display |
| #define LED_USER_PRESET_GREEN      128 | #define LED_USER_PRESET_GREEN      0 | |
| #define LED_USER_PRESET_BLUE         0 | #define LED_USER_PRESET_BLUE       255 | |
| //#define LED_USER_PRESET_STARTUP | #define LED_USER_PRESET_STARTUP | Have the printer display the user preset color on startup |
| //#define STATUS_MESSAGE_SCROLLING | #define STATUS_MESSAGE_SCROLLING | Scroll a longer status message into view |
| //#define LCD_TIMEOUT_TO_STATUS 15000 | #define LCD_TIMEOUT_TO_STATUS 15000 | The timeout (in ms) to return to the status screen from sub-menus |
| //#define SHOW_REMAINING_TIME | #define SHOW_REMAINING_TIME | Display estimated time to completion |
| //#define USE_M73_REMAINING_TIME | #define USE_M73_REMAINING_TIME | Use remaining time from M73 command instead of estimation |
| #define SD_FINISHED_RELEASECOMMAND "M84" | #define SD_FINISHED_RELEASECOMMAND "M84XYE" | keep Z enabled so your bed stays in place |
| #define EVENT_GCODE_SD_ABORT "G28XY" |  #define EVENT_GCODE_SD_ABORT "G27 P2 \nM84 X Y E" | G-code to run on SD Abort Print |
| //#define SCROLL_LONG_FILENAMES | #define SCROLL_LONG_FILENAMES | Scroll long filenames in the SD card menu |
| //#define BABYSTEPPING | #define BABYSTEPPING | Babystepping enables movement of the axes by tiny increments without changing the current position values |
| //#define DOUBLECLICK_FOR_Z_BABYSTEPPING | #define DOUBLECLICK_FOR_Z_BABYSTEPPING | Double-click on the Status Screen for Z Babystepping |
| //#define MOVE_Z_WHEN_IDLE | #define MOVE_Z_WHEN_IDLE | Jump to the move Z menu on doubleclick when printer is idle |
| #define MOVE_Z_IDLE_MULTIPLICATOR 1 | #define MOVE_Z_IDLE_MULTIPLICATOR 10 | Multiply 10mm by this factor for the move step size |
| //#define BABYSTEP_ZPROBE_OFFSET | #define BABYSTEP_ZPROBE_OFFSET | Combine M851 Z and Babystepping | 
| ~~//#define LIN_ADVANCE~~ | ~~#define LIN_ADVANCE~~ | ~~Enabled Linear Pressure Control v1.5~~ |
| ~~#define LIN_ADVANCE_K 0.22~~ | ~~#define LIN_ADVANCE_K 0.00~~ | ~~Setup default LA 1.5~~ |
| ~~//#define EXPERIMENTAL_SCURVE~~ | ~~#define EXPERIMENTAL_SCURVE~~ | ~~Enable this option to permit S-Curve Acceleration~~ |
| #define BLOCK_BUFFER_SIZE 16 | #define BLOCK_BUFFER_SIZE 32 | |
| #define BUFSIZE 4 | #define BUFSIZE 32 | |
| #define TX_BUFFER_SIZE 0 | #define TX_BUFFER_SIZE 32 | |
| //#define EMERGENCY_PARSER | #define EMERGENCY_PARSER | Emergency Command Parser |
| //#define ADVANCED_PAUSE_FEATURE | #define ADVANCED_PAUSE_FEATURE | Enable Advanced Pause Feature |
| #define PAUSE_PARK_RETRACT_FEEDRATE         60 | #define PAUSE_PARK_RETRACT_FEEDRATE         40 | |
| #define FILAMENT_CHANGE_UNLOAD_FEEDRATE     10 | #define FILAMENT_CHANGE_UNLOAD_FEEDRATE     20 | |
| #define FILAMENT_CHANGE_UNLOAD_LENGTH      100 | #define FILAMENT_CHANGE_UNLOAD_LENGTH      120 | |
| #define FILAMENT_CHANGE_SLOW_LOAD_FEEDRATE   6 | #define FILAMENT_CHANGE_SLOW_LOAD_FEEDRATE   10 | |
| #define FILAMENT_CHANGE_SLOW_LOAD_LENGTH     0 | #define FILAMENT_CHANGE_SLOW_LOAD_LENGTH     20 | |
| #define FILAMENT_CHANGE_FAST_LOAD_FEEDRATE   6 | #define FILAMENT_CHANGE_FAST_LOAD_FEEDRATE   40 | |
| #define FILAMENT_CHANGE_FAST_LOAD_LENGTH     0 | #define FILAMENT_CHANGE_FAST_LOAD_LENGTH    100 | |
| #define ADVANCED_PAUSE_PURGE_LENGTH         50 | #define ADVANCED_PAUSE_PURGE_LENGTH          30 | |
| #define FILAMENT_UNLOAD_PURGE_RETRACT       13 | #define FILAMENT_UNLOAD_PURGE_RETRACT         5 | |
| #define PAUSE_PARK_NOZZLE_TIMEOUT           45 | #define PAUSE_PARK_NOZZLE_TIMEOUT           180 | |
| #define FILAMENT_CHANGE_ALERT_BEEPS         10 | #define FILAMENT_CHANGE_ALERT_BEEPS          20 | |
| //#define PARK_HEAD_ON_PAUSE | #define PARK_HEAD_ON_PAUSE | |
| //#define FILAMENT_LOAD_UNLOAD_GCODES | #define FILAMENT_LOAD_UNLOAD_GCODES | |
| #define X_CURRENT_HOME  X_CURRENT | #define X_CURRENT_HOME  200 | Set motor current for homing |
| #define Y_CURRENT       800 | #define Y_CURRENT       850 | Set motor current |
| #define Y_CURRENT_HOME  Y_CURRENT | #define Y_CURRENT_HOME  250 | Set motor current for homing |
| #define Z_CURRENT       800 | #define Z_CURRENT       450 | Set motor current |
| #define Z2_CURRENT      800 | #define Z2_CURRENT      450 | Set motor current |
| #define CHOPPER_TIMING CHOPPER_DEFAULT_12V | #define CHOPPER_TIMING CHOPPER_09STEP_24V | Optimize spreadCycle chopper parameters |
| //#define SENSORLESS_HOMING | #define SENSORLESS_HOMING | Enabled sensorless homing |
| #define X_STALL_SENSITIVITY  8 | #define X_STALL_SENSITIVITY  75 | |
| #define Y_STALL_SENSITIVITY  8 | #define Y_STALL_SENSITIVITY  75 | |
| //#define IMPROVE_HOMING_RELIABILITY | #define IMPROVE_HOMING_RELIABILITY | |
| //#define SQUARE_WAVE_STEPPING | #define SQUARE_WAVE_STEPPING | Create a 50/50 square wave step pulse optimal for stepper drivers |
| //#define STARTUP_COMMANDS "M17 Z" | #define STARTUP_COMMANDS "M17 Z" | Enabled startup command |
| //#define HOST_ACTION_COMMANDS | #define HOST_ACTION_COMMANDS | |
| //#define HOST_PROMPT_SUPPORT | #define HOST_PROMPT_SUPPORT | |




