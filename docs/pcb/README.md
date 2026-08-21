# PCB Manufacturing Files (Gerber)

The PCB designs released so far. All Gerber files are ready to be uploaded directly to a PCB manufacturer.

> **This is not the final list.** Further PCB designs will be added as new panels are released. Check back for updates.

[← Back to main page](../../README.md)

---

## Which PCB Do I Need?

| PCB | Qty needed | Purpose |
|---|---|---|
| [**1. Annunciator**](annunciator.md) | 125× | The illuminated push-button annunciators themselves |
| [**2. RJ45 Direct**](rj45-direct.md) | 27× | Buttons, toggle switches, rotary switches, servos, displays |
| [**3. RJ45 LED Driver**](rj45-driver.md) | 20× | Up to 8 annunciators, with a driver to offload the board |
| [**4. RJ45 Combined**](rj45-combined.md) | 6× | 4 driven annunciator channels + 4 direct connections |
| … | — | *More designs will follow as new panels are released* |

> **Note**
> The quantities above cover the panels released so far. I recommend ordering a few extra of each, in case some are damaged during assembly.

---

## Downloads

| PCB | Gerber files |
|---|---|
| Annunciator | [📥 PCB_Annunciator.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_Annunciator.zip) |
| RJ45 Direct | [📥 PCB_RJ45_Direct.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Direct.zip) |
| RJ45 LED Driver | [📥 PCB_RJ45_Driver.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Driver.zip) |
| RJ45 Combined | [📥 PCB_RJ45_Combined.zip](https://raw.githubusercontent.com/om7ea/B737/main/PCB/PCB_RJ45_Combined.zip) |

*Additional Gerber files will be published here as new panels are released.*

---

## How They Fit Together

The RJ45 boards are the interface between the [Mega 2560 PRO MINI boards](../system-overview.md) and the individual panels. Panels connect using standard Ethernet patch cables. The Annunciator PCB sits inside each illuminated push-button and connects to a driver board with a ZH 1.5 4-pin cable.
