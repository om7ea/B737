# 33. Duct Pressure Gauge

[📦 Download the printable model on MakerWorld](https://makerworld.com/en/models/3330434-boeing-737-overhead-duct-pressure-gauge)

[← Back to model list](README.md)

---

> **Note**
> This gauge is a model of its own - it is not part of any panel model. **One** is needed for the complete project, on the **Pneumatic Panel**.
>
> It is a **two-needle** instrument. Both needles turn on the same axis, the L needle on an acrylic pipe and the R needle on an acrylic rod running inside that pipe, and each one has a servo of its own.

---

## Photos

<table>
<tbody>
<tr>
<td align="center"><img src="../../images/panels/33-duct-pressure-render-assembled.png" alt="The assembled Duct Pressure Gauge"><br><sub>The assembled gauge</sub></td>
</tr>
</tbody>
</table>

---

## How It Works

Each needle is driven by its own **SG90 servo** through a pair of printed gears. The **14-tooth** gear sits on the servo and a **9-tooth** gear on the needle shaft, so a needle turns about one and a half times as far as its servo - the 180° of an SG90 cover the whole scale.

The two shafts run on the same axis, one inside the other. The **L needle** sits on a **3 mm acrylic pipe** turning in two **MR63ZZ** ball bearings, one in the inner part and one in the backlight part. The **R needle** sits on a **2 mm acrylic rod** that runs down the middle of that pipe; at the back the rod turns in a single **MR52ZZ** bearing pressed into the pipe gear, and at the front the pipe itself guides it.

What keeps the two drives apart is height. The two servos sit at different depths in the gears cover, and the two gears on the shafts are different heights as well - the **3 mm pipe gear** and the **2 mm rod gear** - so each servo gear reaches only one of them.

Both shafts are light pipes too: a white LED in the gears cover shines up the rod and the pipe into the needles. The two gears at the back sit in that light path, which is why they are printed in **transparent** PLA.

The dial itself is lit separately, by two LED strips inside the backlight part - see [Backlight](#backlight).

---

## Filament

| | Colour | Filament |
|---|---|---|
| <img src="../../images/icons/transparent.svg" width="12" height="12"> | Transparent | Filament PM PLA Transparent |
| <img src="../../images/icons/white.svg" width="12" height="12"> | White | Bambu PLA Basic Jade White (10100) |
| <img src="../../images/icons/black.svg" width="12" height="12"> | Black | Bambu PLA Basic Black (10101) |

---

## 3D Printed Parts

| Qty | Part | Colour | Notes |
|---:|---|---|---|
| 1× | outer | White | the square face - the UV-printed scale goes on it and it diffuses the backlight |
| 1× | inner | White | the round dial behind the face, with the second UV-printed scale on it |
| 1× | shielding outer+inner | Black | the ring wall between the two printed faces |
| 1× | backlight | Black | the rear plate; carries the second MR63ZZ bearing |
| 1× | gears cover | Black | the bracket for the two servos |
| 1× | pipe gear (3 mm) | Transparent | 9 teeth, on the acrylic pipe; in the light path of the needle LED |
| 1× | rod gear (2 mm) | Transparent | 9 teeth, on the acrylic rod; in the light path of the needle LED |
| 2× | servo gear | Black | 14 teeth, on the servo shafts |
| 1× | L needle | White + Black | on the acrylic pipe; the letter **L** is printed in black |
| 1× | R needle | White + Black | on the acrylic rod; the letter **R** is printed in black |
| 1× | needle cap | Black | covers the hub of the R needle |

All the parts print on a **Smooth** PEI plate.

---

## Electronic and Mechanical Components

| Qty | Part | Reference |
|---:|---|---|
| 2× | **Servo SG90** - 180°, plastic gears | [Product I used](../../images/parts/AE_servo_SG90.png) |
| 2× | **Ball bearing MR63ZZ** - 3 × 6 × 2.5 mm | [Product I used](../../images/parts/AE_bearing_MR63ZZ.png) |
| 1× | **Ball bearing MR52ZZ** - 2 × 5 × 2.5 mm | [Product I used](../../images/parts/AE_bearing_MR52ZZ.png) |
| 1× | **Acrylic pipe** - 2.1 × 3 × 200 mm, transparent; the shaft of the L needle is cut from it | [Product I used](../../images/parts/AE_acrylic_pipe.png) |
| 1× | **Acrylic rod** - 2 mm, transparent; the shaft of the R needle is cut from it | [Product I used](../../images/parts/AE_acrylic_rod.png) |
| 1× | **White 5 mm flat top LED** - the same one the annunciators use | [Product I used](../../images/parts/AE_led_white.png) |
| 1× | **150 Ω resistor** - in series with the white LED | |
| 2× | **LED strip** - the scale backlight | [Product I used](../../images/parts/AE_led_strip.png) |
| 1× | **820 Ω resistor** - in series with the two LED strips | |
| 2× | **Splice connector** - lever type, for the 12 V of the scale backlight | |

The screws that come with the servos are used as well: one holds each servo to the gears cover, and a second fastens its gear to the servo shaft.

---

## Screws

| Qty | Screw | Joins |
|---:|---|---|
| 4× | Dome head M3×8 | backlight + outer |
| 2× | Dome head M3×5 | gears cover + backlight |

---

## UV Print Files

| Qty | File |
|---:|---|
| 1× | A4 PDF - gauge scales |

Two of the scales on that sheet belong to this gauge: the square **DUCT PRESS** face with the tick marks, which goes on the outer part, and the round dial with the numbers, which goes on the inner part. The PDF and the printing instructions are on the [UV Print Files](../uv-print.md) page.

---

## Backlight

### Scale

The scale is lit by two LED strips inside the backlight part, one on each side, shining through the white outer and inner parts from behind. They run on **12 V** taken from the backlighting of the Pneumatic Panel, so the gauge dims together with that panel - see [Power supply](../system-overview.md#power-supply).

The two strips are not wired straight across that 12 V: an **820 Ω resistor** goes in series with the pair. The white parts pass far more light than the printed face of a panel does, so on the bare supply the scale burns out much brighter than the lettering around it. The resistor holds it back to the brightness of the rest of the overhead.

The two strips sit in parallel and the resistor goes in the lead feeding them, close to the strips.

<img src="../../images/panels/gauge-backlight-resistor.png" alt="The two LED strips in parallel with the series resistor in the supply lead" width="420">

### Needles

The needles have a light of their own: a white 5 mm LED in the gears cover, between the two servos, shining up through the transparent gears and on into the acrylic pipe and the acrylic rod. It runs on **5 V** with a **150 Ω** resistor in series, and it lights both needles at once.

> **Note**
> The needle lighting works, but the effect is weak. White PLA does not carry light well over the length of a needle, so a needle glows rather than lights up. It is worth building - but do not expect the needles to stand out the way the scale does.

---

## Wiring

The gauge has four connections.

| Connection | Supply | Comes from |
|---|---|---|
| L needle servo | 5 V | the control signal, **+5 V** and **GND**, all three from the pin headers at **pin 7** of the [RJ45 Direct](../pcb/rj45-direct.md) PCB on the **Pneumatic Panel** - socket **D2** on **Overhead_5** |
| R needle servo | 5 V | the same three, from the pin headers at **pin 6** of that board |
| Needle LED | 5 V | **+5 V** and **GND** from the Pneumatic Panel, through a **150 Ω** resistor - see [Backlight](#backlight) |
| Scale backlight | 12 V | the backlighting of the Pneumatic Panel, through an **820 Ω** resistor - see [Backlight](#backlight) |

> **⚠️ Both servo plugs have to be rewired**
> The SG90 does not leave the factory in the order the RJ45 Direct PCB expects, so a servo will **not** work if you plug it in as it comes. **Swap the red and the yellow wire:**
>
> | | Wire order in the plug |
> |---|---|
> | As delivered | brown - red - yellow |
> | **Needed** | **brown - yellow - red** |
>
> Lift the small tabs on the plastic housing, pull those two crimped contacts out and swap them over. Brown stays where it is. (On some SG90s the yellow wire is orange instead - it is the signal wire either way.)

The 12 V for the scale backlight is brought over from the panel's own backlighting with two **lever-type splice connectors**, one for +12 V and one for GND. Where they sit is up to you - both on the gauge works fine, and so does one on the gauge and one on the panel. There is nothing to screw them to, so **glue them down with super glue.**

---

## Assembly

Screw abbreviations used below: **DH** = dome head.

<table>
<tbody>
<tr>
<td width="55%"><b>1.</b> Screw the two servos to the <b>gears cover</b> with the screws that come in the servo bag.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-01.png" alt="The two servos screwed to the gears cover" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>2.</b> Fasten a 14-tooth <b>servo gear</b> to each servo, again with a screw from the servo bag.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-02.png" alt="The 14-tooth gears fastened to the servo shafts" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>3.</b> Stick the printed foil onto the <b>inner</b> part.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-03.png" alt="The printed foil stuck onto the inner part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>4.</b> Stick the printed foil onto the <b>outer</b> part.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-04.png" alt="The printed foil stuck onto the outer part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>5.</b> Drop the <b>shielding outer+inner</b> part into the outer part.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-05.png" alt="The shielding part dropped into the outer part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>6.</b> Drop the <b>inner</b> part into the shielding.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-06.png" alt="The inner part dropped into the shielding" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>7.</b> Press an <b>MR63ZZ</b> bearing into the inner part.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-07.png" alt="The first MR63ZZ bearing pressed into the inner part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td colspan="2"><b>8.</b> Fit the two <b>LED strips</b> inside the <b>backlight</b> part, one on each side, and bring their leads out. Do not forget the <b>820 Ω resistor</b> in series with the pair - see <a href="#backlight">Backlight</a>. They have to go in before the part is screwed on in the next step.</td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>9.</b> Screw the <b>backlight</b> part on with 4× DH M3×8.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-09.png" alt="The backlight part screwed on with four M3x8 screws" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>10.</b> Press the second <b>MR63ZZ</b> bearing into the backlight part.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-10.png" alt="The second MR63ZZ bearing pressed into the backlight part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>11.</b> Push the <b>acrylic pipe</b> through both bearings. If it will not go, warm it with a hair dryer to soften it slightly. I used a 20 mm length.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-11.png" alt="The acrylic pipe pushed through both bearings" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>12.</b> From the front, glue the <b>L needle</b> onto the pipe with super glue.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-12.png" alt="The L needle glued onto the acrylic pipe from the front" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>13.</b> From the back, glue the <b>pipe gear</b> - 9 teeth, 3 mm high - onto the acrylic pipe.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-13.png" alt="The 3 mm pipe gear glued onto the acrylic pipe from the back" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>14.</b> Press the <b>MR52ZZ</b> bearing into the pipe gear.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-14.png" alt="The MR52ZZ bearing pressed into the pipe gear" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>15.</b> Push the <b>acrylic rod</b> through the MR52ZZ bearing and on down the inside of the pipe. I used 27 mm, but it is safer to cut it to length once it is in place.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-15.png" alt="The acrylic rod pushed through the bearing into the pipe" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>16.</b> From the front, glue the <b>R needle</b> onto the rod.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-16.png" alt="The R needle glued onto the acrylic rod from the front" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>17.</b> Glue the black <b>needle cap</b> onto the R needle.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-17.png" alt="The black cap glued onto the hub of the R needle" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>18.</b> Glue the <b>rod gear</b> - 9 teeth, 2 mm high - onto the acrylic rod.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-18.png" alt="The 2 mm rod gear glued onto the acrylic rod" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>19.</b> Put the gears cover with its two servos in place and screw it down with 2× DH M3×5.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-19.png" alt="The gears cover with both servos screwed onto the backlight part" width="380"></td>
</tr>
</tbody>
<tbody>
<tr>
<td width="55%"><b>20.</b> Push the white <b>LED</b> - the one with the 150 Ω resistor - into the hole between the two servos.</td>
<td align="center"><img src="../../images/panels/33-duct-pressure-step-20.png" alt="The white LED pushed into the hole between the two servos" width="380"></td>
</tr>
</tbody>
</table>
