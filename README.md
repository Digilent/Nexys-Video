# Nexys Video Root Repository

## Nexys Video DMA Audio Demo

### Description

This branch contains sources for the Nexys Video DMA Audio Demo.

This project demonstrates how to use the Nexys Video's Audio Codec and RAM to record samples of audio and play them back.
Vivado is used to build the demo's hardware platform, and Vitis is used to program the bitstream onto the board and to build and deploy a C application.

To use this demo, the Nexys Video must be connected to a computer over MicroUSB, which must be running a serial terminal such as Tera Term or PuTTY.

The audio demo records a 5 second sample from the microphone input (J6) or line in (J7) and plays it back on the headphone output (J4) or line out (J5).
Recording and playback are controlled by the user push buttons, as in the table below:

|  Button  | Function              |
| -------- | --------------------- |
|  BTNL    |  play on line out     |
|  BTNU    |  record from mic in   |
|  BTND    |  play on hph out      |
|  BTNR    |  record from line in  |

For more information on the Nexys Video DMA Audio Demo, including setup instructions, visit its [Demo Page](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/demos/dma-audio) on the Digilent Wiki.

For more information on the Nexys Video, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/start) on the Digilent Wiki.

### Git Navigation Information

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki.
Note that use of git is not required to use this demo.
Digilent recommends the use of project releases, for which instructions can be found in each demo wiki page, linked above.

To see other demos in this repository, see the master branch's [README](https://github.com/Digilent/Nexys-Video).

Some demos do not require some submodules, in these cases, they are still provided to ease switching between demos in git.
When unused, the submodule folder is largely empty, except for a readme containing only the heading "Root commit".
This demo contains the following submodules:

| Submodule | Used by this demo |
|-----------|-------------------|
| HW        | Yes               |
| SW        | Yes               |

This demo was moved into this repository during 2020.1 updates.
Its history prior to these updates can be found in its old repository, linked below:
* https://github.com/Digilent/Nexys-Video-DMA

### Requirements

The following are required for use of this demo.
For more information on how to get any hardware or software you may be missing, see the Demo Page, linked above.

* Nexys Video
* Vivado and Vitis 2021.1 Installations
* Serial Terminal Emulator
* MicroUSB Cables for serial communication and programming
* Audio sink and source, such as audio cables and a computer, microphone, and/or speakers
