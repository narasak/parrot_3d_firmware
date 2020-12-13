# Parrot 3D Printer Firmware
![Parrot 3D Logo](https://github.com/narasak/parrot_3d/blob/master/img/parrot_3d_logo.svg?raw=true)

## Parrot 3D Firmware 2.x

Parrot 3D Firmware is next level for Parrot 3D Printer base on Marlin Firmware 2.x.

Download earlier versions of firmware on the [Releases page](https://github.com/narasak/parrot_3d_firmware/releases).

## New Features
* Now support NeoPixel LED upto 30 LED (Use with BigTreeTech DCDC V1.0 power module)
* Disable Linear Advance and Enable S-Curve Acceleration
* Disable Classic Jerk and Enable Junction Deviation Factor
* Add Chris Warkocki's Custom Command

## Fixed Issue
* Fixed Thermal Runaway

# Configuration For

## Motherboard
* BigTreeTech SKR 1.4 Turbo

## Stepper Drivers
* BigTreeTech TMC2209 1.2 on X, Y, Z, E, E0

## Steppers
* X-axis: LDO 0.9° motor (LDO-42STH48-1684MAC)
* Y-axis: LDO 0.9° motor (LDO-42STH48-1684MAC)
* Z-axis: LDO 1.8° motor (LDO-42STH34-1004L321EC TEFLON COATED LEADSCREW)
* E-axis: LDO 0.9° motor (LDO-42STH25-1404MAC)
* Micro Stepping: 1/16

## Hotend
* Slice Engineering Mosquito/Mosquito Magnum Hotend
* Slice Engineering 50W 24V Heater Cartridge
* Slice Engineering High Temperature Thermistor
* P.I.N.D.A. 2

## LCD Controller
* RERAP Discount Smart Controller

## License

Parrot 3D Firmware is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Parrot 3D firmware as the driver for your Parrot 3D Printer product.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
