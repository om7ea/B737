# 18. Flood Light

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3237863-boeing-737-overhead-flood-light)

[← Back to model list](README.md)

---

> **Note**
> The two LED strips behind the window are the overhead **flood light** itself, not panel backlighting. This panel has no PCB and no patch cable — but the pair of splice connectors screwed to its back is where the 12 V for the whole overhead is distributed.

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/18-flood-light-photo-1-front.jpg" alt="Finished Flood Light panel, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/18-flood-light-photo-2-top-panel.jpg" alt="Printed top panel with the transparent window"><br><sub>Top panel — the window is printed in Transparent</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/18-flood-light-photo-3-bottom-panel.jpg" alt="Printed bottom panel"><br><sub>Bottom panel — the four outer holes go to the main frame, the two inner ones to the standoffs</sub></td>
<td align="center" width="50%"><img src="../../images/panels/18-flood-light-photo-4-led-strips.jpg" alt="Backlight panel with the two LED strips and the DC jack"><br><sub>Backlight panel — the two LED strips and the DC jack</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/18-flood-light-photo-5-splice-connectors.jpg" alt="Rear of the backlight panel with the two splice connectors"><br><sub>Rear side — the two splice connectors and the DC jack</sub></td>
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
| <img src="../../images/icons/black.svg" width="12" height="12"> | Black | Bambu PLA Basic Black (10101) |

---

## 3D Printed Parts

| Qty | Part | Notes |
|---:|---|---|
| 1× | Top panel | print on a **Textured** PEI plate; the window is Transparent, the rest Dark Gray |
| 1× | Bottom panel | print on a **Textured** PEI plate |
| 1× | Backlight panel | |
| 2× | Standoff 16 mm | |

---

## Electronic Components

| Qty | Part |
|---:|---|
| 2× | Splice connector F15, 1 in / 5 out |

These are lever-type splice connectors and they serve the **whole overhead**, not just this panel: one carries **+12 V**, the other **GND**, and the five outputs of each feed one column of panels. See [12 V](../system-overview.md#12-v) in the System Overview for the full distribution.

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 2× | Dome head M3×8 | backlight panel + standoff |
| 2× | Dome head M3×12 | top + standoff |
| 2× | Dome head M3×14 | backlight panel + splice connectors |
| 4× | Dome head M4×8 | bottom + main frame |

The four M4 screws are covered by the top panel, so the finished panel shows only the two M3×12 heads.

---

## Flood Light

| Qty | Part |
|---:|---|
| 2× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

The strips sit in the recess of the backlight panel and shine out through the transparent window. They run on **12 V** from the flood light dimmer, on a DC plug of their own — the second dimmer channel described in [12 V](../system-overview.md#12-v). They are therefore independent of the overhead backlighting and have their own knob on the Center Middle Panel.

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **DH** = dome head.

### 1. Backlight panel — LED strips

<img src="../../images/panels/18-flood-light-01-led-strips.png" alt="The two LED strips fitted into the backlight panel" width="700">

### 2. Backlight panel — DC jack, standoffs and splice connectors

<img src="../../images/panels/18-flood-light-02-backlight-panel.png" alt="Rear of the backlight panel with the DC jack, the two standoffs and the two splice connectors" width="700">

### 3. Bottom panel — mounting to the main frame

<img src="../../images/panels/18-flood-light-03-main-frame.png" alt="Bottom panel screwed to the main frame" width="700">

### 4. Top panel

<img src="../../images/panels/18-flood-light-04-top-panel.png" alt="Top panel screwed down into the standoffs" width="700">
