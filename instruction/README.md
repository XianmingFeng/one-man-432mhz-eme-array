# Antenna Fabrication and Assembly Guide

## 1. Introduction

This document provides a step-by-step guide for fabricating and assembling all components for the Portable 432MHz EME Yagi Array.

**Critical Note:** Please follow these steps in the specified order. Some steps (like 3D printing) are required to create tools (jigs) needed for later steps (like aluminum machining).

For a complete Bill of Materials (BOM), please refer to the main [README.md](/README.md) file.

---

## 2. Required Tools

Before starting, ensure you have the following basic tools:

* 3D Printer
* Hand drill (pistol drill) or drill press
* Hand saw (for aluminum)
* Manual rivet gun
* Soldering iron (for installing heat-set inserts)
* Hex key (Allen wrench) set (M3)
* Wire stripper / Coax cable cutter
* Crimping tool (for RNB-1.25-4 lugs)
* Vector Network Analyzer (VNA) (Highly Recommended for verifying coax length)
* Permanent marker

---

## 3. Part 1: Component Fabrication

This section covers the creation of all custom parts from raw materials.

### Step 3.1: 3D Printing

This is the **first** fabrication step. The 3D-printed parts, especially the drilling jigs, are required for the aluminum machining.

1.  Navigate to the `/CAD/3d_print/` directory.
2.  Read the general printing guidelines in the main `README.md`.
3.  **Crucially**, read the specific `README.md` file *inside each subdirectory* (e.g., `feed_box/`, `element_mount/`, `drilling_jig/`) before printing. These files contain essential instructions on print orientation, supports, and required hardware.
4.  Print all required parts, paying special attention to the parts in the `drilling_jig/` directory, which are needed for Step 3.2.

> **IMPORTANT:** Failure to print the `drilling_jig` parts first will make accurate manual machining of the aluminum tubes extremely difficult.

### Step 3.2: Aluminum Machining

This step involves cutting and drilling all aluminum components for the elements, booms, and H-frame.

#### 3.2.1. Yagi Elements (Reflector & Directors)

Cut the parasitic elements (8mm diameter tubes) to their **full "Final BC Length"** specified in the table below. The "Drilling Midpoint" column indicates the **midpoint (center) of the element**, which is where you must drill the mounting hole.

Use the `element_drill_jig.step` (from the `../3d_print/drilling_jig/` directory) to ensure the hole is drilled precisely at the center. You will need to make 4 identical sets.

| Element | Qty (per Yagi) | Diam (mm) | **Cut Full Length (mm)** (Final BC Length) | **Drilling Midpoint (mm)** (Half L) |
|:---|:---|:---|:---|:---|
| Refl | 1 | 8 | 330.7 | 165.35 |
| D1 | 1 | 8 | 311.7 | 155.85 |
| D2 | 1 | 8 | 306.7 | 153.35 |
| D3 | 1 | 8 | 294.7 | 147.35 |
| D4 | 1 | 8 | 288.7 | 144.35 |
| D5 | 1 | 8 | 284.7 | 142.35 |
| D6 | 1 | 8 | 281.7 | 140.85 |
| D7 | 1 | 8 | 277.2 | 138.6 |
| D8 | 1 | 8 | 273.7 | 136.85 |
| D9 | 1 | 8 | 270.7 | 135.35 |
| D10 | 1 | 8 | 268.7 | 134.35 |
| D11 | 1 | 8 | 266.7 | 133.35 |
| D12 | 1 | 8 | 258.7 | 129.35 |

*Note: The Driven Element (DE) is a 10mm tube and is prepared as part of the Feed Box assembly (Part 5.1).*

#### 3.2.2. Yagi Booms & H-Frame

Machine the aluminum square tubes for the Yagi booms and the H-frame according to the `.step` files in the `/CAD/aluminum_pipe/` directory.

**Manufacturing Recommendations:**
* **Manual (DIY):** Cut parts with a hand saw and use a drill press. It is **ESSENTIAL** to use the 3D-printed jigs from the `/CAD/3d_print/drilling_jig/` directory (e.g., `hinge_drill_jig.step`, `mast_drill_jig.step`) for all hinge and alignment holes.
* **Professional (CNC):** The `.step` files are CAM-ready and can be sent directly to a machining service for laser cutting or CNC milling.

**Machining Summary:**

| Module | Part File(s) | Material | Qty | Key Machining Notes |
|:---|:---|:---|:---|:---|
| **Yagi Booms** | `yagi_boom_front.step`<br>`yagi_boom_middle.step`<br>`yagi_boom_rear.step` | 20x20x1mm Square Tube | 4 of each<br>(12 total) | • Cut to length as per STEP file.<br>• Drill element holes.<br>• **Critical:** Use `hinge_drill_jig.step` for all hinge/latch holes at the ends. |
| **H-Frame** | `stacking_vertical_mast.step` | 25x25x1mm Square Tube | 4 | • Forms the two vertical legs.<br>• **Critical:** Use `mast_drill_jig.step` for hinge holes. |
| **H-Frame** | `stacking_horizontal_spreader.step` | 30x30x1mm Square Tube | 1 | • The central horizontal spine.<br>• **Critical:** Use `spreader_drill_jig.step` for hinge holes. |
| **Adapters** | `boom_sleeve.step` | 25x25x2.5mm Square Tube | 8 | • Adapts 20mm boom to 25mm T-connector.<br>• **Manufacture:** Cut tube in half *lengthwise*. Low precision required. |

