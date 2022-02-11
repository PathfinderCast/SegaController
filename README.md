# SegaController #

Read Sega Genesis (Mega Drive) and Master System (Mark III) controllers in your Arduino sketches.

[![Arduino Sega Genesis Controller](https://img.youtube.com/vi/mRGwLuHvMs0/hqdefault.jpg)](https://youtu.be/mRGwLuHvMs0)

## Installation ##

1. Download [SegaController.zip](https://github.com/PathfinderCast/SegaController/releases/latest)
2. Open the Arduino IDE
3. Open "Sketch > Include Library > Add .ZIP Library..."
4. Select the zip file you downloaded in step 1

## Usage ##

The controller pins are as follows, looking face on to the (female) DB9 plug:

    5 4 3 2 1
     9 8 7 6

See this [Google doc](https://docs.google.com/spreadsheets/d/1AowehgtFR0qmP2av_2KbIE8AoV2BKuSi6NTsK86RDzs/edit?usp=sharing) for additional wiring layout

1. Connect controller pin 5 to +5VCC
2. Connect controller pin 8 to GND
3. Connect pins 1,2,3,4,6,8,9  to a digital I/O pin 2-7 on your Arduino
4. Connect pin 7 to the digital I/O pin 8 on your Arduino
4. In your sketch, include the SegaController library

## Examples ##

There are two example sketches included which make use of the SegaController library. See "File > Examples > SegaController" in the Arduino IDE after installation. Make sure the digital pins you've wired matches those chosen in the code.

### SegaControllerSerialReader ###

This sketch reads the state of a single controller and reports it via the Serial interface. Note that it only reports when the state has changed (a button has been pressed or released). It's good for validating you've got your pins wired up properly.

### SegaControllerKeyboardReader ###

This sketch reads the state of a single controller and simulates key presses via the Keyboard interface. You can specify which buttons correspond to which keys in the sketch. This sketch requires a 32u4 based board (such as the Leonardo, Micro, or Due).


#### Attribution ####

Modified and Published under MIT license
Copyright (c) 2017 Jon Thysell
For details on how SegaController reads the controller's state, see [How To Read Sega Controllers](https://github.com/jonthysell/SegaController/wiki/How-To-Read-Sega-Controllers).
