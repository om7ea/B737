# 16. Landing Gear Indicator Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3223506-boeing-737-overhead-landing-gear-indicator-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/16-landing-gear-photo-1-front.jpg" alt="Finished Landing Gear Indicator Panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/16-landing-gear-photo-2-rear.jpg" alt="Rear of the panel with the three annunciators"><br><sub>Rear side - the three annunciators and their cables</sub></td>
</tr>
</tbody>
</table>

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/dark-gray.svg" width="12" height="12"> | Dark Gray | C-Tech Premium Line PLA RAL7011 |

---

## 3D Printed Parts

| Qty | Part | Notes |
|---:|---|---|
| 1× | Bottom panel | print on a **Textured** PEI plate |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 5× | Dome head M4×10 | bottom + main frame |

---

## Annunciators

| Qty | Type |
|---:|---|
| 3× | Black background, green LED |

The annunciators are a separate model shared with the other panels - they are **not included** in this download.

| | |
|---|---|
| 📦 Printable model | [Boeing 737 Overhead - Annunciators](https://makerworld.com/en/models/3121595-boeing-737-overhead-annunciators) |
| 🔧 Build notes | [Annunciators](02-annunciators.md) |
| 🔌 PCB, BOM and wiring | [Annunciator PCB](../pcb/annunciator.md) |

---

## Wiring

This panel has no PCB and no patch cable of its own. All three annunciators are wired across to a PCB on the **Engine and Oxygen Panel**, whose cable goes to socket **D3** on **Overhead_2a**.

| Header | Annunciator |
|---:|---|
| 1 | RIGHT GEAR |
| 7 | LEFT GEAR |
| 8 | NOSE GEAR |

The remaining headers of that board serve the Engine and Oxygen Panel itself. The ZH cables to the annunciators come from there, so nothing here connects to a MEGA 2560 directly.

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **DH** = dome head.

### 1. Annunciators

<img src="../../images/panels/16-landing-gear-01-annunciators.png" alt="Annunciators fitted into the panel" width="700">

### 2. Mounting to the main frame

<img src="../../images/panels/16-landing-gear-02-main-frame.png" alt="Panel screwed to the main frame" width="700">
