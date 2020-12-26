# Parrot 3D Printer Firmware
![Parrot 3D Logo](https://github.com/narasak/parrot_3d/blob/master/img/parrot_3d_logo.svg?raw=true)

## Parrot 3D Firmware 2.x

Parrot 3D Firmware is next level for Parrot 3D Printer base on Marlin Firmware 2.x.

Download earlier versions of firmware on the [Releases page](https://github.com/narasak/parrot_3d_firmware/releases).

## New Features
* Now support NeoPixel LED upto 30 LED (Use with BigTreeTech DCDC V1.0 power module)
* Enable Linear Advance with S-Curve Acceleration
* Enable Junction Deviation Factor
* Driver monitoring for error conditions like over temperature and short to ground.
* Support filament run out
* Add Chris Warkocki's Custom Command
* Stronger stepper motor movement
* Many more...

## Fixed Issue
* A fixed thermal runaway when use in cold winter.
* A fixed stepper motor noise when run fast. (Noise come from TMC StealthChop mode.)
* Many more...

# Configuration For

## Motherboard
* BigTreeTech SKR 1.4 Turbo

## Stepper Drivers
* BigTreeTech TMC2209 1.2 on X, Y, Z, E, E0

## Steppers
* X-axis: LDO 1.8° motor (LDO-42STH40-1Q04ASC)
* Y-axis: LDO 1.8° motor (LDO-42STH40-1Q04ASC)
* Z-axis: LDO 1.8° motor (LDO-42STH34-1004L321EC TEFLON COATED LEADSCREW)
* E-axis: 
  * LDO 1.8° motor (LDO-42STH25-1004AH)
  * LDO 1.8° motor (LDO-42STH20-1004AS2)
  * Bondtech Upgrade Kit for Prusa i3 MK3S & MK2.5S
* Micro Stepping: 1/16

## Hotend
* Slice Engineering Mosquito/Mosquito Magnum Hotend
* Slice Engineering 50W 24V Heater Cartridge
* Slice Engineering High Temperature Thermistor
* P.I.N.D.A. 2

## LCD Controller
* BIGTREETECH TFT35 V3

## License

Parrot 3D Firmware is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Parrot 3D firmware as the driver for your Parrot 3D Printer product.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
