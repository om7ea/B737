# 15. PSEU Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3223471-boeing-737-overhead-pseu-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/15-pseu-photo-1-front-v2.jpg" alt="Finished PSEU Panel, front, with the INDEX TO LOCK plate"><br><sub>Finished panel - the index plate is Black with the lettering in Jade White</sub></td>
<td align="center" width="50%"><img src="../../images/panels/15-pseu-photo-2-rear.jpg" alt="Rear of the panel with the annunciator"><br><sub>Rear side - the annunciator and its cable</sub></td>
</tr>
</tbody>
</table>

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/dark-gray.svg" width="12" height="12"> | Dark Gray | C-Tech Premium Line PLA RAL7011 |
| <img src="../../images/icons/white.svg" width="12" height="12"> | White | Bambu PLA Basic Jade White (10100) |
| <img src="../../images/icons/black.svg" width="12" height="12"> | Black | Bambu PLA Basic Black (10101) |

---

## 3D Printed Parts

| Qty | Part | Notes |
|---:|---|---|
| 1× | Bottom panel | print on a **Textured** PEI plate |
| 1× | Index plate | the INDEX TO LOCK plate; print on a **Textured** PEI plate |
| 1× | Flat washer | goes under the screw that holds the index plate |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 1× | Dome head M4×8 | index plate + bottom |
| 5× | Dome head M4×10 | bottom + main frame |

---

## Annunciators

| Qty | Type |
|---:|---|
| 1× | Black background, yellow LED |

The annunciators are a separate model shared with the other panels - they are **not included** in this download.

| | |
|---|---|
| 📦 Printable model | [Boeing 737 Overhead - Annunciators](https://makerworld.com/en/models/3121595-boeing-737-overhead-annunciators) |
| 🔧 Build notes | [Annunciators](02-annunciators.md) |
| 🔌 PCB, BOM and wiring | [Annunciator PCB](../pcb/annunciator.md) |

---

## Wiring

This panel has no PCB and no patch cable of its own. Its single annunciator is wired across to a PCB on the **[LE Devices and ELT Panel](17-le-devices-and-elt-panel.md)**, where it takes header **4** - that PCB's cable goes to socket **D0** on **Overhead_1a**.

The ZH cable to the annunciator comes from that panel, so nothing here connects to a MEGA 2560 directly.

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **DH** = dome head.

### 1. Annunciator and index plate

<img src="../../images/panels/15-pseu-01-annunciator-and-index-plate.png" alt="Annunciator fitted into the panel and the index plate screwed on with the flat washer" width="700">

### 2. Mounting to the main frame

<img src="../../images/panels/15-pseu-02-main-frame.png" alt="Panel screwed to the main frame" width="700">
