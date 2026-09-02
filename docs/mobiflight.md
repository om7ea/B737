# MobiFlight Configuration

The complete MobiFlight configuration for the overhead panel - the board definitions and the simulator mapping for every switch, button, LED, servo and display.

[← Back to main page](../README.md)

---

[📥 Download all configuration files - MobiFlight_Overhead.zip](https://raw.githubusercontent.com/om7ea/B737/main/MobiFlight/MobiFlight_Overhead.zip)

> **Read [Before you import](#before-you-import) first.** The configuration will not work on your hardware until you re-assign the boards - the files reference my boards by serial number.

---

## What Is In The Download

Eight files, all plain text - you can open any of them in a text editor.

| File | Format | Contents |
|---|---|---|
| `Overhead.mfproj` | MobiFlight Project (JSON) | The whole simulator mapping - 394 configurations |
| `Overhead_1a.mfmc` | Module Config (XML) | Board definition - which pin is a button, an LED, a servo |
| `Overhead_1b.mfmc` | Module Config (XML) | Board definition |
| `Overhead_2a.mfmc` | Module Config (XML) | Board definition |
| `Overhead_2b.mfmc` | Module Config (XML) | Board definition |
| `Overhead_3.mfmc` | Module Config (XML) | Board definition |
| `Overhead_4.mfmc` | Module Config (XML) | Board definition |
| `Overhead_5.mfmc` | Module Config (XML) | Board definition |

The two formats do different jobs and are used at different moments:

- A **`.mfmc`** file describes **the hardware on one board** - it is uploaded into the board's own memory, once, when you set the board up. Seven boards, seven files.
- The **`.mfproj`** file describes **what the hardware does in the simulator** - which PMDG variable each input triggers and which variable each LED follows. It stays on the PC and is opened in MobiFlight.

---

## Requirements

| | Requirement |
|---|---|
| **MobiFlight** | Version 11 or newer - the `.mfproj` project format does not exist in version 10 |
| **Simulator** | Microsoft Flight Simulator 2020 |
| **Aircraft** | PMDG 737-800. 295 of the input actions are PMDG event IDs, so the configuration is specific to this aircraft |
| **FSUIPC** | Required. Ten outputs read FSUIPC offsets directly and will stay dark without it |

---

## Before You Import

**MobiFlight identifies a board by its serial number, not by its name.** The files contain the serial numbers of my seven boards:

| Board | Serial number in the files |
|---|---|
| Overhead_1a | `SN-4F6-017` |
| Overhead_1b | `SN-7F0-2F8` |
| Overhead_2a | `SN-D8F-39D` |
| Overhead_2b | `SN-536-893` |
| Overhead_3 | `SN-9FB-4DA` |
| Overhead_4 | `SN-1FD-E25` |
| Overhead_5 | `SN-0F7-DFB` |

Your boards will have different serial numbers, so after opening the project **every configuration that drives hardware will show its board as missing**. This is expected and it is not a broken download. You have to point each configuration at your own board - MobiFlight can do this for a whole board at once, you do not have to edit 394 rows by hand.

Give your boards the same names (`Overhead_1a` … `Overhead_5`) before you start. It makes the re-assignment far easier to follow, because the board name is the only thing that connects a configuration to the hardware once the serial numbers no longer match.

---

## How To Import

1. **Set up the boards.** Connect one Mega 2560 PRO MINI, let MobiFlight upload its firmware, then load the matching `.mfmc` file into it and upload it to the board. Repeat for all seven. Do them one at a time - every board looks the same in the list until it has a name.
2. **Open the project.** `File → Open` and select `Overhead.mfproj`. All 394 configurations appear.
3. **Re-assign the boards.** See [Before you import](#before-you-import) above.
4. **Test without the simulator.** MobiFlight can send a test value to any output, which lights the LED on the desk. This is the fastest way to find a swapped patch cable before you go looking for the fault in the simulator.

---

## What The Configuration Contains

### Per board

| Board | Serial number | Configurations | Devices defined |
|---|---|---:|---|
| Overhead_1a | `SN-4F6-017` | 51 | 10× Button, 43× Output |
| Overhead_1b | `SN-7F0-2F8` | 35 | 20× Button, 18× Output, 1× Servo |
| Overhead_2a | `SN-D8F-39D` | 63 | 36× Button, 20× Output, 1× LED module, 1× Servo, 1× LCD display |
| Overhead_2b | `SN-536-893` | 67 | 38× Button, 27× Output, 2× Servo |
| Overhead_3 | `SN-9FB-4DA` | 53 | 45× Button, 5× Output, 2× Servo |
| Overhead_4 | `SN-1FD-E25` | 56 | 17× Button, 36× Output, 3× Servo |
| Overhead_5 | `SN-0F7-DFB` | 47 | 20× Button, 2× Encoder, 3× Analog input, 17× Output, 1× LED module, 3× Servo |

**Devices** are the physical things wired to a board, as defined in the `.mfmc` files - 372 in total. **Configurations** are the mappings in the project - 394 in total. The two numbers differ because one device can be used by more than one configuration: the two LED modules, for example, are driven by seven configurations between them, one per display field.

*Output* means a single LED channel - the annunciators. A toggle switch with a guard takes two Button entries, one for the switch and one for the guard.

### How inputs reach the simulator

| Action type | Count | |
|---|---:|---|
| PMDG event ID | 295 | The normal case - a switch fires the PMDG event for that lever |
| MSFS2020 custom input | 33 | For controls PMDG exposes as a custom event rather than an event ID |
| MobiFlight variable | 26 | Writes an internal variable, used where a control needs its own state |

A switch normally fires one action when it is pressed and another when it is released, so these counts are higher than the number of switches.

### How outputs read the simulator

| Source | Count | |
|---|---:|---|
| SimConnect | 173 | Reads a PMDG `L:` variable, e.g. `(L:switch_2256_73X, number)` |
| MobiFlight variable | 20 | Reads an internal variable set by an input |
| FSUIPC | 10 | Reads an FSUIPC offset directly |

---

## Notes

- **The configuration is complete.** It covers the whole overhead panel, including the panels whose models have not been published yet, and will not change as further models are released.
- **Panels are not split neatly one board per section.** The name of a configuration begins with the overhead section it belongs to (`Overhead_4_Oxygen panel_…`), which is *not* always the board that drives it - the Oxygen panel, for instance, is split between two boards. Which board drives a panel is in the **Wiring** section of that panel's [model page](models/README.md).
- **Twenty-two configurations have no board assigned.** This is intentional, not a gap. Sixteen of them are guarded switches: the physical switch writes an internal variable, and these entries turn that variable into the two PMDG events the guard and the lever need. The other six calculate a value that a servo or the IRS display then reads through a config reference - the two engine start servos, for example, take their position from them.
