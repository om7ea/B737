# PCB Manufacturing Files (Gerber)

The PCB designs released so far. All Gerber files are ready to be uploaded directly to a PCB manufacturer.

> **This is not the final list.** Further PCB designs will be added as new panels are released. Check back for updates.

[← Back to main page](../../README.md)

---

## Which PCB Do I Need?

<table>
<thead>
<tr>
<th></th>
<th>PCB</th>
<th>Qty needed</th>
<th>Purpose</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="annunciator.md"><img src="../../images/pcb/PCB_Annunciator.png" width="200"></a></td>
<td><a href="annunciator.md"><strong>1. Annunciator</strong></a></td>
<td>125×</td>
<td>The illuminated push-button annunciators themselves</td>
</tr>
</tbody>
<tbody>
<tr>
<td><a href="rj45-direct.md"><img src="../../images/pcb/PCB_RJ45_Direct_top.png" width="200"></a></td>
<td><a href="rj45-direct.md"><strong>2. RJ45 Direct</strong></a></td>
<td>27×</td>
<td>Buttons, toggle switches, rotary switches, servos, displays</td>
</tr>
</tbody>
<tbody>
<tr>
<td><a href="rj45-driver.md"><img src="../../images/pcb/PCB_RJ45_Driver_top.png" width="200"></a></td>
<td><a href="rj45-driver.md"><strong>3. RJ45 LED Driver</strong></a></td>
<td>20×</td>
<td>Up to 8 annunciators, with a driver to offload the board</td>
</tr>
</tbody>
<tbody>
<tr>
<td><a href="rj45-combined.md"><img src="../../images/pcb/PCB_RJ45_Combined_top.png" width="200"></a></td>
<td><a href="rj45-combined.md"><strong>4. RJ45 Combined</strong></a></td>
<td>6×</td>
<td>4 driven annunciator channels + 4 direct connections</td>
</tr>
</tbody>
<tbody>
<tr>
<td></td>
<td>…</td>
<td>—</td>
<td><em>More designs will follow as new panels are released</em></td>
</tr>
</tbody>
</table>

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
