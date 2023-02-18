# PCB

There are 3 PCBs in this repo. The ConnectorBoard is responsible for the connection between the radio and the module. The MainBoard contains the ESP32 and a JST GH port for flashing. Flashing works in the same way as the ESP32 devkits with esptool.py. An additional USB-FTDI device is required for this. The IO board contains all the buttons and the display for the user. The PCB was divided into three parts to ensure that it can be installed in a shell as modularly as possible. Also, in the event of circuit faults, you don't have to order everything.

## Notes

- It's important to ensure that a display with 14 pins is used. There are also some displays which are sold with 15 pins.
- If the module always starts in download mode, the capacitor C6 on the main PCB must be removed. C6 is originally responsible for debouncing the button, but puts the ESP32 into flash mode the first time it's booted.

## Used as reference

- schematic of the ESP32 DevKitC development board
- ShenZhen QDTech Co.,LTD 0.91 OLED Schematic und Allvision technology Inc. OEL Display Module Product Specification.
