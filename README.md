# CCD-Arduino-Mega

! Work in Progress - Entirely untested !


An Arduino mega shield for interfacing with Chrysler's legacy CCD databus.

This project is a shield for the Arduino Mega 2560. It is designed to hold all the parts necessary to interface with Chrysler's legacy databus CCD, utilized in Chrysler vehicles from the late 80s to late 90s.

The shield can hold a CCD chip in PDIP 14 formfactor, which enables the communication between Arduino Mega and a CCD-databus. For this scenario a quartz oscillator is needed on the PCB.

Known variants/labels of this chip are:

- Intersil CDP68HC68S1E (PDIP 14)
- Harris 4374040 (PDIP 14)
- Harris 306846 (PDIP 14)
- Signetics 4517535 (PDIP 14)

- Intersil CDP68HC68S1M (SOIC 20)
- Philips 4651148 (SOIC 20)
- Philips 04833637 (SOIC 20)
- Signetics 4632650 (SOIC 20)


Additionally, this board can hold the CCDBusTranceiver_v300 from https://github.com/laszlodaniel/CCDBusTransceiver
No oscillator is needed here, this is the preferred method.


There are three jumpers available for setting bus termination and bus bias voltage.

A pushbutton and two LEDs are also available for whatever one could use them.

There is no specific software available at this point.

This device is meant to be able to tinker with ECUs/BCMs/EATX-Controllers etc. on a testbench, without having to worry about the circuits around the CCD interfacing-chip.

It probably can also be used to sniff CCD messages in a vehicle, or trigger diagnostic commands.
It is not a full blown diagnostic device and will never be, since it is missing some other features Chrysler used in old vehicles.

The board is powered via the USB connection of the Arduino, and also enables the serial communication with a serial console or program.
The simplest way to get started is to use the serial passthrough example sketch and set the baud rate communication to the chip to 7812,5 Baud (CCD bus baud speed).


Related and highly respected work:

Juha Niinikoski
http://www.kolumbus.fi/juha.niinikoski/CCD_bus/ccd_display.htm

Boundary Condition / László Dániel
https://chryslerccdsci.wordpress.com
https://github.com/laszlodaniel/ChryslerCCDSCIScanner
https://github.com/laszlodaniel/CCDLibrary
https://github.com/laszlodaniel/CCDBusTransceiver

Geoff / moparchem.com / Ladybug / Dcal

ShelGame at turbo-mopar.com
http://www.turbo-mopar.com/forums/member.php?141-ShelGame

wowzer at turbo-mopar.com
http://www.turbo-mopar.com/forums/member.php?1068-wowzer

majekw
https://github.com/majekw/sigrok-ccd-pd

xerootg
https://github.com/xerootg

NickInTimeDesign
https://nickintimedesign.com

AR1972
https://github.com/AR1972/jeep_2.5L

MWisBest
https://github.com/MWisBest/DRBDBReader

