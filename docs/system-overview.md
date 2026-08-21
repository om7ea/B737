# System Overview

How the overhead panel connects to the simulator.

[← Back to main page](../README.md)

---

## The Idea

The whole overhead panel behaves as a **single plug-and-play USB device**. All electronics are enclosed inside the panel and connected to an internal USB hub, so linking the finished panel to the PC takes **one USB cable**.

<img src="../images/system_overview.png" alt="System overview diagram" width="800">

---

## Software (PC side)

| Component | Role |
|---|---|
| **Microsoft Flight Simulator 2020** | The simulator itself |
| **PMDG 737-800** | Aircraft model that exposes the real 737 systems and variables |
| **MobiFlight** | Bridges the hardware and the simulator — maps each switch, button and LED to a PMDG variable |

MobiFlight does the heavy lifting: switches and LEDs are configured in its graphical interface, so **no programming is required**. The Arduino boards run the standard MobiFlight firmware, which MobiFlight uploads for you when the board is first added.

---

## Hardware (inside the panel)

| Component | Quantity | Purpose |
|---|---|---|
| **Arduino Mini Mega 2560** | 7× | Each board drives one group of panels |
| **USB hub** | 1× | Connects all seven boards to the single USB cable |
| **RJ45 breakout PCBs** | 53× | Link the individual panels to the boards — see [PCB documentation](pcb/README.md) |

Each Mega 2560 is registered in MobiFlight as a separate device, which keeps the configuration manageable and makes it easy to work on one section of the overhead at a time.

### Why seven boards

A single Mega 2560 does not have enough I/O pins for the complete overhead panel. Splitting the panel across seven boards also means that a wiring fault in one section does not take down the entire overhead.

### Connection to panels

Panels attach to the boards through RJ45 connectors, using standard Ethernet patch cables. Three PCB variants cover the different needs:

- **RJ45 Direct** — buttons, toggle switches, rotary switches, servos, displays
- **RJ45 LED Driver** — up to 8 annunciators; the ULN2803 driver powers the LEDs so the Arduino is not overloaded
- **RJ45 Combined** — 4 driven annunciator channels + 4 direct connections

See [PCB Manufacturing Files](pcb/README.md) for details, BOM and wiring.

---

## 🚧 To be documented

These sections are still to be written:

- **Power supply** — voltage, current rating, and whether the USB hub is powered
- **Board assignment** — which panels are connected to which Mega 2560
- **MobiFlight configuration** — settings and, if released, downloadable config files
