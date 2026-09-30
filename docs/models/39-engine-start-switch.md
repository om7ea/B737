# 39. Engine Start Switch

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3375879-boeing-737-overhead-engine-start-switch)

[← Back to model list](README.md)

---

> **Note**
> This switch is a model of its own - it is not part of any panel model. **Two** are needed for the complete project, both on the **Engine Start Panel** - one for each engine.

---

## Photos

<table>
<tbody>
<tr>
<td align="center" width="50%"><img src="../../images/panels/39-engine-start-photo-1-front.jpg" alt="Finished Engine Start Switch with its knob and servo"><br><sub>The finished switch, with its knob fitted</sub></td>
</tr>
</tbody>
</table>

---

## How It Works

The knob turns a **12-position rotary switch RS26** through two printed rods, set to the four positions **GRD / OFF / CONT / FLT**. A spring keeps the knob pulled out, and out of **OFF** it can only be turned after it has been **pushed in** - without pushing, it does not turn.

An **MG90S servo** beside the switch turns the knob back from **GRD** to **OFF** once the simulator releases the starter, the way the real aircraft does it.

---

## 3D Printed Parts

| Per switch | Total for 2 | Part |
|---:|---:|---|
| 1× | 2× | top case |
| 1× | 2× | top rod |
| 1× | 2× | bottom case |
| 1× | 2× | bottom case cover |
| 1× | 2× | bottom rod |

The colour of the filament and the type of the build plate are up to you - the whole switch is hidden behind the panel.

---

## Switches and Buttons

| Per switch | Total for 2 | Type |
|---:|---:|---|
| 1× | 2× | Rotary switch RS26, 12 positions |

The RS26 has an adjustable end stop - set it to **4** positions.

---

## Rotary Knobs

The knobs are a separate model shared with the panels - they are **not included** in this download.

| Per switch | Total for 2 | Part |
|---:|---:|---|
| 1× | 2× | General knob, D shaft |
| 1× | 2× | General knob indicator |

| | |
|---|---|
| 📦 Printable model | [Boeing 737 Overhead - Rotary Knobs](https://makerworld.com/en/models/3066127-boeing-737-overhead-rotary-knobs) |

---

## Electronic and Mechanical Components

| Per switch | Total for 2 | Part | Reference |
|---:|---:|---|---|
| 1× | 2× | **Servo MG90S** - 180°, metal gears | [Product I used](../../images/parts/AE_servo_MG90S.png) |
| 1× | 2× | **Spring** - 9.5 × 19 mm | |

The MG90S has metal gears, so it copes with a heavier load than the SG90 used in the gauges.

The three screws and the single arm that come with the servo are used as well.

---

## Screws

| Per switch | Total for 2 | Screw | Joins |
|---:|---:|---|---|
| 6× | 12× | Dome head M3×8 | bottom case + top case, bottom case + bottom case cover |

---

## Wiring

Both switches are wired to two RJ45 Direct PCBs on the Engine Start Panel - sockets **D4** and **D6** on **Overhead_3**.

| Connection | ENG 1 switch | ENG 2 switch |
|---|---|---|
| Servo - control signal, **+5 V** and **GND** | pin headers at **pin 7**, socket **D6** | pin headers at **pin 8**, socket **D6** |
| GRD | pin **8**, socket **D4** | pin **4**, socket **D4** |
| OFF | pin **7**, socket **D4** | pin **3**, socket **D4** |
| CONT | pin **6**, socket **D4** | pin **2**, socket **D4** |
| FLT | pin **5**, socket **D4** | pin **1**, socket **D4** |

> **⚠️ The servo plug has to be rewired**
> The MG90S does not leave the factory in the order the RJ45 Direct PCB expects, so the servo will **not** work if you plug it in as it comes. **Swap the red and the orange wire:**
>
> | | Wire order in the plug |
> |---|---|
> | As delivered | brown - red - orange |
> | **Needed** | **brown - orange - red** |
>
> Lift the small tabs on the plastic housing, pull those two crimped contacts out and swap them over. Brown stays where it is.

---

## Assembly Diagram

Screw abbreviations used in the diagram: **DH** = dome head.

<img src="../../images/panels/39-engine-start-01-exploded.png" alt="Exploded view of the Engine Start Switch" width="800">
