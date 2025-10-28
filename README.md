# Portable 432MHz (70cm) EME Yagi Array

**A lightweight, tool-less, single-person-portable 2x2x14-element Yagi array for 432 MHz EME operations.**

---

[中文](/README_zh.md) | [Deutsche](/README_de.md) | [日本語](/README_ja.md)

## Overview

This project provides an open-source design for a 432 MHz (70cm) EME (Earth-Moon-Earth) antenna array. 

The motivation for this design stems from a personal need: the inability to install permanent antennas at home required all amateur radio equipment to be designed around portability. This antenna system is the solution for operators who must travel to the field to get on the air.

While traditional EME arrays are often large and permanently installed, this design focuses on achieving the minimum required gain for EME while prioritizing **portability, light weight, and rapid, single-person operation.**

## Proven Field Use & Air Travel

This system is not just a concept. Its usability was successfully confirmed during the **VK9QO Christmas Island DXpedition in 2025**.

The entire system is compliant with air travel requirements and can be checked as luggage. This makes it an ideal and proven solution for "Rovers" and DXpeditioners who wish to carry high-gain equipment to remote or rare DXCC entities to conduct EME operations.

## Key Features

* **Single-Person Portability:** The total weight of the entire array system, including the carrying bag, is **under 10 kg**.
* **Compact Storage:** All components are designed to be stored in a single fishing rod bag, making it easy for one person to carry.
* **Tool-less Assembly:** No tools (screwdrivers, wrenches, etc.) are required for field setup or teardown. The entire process can be completed by hand.
* **Rapid Deployment & Takedown:** The design is optimized for speed. This is achieved by:
    * Minimizing the number of loose parts.
    * Keeping most components connected as a single unit during storage.
    * Utilizing a simple "unfold-and-lock" and "unlock-and-fold" mechanism for deployment and retraction.

## Design Philosophy: Accessibility & Low Cost

A primary goal of this project is to enable anyone to easily build this antenna system. The design intentionally avoids complex machining processes (like CNC milling) to lower the barrier to entry.

Builders should be able to complete the entire antenna with only the most basic tools:
* Hand drill (pistol drill)
* Hand saw
* Manual rivet gun
* Pipe bender
* 3D Printer (All required `.step` files are available in the [`/CAD/3d_print`](/CAD/3d_print) directory)

**A note on 3D Printers:** We understand that not everyone owns a 3D printer. However:
1.  The accessibility and affordability of a home 3D printer are significantly higher than that of a home CNC machine.
2.  Even if you don't own one, using a 3D printing service is vastly more cost-effective and accessible than commissioning CNC machined parts.

## 3D Printing Guidelines

All 3D printed parts are located in the `/CAD/3d_print` directory.

### General Recommendations
Most parts function as mechanical components and are under moderate stress. The following general settings are recommended for strength and durability:

* **Material:** PETG (or ABS/ASA for better weather/UV resistance)
* **Layer Height:** 0.2mm
* **Wall Thickness:** 4 Layers
* **Infill Density:** 25% (or higher)
* **Infill Pattern:** Cross Hatch / Gyroid / or similar strong pattern

### **Critical Instructions**
**Each 3D print part subdirectory (e.g., `/CAD/3d_print/feed_box/`, `/CAD/3d_print/element_mount/`) now contains its own detailed, multi-lingual `README.md` file.**

You **MUST** read the specific `README.md` file in each part's directory before printing. These files contain essential, part-specific instructions for:
* Print Orientation
* Support settings (e.g., which parts require supports and which must not have them)
* Part-specific hardware (like heat-set inserts)

Failure to follow these part-specific instructions may result in parts that do not fit or function correctly.

## Technical Specifications

* **Band:** 432 MHz (70cm)
* **Array Configuration:** 2x2x14-element Yagi array (Four 14-element Yagis stacked in a 2x2 grid).
* **Polarization:** Horizontal.
* **Stacking Frame:** Custom H-frame.

### Theoretical Performance (Simulated)

**Single 14-el Yagi:**
* **Gain:** 16.38 dBi
* **Front-to-Back Ratio:** 33.02 dB
* **3dB Beamwidth (Horizontal):** 30.8°
* **3dB Beamwidth (Vertical):** 29.2°

