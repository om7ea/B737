# 5. Flight Control Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3153234-boeing-737-overhead-flight-control-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/05-flight-control-photo-1-front.jpg" alt="Finished Flight Control Panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/05-flight-control-photo-2-top-panel.jpg" alt="Printed top panel"><br><sub>Printed top panel</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/05-flight-control-photo-3-bottom-panel.jpg" alt="Printed bottom panel"><br><sub>Printed bottom panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/05-flight-control-photo-4-diffuser.jpg" alt="Diffuser panel fitted with the switches, guards and annunciators"><br><sub>Diffuser panel fitted, before the top panel goes on</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/05-flight-control-photo-5-rear.jpg" alt="Rear of the panel with the four PCBs and wiring"><br><sub>Rear side — the four PCBs, wiring and DC jack</sub></td>
<td width="50%"></td>
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
| 4× | PCB frame | |
| 6× | M4 washer | |
| 4× | Standoff 16 mm | |

---

## Switches and Buttons

| Qty | Type |
|---:|---|
| 2× | KN3(C)-103, ON/OFF/ON |
| 4× | KN3(C)-101 or KN3(C)-102, ON/OFF |
| 1× | KN3(C)-123, (ON)/OFF/(ON) |
| 4× | Toggle switch safety aircraft guard, black |
| 1× | Toggle switch safety aircraft guard, red |

The four black guards go on the FLT CONTROL and SPOILER switches, the red one on the ALTERNATE FLAPS ARM switch. The ALTERNATE FLAPS UP/DOWN and YAW DAMPER switches are left unguarded.

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 1× | Flat head M3×6 | bottom + diffuser |
| 4× | Flat head M3×12 | bottom + standoff |
| 6× | Flat head M4×16 | bottom + main frame |
| 8× | Dome head M3×5 | PCB + backlight |
| 4× | Dome head M3×8 | top + bottom |
| 4× | Dome head M3×8 | backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 9× | Black background, yellow LED |

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
| 1× | [RJ45 Direct](../pcb/rj45-direct.md) | pins 7–8 | [📥 PCB_RJ45_Direct.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Direct.zip) |
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–5 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 5–8 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |

Mounting and connections are shown in [step 4](#4-backlight-panel--pcbs-and-dc-jack) of the assembly diagram. Which annunciator and which switch each connection carries is in [Wiring](#wiring).

---

## Wiring

The nine annunciators and the ten switch inputs take four PCBs, and they do not all hang off the same MEGA 2560 — three go to `Overhead_1a`, one to `Overhead_1b`. Each PCB is connected by one Ethernet patch cable to a socket on the [RJ45 Hub Shield](../pcb/rj45-hub-shield.md).

| PCB | Patch cable goes to | Connections used |
|---|---|---|
| **PCB 1** | socket **D4** on **Overhead_1a** | pins 1–8 |
| **PCB 2** | socket **D6** on **Overhead_1b** | pins 7–8 |
| **PCB 3** | socket **D5** on **Overhead_1a** | headers 1–5 |
| **PCB 4** | socket **D6** on **Overhead_1a** | headers 5–8 |

Two of the cables go to a socket marked **D6**, but on different hub shields — PCB 2 to the one on `Overhead_1b`, PCB 4 to the one on `Overhead_1a`.

The socket labels **D0–D6**, **A1** and **A2** are silkscreened on the hub shield.

<img src="../../images/panels/05-flight-control-wiring-pcbs.jpg" alt="Rear of the panel with the four PCBs marked" width="700">

The rear of the panel. **PCB 1** and **PCB 2** are the boards with the blue screw terminals — eight of them on PCB 1, two on PCB 2. Of the other two, **PCB 3** has five ZH headers wired and **PCB 4** four.

### PCB 1 — socket D4 on Overhead_1a

| Pin | Switch |
|---:|---|
| 1 | FLT CONTROL B — STBY RUD |
| 2 | FLT CONTROL A — STBY RUD |
| 3 | FLT CONTROL B — B ON |
| 4 | FLT CONTROL A — A ON |
| 5 | SPOILER A |
| 6 | ALTERNATE FLAPS ARM |
| 7 | ALTERNATE FLAPS — UP |
| 8 | ALTERNATE FLAPS — DOWN |

**The switches share a single ground return.** Each switch takes one of its terminals to its own pin. The opposite terminals are commoned — daisy-chained from one switch to the next — and the chain ends at a **-** (ground) contact.

### PCB 2 — socket D6 on Overhead_1b

| Pin | Switch |
|---:|---|
| 7 | SPOILER B |
| 8 | YAW DAMPER |

The remaining pins on this board are not used.

### PCB 3 — socket D5 on Overhead_1a

The five annunciators in the lower half of the panel — the four-high column at the bottom right, plus the YAW DAMPER annunciator above the yaw damper switch.

| Header | Annunciator |
|---:|---|
| 1 | MACH TRIM FAIL |
| 2 | AUTO SLAT FAIL |
| 3 | SPEED TRIM FAIL |
| 4 | FEEL DIFF PRESS |
| 5 | YAW DAMPER |

Headers 6 to 8 are not populated.

### PCB 4 — socket D6 on Overhead_1a

The four annunciators in the upper half of the panel. Three of them read **LOW PRESSURE**, so the printed text does not tell them apart: two sit directly under the FLT CONTROL switches, the third under STANDBY HYD below LOW QUANTITY.

| Header | Annunciator |
|---:|---|
| 5 | LOW PRESSURE — STANDBY HYD |
| 6 | LOW QUANTITY |
| 7 | LOW PRESSURE — FLT CONTROL A |
| 8 | LOW PRESSURE — FLT CONTROL B |

Headers 1 to 4 are not populated.

---

## Backlight

| Qty | Part |
|---:|---|
| 10× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

Powered from the **12 V** supply — see [Power supply](../system-overview.md#power-supply).

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Top panel

<img src="../../images/panels/05-flight-control-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel — diffuser, switches, annunciators and standoffs

<img src="../../images/panels/05-flight-control-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Backlight panel — LED strips

<img src="../../images/panels/05-flight-control-03-backlight-leds.png" alt="Backlight LED strips" width="700">

### 4. Backlight panel — PCBs and DC jack

<img src="../../images/panels/05-flight-control-04-backlight-pcb.png" alt="Backlight panel PCB mounting" width="700">
