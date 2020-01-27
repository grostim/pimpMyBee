## Welcome to the pimpMyBee documentation!

An attempt to develop custom firmware for xiaomi Zigbee devices.

## Foreword

Be warned: This is a work in progress.
At this stage, there is no stepping back: if you decide to flash you device with a custom firmware, you won't be able to revert to the factory firmware. The device will not be usable anymore with the Xiaomi Gateway.

### Getting started
* [Get access to the programming port](hardware.md)
* [Install the required software](software.md)
* [How to flash a firmware](flash.md)

### Customs firmware
* [License](LICENSE.md)
* [Use your xiaomi devices as a zigbee sniffer (By Jerome-PS)](https://github.com/Jerome-PS/JN516xSniffer)
* [Use your Xiomi gateway as a zigbee router (repeater)](firmware/GatewayV1.md)

### Development
* [How to install the development software suite - WORK IN PROGRESS]
* [pinout of various xiaomi modules](pinout.md)

### ToDo List and future developments

[ ] Versionize / tagging of the workable binaries.
[ ] clean up the repeater firmware. Remove unused switch functions. Make it discoverable by zigbee2mqtt.
[ ] Make a custom firmware for the button switches. (Make them use the standard on/off clusters and make them bindable).
