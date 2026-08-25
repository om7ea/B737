# 5. RJ45 Hub Shield

<img src="../../images/pcb/PCB_RJ45_Hub_Shield_top.png" alt="RJ45 Hub Shield PCB - top" width="300"><img src="../../images/pcb/PCB_RJ45_Hub_Shield_bottom.png" alt="RJ45 Hub Shield PCB - bottom" width="300">

[📥 Download Gerber files - PCB_RJ45_Hub_Shield.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Hub_Shield.zip)

[← Back to PCB overview](README.md)

---

## Purpose

A shield for the **MEGA 2560 PRO MINI**. It plugs straight onto the board and breaks the I/O out to **nine RJ45 sockets**, so up to nine panel cables connect directly at the board end instead of being wired to it one by one.

The sockets are silkscreened **D0–D6** for the digital groups and **A1, A2** for the analog ones. The power terminal feeds **5 V** into the shield, which supplies both the RJ45 sockets and the MEGA 2560 PRO MINI itself.

Board size: **81.5 × 58.5 mm**.

## Quantity

A total of **7** PCBs are required for the complete project — one for each of the seven [MEGA 2560 PRO MINI boards](../system-overview.md#the-boards). I recommend ordering a few extra in case some are damaged during assembly.

---

## Bill of Materials (BOM)

| Qty | Part | Reference |
|---:|---|---|
| 9× | **RJ45 connector** — 5224 8P8C in-line, vertical 180°, full plastic | [Product I used](../../images/parts/AE_RJ45.png) |
| 1× | **Electrolytic capacitor 47 µF / 16 V** — radial, 3.5 mm lead pitch | |
| 1× | **Ceramic capacitor 100 nF** | |
| 1× | **KF301-2P screw terminal** — 5.08 mm pitch, for the 5 V input | [Product I used](../../images/parts/AE_KF301.png) |
| or 2× | **4.8 mm PCB male Faston terminal** — one leg clipped off, this is what I used | [Product I used](../../images/parts/AE_plug_male.png) |
| 1 set | **2.54 mm double-row pin headers** — see the table below | |
| 1 set | **2.54 mm double-row female sockets** — same sizes, soldered into the MEGA 2560 PRO MINI | |
| 1× | **330 Ω resistor (0805)** — optional | |
| 1× | **Green LED (0805)** — optional | |

### Header Sizes

The shield carries the full pin count of the MEGA 2560 PRO MINI in three double rows:

| Qty | Size | Pins |
|---:|---|---:|
| 1× | 2×21 | 42 |
| 1× | 2×16 | 32 |
| 1× | 2×3 | 6 |

The **pin headers usually come in the bag with the MEGA 2560 PRO MINI**, so there is no need to buy them separately. Only the matching **female sockets** have to be ordered.

---

## Assembly Notes

- The RJ45 sockets, the 47 µF electrolytic capacitor and the optional power LED go on the **top** side. The pin headers and the 100 nF capacitor go on the **bottom** side.
- I soldered the **pin headers into the shield** and the **female sockets into the MEGA 2560 PRO MINI**, so the shield sits on top of the board. The other way round works just as well.
- The 100 nF capacitor has no footprint of its own — solder it directly across the two power terminal pads on the underside, in parallel with the 47 µF.
- Each RJ45 connector has two plastic mounting posts; make sure both drop into their holes before soldering, otherwise the connector sits crooked.
