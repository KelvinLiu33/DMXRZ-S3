# DMXRZ-S3

Portable DMX512 & RDM field controller (ESP32-S3): onboard battery, 2.0″ touch UI, DMX/RDM, SM/UCS DMX IC write, RZ pixel out, and one-universe Wi-Fi Art-Net.

Get the product from Tindie — that is the supported path. This repository is for **buyers**: English guides, signed OTA firmware, and hardware reference files (schematic PDF, EasyEDA Pro project, BOM). It is **not** set up as a DIY build kit.

## Buy a unit

→ **[Portable DMX512 & RDM Field Controller — F111 Studio on Tindie](https://www.tindie.com/products/f111/portable-dmx512-rdm-field-controller/)**

## Contents

| Path | Description |
|------|-------------|
| [`hardware/DMXRZ-S3-V1.5-schematic.pdf`](hardware/DMXRZ-S3-V1.5-schematic.pdf) | Schematic (PDF, EasyEDA export) |
| [`hardware/easyeda/`](hardware/easyeda/) | EasyEDA Pro `.epro`, schematic PDF, component BOM (xlsx), interactive BOM (HTML) |
| [`guides/DMXRZ-S3-main-screens-en.pdf`](guides/DMXRZ-S3-main-screens-en.pdf) | English on-device screen manual |
| [`guides/DMXRZ-S3-web-console-en.pdf`](guides/DMXRZ-S3-web-console-en.pdf) | English web console manual |
| [`firmware/`](firmware/) | Signed OTA images + [`CHANGELOG.md`](firmware/CHANGELOG.md) |
| [`images/`](images/) | Product photos (for docs / Tindie Markdown hotlinks) |
| [`mechanical/`](mechanical/) | Enclosure / 3D-print STL (reference for buyers) |

## Firmware (OTA)

For a unit purchased from Tindie:

1. Download a **signed** `ESP32S3_DMXRDM_*.bin` from [`firmware/`](firmware/) (prefer the newest file; see [`CHANGELOG.md`](firmware/CHANGELOG.md)).
2. On the unit, open the web console → **Settings**, and upload that `.bin`.
3. Unsigned images are rejected; the unit keeps the current firmware.
4. Confirm the build under **Settings → About** (`VERSION` / `版本`).

Questions: **[kevinliu199533@gmail.com](mailto:kevinliu199533@gmail.com)**.

## Field notes

**Battery.** Shipping units use a **604050** cell, **1500 mAh**. USB-C powers the unit and charges the pack. While charging, the screen shows **Charging** (no percentage / bars until charging stops).

**Art-Net.** One universe. Unicast to the unit’s IP — do **not** use a `.255` broadcast address. Universe **1** on the unit = universe **0** in the console. Turn **Color / COLORS** test off before the console should drive the output.

## Hardware files

Schematic PDF and EasyEDA Pro project/BOM exports in [`hardware/easyeda/`](hardware/easyeda/) are published here as **reference** for the Tindie product (hardware rev **1.5**, 2026-09-13). Signed OTA firmware is in [`firmware/`](firmware/).
