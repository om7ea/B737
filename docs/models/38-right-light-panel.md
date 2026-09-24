# 38. Right Light Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3350735-boeing-737-overhead-right-light-panel)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-1-front.jpg" alt="Finished Right Light Panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-2-top-panel.jpg" alt="The printed top panel"><br><sub>The top panel - Dark Gray with the lettering in Jade White</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-3-index-plate.jpg" alt="The printed INDEX TO LOCK plate"><br><sub>The index plate - Black with the lettering in Jade White</sub></td>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-4-bottom-panel.jpg" alt="The printed bottom panel"><br><sub>The bottom panel - the opening is where the diffuser shows through</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-5-diffuser.jpg" alt="The diffuser panel with the five switches fitted"><br><sub>The diffuser panel with all five switches fitted</sub></td>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-6-diffuser-fitted.jpg" alt="Bottom panel with the diffuser and the switches fitted"><br><sub>The diffuser and the switches in the bottom panel, before the top panel goes on</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/38-right-light-photo-7-rear.jpg" alt="Rear of the finished panel"><br><sub>Rear side - the backlight panel, the DC jack and the PCB</sub></td>
<td align="center" width="50%"></td>
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
| 1× | Index plate | the INDEX TO LOCK plate at the right end; print on a **Textured** PEI plate |
| 1× | Diffuser panel | print on a **Smooth** PEI plate |
| 1× | Backlight panel | |
| 1× | PCB frame | |
| 4× | Standoff 16 mm | |
| 1× | Flat washer | goes under the screw that holds the index plate |

---

## Switches and Buttons

| Qty | Type |
|---:|---|
| 4× | KN3(C)-101, ON/OFF |
| 1× | KN3(C)-103, ON/OFF/ON |

The four two-position switches are LOGO, ANTI COLLISION, WING and WHEEL WELL. The three-position one is POSITION - STROBE & STEADY / OFF / STEADY.

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 3× | Flat head M3×12 | bottom + standoff |
| 2× | Dome head M3×5 | PCB + backlight |
| 8× | Dome head M3×8 | top + bottom, diffuser + standoff, backlight + standoff |
| 7× | Dome head M4×8 | bottom + main frame, index plate + bottom |

Three of the four standoffs are screwed to the bottom panel with the M3×12 screws; the fourth is screwed through the diffuser with M3×8.

---

## PCB

| Qty | PCB | Connections used | Gerber files |
|---:|---|---|---|
| 1× | [RJ45 Direct](../pcb/rj45-direct.md) | pins 1-6 | [📥 PCB_RJ45_Direct.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Direct.zip) |

Mounting is shown in [step 3](#3-backlight-panel---pcb-and-dc-jack) of the assembly diagram. Which switch each connection carries is in [Wiring](#wiring).

---

## Wiring

The panel has a single PCB. It is connected by one Ethernet patch cable to a socket on the [RJ45 Hub Shield](../pcb/rj45-hub-shield.md).

| PCB | Patch cable goes to | Connections used |
|---|---|---|
| **PCB 1** | socket **D5** on **Overhead_3** | pins 1-6 |

The socket labels **D0-D6**, **A1** and **A2** are silkscreened on the hub shield.

<img src="../../images/panels/38-right-light-wiring-rear.jpg" alt="Rear of the panel with the PCB marked" width="700">

The rear of the panel. **PCB 1** is the only board, on its frame below the backlight panel; the DC jack sits at the far left of the same panel. The white wires run from the board up to the switches; the brown wire daisy-chains the opposite terminals of all five switches together.

### PCB 1 - socket D5 on Overhead_3

| Pin | Switch |
|---:|---|
| 1 | WHEEL WELL |
| 2 | WING |
| 3 | ANTI COLLISION |
| 4 | POSITION - STEADY |
| 5 | POSITION - STROBE & STEADY |
| 6 | LOGO |

Pins 7 and 8 are not used.

**All the switches share a single ground return.** Each switch takes one of its terminals to its own pin on the Direct PCB. The opposite terminals are commoned - daisy-chained from one switch to the next - and the chain ends at a **-** (ground) contact.

---

## Backlight

| Qty | Part | Reference |
|---:|---|---|
| 4× | LED strip | [Product I used](../../images/parts/AE_led_strip.png) |
| 1× | DC jack 5.5 × 2.5 mm | [Product I used](../../images/parts/AE_dc_jack.png) |

Powered from the **12 V** supply - see [Power supply](../system-overview.md#power-supply).

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Bottom panel - diffuser, index plate, switches and standoffs

<img src="../../images/panels/38-right-light-01-bottom-panel-assembly.png" alt="Bottom panel with the diffuser, the index plate, the five switches and the standoffs" width="700">

### 2. Backlight panel - LED strips

<img src="../../images/panels/38-right-light-02-backlight-leds.png" alt="The four backlight LED strips" width="700">

### 3. Backlight panel - PCB and DC jack

<img src="../../images/panels/38-right-light-03-pcb-and-jack.png" alt="Backlight panel with the RJ45 Direct PCB and the DC jack" width="700">

### 4. Top panel

<img src="../../images/panels/38-right-light-04-top-panel.png" alt="The top panel screwed to the bottom panel" width="700">
