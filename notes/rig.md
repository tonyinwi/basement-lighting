# Rig: room, fixtures, patch

## Room geometry
Units are inches. X is measured from the left I-beam, Y from the mirror-ball wall, and Z is height off the floor. Left and right are as seen from the back, facing the speakers.

| Item | Measurement |
|---|---|
| I-beam to I-beam | 187" (15'7"), centers |
| Mirror-ball wall to speaker wall | 378" (31'6") by laser. An earlier tape measure gave 30'10". |
| Joists | 86" (7'2") |
| I-beam bottoms | 76" (6'4"). The I-beam does not run all the way to the back wall. |
| Centerline | X 93.5", the Tripar line. Everything centers on it. |
| Mirror ball | 16" ball, top at 79", 12" off the left I-beam, at the back wall |
| Front bar | 16" (1'4") off the speaker wall (Y 362), bottom at 80" (6'8") |
| DJ booth | Off to the side. Not relevant to the rig. |

## Fixtures (Universe 1)
Listed from the front (speakers) toward the back.

| SoundSwitch name | Addr | Ch | Model | X | Y | Z | Mount / aim |
|---|---|---|---|---|---|---|---|
| W Shocker 417 | 417-424 | 8 (Mode 3) | Shocker Panel 180 USB | 93.5 | 376 | 48 | Under the center speaker, facing the room |
| W Haze 141 | 141-142 | 2 | Z-350 hazer | ~80 | ~370 | 12 | Floor next to the sub. Wireless DMX bridge. |
| F3 Mega64 126 | 126-134 | 9 | Mega 64 Profile Par | 94 | 369 | ~74 | Front bar, washing the speaker wall |
| F1 Spot 1 | 1-13 | 13 | Intimidator Spot 255 IRC | 60 | 362 | 69 | Front bar, hung upside down |
| F2 Scan360 300 | 300-313 | 14 | Intimidator Scan 360 (v2) | 74 | 362 | 72 | Front bar, mirror on top |
| F4 Scan360 315 | 315-326 | 12 | Intimidator Scan 360 Rev 2 (v4), custom profile "Intimidator Scan 360 Rev 2 tony" | 114 | 362 | 72 | Front bar, mirror on top |
| F5 Spot 14 | 14-26 | 13 | Intimidator Spot 255 IRC | 126 | 362 | 69 | Front bar, hung upside down |
| F Pocket Beam 27 | 27-39 | 13 (Mode 3) | ADJ Inno Pocket Beam Q4 (INN288) | ~38 | ~339 | <77 | Below the Vortex, about 1 ft toward the speaker wall. Lights the tiny mirror ball. |
| F Vortex 405 | 405-416 | 12 | Eliminator Vortex (VOR100) | ~38 | 327 | 77 | 2'11" in front of the front bar. Moonflower that throws beams everywhere. |
| C1 Tripar 64 | 64-73 | 10 | Mega Tripar Profile Plus | 93.5 | 251 | 86 | Joist bay, pointing down |
| C2 Tripar 74 | 74-83 | 10 | Mega Tripar Profile Plus | 93.5 | 187 | 86 | Joist bay, pointing down |
| C3 Tripar 84 | 84-93 | 10 | Mega Tripar Profile Plus | 93.5 | 123 | 86 | Joist bay, pointing down |
| C4 Tripar 94 | 94-103 | 10 | Mega Tripar Profile Plus | 93.5 | 59 | 86 | Joist bay, pointing down. The Tripars are spaced 64" apart. |
| L1 Scan 149 | 149-159 | 11 | Intimidator Scan 110 | 0 | 235 | 79 | Left I-beam, mirror toward the floor center |
| R1 Scan 182 | 182-192 | 11 | Intimidator Scan 110 | 187 | 235 | 79 | Right I-beam, opposite 149 |
| L2 Scan 160 | 160-170 | 11 | Intimidator Scan 110 | 0 | 175 | 79 | Left I-beam |
| R2 Scan 193 | 193-203 | 11 | Intimidator Scan 110 | 187 | 175 | 79 | Right I-beam, opposite 160 |
| L3 Scan 171 | 171-181 | 11 | Intimidator Scan 110 | 0 | 115 | 79 | Left I-beam |
| R3 Scan 204 | 204-214 | 11 | Intimidator Scan 110 | 187 | 115 | 79 | Right I-beam, opposite 171. **Broken**, but it stays in programming. |
| L Saber 52 | 52-63 | 12 | Saber Spot Go | 0 | 82 | 76 | Upright on the left I-beam, aimed back at the mirror ball |
| WiFLY Bar QA5 (lounge) | 104-125 | 22 | WiFLY Bar QA5 (wireless DMX) | ~96 | ~-56 | 86 | Lounge behind the back wall, on the joists, aimed left at the fireplace. Its name won't change in SoundSwitch. |

**Other details:**
- All Scan 110s hang at 6'7". They are spaced about 5' (60") apart along each beam.
- **Tiny mirror ball:** sits in front of the Fog Fury and is lit by the Pocket Beam. Its exact position hasn't been measured yet.

**Not patched:**
- **Pocket Rolls:** removed. One was moved to another part of the basement and should be re-added.
- **Laser** (to the right of Spot 14): not enabled and not patched.

## Groups
A pair shares a group. A one-off gets its own group.

| Type | Group | Fixtures |
|---|---|---|
| Mover Primary | G1 | F1 Spot 1, F5 Spot 14 |
| Mover Primary | G2 | F2 Scan360 300, F4 Scan360 315 |
| Mover Secondary | G1 | L1 149, R1 182 |
| Mover Secondary | G2 | L2 160, R2 193 |
| Mover Secondary | G3 | L3 171, R3 204 |
| Mover Tertiary | G1 | F Vortex 405 |
| Mover Tertiary | G2 | F Pocket Beam 27 |
| Spot Primary | G1 | L Saber 52 |
| Wash Primary | G1-G4 | C1 64, C2 74, C3 84, C4 94 |
| Wash Secondary | G1 | F3 Mega64 126 |
| Wash Tertiary | G1 | WiFLY Bar QA5 104 |
| Strobe/Blinder | G1 | W Shocker 417 |
| Smoke/Atmos | G1 | W Haze 141 |

## SoundSwitch project
- SoundSwitch 2.11 with a Control One.
- **Project file:** `/Users/tonyw/Dropbox/SoundSwitch/Claude.ssproj`
- **Venues:** the **disk venue** is the working copy. The **USB venue** is the Control One copy, which needs File > Export to Control One to update.
- **Saving:** fixtures, looks, positions and Autoloops save with **File > Save Project**, which only exists in Edit mode. Save Lightshow (Cmd-S) saves the current track's script.
