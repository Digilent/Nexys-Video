# Nexys Video Root Repository

## Nexys Video HDMI Demo

### Description

This branch contains sources for the Nexys Video HDMI Demo.

This project demonstrates how to use the USB-UART Bridge, HDMI Sink and HDMI Source with a Microblaze processor.
Vivado is used to build the demo's hardware platform, and Xilinx SDK is used to program the bitstream onto the board and to build and deploy a C application.
Video data streams in through the HDMI in port and out through the HDMI out port.
A UART interface is available to configure what is output through HDMI.
There are 3 display frame buffers that the user can choose to display or write to. The configuration options are shown in the table below.

The demo uses the usb-uart bridge to configure the HDMI Display , the Nexys Video must be connected to a computer over MicroUSB, which must be running a serial terminal, such as Tera Term or PuTTY.

| Option    | Function                                                                                                                  |
| --------- | ------------------------------------------------------------------------------------------------------------------------- |
| 1         | Change the resolution of the HDMI output to the monitor.                                                                  |
| 2         | Change the frame buffer index.                                                                                            |
| 3/4       | Store a test pattern in the chosen video frame buffer - color bar or blended.                                             |
| 5         | Start/Stop streaming video data from HDMI to the chosen video frame buffer.                                               |
| 6         | Change the video frame buffer that HDMI data is streamed into.                                                            |
| 7         | Invert and store the current video frame into the next video frame buffer and display it.                                 |
| 8         | Scale the current video frame to the display resolution, store it into the next video frame buffer, and then display it.  |

NOTE: The drawing functions (Functions 3, 4, 7, and 8) were designed for the Zynq processor. In its current state, these functions run VERY slowly on the Microblaze processor, so it is advised not to use these functions for the time being. It is possible that the floating point calculations are slowing these functions down. 

For more information on the Nexys Video HDMI Demo, including setup instructions, visit its [Demo Page](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/demos/hdmi) on the Digilent Wiki.

For more information on the Nexys Video, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/start) on the Digilent Wiki.

### Git Navigation Information

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki. Note that use of git is not required to use this demo. Digilent recommends the use of project releases, for which instructions can be found in each demo wiki page, linked above.

To see other demos in this repository, see the master branch's [README](https://github.com/Digilent/Nexys-Video).

Some demos do not require some submodules, in these cases, they are still provided to ease switching between demos in git. When unused, the submodule folder is largely empty, except for a readme containing only the heading "Root commit". This demo contains the following submodules:

| Submodule | Used by this demo |
|-----------|-------------------|
| HW        | Yes               |
| SW        | Yes               |

This demo was moved into this repository during 2020.1 updates. Its history prior to these updates can be found in its old repository, linked below:
* https://github.com/Digilent/Nexys-Video-HDMI

### Requirements

The following are required for use of this demo. For more information on how to get any hardware or software you may be missing, see the Demo Page, linked above.

* Nexys Video
* Vivado and Vitis 2022.1 installations with Digilent's board files
* Serial Terminal
* MicroUSB Cables for programming and serial communication
* HDMI source (likely a computer)
* HDMI sink (monitor or TV)
* 2 HDMI cables