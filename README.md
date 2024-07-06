# Hardware
This is an Open Source Hardware USB to CAN-FD interface.
The design goal of this PCB was to provide two isolated CAN-FD channels capable of 8MBit/s for the data phase.

## D5035-01
![USB_CAN-FD](/images/D5035-01.jpg?raw=true)
The PCBs D5035-01-xx are based on the ATSAME51J microcontroller from Microchip.
Any ATSAME51J1x-Axx can be used, so every variant in TQFP-64, the bootloader and the firmware work on all three memory sizes.

D5035-01-08 likely is the final version.
I switched from using CAN-FD transceivers to CAN-SIC transceivers.

There is a full BOM included now: D5035-01_BOM_Release.xlsx
It has order codes from Mouser as example and the sum of the parts I selected came out as just below 29 Euros exclucding taxes when ordering only parts for a single unit.
The most expensive parts are the digital isolators, the controller, the CAN transceivers, the DCDC converter and the oscillator, which already cover more than half of the BOM costs which leaves no room to bringt the costs down - except when buying in bulk.
Cheaping out on components like the D-Sub 9 would be possible, but I really advise against it, I already chose a component that is inexpensive for it's specification, it is important for the application to use a gold plated D-Sub with at least 200 mating cycles.

The board is 69 mm x 39 mm.

## D5035-03
The PCB D5035-03-01 is designed as a carrier board for the Teensy 4.0.
This is more a prove of concept, a child of the current chip-shortage.

And it works, but it turned out to be rather fidgety to access the pins
for the single CAN-FD available and the 61 mm x 33 mm case does not work well for this version.

## D5035-05
![USB_CAN-FD](/images/D5035-05.jpg?raw=true)
The PCBs D5035-05-xx are based on the STM32G0B1CET6 microcontroller.
The board is slightly larger at 69 mm x 39 mm.

## Case
There are two versions of a 3D printable case available in this repository:
D5035-01 - 39 mm x 74.1 mm
D5035-05 - 45 mm x 82.14 mm

Assembly requires two press-fit light pipes for the status LEDs, two lengths of black 3.2 mm heat shrink tubing to hold the light pipes in place and four countersunk screws.

LFB063CTP - DigiKey LFB063CTP-ND - Mouser 593-LFB063CTP
M3 x 16 mm, countersunk, preferably Torx / A2 (ISO 14581)

## Whats next
There is an idea for a PCB with a different controller but unfortunately these are not
available anywhere, so this got pushed back.

## Beyond CAN
A board with 100Base-T1 or 10Base-T1S is also something we think about.

## Firmware
The open source firmware for this project is here: https://github.com/jgressmann/supercan

## Windows application
An open source Windows application that works with this interface is here: https://github.com/TDahlmann/canpp
