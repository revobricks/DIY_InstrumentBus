# DIB version 1.3

## Introduction
This is a further development on the DIB v1.2 specifications. The DIB v1.3 is (mostly) backward compatible with v1.2 devices. Particular, DIB v1.2 modules like PSUs ect. can be reused. Most important changes:
1. A CE and FCC conform AC/DC power supply, similiar to a ATX PSU. This allows non-high voltages trained persons to mount or replace this part, or to build kits. 
2. The DIB modules can be either controlled by the MCU board, or a standard Raspberry Pi 4 or 5. Each slot can be independently connect either to the MCU or the RasPi.
3. Introducing "slot select" signals, replacing the A0/A1/A3 coding bus.
4. Introducing USB direct to the DIB modules, adding a USB Hub to the main board. This simpifies the porting for existing projects, what uses a USBTME bus already.
5. Introducing a CAN-FD bus to the DIB modules. This allows a bidirectional communication, a trigger bus, module-to-module communication and hardware packet filtering.
7. Adding a second fan, so that one fan cool the PSU, and the second fan cool the DIB modules.
8. Introducing a CAN and CAN-FD connector for external instruments, with a RJ11-4pin connector. Up to 127 external devices or instruments can be connected in a daisy-chain cabling. 

Otherwise, all DIB v1.2 specifications all valid.

## Background
Parts of the DIB community develop into a different direction, the DIB-2 development. This branch development brakes backwared compatibility, introduces non-DIY friendly parts like PCB-connectors what require hard-gold plating, PCIe bus, and so on. So the DIB v1.3 will come to rescue with backwards-compatibility to 1.2, DIY friendly parts. 
