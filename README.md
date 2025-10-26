# Portable 432MHz (70cm) EME Yagi Array

**A lightweight, tool-less, single-person-portable 2x2x14-element Yagi array for 432 MHz EME operations.**

---

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
* 3D Printer (All required `.step` files are available in the [`/CAD/3d_print`](/CAD/3d_print) directory)

**A note on 3D Printers:** We understand that not everyone owns a 3D printer. However:
1.  The accessibility and affordability of a home 3D printer are significantly higher than that of a home CNC machine.
2.  Even if you don't own one, using a 3D printing service is vastly more cost-effective and accessible than commissioning CNC machined parts.

## Technical Specifications

* **Band:** 432 MHz (70cm)
* **Array Configuration:** 2x2x14-element Yagi array (Four 14-element Yagis stacked in a 2x2 grid).
* **Polarization:** Horizontal.
* **Stacking Frame:** Custom H-frame.

## Design Details

### H-Frame Stacking System

The H-frame used to stack the four Yagis is designed for tool-less, rapid deployment. Its design is inspired by the folding leg mechanism of a portable table. This concept allows the frame to be deployed and locked into place, or unlocked and folded for storage, in seconds.

*The initial idea for this folding H-frame concept came from **BI1QGX**.*

### Modified 14-Element Yagi

The basic design of the 14-element Yagi is based on the **GTV 70-14m by DG7YBN**.

However, this project introduces significant modifications to the original design to optimize it for portability and rapid assembly. These optimizations include:
* Redesigned boom segments.
* Modified element brackets.
* A new feedbox design.

These changes make the antenna elements easier to pack and quicker to assemble in the field without sacrificing performance.

## Repository Contents

All design files are located in the `/CAD` directory.

* [`/CAD/3d_print`](/CAD/3d_print): Contains all `.step` files for parts that need to be 3D printed (e.g., jigs, brackets, feedbox parts).
* [`/CAD/aluminum_pipe`](/CAD/aluminum_pipe): Contains `.step` files for the aluminum components (boom sections, stacking frame parts) for reference and dimensioning.
* `LICENSE`: The project's open-source license.
* `README.md`: This file.

## Project Status

* **Available Now:**
    * Initial 3D CAD files (`.step`) for all 3D printed parts and aluminum components are available in the `/CAD` directory.
* **To Be Added:**
    * Complete Bill of Materials (BOM) (e.g., specific aluminum pipe sizes, screws, rivets).
    * Detailed Assembly Instructions & Photos/Videos.
    * Simulation Files (e.g., EZNEC/4nec2).
    * Print-ready `.stl` files (recommended).

## Acknowledgements

* **DG7YBN** for the original GTV 70-14m antenna design.
* **BI1QGX** for the foundational concept of the folding H-frame.


## License

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
