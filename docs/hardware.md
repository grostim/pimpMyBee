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

JN5169 | JP1 | Function
------------- | ------------- | -------------
28 | 1 | TXD0
29 | 2 | RXD0
22 | 3 | SPIMISO
9/30 | 4 | VDD
3 | 5 | RESETN
21/39 | 6 | VSS

The MCU pins relate to the following schematic:
![](https://i0.wp.com/faire-ca-soi-meme.fr/wp-content/uploads/2017/02/jn5169-1.png?w=822)

And you will find below some examples of this connector in the xiaomi devices:

![](https://alephsecurity.com/assets/img/xiaomi/mcu-board-top-side.png)
>Xiaomi Smart Plug (ZNCZ02LM)

![](https://i2.wp.com/faire-ca-soi-meme.fr/wp-content/uploads/2017/02/pin_JN5169.jpg?w=371)
>Xiaomi temperature and humidity sensor (WSDCGQ01LM)

![](https://reho.st/medium/https://lh3.googleusercontent.com/hnhe13Uu22iNSJHEwouhv_imEOF6m43YmDjfyei6V8hDm0TDgiHCEkZ6k-Dov3HOQzGVC4T8ohX8mMrZa4IvIWhF3c9EfjpKJF34-9bM24KkX0a6nEmNvpgOlsSEn1orOQSLYe4Aj03298I7O5vWlG7nfwHqU-YgOFKvao9O2euxM4BOvG8Ch73J7c1L5pUKPfg2ctR9qec0RkSl9TYCLEBD2z-ayWQXMjGeGw-uU3Co-M1cBlBD2qT4pMOlcTMo4_U4tRDn_jDhrRbfpaIW9POFkxoVjjvJlp28gzkPoouEzUk1LVR4msU_WBAx816R4Avb59-rgw-4bDNNwbLDhifQ343Hue8z2IcfRooDFWfmcDSIkkQlGmVJWuKzJHknYYjxVjncwD4g1DjfYS_PIZvlMNqJtcceekKJdk3h-iyBO97pvU4PhFZnSOF-0XlXtT9vxFmjmrbOL8RgvMuRCFy51Zw4XkoQ7PdK48mqh6YuiLE6IDBu6ihFRO4SVvlfMNIf-WRONRWe9Yh1FKp0t2oFdqomZqjKNXWeLXEeR3wjSaEmS2ojehcQkDcXVQ2n2VUNpBL22Y5bzfNcVYSOTsR1T6POAIcAm_s6_LFXMoflBuqcWp8myhgr5bsw4yKsElbof_hosSj28v6hxcfMrtX2O3u3whhEF8LBpNZjkd3NIjD4fDhwJrY=w916-h1626-no)
>Xiaomi Gateway V1

## Physical connection to the serial interface.

Several options are available.

### direct welding
Depending on the pitch between each pad of the connector, this may be quite easy or very difficult.
Some very fine wire might be required for the devices with 1.27mm pitch (most small devices)
![](https://reho.st/medium/https://lh3.googleusercontent.com/A0tZ627IYzesw4NHzBaI7ok1P7BfP4gIL4yDwzjY60Oe68NfbwAFJUqjEli2lcpB4lEPOrh4ZRzJUVe_hC_KgtbDoh0xSDSU9IYRkVwGuhPqZCeSFj3jJc_ODasG79MpmCfpTsTw1z0ly0zpHjJ6l5TLtAd1XEMS9V9VVTdfO7MEnrtUULn86ukYTUf5PAsAKEliybwmfyzuP0re9nvdKnnlM7hlytHAzxQwH1AK3Nqb-eDTWmiSuFo381ZOl740xQdjxlsCTuN3GPhsXZT1UQPZt053F9xv1lwPWiZ4BWU73RT8theiKgYc7QaVQIj5o62dzxEJ-GAi39mo5kcNr4Sw-ayPPLBLi5GCHmbToqojNKwFjnxXGfEpmtFKuEKPRwJge48i211z1Bh1HzA8jzGzPJ-bPU7wdy_slmQ1wVqN5cqdyLmT2uKeeCs5qOLPrXAIknVDJhPWdEp3eVr6wSI4Hxz4OAuaxcIKy4eMzbwcEfSXp5JxSGCiErFexJ0Ex1jU36FArx-y_7JzBljuptnUdXQ3gdVAv6GVCEXYvDpShHUaVVho_1wGkD9UJK2BEaucHQuHiF4sBBZU1K1_6QPQUuOLh4pU5bburHr5KbA23b2SR5x_NCsZVVIWFa_G8SR6O_YN1IYhxn89Zv8-McjkWHdstK3jqpPz6A4yIUICCE6YXQC__q8=w2892-h1626-no)
>My ugly weldings on the Gateway (2mm pitch)

![](https://github.com/Jerome-PS/JN516xSniffer/raw/master/doc/Xiaomi_Door_sensor.JPG)
>Weldings on an Aqara door sensor (1.27mm pitch)

### Clips

Using [this clip](https://amzn.to/2GgbbQS), you can arrange a connection to the pads as long as they are spaced 1.27mm away.

![](https://reho.st/medium/https://lh3.googleusercontent.com/5kOf88YBkg9_9D2db0H5VgiOVITCCicsO-9P5u8vrkxVuHCh15nny23bofsxt49N2ZsI7uwC2WK-sJgaUK4vdsE0jKglCnR_vwYRPVnIRIshLZ08sbBg2X21TvAriRVimXE5GwaAYitMLnpJgPzS7fvCC5F_wxjXteNxW5L3n8g5OIib6qdT6wjp3ZbLEXgmJQ9u3Y6gE-b0YypJJ2zqpEIh_bHbOghLB7q3rrkJIAOsY2DBJkGtHV5YPf8vRXNc2knHtEGygrgXOwORVzsJnfOmB3RVrGmrGGbxBm-NrQOP7boGFKOBUpaPv_y4XZEgKJeuEkcWe9gzohcx2Uz7ahcUMTPkvEFykgR-8B-AQd7r6E1xy1or9ZMEOC4nQbU0_mMcX3s15LgoN6MsxYeMammYtkkfYLQ_6JUgZ4gbCual3I0YxYbkRO5WZGS568hj7FY8mmnrHACxqdutysJg5nbH-GYaXtrq4MWAFGHjog0WwncHcysjCXtWp_O-P5_hHfIs4Gg-0f-gnY4jH57i-1_4t2LA9mn7hV_mAf5NKi8oY3G4ABN4zkPXM5p57hfDifoahMRpe9BAEKFV0F38acSX4b9AK5pZsf9ilqwpLer00ksRSZJU1S62ipufmDDa6wU2LlW_z2TLWQdAzhhC2oLMK1fiU8bTrOUv0ke5vKjLvAJfdEZ4424=w2892-h1626-no)
> Clip on a WXKG02LM

This solution is not perfect though:
- Aligning the clip and the pads is tricky. The clip may move easily during flashing.
- The clip might not be able to reach the pads for some devices where the pads are too far from the edge.

### pogo pins
This is an option that i have not investigated yet, but i am pretty sure a custom connector based on pogo pins could be made for each type of sensor.
That would be probably the best solution.