**Full 2x2 Array:**
* **Gain:** 22.32 dBi
* **Front-to-Back Ratio:** 33.29 dB
* **3dB Beamwidth (Horizontal):** 14°
* **3dB Beamwidth (Vertical):** 13.2°
* **Antenna Temperature ($T_{ant}$):** 74.3 K
* **G/T Ratio:** 3.6 dB
> *Performance figures ($T_{ant}$, G/T) calculated assuming $T_{sky}$ = 27 K and $T_{earth}$ = 1800 K.*

## Mounting System (Tripod)

The array system is designed to be mounted on a standard tripod. The connection is made using the 3D printed part **`spearder_mount`** (files available in `/CAD/3d_print`).

This mount connects the array's H-frame to a tripod head's quick-release (QR) plate.

**Quick-Release Plate Requirements:**
The `spearder_mount` part is designed to be versatile. It is compatible with any long-slot style QR plate that meets these criteria:
* **Length:** Greater than 80mm.
* **Mounting:** Uses a long slot for the bolt (not a single fixed-position hole).
* **Bolt:** Compatible with a standard 1/4" (imperial) tripod bolt.

*As an example, the author uses a 38mm wide Arca-Swiss style QR plate paired with a fluid video head.*

**Tripod Recommendation:**
It is highly recommended to use a tripod with a **minimum height of 1.8 meters (approx. 6 feet)**.

* **Reason:** A tripod that is too short will cause the tail end of the antenna array to hit or drag on the ground when rotating to high elevation angles (e.g., tracking the moon).

## Design Details

### H-Frame Stacking System

The H-frame used to stack the four Yagis is designed for tool-less, rapid deployment. Its design is inspired by the folding leg mechanism of a portable table. This concept allows the frame to be deployed and locked into place, or unlocked and folded for storage, in seconds.

*The initial idea for this folding H-frame concept came from **BI1QGX**.*

### Modified 14-Element Yagi

