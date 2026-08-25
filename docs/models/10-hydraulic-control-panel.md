# 10. Hydraulic Control Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3212634-boeing-737-overhead-hydraulic-control-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/10-hydraulic-photo-1-front.jpg" alt="Finished Hydraulic Control Panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/10-hydraulic-photo-2-top-panel.jpg" alt="Printed top panel"><br><sub>Printed top panel</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/10-hydraulic-photo-3-diffuser.jpg" alt="Diffuser panel fitted"><br><sub>Diffuser panel fitted, before the top panel goes on</sub></td>
<td align="center" width="50%"><img src="../../images/panels/10-hydraulic-photo-4-rear.jpg" alt="Rear of the panel with PCBs and wiring"><br><sub>Rear side — PCBs, wiring and DC jack</sub></td>
</tr>
</tbody>
</table>

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/dark-gray.svg" width="12" height="12"> | Dark Gray | C-Tech Premium Line PLA RAL7011 |
| <img src="../../images/icons/bone-white.svg" width="12" height="12"> | Bone White | Bambu PLA Matte Bone White (11103) |
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
| 4× | KN3(C)-101 or KN3(C)-102, ON/OFF |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 4× | Flat head M3×12 | bottom + standoff |
| 4× | Flat head M4×16 | bottom + main frame |
| 5× | Dome head M3×5 | PCB + backlight, counterplate + bottom |
| 2× | Dome head M3×10 | top + bottom |
| 4× | Dome head M3×8 | backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 6× | Black background, yellow LED |

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
| 1× | [RJ45 Direct](../pcb/rj45-direct.md) | pins 5–8 | [📥 PCB_RJ45_Direct.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Direct.zip) |
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–6 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |

Mounting and connections are shown in [step 5](#5-backlight-panel--pcbs-and-dc-jack) of the assembly diagram. Which switch and which annunciator each connection carries is in [Wiring](#wiring).

---

## Wiring

The four toggle switches and the six annunciators are on two different PCBs, but both reach the **same** MEGA 2560 — `Overhead_4`. Each PCB is connected by one Ethernet patch cable to a socket on the [RJ45 Hub Shield](../pcb/rj45-hub-shield.md).

| PCB | Patch cable goes to | Connections used |
|---|---|---|
| **PCB 1** — [RJ45 Direct](../pcb/rj45-direct.md) | socket **D6** on **Overhead_4** | pins 5–8 |
| **PCB 2** — [RJ45 LED Driver](../pcb/rj45-driver.md) | socket **D4** on **Overhead_4** | headers 1–6 |

The socket labels **D0–D6**, **A1** and **A2** are silkscreened on the hub shield.

<img src="../../images/panels/10-hydraulic-wiring-pcbs.jpg" alt="Rear of the panel with the two PCBs marked" width="700">

The rear of the panel. **PCB 1** is the one with the blue screw terminals going down to the switches; **PCB 2** carries the red and black annunciator wiring.

### PCB 1 — socket D6 on Overhead_4

| Pin | Switch |
|---:|---|
| 5 | ENG 1 |
| 6 | ELEC 2 |
| 7 | ELEC 1 |
| 8 | ENG 2 |

Pins 5 to 8 follow the switches left to right as they appear on the front of the panel.

**The four switches share a single ground return.** Each switch takes one of its terminals to its own pin on the Direct PCB. The opposite terminals are commoned — daisy-chained from one switch to the next — and the chain ends at a **-** (ground) contact.

### PCB 2 — socket D4 on Overhead_4

| Header | Annunciator |
|---:|---|
| 1 | LOW PRESSURE — ENG 2 |
| 2 | LOW PRESSURE — ENG 1 |
| 3 | OVERHEAT — B |
| 4 | LOW PRESSURE — ELEC 2 |
| 5 | OVERHEAT — A |
| 6 | LOW PRESSURE — ELEC 1 |

Headers 7 and 8 are not populated.

Four of the annunciators read **LOW PRESSURE** and two read **OVERHEAT**, so the printed text alone does not tell them apart. Each LOW PRESSURE sits directly above the pump switch it belongs to, and the two OVERHEAT annunciators belong to hydraulic systems **A** and **B**, marked at the bottom of the panel.

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

<img src="../../images/panels/10-hydraulic-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel — switches, annunciators and standoffs

<img src="../../images/panels/10-hydraulic-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Diffuser panel and counterplate

<img src="../../images/panels/10-hydraulic-03-diffuser.png" alt="Diffuser panel assembly" width="700">

### 4. Backlight panel — LED strips

<img src="../../images/panels/10-hydraulic-04-backlight-leds.png" alt="Backlight LED strips" width="700">

### 5. Backlight panel — PCBs and DC jack

<img src="../../images/panels/10-hydraulic-05-backlight-pcb.png" alt="Backlight panel PCB mounting" width="700">
