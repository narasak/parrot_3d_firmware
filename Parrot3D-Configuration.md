# Parrot 3D

## Change from [Parrot3D (Develop Main Branch)](https://github.com/narasak/parrot_3d_firmware/tree/develop/main)

### Configuration.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| **============================== <br/> Temperature <br/> ==============================** |||
| #define TEMP_SENSOR_0 67 | #define TEMP_SENSOR_0 5 | 5: is for E3D Thermistor 67: is for SE HT Thermistor |
| #define DEFAULT_Kp  28.53 | #define DEFAULT_Kp  24.45 | Default Hot End PID (Kp Value) |
| #define DEFAULT_Ki   2.99 | #define DEFAULT_Ki   4.59 | Default Hot End PID (Ki Value) |
| #define DEFAULT_Kd 168.08 | #define DEFAULT_Kd  32.57 | Default Hot End PID (Kd Value) |