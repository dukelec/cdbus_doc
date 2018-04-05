
## Preface

When we need to transmit information, it involves communication.
Communication can be roughly divided into two categories: Wired communication and wireless communication.
Wired communication, such as copying files via U disk, viewing video via HDMI, wireless communication such as mobile WiFi, brain telepathy.
Do you think that the latter is obviously not stable enough? Yes, the communication protocol introduced in the next section is for wired communication, and it is for industrial applications that require high reliability.
If you don't know much about related fields, imagine using it as an alternative to Ethernet, at least I often watch YouTube through it.



## CDBUS Protocol for Asynchronous Serial Communication -- simple, common, flexible, efficient, safe and open

### Simple:
 - The most simple protocol, it works at a glance;
 - Trivial tasks are taken over by hardware, reducing the workload of developers and CPUs, and accelerating project development;
 - With the upper layer CDNET protocol stack, it can automatically handle flow control, integrity, data fragment and etc, and can also set up multiple networks (CDNET is a compact, real-time, efficient upper layer protocol for CDBUS).

### Common:
 - CDBUS based on the most common Asynchronous Serial Communication, can be used for bus or ordinary serial communication;
 - Use standard RS-485 interface chip and circuit (This is the most used scenario, other scenarios include single-wire serial bus);
 - Backward compatible with traditional RS-485 hardware;
 - With CDNET-TUN tools, protocols such as IPv4/v6 can be supported to facilitate IoT applications and connect seamlessly to various wired and wireless networks.

### Flexible:
 - Support multi-host, concurrent read and write, broadcast, free reporting and etc;
 - Hot-swappable, for example, arm end tools can be replaced automatically.

### Efficient:
 - Basic stand-alone controller CDCTL-Bx supports 10Mbps rate (Exchange data between controller and CPU could through 20MHz SPI interface with DMA);
 - Simultaneous reading and writing: The host continuously issues commands to multiple devices, and then continuously receives responses, avoid that the delay of the command is amplified by N times the number of devices in traditional RS-485;
 - Video transmission and motion control can use a single bus to avoid complicated wiring problems (Recommended for visual processing on the camera side, video transmission is only for preview so that more video can be transmitted);
 - High synchronization: Synchronizes the operation of each node by broadcasting at the speed of light (There is no forwarding delay like EtherCAT and it avoids the complicated synchronization problems).

### Safe:
 - Use hardware controllers to avoid bus faults due to software bugs;
 - High real-time performance: Because of the guarantee of priority, you can even use the rest of your bandwidth to listen to music and watch videos while in industrial control;
 - Support multiple hosts: Host failure can be seamlessly switched to standby host, without delaying production or even avoiding accidents.

### Open:
 - The IP core is open source, you can use it freely in FPGA;
 - Open source debugging tools, libraries, and sample projects are all available.



## Demos

### RS-485 Prevent Fake Cat Invasion (Peer-to-peer network video surveillance)
<img alt="cv_demo" src="img/cv_demo.jpg" width="90%">

Full video:
 - https://youtu.be/qX5dh4wcfSk


The Raspberry Pi can output preview video and control command at the same time. We can monitor the recognition process on the PC. When problems are encountered, it is convenient to know the reason and adjust the parameters, and disconnecting the PC will not affect the demo operation.

<img alt="cv_demo" src="img/cv_demo.svg" width="100%">

The human head shape board above the Raspberry Pi is a solderless socket board for CDCTL-Bx. It uses our CDBITE connection method: Bite the module with the probe.

The demo uses CDNET-TUN to set up a standard LAN, which allows video transmission without writing any code.
And for controlling the slider, such as programming in Python via standard Socket communication, requires only 4 lines of code including the import statement, to control its movement and ensure that the command is delivered accurately.
In addition, the Raspberry Pi can access the internet at any time through the PC, and it is easy to update software and for remote control.

However, for applications where high real-time performance is required, both the PC and the MCU can use the underlying CDNET protocol stack directly, which is very convenient to use.

### Virtual Serial Port (Multiple devices on one bus)

The following methods can greatly simplify the connection of the equipments, support any protocol and do not need to modify the host software:
<img alt="virtual_serial_port" src="img/virtual_serial_port.svg" width="100%">

The demo is also based on the CDNET protocol, so controlling the motor and accessing the Internet is not a problem while the serial port is being transparently transmitted.

You can also transparently transmit serial data through pure hardware without additional software:
<img alt="transparent_transmission" src="img/transparent_transmission.svg" width="100%">



## Product List
 - CDCTL-Bx module (I<sup>2</sup>C/SPI basic type) (There are also blank modules available)
 - CDCTL-Bx-Socket (Solderless socket board)
 - CDBUS-Bridge
 - Booking: CDCTL-Hx (SPI high speed type), CDCTL-Px (Mini-PCIe type)
 - Contact Us: http://dukelec.com/en/#contact


## Data Link
 - CDBUS Protocol and IP Core: https://github.com/dukelec/cdbus_ip
 - CDCTL-Bx Datasheet: http://dukelec.com/en/download.html
 - CDNET Protocol and library: https://github.com/dukelec/cdnet
 - CDNET-TUN: https://github.com/dukelec/cdnet_tun
 - CDBUS-Bridge: https://github.com/dukelec/cdbus_bridge_fw
 - More resources: https://github.com/dukelec?tab=repositories


