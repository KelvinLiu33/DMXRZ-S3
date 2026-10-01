# DMXRZ-S3

Portable DMX512/RDM field controller. This repository holds the hardware drawings and the English user guides.

Hardware drawings in this repository are revision **1.5 (2026-09-13)**.

| Path | What it is |
|------|------------|
| [hardware/](hardware/) | Schematic and assembly BOM |
| [guides/DMXRZ-S3-main-screens-en.pdf](guides/DMXRZ-S3-main-screens-en.pdf) | English screen manual. Home, then the second, third, and fourth menu levels |
| [guides/DMXRZ-S3-web-console-en.pdf](guides/DMXRZ-S3-web-console-en.pdf) | English web console manual. Wi-Fi, the scan-in steps, and each web page |

The battery installed in shipping units is a 604050 cell, 1500 mAh. USB-C runs the unit and charges that battery. While the cell is charging, the screen shows **Charging**. It does not show a percentage or the battery bars. Those return when charging stops.

Art-Net is one universe. In the console, set the destination to the unit's IP address. Do not use a `.255` broadcast address. Universe 1 on the unit is Universe 0 in the console. Turn Color Test off before the console should drive the output.

Signed firmware is published on the Releases page when a build is ready.
