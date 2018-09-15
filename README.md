# GBATurbo
Cheap DIY speed adjustment for the GBA

Costs about 8 USD


Part List:

[MCP4151-503E](https://www.digikey.com/short/jw8d82)

[ATtiny85-20SUR](https://www.digikey.com/short/jw8dpp)

[LTC1799HS5](https://www.digikey.com/short/jw8dzf)


## Flashing with an arduino

### Requirements


* An Arduino (yes really)
* A 10uF Capacitor to bridge GND & Reset on the Arduino
* The Arduino Software
* [This board manager url](https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json)

### Pinout

|  Name | Arduino | GBATurbo |
|:-----:|:-------:|:--------:|
| Reset |    10   |    RST   |
|  MOSI |    11   |   MOSI   |
|  MISO |    12   |   MISO   |
|  SCK  |    13   |    SCK   |
|  VCC  |   +5V   |    VCC   |
|  GND  |   GND   |    GND   |
