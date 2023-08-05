# Klipper config for a voron micron 180

All main MCU pins are configured for a BTT Octopus v1.1

## Mods
* Kickly
* Sensorless homing
* BTT EBB36
* mini12864 (Not really a mod, but it's not stock)

## Notes
If you plan on copying this config you will need to make sure you have all the same mods as me, or you will need to change the config to match your printer. Even with the same mods some stuff will still need to be changed such as the mcu serial, BTT EBB36 mcu serial and your klicky variables.

This config does also have a rather peculiar homing sequence due to the EBB36 wiring sometimes snagging on the Z axis drag chain. Because of this the printer first homes the X axis befor backing off to `X:90` and then homing the Y axis. It does this to allow the EBB36 and wires to slot between the drag chail loop. If you don't have this issue you can remove the `G1 X-90 F3000` from the `_HOME_X` macro in the `sensorless.cfg` file.