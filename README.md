# Nexys Video Root Repository

## Nexys Video AXI PS/2 Keyboard Demo

### Description

This branch contains sources for the Nexys Video AXI PS/2 Keyboard Demo.

This project demonstrates how to use the Nexys Video's USB HID Host port and USB UART bridge with Microblaze.
Vivado is used to build the demo's hardware platform, and Vitis is used to program the bitstream onto the board and to build and deploy a C application.
When programmed onto the board, whenever the user presses a key on a keyboard connected to the USB HID port (J15, labeled "USB HOST"), a scan code is sent to the FPGA through a PS/2 interface.
This scan code is read, converted to ASCII and transmitted to the computer via the USB-UART bridge.
In practice, this means that keys pressed on the keyboard connected to the Nexys Video are echoed over the serial connection.

To use this demo, the Nexys Video must be connected to a computer over MicroUSB, which must be running a serial terminal such as Tera Term or PuTTY.

For more information on the Nexys Video AXI PS/2 Keyboard Demo, including setup instructions, visit its [Demo Page](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/demos/axi-ps2) on the Digilent Wiki.

For more information on the Nexys Video, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/start) on the Digilent Wiki.

### Known Issues

* Interrupting the demo's initialization sequence with key presses can result in incorrect behavior.
* Not all ASCII codes are supported by the software example.
* Only keyboards are directly supported. Other PS/2 peripherals, such as mice, require additional modifications to the software.

### Git Navigation Information

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki. Note that use of git is not required to use this demo. Digilent recommends the use of project releases, for which instructions can be found in each demo wiki page, linked above.

To see other demos in this repository, see the master branch's [README](https://github.com/Digilent/Nexys-Video).

Some demos do not require some submodules, in these cases, they are still provided to ease switching between demos in git. When unused, the submodule folder is largely empty, except for a readme containing only the heading "Root commit". This demo contains the following submodules:

| Submodule | Used by this demo |
|-----------|-------------------|
| HW        | Yes               |
| SW        | Yes               |

This demo was moved into this repository during 2020.1 updates. Its history prior to these updates can be found in its old repository, linked below:
* https://github.com/Digilent/Nexys-Video-AXI-PS2-Keyboard

### Requirements

The following are required for use of this demo. For more information on how to get any hardware or software you may be missing, see the Demo Page, linked above.

* Nexys Video
* Vivado and Vitis 2020.1 Installations
* Serial Terminal Emulator
* MicroUSB Cables for programming and serial communication
* USB Keyboard