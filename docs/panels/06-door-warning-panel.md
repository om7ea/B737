# 6. Door Warning Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3163604-boeing-737-overhead-door-warning-panel)

[← Back to panel list](README.md)

---

## Photos

<img src="../../images/panels/06-door-warning-photo-1-front.jpg" alt="Finished Door Warning Panel, front" width="700">

*Finished panel*

<img src="../../images/panels/06-door-warning-photo-2-rear.jpg" alt="Rear of the panel with the two PCBs" width="700">

*Rear side — the two PCBs and wiring*

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/dark-gray.svg" width="12" height="12"> | Dark Gray | C-Tech Premium Line PLA RAL7011 |
| <img src="../../images/icons/black.svg" width="12" height="12"> | Black | Bambu PLA Basic Black (10101) |

---

## 3D Printed Parts

| Qty | Part | Notes |
|---:|---|---|
| 1× | Bottom panel | print on a **Textured** PEI plate |
| 1× | Backlight panel | carries the PCBs — this panel is not backlit, see [Backlight](#backlight) |
| 2× | PCB frame | |
| 4× | M4 washer | |
| 4× | Standoff 16 mm | |

---

## Switches and Buttons

None — this panel carries annunciators only.

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 4× | Flat head M3×12 | bottom + standoff |
| 4× | Flat head M4×16 | bottom + main frame |
| 4× | Dome head M3×5 | PCB + backlight |
| 4× | Dome head M3×8 | backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 12× | Black background, yellow LED |

The annunciators are a separate model shared with the other panels — they are **not included** in this download.

| | |
|---|---|
| 📦 Printable model | [Boeing 737 Overhead - Annunciators](https://makerworld.com/en/models/3121595-boeing-737-overhead-annunciators) |
| 🔧 Build notes | [Annunciators](02-annunciators.md) |
| 🔌 PCB, BOM and wiring | [Annunciator PCB](../pcb/annunciator.md) |

---

## PCB

| Qty | PCB | Connections used | Gerber files |
|---:|---|---|---|
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–8 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–4 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |

Mounting is shown in [step 2](#2-backlight-panel--pcbs) of the assembly diagram.

---

## Backlight

**This panel is not backlit.** It has no LED strips and no DC jack.

The printed part is still called *backlight panel* to keep the naming consistent with the other panels — here it only carries the two PCBs.

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Bottom panel — annunciators and standoffs

<img src="../../images/panels/06-door-warning-01-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 2. Backlight panel — PCBs

<img src="../../images/panels/06-door-warning-02-backlight-pcb.png" alt="PCB mounting on the backlight panel" width="700">
