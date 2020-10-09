# Nexys Video Root Repository

## Nexys Video GPIO Demo

### Description

This branch contains sources for the Nexys Video GPIO Demo.

This project is a Vivado demo using the Nexys Video's switches, LEDs, pushbuttons, onboard OLED display and USB UART bridge, written in VHDL and Verilog. When programmed onto the board, all eight of the switches are tied to their corresponding LEDs. Every time a switch is toggled, the LED directly above it will toggle with it. On startup the onboard OLED will display the full alphabet and numbers 0-9. After a second of displaying the alphabet/numbers the OLED will turn off for a second and then display the message “This is Digilent's Nexys Video”. 

To use the USB-UART bridge feature of this demo, the Nexys Video must be connected to a serial terminal on the computer it is connected to over the MicroUSB cable. Whenever the reset button or BTNC is pressed, the Nexys Video sends the line “Nexys Video GPIO/UART DEMO!” to the serial terminal. Whenever one of the D-pad buttons other than BTNC is pressed, the line “Button press detected!” is sent.

For more information on the Nexys Video GPIO Demo, including setup instructions, visit its [Demo Page](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/demos/gpio) on the Digilent Wiki.

For more information on the Nexys Video, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/start) on the Digilent Wiki.

### Git Navigation Information

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki. Note that use of git is not required to use this demo. Digilent recommends the use of project releases, for which instructions can be found in each demo wiki page, linked above.

To see other demos in this repository, see the master branch's [README](https://github.com/Digilent/Nexys-Video).

Some demos do not require some submodules, in these cases, they are still provided to ease switching between demos in git. When unused, the submodule folder is largely empty, except for a readme containing only the heading "Root commit". This demo contains the following submodules:

| Submodule | Used by this demo |
|-----------|-------------------|
| HW        | Yes         |
| SW        | No         |

This demo was moved into this repository during 2020.1 updates. Its history prior to these updates can be found in its old repository, linked below:
* https://github.com/Digilent/Nexys-Video-GPIO

### Requirements

The following are required for use of this demo. For more information on how to get any hardware or software you may be missing, see the Demo Page, linked above.

* Nexys Video
* Vivado 2020.1 Installation
* MicroUSB Cable
* Serial Terminal Emulator
* Monitor with VGA Port
* VGA Cable
* USB Mouse
