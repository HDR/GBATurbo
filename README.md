# GBATurbo
Cheap DIY game speed adjuster for the GBA

The entire pcb and it's components come in at around 5.50 USD

The PCB measures 20.5 by 9.8 mm.

[OSHPark Project](https://www.oshpark.com/shared_projects/w5yUIHU1)

**Front**

![Front of pcb](board_front.png)


**Back**

![Back of pcb](board_back.png)

Note: These are untested, and no flashable code has been written for the ATtiny85

BOM:

**U1:** [ATtiny85-20SUR](https://www.arrow.com/en/products/attiny85-20sur/microchip-technology)

**U2:** [MCP4151-503E](https://www.arrow.com/en/products/mcp4151-503esn/microchip-technology)

**U3:** [LTC1799CS5](https://www.arrow.com/en/products/ltc1799cs5trmpbf/analog-devices)

**C1:** [Capacitor 0603 0.1uF](https://www.arrow.com/en/products/c0603x104k3ractu/kemet-corporation)


## Flashing with an arduino

### Requirements


* An Arduino (yes really)
* A 10uF/25V Capacitor to bridge GND & Reset on the Arduino
* The Arduino Software

### Pinout

|  Name | Arduino | GBATurbo |
|:-----:|:-------:|:--------:|
| Reset |    10   |    Reset   |
|  MOSI |    11   |   MOSI   |
|  MISO |    12   |   MISO   |
|  SCK  |    13   |    SCK   |
|  VCC  |   +5V   |    VCC   |
|  GND  |   GND   |    GND   |


![Wiring](

### Flashing the Attiny85

1. Open Ardiuno IDE and click "File > Preferences" and paste this url ```https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json``` into "Additional board manager urls"

2. Go to Tools > Board > Manager and find "ATTiny" and install it.

3. Connect your arduino based on the pins listed above, don't forget the 10uF capacitor to bridge GND & Reset on the arduino. (Make sure the anode goes to ground)

4. Under tools set up the following settings.

|  Setting |  Value  |
|:-----:|:-------:|
|  Board  |    ATtiny25/45/85   |
|  Processor |    Atiny85   |
|  Clock |    Internal 8 MHz   |
|  Port  |    COMX (Arduino *)   |
|  Programmer  |   Arduino as ISP   |
