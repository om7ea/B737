# 12. Voice Recorder Switch

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3214222-boeing-737-overhead-voice-recorder-switch)

[← Back to model list](README.md)

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-1-front.jpg" alt="Finished Voice Recorder Switch, front"><br><sub>Finished panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-2-top-panel.jpg" alt="Printed top panel"><br><sub>Printed top panel</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-3-bottom-panel.jpg" alt="Printed bottom panel"><br><sub>Printed bottom panel</sub></td>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-4-diffuser.jpg" alt="Diffuser panel with the switch fitted"><br><sub>Diffuser panel with the switch fitted</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-5-diffuser-fitted.jpg" alt="Diffuser panel fitted into the bottom panel"><br><sub>Diffuser panel fitted, before the top panel goes on</sub></td>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-6-backlight-leds.jpg" alt="Inside of the backlight panel with the LED strip"><br><sub>Backlight panel from the inside - LED strip and DC jack wiring</sub></td>
</tr>
</tbody>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-7-backlight-dc-jack.jpg" alt="Outside of the backlight panel with the DC jack"><br><sub>Backlight panel from the outside - DC jack</sub></td>
<td align="center" width="50%"><img src="../../images/panels/12-voice-recorder-switch-photo-8-rear.jpg" alt="Rear of the assembled panel"><br><sub>Rear side - backlight panel mounted, switch terminals and DC jack</sub></td>
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
| 2× | M4 washer | |
| 4× | Standoff 16 mm | |

---

## Switches and Buttons

| Qty | Type |
|---:|---|
| 1× | KN3(C)-101 or KN3(C)-102, ON/OFF |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 1× | Flat head M3×6 | bottom + diffuser |
| 4× | Flat head M3×12 | bottom + standoff |
| 2× | Flat head M4×16 | bottom + main frame |
| 6× | Dome head M3×8 | top + bottom, backlight + standoff |

---

## Wiring

This panel has no PCB and no patch cable of its own. Its single switch is wired across to a PCB on the **Temperature Control Panel**, where it takes pin **5** - that PCB's cable goes to socket **A2** on **Overhead_5**.

**Both wires come from that panel**, the signal and the ground return, so nothing here connects to a MEGA 2560 directly.

---

## Backlight

| Qty | Part |
|---:|---|
| 1× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

Powered from the **12 V** supply - see [Power supply](../system-overview.md#power-supply).

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Top panel

<img src="../../images/panels/12-voice-recorder-switch-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel - diffuser, switch and standoffs

<img src="../../images/panels/12-voice-recorder-switch-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Backlight panel - LED strip

<img src="../../images/panels/12-voice-recorder-switch-03-backlight-leds.png" alt="Backlight LED strip" width="700">

### 4. Backlight panel - DC jack

<img src="../../images/panels/12-voice-recorder-switch-04-backlight-dc-jack.png" alt="Backlight panel DC jack mounting" width="700">
