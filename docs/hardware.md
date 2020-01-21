# Hardware connection

## Foreword
This is heavily based on the research of these tinkerers:
- [Aleph Security](https://alephsecurity.com/2019/07/01/xiaomi-zigbee-1/)
- [FaireCaSoiMeme](http://faire-ca-soi-meme.fr/hack/2017/02/27/hack-xiaomi-mi-smart-temperature-and-humidity-sensor/)

## Serial connector

It seems that all xiaomi/Aqara/Lumi zigbee devices are based on the same MCU : NXP JN5169.
This chip provide a serial interface for programming and xiaomi has been kind enough to make the pins available on a standard connector on each device.
This connector is usually tagged JP1 and has 6 pins.

Here is the property of each pin:
