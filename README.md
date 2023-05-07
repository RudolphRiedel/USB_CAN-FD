# Hardware
This is an Open Source Hardware USB to CAN-FD interface.  
The design goal of this PCB was to provide two isolated CAN-FD channels capable of 8MBit/s for the data phase.  

## D5035-01
![USB_CAN-FD](/images/D5035-01.jpg?raw=true)
The PCBs D5035-01-xx are based on the ATSAME51J microcontroller from Microchip.  
Any ATSAME51J1x-Axx can be used, so every variant in TQFP-64, the bootloader and the firmware work on all three memory sizes.

This is WIP, the first five revisions are up and running.  
New for D5035-01-05: switched from a crystal to an oscillator to reduce the drift in the timestamps.  
The board is 58 mm x 33 mm for revisions 1 to 5, revision 6 will use a larger board of 69 mm x 39 mm.

## D5035-03
The PCB D5035-03-01 is designed as a carrier board for the Teensy 4.0.  
This is more a prove of concept, a child of the current chip-shortage.  

And it works, but it turned out to be rather fidgety to access the pins
for the single CAN-FD available and the 58 mm x 33 mm case does not work well for this version.

## D5035-05
![USB_CAN-FD](/images/D5035-05.jpg?raw=true)
The PCBs D5035-05-xx are based on the STM32G0B1CET6 microcontroller.  
The board is slightly larger at 69 mm x 39 mm.  

This is WIP, the first revision is up and running.  
PCBs for the second revision are ordered.  

## Whats next
There is an idea for a PCB with a different controller but unfortunately these are not
available anywhere, so this got pushed back.

## Beyond CAN
A board with 100Base-T1 or 10Base-T1S is also something we think about.

## Firmware
The open source firmware for this project is here: https://github.com/jgressmann/supercan

## Windows application
An open source Windows application that works with this interface is here: https://github.com/TDahlmann/canpp