---

## 4. Part 2: Component Preparation

This section covers the preparation of off-the-shelf components before final assembly.

### Step 4.1: Coaxial Feedlines

Each of the four Yagis requires a 3/4 wavelength ($3/4 \lambda$) coaxial feedline (balun).

1.  **Verify Velocity Factor (VF):** The VF for SVY-50-3 coax is approximately **0.66**. For best results, use a VNA to measure the precise VF of your specific coax cable.
2.  **Calculate Length:** The formula is: $(\text{Wavelength} \times 0.75) \times \text{VF}$.
    * Example calculation: $(69.4 \text{ cm} \times 0.75) \times 0.66 = \mathbf{34.353 \text{ cm}}$
3.  **Cut Cables:** Cut **4** identical lengths of SVY-50-3 coax based on your calculation.
4.  **Prepare Ends (One Side):** On *one end* of each of the 4 cables:
    * Strip back ~1.5 cm of the outer jacket to expose the shield.
    * Carefully push the braided shield back, exposing the inner dielectric.
    * Strip back ~0.5 - 1 cm of the dielectric to expose the center core.
    * Twist the braided shield neatly into a single "pigtail."
5.  **Crimp Lugs:**
    * Crimp one **RNB-1.25-4** copper lug onto the center core.
    * Crimp one **RNB-1.25-4** copper lug onto the twisted shield pigtail.
    * You now have 4 coax cables, each with one end terminated in two lugs.

---

## 5. Part 3: Sub-Assembly

This section covers the assembly of the main modules.

### Step 5.1: Feed Box & Driven Element Assembly

This is a critical step that requires careful attention to detail. You will be building **two pairs** of mirrored feed boxes.

> **CRITICAL WARNING: Symmetrical Assembly Required**
>
> Because two Yagis mount "right-side up" and two mount "upside down" on the H-frame, you **MUST** build two "standard" feed boxes and two "mirrored" (symmetrical) feed boxes.
>
> If all four feed boxes are identical, two antennas will be 180° out of phase, and the array will **NOT** work.

To be clear, you must build two of each configuration shown below:

| Assembly Type | Quantity to Build | Wiring Configuration |
|:---|:---|:---|
| **"Standard" (L)** | 2 | **Center Core** $\rightarrow$ **Left** DE Half<br>**Shield** $\rightarrow$ **Right** DE Half |
| **"Mirrored" (R)** | 2 | **Center Core** $\rightarrow$ **Right** DE Half<br>**Shield** $\rightarrow$ **Left** DE Half |

#### Assembly Process:

1.  **Install Heat-Set Inserts:** Using a soldering iron, melt **M3x4x5** brass inserts into:
    * The bottom and both sides of the T-shaped `feed_box_middle` part.
    * The corresponding holes in the `feed_box_front` and `feed_box_rear` covers.
2.  **Install Center Bolt:**
    * Take one **M3x40** socket head cap screw.
    * Screw it down *from the top* of the T-part (`feed_box_middle`).
    * Thread it *through* the heat-set insert at the bottom of the T-part.
    * Tighten this screw firmly. It should be locked in place by the insert and not rotate.
3.  **Install Driven Element (DE):**
    * Insert the bent 10mm diameter aluminum tube (the Driven Element) into the T-part.
    * **CRITICAL ALIGNMENT:** Rotate the DE so that the *direction of its bend* is the *same* as the direction of the heat-set inserts on the sides of the T-part.
4.  **Connect Feedline:**
    * Take one of the prepared coax cables from Step 4.1.
    * Use two **M3x8** button head screws.
    * Feed the screws from the *opposite side* of the side-inserts (i.e., from the "inside" of the T-part).
    * Pass the screws through the holes in the Driven Element.
    * Attach the two crimped lugs (Core and Shield) to the screws.
5.  **FINAL CHECK (Standard vs. Mirrored):**
    * **For 2 assemblies:** Attach the **Center Core** lug to the **Left** DE half and the **Shield** lug to the **Right** DE half.
    * **For the other 2 assemblies:** Attach the **Center Core** lug to the **Right** DE half and the **Shield** lug to the **Left** DE half.
6.  **Mark Assemblies:** Use a permanent marker to clearly label the "Standard" and "Mirrored" assemblies (e.g., "L" and "R") so you do not mix them up during final assembly.

---

*(Tutorial sections below will be added based on future information)*

### Step 5.2: Yagi Boom Assembly (Hinges & Mounts)

*(Instructions for attaching hinges, latches, and 3D-printed caps to the boom sections to be added here.)*

### Step 5.3: Parasitic Element Installation

*(Instructions for attaching the 52 `element_mount` parts and the elements to the booms to be added here.)*

---

## 6. Part 4: Final Assembly

### Step 6.1: H-Frame Assembly

*(Instructions for assembling the vertical and horizontal H-frame parts with the 90-degree folding hinges to be added here.)*

### Step 6.2: Mounting Yagis to H-Frame

*(Instructions for mounting the four Yagi assemblies to the H-frame quick-release connectors to be added here.)*

### Step 6.3: Connecting Phasing Lines

*(Instructions for connecting the four feed boxes to the power divider/phasing harness to be added here.)*