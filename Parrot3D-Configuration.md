# Parrot 3D

## Change from [Parrot3D (Develop Main Branch)](https://github.com/narasak/parrot_3d_firmware/tree/develop/main)

### Configuration.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| **============================== <br/> Driver <br/> ==============================** |||
| #define DEFAULT_AXIS_STEPS_PER_UNIT { 200, 200, 400, 830 } | #define DEFAULT_AXIS_STEPS_PER_UNIT { 100, 100, 400, 415 } | Default Axis Steps Per Unit For 1.8 and BMG |

### Configuration_adv.h

| From     | To (SKR_1.4_TURBO) | Description |
|----------|------------|------------|
| **============================== <br/> Driver <br/> ==============================** |||
| #define X_CURRENT       800 | #define X_CURRENT       500 | Set motor current |
| #define Y_CURRENT       850 | #define Y_CURRENT       600 | Set motor current |
| #define E0_CURRENT      800 | #define E0_CURRENT      550 | Set motor current |
