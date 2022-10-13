# CrallyBoard
Smart Home System / Alarm System / Input Output System for Raspberry Pi CM4

***THIS IS JUST A DOCUMENTATION FOR MYSELF! YOU CAN USE IT, BUT THERE MAY BE MISSING SOME STEPS!***


This is a custom Board made for Raspberry Pi CM4 Module

It contains:

- 16 Inputs via GPIO (with 3,3V Z-Diodes) connected through a PIN-Header to eventually add some Input-Handling PCBs in future
- 1 seperate Input via GPIO
- 16 Ouputs via MCP23017 (I2C). Outputs from MCP over OptoCoupler to a PinHeader to directly connect these Output-Relays-Modules (https://www.amazon.de/-/en/AZDelivery-optocoupler-low-level-compatible-including/dp/B07N2Z1DWG/ref=sr_1_2?crid=32S2CZSB2PI05&keywords=12v%2B16%2Bch%2Brelais%2Bmodul&qid=1665641353&sprefix=12v%2B16%2Bch%2Brelays%2Bmodule%2Caps%2C74&sr=8-2&th=1)
- 1 OnBoard Output Relays directly via GPIO
- 1 Display Port for SSD1306 (I2C) (3V or 5V)
- 1 RTC Port for DS3231 (I2C) (3V or 5V)
- 1 RS-485 Port
- 1 free to use I2C Port (3V or 5V)
- 1 free to use onboard button
- 1 USB OTG Port
- 1 Double USB Port for using with RPi
- 1 Ethernet Gigabit Port with PoE
- 1 PCI-E 1x Port
- 2 FAN-Ports (5V and 12V)


Main Supply Power:

There yre several Options:

- PoE when AG5300 or AG5400 is on board
- USB-C (min. 15W)
- Directly 7-15V via "12V IN"-Port
- 16-30V via "16-30V IN"-Port

When using 16-30V Power Supply you were able to connect a Gel Lead Battery. With the potentiometer you can adjust the Battery Load Voltage (max. 15V due to Zener Diodes).
Also there is a deep discharge protection via ICL7665. It disconnects the Output from Battery at around <11,2V and reconnects at around >13V.

Well, the values are not that accurate and I know that the circuit isn't very professional. But for my usage it's working well enough.

For the 3V Line on the board you can choose (via jumper) to use the 3V comming from the RPi or use a seperate regulator (TL1963A-33DCYR).



I personally use it as Smart Home System and Alarm System. The Software is written with python and php. Maybe I will add it to the repository later...
