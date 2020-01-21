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

![](https://i2.wp.com/faire-ca-soi-meme.fr/wp-content/uploads/2017/02/pin_JN5169.jpg?w=371)
>Xiaomi temperature and humidity sensor (WSDCGQ01LM)


![](https://reho.st/medium/https://lh3.googleusercontent.com/lVRcHyYeesE0HHpkHVFRHHTjuAQFc94MYWnX5g0FsZwa89conzcIZmzghf9C4QCdje8yWStq5I51JhmCfNcbfFeltKDz-t7eI1SRKXJYYdra5XJfH5rTT-GAooOZ7fBA1B6oKNPMd3F7ZMYviP2fzTGtvuqmGi1rnbxO0aufZUtrYxMypA-zf54EW-hFE3L0gMGmwfJIU5jsLa40A3m3BKiI5w9eArrAMfQMy-0n1LbAAwwLLY7CszvLJwCOYnTpvvFv3pKm5yv7OSc_IihX8ezBs5sGsuv6t00yVUGc2lGzjA6mjhXVjVsj0XZDJbDlgbUaqg0merwtrYerIB4HiTqd91XYBLby8pututIPVY2LweEhWHvp7lntkLh9_rFQfPRFCg-HvE7yV3q8FyeSes6ViZNjjVXg8fdtpfd2wpcVOmDB5iooOnTtOO1qk2GRbafXq6jIh8_bJnqrGbZVVraceDIKB8TY3iKmrnwI-83HZ6rnWiPssf2YxMByhB0r1brgtjHEzHVF02lzJwKVVHVO9kv2F92D1yKrcBOOQIKiylXCHy59uWwb7HwzsTe-w37DVwZeffjPdl_RsOwooLjfHM5i8Zm2D4I_EA8FPlWCFvYg-xlfomnRXDsza02Mdrgwv7tfPaNfUL09-feQp11kMgAqZKzO_bMQJw9qG0HxB1oLB-k7wos=w2640-h1486-no)
>Xiaomi Gateway V1
