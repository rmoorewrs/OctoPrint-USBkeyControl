# OctoPrint-Octoremote

## Work in Progress! Use with care ##

Octoremote is a system to control serveral functions of your printer with a simple press of a button. Control the axis movement, manual extrusion and homing without the need of navigating through the printer menu or opening the Octopi GUI in your browser. 

OctoRemote consists of two components, the Octoprint plugin and an arduino based hardware controller. The controller and the plugin communicate through a serial connection using a simple byte-based protocol. As OctoRemote is based on Octoprint it is totally printer independent and works easily with any Octorprint compatible printer. At the moment following printer actions are implemented:

* Homing X&Y and Z
* Moving of all axis
* Extrude/Retract material
* Stop Print
* Pause Print
* Start/Resume Print
* Select Extruder
* Select movement distance (4 options)

## Setup

Install via the bundled [Plugin Manager](https://github.com/foosel/OctoPrint/wiki/Plugin:-Plugin-Manager)
or manually using this URL:

    https://github.com/pkElectronics/OctoPrint-Octoremote/archive/master.zip

The plugin repository also contains the source code of the Arduino program which is necessary for the hardware controller. Installation if described in detail in the Hardware section.

## Configuration

**TODO:** Describe your plugin's configuration options (if any).

## Hardware

There are two possible hardware configurations available, a simple breadboard version using an Arduino UNO, a 4x4 matrix keypad and 8 leds. 

![Alt text](/doku/Fritzing.PNG)

Of course you could build the circuit in a different way, you just have to change the pin assignments in the software.

If you stick to the recommended schematic you will end up with a key assignment like this:

![Alt text](/doku/Keypad.PNG)

In the future there will also be a custom made PCB which includes all necessary parts and uses cherry mx switches for the keys. The device will still be compatible with the Arduino IDE for easy upgrading and hacking. Development of the PCB has not yet started but is scheduled for mid of april.

Regardless of the type of the used hardware, programming is done using the Arduino IDE and the sourcecodes from the arduino/OctoRemote/ folder.
