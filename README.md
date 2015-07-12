creatr-hs-arduino-firmware
==========================

This is CHILI's take on the firmware for Leapfrog Creatr HS hardware board. It is based on the firmware given in:
http://support.lpfrg.com/support/solutions/articles/1000179838-uploading-the-creatr-hs-firmware.

build
-----

You need Arduino IDE 1.0.6 to build the code. The project to build is CreatrHSProduction20150115.ino.

flash
-----

1. **IMPORTANT:** Disconnect first the main USB cable that is connected to the back of the machine from your PC.
1. Disconnect the B type USB cable end from the top left connector on the main Creatr HS board. It should be fairly exposed when the top plate covering the electronics is unmounted.
1. Connect your PC to this connector (via another external cable). The board should appear as an FT232 UART port.
1. In the Arduino IDE, under Tools -> Serial port, select the appropriate serial port (probably looks like **/dev/ttyUSBx**).
1. In the Arduino IDE, under Tools -> Board, select **Arduino Mega 2560 or Mega ADK**.
1. In the Arduino IDE, under Tools -> Programmer, select **AVRISP mkII** (should be the default).
1. Flash (no need to reboot).
1. Unplug the B type cable from your PC and reconnect the first cable that you unplugged. You may now connect the main cable from the back of the machine to your PC.
1. In Simplify 3D, under Machine Control Panel, connect to the appropriate serial port (probably looks like **/dev/ttyUSBx**) with 115K baud.
1. Send `M500` and then `M502` under Communication.
1. Done (no need to reboot).

