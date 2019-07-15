Repo notes for MakeHawkESP32
====================
Overview
=======
Gets the MakerHawk ESP32 with Wifi, Bluetooth, LoRaWAN dev board up and running.

Firstly there is a project to check some features of the board. It's got a small but neat screen which is great for seeing what's going on.

Once the board has been explored, move on to getting the LoRaWAN connection to The Things Network (TTN) up and running.

Pre-reqs
=======
A Micro USB cable and the board itself are the only hardware required.
You'll need the Arduino IDE installed and to have ensured it can see arduinos through the serial port.

Getting used to the board
==========================
Follow [ this tutorial ](https://docs.heltec.cn/#/en/user_manual/how_to_install_esp32_Arduino). Note that it refers to a 'Wireless Stick' board - change this
to be the WiFi LoRa 32 V2. The tutorial installs the arduino libraries and board definitions you need.

The WiFi_LoRa_32FactoryTest_NT sketch is a modification of the example sketch. I modified it primarily to lengthen the timers for display on startup, otherwise they can't easily be read. I've also fixed a handful of bugs.
Note that near the top of the sketch is the wifi settings. You can change these to your local Wifi network, although it doesn't really affect the functioning of the program.


Getting the LoRaWAN comms up and running
==========================
Note - I haven't actually connected to TTN because there are no base stations in range.

[ This tutorial ](https://robotzero.one/heltec-lora32-lorawan-node/) is invaluable. Basically follow it through: it signs you up to TTN, makes an application and adds a device.

The makerhawk_esp32_NT_print_id sketch prints out the chip ID in the comms console - you need this to generate the keys in TTN.

The OTAA_NT sketch (supposedly) makes the LoRAWAN connection. Next step - confirm that works.

