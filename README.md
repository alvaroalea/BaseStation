What is this Fork
-----------------

In this link to a forum:
http://model-railroad-hobbyist.com/node/27318
it's posible to download a fork of the DCC++ command station that use a keypad an 16x2 LCD to managed the BaseStation.

As far A I know, for this modification he remove the serial comunication, also use a LcdKeyPad library I can not locate.

So, I update it to use adafruit Library, (BTW it use only I2C, not the analog pin) and restore serial comunication.
I'm on the way to use a external motor shield based on L298N, in this way I will free a pair of pins for other use.

What’s DCC++
------------

DCC++ is an open-source hardware and software system for the operation of DCC-equipped model railroads.

The system consists of two parts, the DCC++ Base Station and the DCC++ Controller.

The DCC++ Base Station consists of an Arduino micro controller fitted with an Arduino Motor Shield that can be connected directly to the tracks of a model railroad.

The DCC++ Controller provides operators with a customizable GUI to control their model railroad.  It is written in Java using the Processing graphics library and IDE and communicates with the DCC++ Base Station via a standard serial connection over a USB cable or wireless over BlueTooth.

What’s in this Repository
-------------------------

This repository, BaseStation-Uno, contains a complete DCC++ Base Station sketch designed for compiling and uploading into an Arduino Uno.  All sketch files are in the folder named DCCpp_Uno. More information about the sketch can be found in the included PDF file.

To utilize this sketch, simply download a zip file of this repository and open the file DCCpp_Uno.ino within the DCCpp_Uno folder using your Arduino IDE.  Please do not rename the folder containing the sketch code, nor add any files to that folder.  The Arduino IDE relies on the structure and name of the folder to properly display and compile the code.

The latest production release of the Master branch is 1.2.1:

* Supports both the Arduino Uno and Arduino Mega
* Built-in configuration for both the original Arduino Motor Shield as well as a Pololu MC33926 Motor Shield
* Built-in configuration and support of Ethernet Shields (for use with Mega only)

For more information on the overall DCC++ system, please follow the links in the PDF file.

Detailed diagrams showing pin mappings and required jumpers for the Motor Shields can be found in the Documentation Repository

The Master branch contains all of the Base Station functionality showed in the DCC++ YouTube channel with the exception of 2 layout-specific modules:

* Control for an RGB LED Light Strip using pins 44, 45, and 46 on the Mega
* An embedded AutoPilot routine that randomly selects a train to run through the entire layout, after which it is brought back into its original siding and the the patterns repeats with another randomly-selected train.  This is the AutoPilot routine showed on the DCC++ YouTube channel.  It does not require any computer, not DCC++ Controller to be running (DCC++ Controller contains a much more complicated 3-train Auto Pilot mode, also as shown on the DCC++ YouTube channel).

Since these modules are very layout-specififc, they are not included in the Master branch.  However, they are included in the Development branch.  Please feel free to download and copy any relevant code to customize your own version of DCC++ Base Station.

-December 27, 2015

