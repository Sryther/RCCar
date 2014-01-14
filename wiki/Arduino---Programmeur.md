Source : [Arduino - Programmeur](http://arduino.cc/en/Hacking/Programmer)

## Programming

The Arduino Uno can be programmed with the Arduino software ([download](http://arduino.cc/en/Main/Software)). Select "Arduino Uno from the Tools > Board menu (according to the microcontroller on your board). For details, see the [reference](http://arduino.cc/en/Reference/HomePage) and [tutorials](http://arduino.cc/en/Tutorial/HomePage).

The ATmega328 on the Arduino Uno comes preburned with a [bootloader](http://arduino.cc/en/Tutorial/Bootloader) that allows you to upload new code to it without the use of an external hardware programmer. It communicates using the original STK500 protocol ([reference](http://www.atmel.com/dyn/resources/prod_documents/doc2525.pdf), [C header files](http://www.atmel.com/dyn/resources/prod_documents/avr061.zip)).

You can bypass the bootloader and program the microcontroller through the ICSP (In-Circuit Serial Programming) header; see [these instructions](http://arduino.cc/en/Hacking/Programmer) for details.

The ATmega16U2 (or 8U2 in the rev1 and rev2 boards) firmware source code is available . The ATmega16U2/8U2 is loaded with a DFU bootloader, which can be activated by:

* On Rev1 boards: connecting the solder jumper on the back of the board (near the map of Italy) and then resetting the 8U2.
* On Rev2 or later boards: there is a resistor that pulling the 8U2/16U2 HWB line to ground, making it easier to put into DFU mode. 

You can then use [Atmel's FLIP software](http://www.atmel.com/dyn/products/tools_card.asp?tool_id=3886) (Windows) or the [DFU programmer](http://dfu-programmer.sourceforge.net/) (Mac OS X and Linux) to load a new firmware. Or you can use the ISP header with an external programmer (overwriting the DFU bootloader). 

[See this user-contributed tutorial](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1285962838) for more information. 