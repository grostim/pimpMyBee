# Target

Xiaomi Gateway Version 1
(It may, or may not, work with other versions).

# Behavior

This firmware is based on the NXP app note JN-AN-1189 and more specifically the MainsPowerOutlet example.
This means that the flashed gateway will behave as a mains power outlet zigbee device, even if, obviously, the gateway has no relay tied to any of its output.
(As far as i have investigated, no useful components is tied to the JN5169 chip of the gateway. Leds, speaker, button, etc.. are connected to the wifi chip pins).
Therefore, the only useful application of this purpose is that the gateway will now act as a router and will be able to extend your zigbee network.

I use it with zigbee2mqtt. This work well, even if it is shown as an unrecognized device by zigbee2mqtt. However, it is still behaving as exepected a router.

There is some debugging message that can be monitored on the serial output while running. (especially while joining the network).

# Screenshots

![](https://reho.st/self/14419de16c36c76dd2dfdf7ff312e150af386a8d.png)
>Zigbee2mqtt Debugging output while joining my network

![](https://reho.st/self/16c2756540aa83733728d844f9ceb3ed40c519f3.png)
>Debugging output while joining my network

![](https://reho.st/medium/self/9c6515e1bf7bb639dc9c1add9ca679e1a9f509ff.png)
>The flashed gateway acting as a router in my network

# Download

[]()
