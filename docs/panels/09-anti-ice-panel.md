# 9. Anti-ice Panel

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3197814-boeing-737-overhead-anti-ice-panel)

[← Back to panel list](README.md)

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
| 3× | KN3(C)-101 or KN3(C)-102, ON/OFF |

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 3× | Flat head M3×6 | bottom + diffuser |
| 4× | Flat head M3×12 | bottom + standoff |
| 4× | Flat head M4×16 | bottom + main frame |
| 5× | Dome head M3×5 | PCB + backlight, counterplate + bottom |
| 2× | Dome head M3×10 | top + bottom |
| 4× | Dome head M3×8 | backlight + standoff |

---

## Annunciators

| Qty | Type |
|---:|---|
| 2× | Black background, yellow LED |
| 4× | Blue background, white LED, dual brightness |

The annunciators themselves are a separate model — see [Parts from Other Models](#parts-from-other-models) below. For their PCB, BOM and wiring, see [Annunciator PCB](../pcb/annunciator.md).

---

## PCB

| Qty | PCB | Connections used | Gerber files |
|---:|---|---|---|
| 1× | [RJ45 LED Driver](../pcb/rj45-driver.md) | headers 1–8 | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |
| 1× | [RJ45 Combined](../pcb/rj45-combined.md) | pins 3–4 and 5–8 | [📥 PCB_RJ45_Combined.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Combined.zip) |

Mounting and connections are shown in [step 5](#5-backlight-panel--pcbs-and-dc-jack) of the assembly diagram.

---

## Backlight

| Qty | Part |
|---:|---|
| 3× | LED strip |
| 1× | DC jack 5.5 × 2.5 mm |

Powered from the **12 V** supply — see [Power supply](../system-overview.md#power-supply).

---

## Parts from Other Models

The following components are shared with other panels and are **not included** in this model. Download them separately:

| Part | Model |
|---|---|
| Annunciators | [Boeing 737 Overhead - Annunciators](https://makerworld.com/en/models/3121595-boeing-737-overhead-annunciators) |

---

## Assembly Diagram

Screw abbreviations used in the diagrams: **FH** = flat head, **DH** = dome head.

### 1. Top panel

<img src="../../images/panels/09-anti-ice-01-top-panel.png" alt="Top panel assembly" width="700">

### 2. Bottom panel — switches, annunciators and standoffs

<img src="../../images/panels/09-anti-ice-02-bottom-panel.png" alt="Bottom panel assembly" width="700">

### 3. Diffuser panel

<img src="../../images/panels/09-anti-ice-03-diffuser.png" alt="Diffuser panel assembly" width="700">

### 4. Backlight panel — LED strips

<img src="../../images/panels/09-anti-ice-04-backlight-leds.png" alt="Backlight LED strips" width="700">

### 5. Backlight panel — PCBs and DC jack

<img src="../../images/panels/09-anti-ice-05-backlight-pcb.png" alt="Backlight panel PCB mounting" width="700">
