This section is about mmwave presence sensors, mainly the HLK-LD series, since they are supported in ESPHome.

Some notes about the LD2420:
1. There is a certain uncertainty about which pin is the TX-pin: OT1 or OT2 (some sources say it depends on the firmware version; newer versions allegedly use OT2).
I can confirm that my LD2402, running version v1.6.1, uses OT1 as TX of the LD2402.
(OT2 is output, not really needed in Home Assistant; althougu you could use it to drive an LED).

2. Voltage required
The LD2420 needs 3V3. Don't use 5V or you riks damaging the board (I didn't test, some sources say it will damage/destroy the board).

3. Baud settinhgs
There's also some conflicting information out there on what baud rate to use. Here's confirming the board uses 115200 baud (256000 doesn't work!!! ask me how I know), other at default settings.

Additional note: don’t use the hardware RX/TX lines of the ESP32, they will conflict with the UART mode required to communicate with the LD2420 (or any other board for that matter).
Make sure to read the documentation on what ports of the ESP32 are available, some are reserved or conflict with external hardware.



