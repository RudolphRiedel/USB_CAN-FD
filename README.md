# USB_CAN-FD

This is an Open Source Hardware USB to CAN-FD Interface.
The design goal of this PCB was to provide two isolated CAN-FD channels capable of 8MBit/s for the data phase.

The PCBs D5035-01-xx are based on the ATSAME51J microcontroller from Microchip.
Any ATSAME51J1x-Axx can be used, so every variant in TQFP-64, the bootloader and the firmware work on all three memory sizes.
This is WIP, the first four Revisions are up and running.

The PCB D5035-03-01 is designed as a carrier board for the Teensy 4.0.
This is more a prove of concept, a child of the current chip-shortage.
And it works but it turned out to be rather fidgety to access the pins
for the single CAN-FD available and the case does not work well for this version.

There is an idea for a PCB with a different controller but unfortunately these are not
available anywhere, so this got pushed back.

The open source firmware for this project is here: https://github.com/jgressmann/supercan

An open source Windows application that works with this interface is here: https://github.com/TDahlmann/canpp
