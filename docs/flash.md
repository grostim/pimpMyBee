
# Flashing a MCU

## Get your firmware

- Browse to the [index page](index.md#customs-firmware) and choose the firmware you need.
- Download it and move it to `C:\NXP\ProductionFlashProgrammer`

* * *
**Before continuing, think again: There is no coming back. We won't be able to re-install the stock firmware. You won't be able to use it again with the original xiaomi framework. You may also brick your devices. You are on you own, i decline any responsibility if your device get damage.**
* * *

Still here ? 
Ok, let's continue.

## Flashing procedure

That's the easy part:
- open a command line window and got to the following directory `C:\NXP\ProductionFlashProgrammer`
- run `JN51xxProgrammer.exe -s COMx -f FIRMWARE.bin` where COMx is the specific COM number for your serial module and FIRMWARE.bin is the firmware you want to flash.
- This will erase the flash and program it with the new firmware.
- Xiaomi has enabled CRP-1 code read protection. Thus, it is normal if the flash read fails after programming.
- When you will reboot, the devices will run the new firmware and try to join an exisiting zigbee network.
