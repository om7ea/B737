# 8. Window and Probe Heat Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3196345-boeing-737-overhead-window-and-probe-heat-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/08-window-probe-heat-photo-1-front.jpg" alt="Finished Window and Probe Heat Panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/08-window-probe-heat-photo-2-top-panel.jpg" alt="Printed top panel"><br><sub>Printed top panel</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/08-window-probe-heat-photo-3-diffuser.jpg" alt="Diffuser panel fitted"><br><sub>Diffuser panel fitted, before the top panel goes on</sub></td>
<td align="center" width="50%"><img src="../../images/panels/08-window-probe-heat-photo-4-rear.jpg" alt="Rear of the panel with PCBs and wiring"><br><sub>Rear side — PCBs, wiring and DC jack</sub></td>
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
| 3× | PCB frame | |
| 4× | M4 washer | |
| 4× | Standoff 16 mm | |

---

## Switches and Buttons

| Qty | Type |
|---:|---|
| 6× | KN3(C)-101 or KN3(C)-102, ON/OFF |
| 1× | KN3(C)-123, (ON)/OFF/(ON) |
| 1× | PBS-110 push button, black |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 2× | Flat head M3×6 | bottom + diffuser |
| 4× | Flat head M3×12 | bottom + standoff |
| 4× | Flat head M4×16 | bottom + main frame |
| 7× | Dome head M3×5 | PCB + backlight, counterplate + bottom |
| 2× | Dome head M3×10 | top + bottom |
| 2× | Dome head M3×8 | top + bottom |
| 4× | Dome head M3×8 | backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 12× | Black background, yellow LED |
| 4× | Black background, green LED |

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
| 2× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–8 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |

Mounting and connections are shown in [step 5](#5-backlight-panel--pcbs-and-dc-jack) of the assembly diagram. Which switch and which annunciator each connection carries is in [Wiring](#wiring).

---

## Wiring

This panel takes three PCBs, and all three reach the **same** MEGA 2560 — `Overhead_4`. Each PCB is connected by one Ethernet patch cable to a socket on the [RJ45 Hub Shield](../pcb/rj45-hub-shield.md).

| PCB | Patch cable goes to | Connections used |
|---|---|---|
| **PCB 1** | socket **A1** on **Overhead_4** | pins 1–8 |
| **PCB 2** | socket **A2** on **Overhead_4** | headers 1–8 |
| **PCB 3** | socket **D0** on **Overhead_4** | headers 1–8 |

The socket labels **D0–D6**, **A1** and **A2** are silkscreened on the hub shield.

<img src="../../images/panels/08-window-probe-heat-wiring-pcbs.jpg" alt="Rear of the panel with the three PCBs marked" width="700">

The rear of the panel. **PCB 1** is the one with the blue screw terminals. The other two sit next to the annunciators they serve: **PCB 2** at the top for the window heat annunciators, **PCB 3** at the bottom for the probe annunciators.

### PCB 1 — socket A1 on Overhead_4

| Pin | Switch |
|---:|---|
| 1 | PROBE HEAT — B |
| 2 | WINDOW HEAT — R SIDE |
| 3 | WINDOW HEAT — R FWD |
| 4 | WINDOW HEAT — L FWD |
| 5 | TEST — OVHT |
| 6 | PROBE HEAT — A |
| 7 | WINDOW HEAT — L SIDE |
| 8 | TEST — PWR TEST |

**The TEST switch takes two pins.** It is the three-position (ON)/OFF/(ON) switch in the middle of the panel, and each of its two active positions needs its own connection: pin 5 for OVHT, pin 8 for PWR TEST.

**The TAT TEST button is not on this panel's PCBs.** All eight pins of the Direct board are used by the switches above, so the push button is wired across to pin 5 of the Combined PCB on the [Anti-ice Panel](09-anti-ice-panel.md). It is the loose white wire leaving the panel at the bottom of the photo above.

### PCB 2 — socket A2 on Overhead_4

The eight window heat annunciators, at the top of the panel. The four **ON** annunciators are the green ones; the four **OVERHEAT** are yellow.

| Header | Annunciator |
|---:|---|
| 1 | ON — R SIDE |
| 2 | ON — R FWD |
| 3 | ON — L FWD |
| 4 | ON — L SIDE |
| 5 | OVERHEAT — L SIDE |
| 6 | OVERHEAT — L FWD |
| 7 | OVERHEAT — R FWD |
| 8 | OVERHEAT — R SIDE |

### PCB 3 — socket D0 on Overhead_4

The eight probe annunciators, in the two columns at the bottom of the panel. Headers 1 to 4 serve the right-hand column, 5 to 8 the left-hand one.

| Header | Annunciator |
|---:|---|
| 1 | AUX PITOT |
| 2 | R ALPHA VANE |
| 3 | R ELEV PITOT |
| 4 | F/O PITOT |
| 5 | CAPT PITOT |
| 6 | L ELEV PITOT |
| 7 | L ALPHA VANE |
| 8 | TEMP PROBE |


**The switches share a single ground return.** Each switch takes one of its terminals to its own pin on the Direct PCB. The opposite terminals are commoned — daisy-chained from one switch to the next — and the chain ends at a **-** (ground) contact.

---

## Backlight

| Qty | Part |
|---:|---|
| 5× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

Powered from the **12 V** supply — see [Power supply](../system-overview.md#power-supply).

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Top panel

<img src="../../images/panels/08-window-probe-heat-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel — switches, button, annunciators and standoffs

<img src="../../images/panels/08-window-probe-heat-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Diffuser panel

<img src="../../images/panels/08-window-probe-heat-03-diffuser.png" alt="Diffuser panel assembly" width="700">

### 4. Backlight panel — LED strips

<img src="../../images/panels/08-window-probe-heat-04-backlight-leds.png" alt="Backlight LED strips" width="700">

### 5. Backlight panel — PCBs and DC jack

<img src="../../images/panels/08-window-probe-heat-05-backlight-pcb.png" alt="Backlight panel PCB mounting" width="700">
