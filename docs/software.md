In this section, we will install the software required to flash the JN5169 MCUs.

# Pre-requisites:

- A computer running Windows 7 pr newer (If you are a Mac or Linux users, you can use a virtualized machine running windows. you will need to forward the usb connection to the virtual machine).
- your USB to serial module drivers must to be installed.


# Software download and installation:

- Download and install the [Production Flash Programmer](https://www.nxp.com/downloads/en/software-development-kits/JN-SW-4107.zip)
- Take a few minutes to read the [corresponding user manual](https://www.nxp.com/docs/en/user-guide/JN-UG-3099.pdf)

# Test it !

- Connect the usb-to-serial interface to both your computer and your module. **Check again if it is set at 3.3V!**
- open a command line window and got to the following directory `C:\NXP\ProductionFlashProgrammer`
- run `JN51xxProgrammer.exe -l` This should list the available COM port. 

Identify the COM number used by your usb to serial module.
- run `JN51xxProgrammer.exe -s COMx --deviceconfig` where COMx is the specific COM number for your serial module.

This should output some info about the MCU such as its MAC address and the type of chip.
If it output an error message check your connection, the drivers of your module and try again.

If it's ok you good to go and move to the next step: [flashing a custom firmware](flash.md)
