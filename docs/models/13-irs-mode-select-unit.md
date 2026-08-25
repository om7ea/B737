# 13. IRS Mode Select Unit

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3214377-boeing-737-overhead-irs-mode-select-unit)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/13-irs-mode-select-photo-1-front.jpg" alt="Finished IRS Mode Select Unit, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/13-irs-mode-select-photo-2-top-panel.jpg" alt="Printed top panel"><br><sub>Printed top panel</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/13-irs-mode-select-photo-3-diffuser.jpg" alt="Diffuser panel and rotary switches fitted"><br><sub>Diffuser panel and rotary switches fitted, before the top panel goes on</sub></td>
<td align="center" width="50%"><img src="../../images/panels/13-irs-mode-select-photo-4-rear.jpg" alt="Rear of the panel with PCBs and wiring"><br><sub>Rear side — PCBs, wiring and DC jack</sub></td>
</tr>
</tbody>
</table>

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/dark-gray.svg" width="12" height="12"> | Dark Gray | C-Tech Premium Line PLA RAL7011 |
| <img src="../../images/icons/transparent.svg" width="12" height="12"> | Transparent | Filament PM PLA Transparent |
| <img src="../../images/icons/white.svg" width="12" height="12"> | White | Bambu PLA Basic Jade White (10100) |
| <img src="../../images/icons/black.svg" width="12" height="12"> | Black | Bambu PLA Basic Black (10101) |

---

## 3D Printed Parts

| Qty | Part | Notes |
|---:|---|---|
| 1× | Top panel | print on a **Textured** PEI plate |
| 1× | Bottom panel | print on a **Textured** PEI plate |
| 1× | Diffuser panel | print on a **Smooth** PEI plate |
| 1× | Backlight panel | |
| 2× | PCB frame | |
| 4× | M4 washer | |
| 4× | Standoff 16 mm | |

---

## Switches and Buttons

| Qty | Type |
|---:|---|
| 2× | Rotary switch SR16, 4 positions |

---

## Rotary Knobs

The knobs for the two IRS mode selectors are a separate model shared with the other panels — they are **not included** in this download.

| | |
|---|---|
| 📦 Printable model | [Boeing 737 Overhead - Rotary Knobs](https://makerworld.com/en/models/3066127-boeing-737-overhead-rotary-knobs) |
| 🔧 Build notes | [Rotary Knobs](03-rotary-knobs.md) |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 1× | Flat head M3×6 | bottom + diffuser |
| 4× | Flat head M3×12 | bottom + standoff |
| 4× | Flat head M4×16 | bottom + main frame |
| 4× | Dome head M3×5 | PCB + backlight |
| 6× | Dome head M3×8 | top + bottom, backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 7× | Black background, yellow LED |
| 2× | Black background, white LED |

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
| 1× | [RJ45 Direct](../pcb/rj45-direct.md) | pins 1–8 | [📥 PCB_RJ45_Direct.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Direct.zip) |
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–8 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |

Mounting and connections are shown in [step 4](#4-backlight-panel--pcbs-and-dc-jack) of the assembly diagram.

---

## Backlight

| Qty | Part |
|---:|---|
| 3× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

Powered from the **12 V** supply — see [Power supply](../system-overview.md#power-supply).

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Top panel

<img src="../../images/panels/13-irs-mode-select-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel — diffuser, rotary switches, annunciators and standoffs

<img src="../../images/panels/13-irs-mode-select-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Backlight panel — LED strips

<img src="../../images/panels/13-irs-mode-select-03-backlight-leds.png" alt="Backlight LED strips" width="700">

### 4. Backlight panel — PCBs and DC jack

<img src="../../images/panels/13-irs-mode-select-04-backlight-pcb.png" alt="Backlight panel PCB mounting" width="700">