The basic design of the 14-element Yagi is based on the **[GTV 70-14m by DG7YBN](https://dg7ybn.de/432MHz/GTV70_14.htm)**.
#### Electrical Design & Boom Correction

The electrical design adopts the data from DG7YBN and applies a Boom Correction (BC) factor to compensate for the effects of the conductive 20x20x1mm square aluminum boom. The elements are mounted 5mm above the boom (distance from the element's bottom to the boom's top surface).

The table below shows the original NEC free-space length (FL NEC), the final boom-corrected length (BC), and the required half-length (Half L) for element construction.

| \[mm\] | Diam | Pos Boom | FL NEC | BC    | Half L |
|:-------|:-----|:---------|:-------|:------|:-------|
| Refl   | 8    | 40       | 328    | 330.7 | 165.35 |
| DE     | 10   | 144.5    | 313.4  | 316.1 | 158.05 |
| D1     | 8    | 193      | 309    | 311.7 | 155.85 |
| D2     | 8    | 286      | 304    | 306.7 | 153.35 |
| D3     | 8    | 468      | 292    | 294.7 | 147.35 |
| D4     | 8    | 681      | 286    | 288.7 | 144.35 |
| D5     | 8    | 928      | 282    | 284.7 | 142.35 |
| D6     | 8    | 1192     | 279    | 281.7 | 140.85 |
| D7     | 8    | 1477     | 274.5  | 277.2 | 138.6  |
| D8     | 8    | 1764     | 271    | 273.7 | 136.85 |
| D9     | 8    | 2054     | 268    | 270.7 | 135.35 |
| D10    | 8    | 2345     | 266    | 268.7 | 134.35 |
| D11    | 8    | 2627     | 264    | 266.7 | 133.35 |
| D12    | 8    | 2860     | 256    | 258.7 | 129.35 |

For a detailed explanation of the Boom Correction methodology, please visit [DG7YBN's BC page](https://dg7ybn.de/BC_numbers/BC.htm).

#### Mechanical Optimizations

In addition to the electrical design, this project introduces significant *mechanical* modifications to the original design to optimize it for portability and rapid assembly. These optimizations include:
* Redesigned boom segments and folding hinges.
* A new feedbox design.
* A specialized element mounting system (see below).

#### Element Mount (The `element_mount` part)

A key feature of this design is the 3D-printed element mount (`element_mount.step`) used for all parasitic elements (reflectors and directors).

* **Dual-Slot Design:** The part features two slots. One slot holds the element perpendicular to the boom for operation. A second slot, at a near-perpendicular angle, is used to hold the element in its folded (stowed) position.
* **Interference-Free Storage:** The "storage" slot is intentionally offset by a small angle (the `parking_angle`). This ensures that when folded, the elements do not lie perfectly parallel to the boom, preventing them from interfering with adjacent elements or the mounting bolt heads.
* **General-Purpose Parametric Design:** This element mount is a universal, general-purpose design, suitable for many Yagi projects using square booms and round elements. It has been released as its own **parametric OpenSCAD project**.

For full details, parameters (to adapt it for your own boom size, element diameter, storage angle, etc.), and `.scad` files, please see the dedicated project repository:
**[https://github.com/XianmingFeng/yagi_element_mounting](https://github.com/XianmingFeng/yagi_element_mounting)**

## Bill of Materials (BOM)

This is a partial BOM and will be updated as the project progresses.

| Category                      | Part                                                 | Qty |
|:------------------------------|:-----------------------------------------------------|:----|
| Yagi Elements & Feedbox       | `element_mount` 3D Printed Part                      | 52  |
|                               | Socket Head Cap Screw (Half-thread) M3x40            | 52  |
|                               | Wing Nut M3                                          | 56  |
|                               | `feed_box_front` 3D Printed Part                     | 4   |
|                               | `feed_box_middle` 3D Printed Part                    | 4   |
|                               | `feed_box_rear` 3D Printed Part                      | 4   |
|                               | `feed_box_isolator` 3D Printed Part                  | 4   |
|                               | Button Head Hex Socket Screw M3x8                    | 8   |
|                               | Socket Head Cap Screw M3x40                          | 4   |
|                               | Knurled Brass Nut (Heat-set Insert) M3x4x5           | 36  |
|                               | Socket Head Cap Screw M3x24                          | 28  |
|                               | Copper Terminal Lug RNB-1.25-4                       | 16  |
|                               |                                                      |     |
| Yagi Boom Folding Mechanism   | Small Double Spring Toggle Latch (No lock hole)      | 8   |
|                               | Latch Catch A320B-0-2                                | 8   |
|                               | Iron Gooseneck Hinge 20mm                            | 16  |
|                               | Round Head Blind Rivet M4x5                          | 96  |
|                               | `boom_hinge_cap_front` 3D Printed Part               | 8   |
|                               | `boom_hinge_cap_rear` 3D Printed Part                | 8   |
| Boom-to-H-Frame Quick Release | Square Tube 2-Way T-Connector 25x25                  | 4   |
|                               | Wing Bolt M6x30                                      | 4   |
|                               | Wing Nut M6                                          | 4   |
|                               | V-Spring Clip F5mm Single Pin (Hollow), L:37mm H:8mm | 4   |
|                               | Round Head Blind Rivet M5x8                          | 8   |
| H-Frame Folding Mechanism     | 90-Degree Folding Table Leg Hinge, Mini Size, Right  | 2   |
|                               | 90-Degree Folding Table Leg Hinge, Mini Size, Left   | 2   |
|                               | Round Head Blind Rivet M5x6                          | 24  |

## Repository Contents

* **`/CAD`**: Contains all 3D model files.
    * **`/CAD/3d_print`**: Contains `.step` files for all 3D printed parts. Each subdirectory (e.g., `feed_box/`, `element_mount/`) also contains a specific, multi-lingual `README.md` with detailed printing instructions. See the **3D Printing Guidelines** section above.
    * **`/CAD/aluminum_pipe`**: Contains `.step` files for all aluminum tube/pipe components, for reference and dimensioning.
* **`LICENSE`**: The project's open-source license.
* **`README.md`**: This file (English).
* **`README_zh.md`**: Chinese translation.
* **`README_de.md`**: German translation.
* **`README_ja.md`**: Japanese translation.

## Project Status

* **Available Now:**
    * Initial 3D CAD files (`.step`) for all 3D printed parts and aluminum components are available in the `/CAD` directory.
    * Detailed, part-specific printing instructions are available in each `/CAD/3d_print` subdirectory.
    * Electrical design data (element lengths and positions) are in this README.
    * A partial Bill of Materials (BOM) is now available.
* **To Be Added:**
    * Complete Bill of Materials (BOM) (e.g., specific aluminum pipe sizes, screws).
    * Detailed Assembly Instructions & Photos/Videos.
    * Simulation Files (e.g., EZNEC/4nec2).
    * Print-ready `.stl` files (recommended).
## Acknowledgements

* **DG7YBN** for the original [GTV 70-14m](https://dg7ybn.de/432MHz/GTV70_14.htm) antenna design and [Boom Correction methodology](https://dg7ybn.de/BC_numbers/BC.htm).
* **BI1QGX** for the foundational concept of the folding H-frame.

## License

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
