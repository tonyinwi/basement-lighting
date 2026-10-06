# Calibration and positions

## Method (repeat for each fixture or pair)
1. In Perform mode, go to Static Looks > Bank 4. Right-click **CAL Test** and choose Edit.
2. Set the fixture(s) under test to full intensity, white, and the position being worked on. Set everything else to 0.
3. Click **Edit Positions**. Select the position, then the fixture's row, set P/T invert if needed, and drag its dot.
4. Click **Apply**, then **OK**. **OK is what moves the light.** Check the camera, allowing about 5 s of lag.
5. Repeat until it's close. Tony then fine-tunes physically (left/right, up/down only).
6. Switch to Edit mode and **File > Save Project**. Do this after every fixture.

## Camera setup
- iPhone on a tripod on the centerline, about 1 ft behind C4, facing the speakers.
- Continuity Camera feed in Photo Booth on the Mac, side by side with SoundSwitch.
- **The image is mirrored:** the bar side shows on image left, and the L I-beam on image right.
- Photo Booth only refreshes while its window is visible. It pauses ("Click Photo Booth to resume") in the background.
- To align or debug, take one white capture per fixture, or give each fixture a different color.

## Invert settings and Floor Center results
| Fixture | Pan invert | Tilt invert | Floor Center | Notes |
|---|---|---|---|---|
| F1 Spot 1 | ON | off | DONE | Crosshair up = toward the speakers |
| F5 Spot 14 | ON | off | DONE | |
| F2 Scan360 300 | off | off | DONE | Mirror scanner. Up = toward the ball. |
| F4 Scan360 315 | off | off | DONE | Crosshair left = beam to the seating side |
| L1 Scan 149 | off | off | DONE | Crosshair right = pool toward the ball. Up = pool across toward the bar side. |
| R1 Scan 182 | ON | off | DONE | With pan invert on, it behaves like L1 |
| L2 Scan 160 | off | off | DONE | |
| R2 Scan 193 | ON | off | DONE | Overlaps L2 perfectly in one round pool |
| L3 Scan 171 | off | off | DONE | Physically fine-tuned against R2 |
| R3 Scan 204 | ON | off | programmed | Broken. Should land on Floor Center once it's repaired. |
| F Pocket Beam 27 | off | off | - | Moving head mounted upright. At grid center it points straight up. |

**Front bar check:** done one fixture at a time, anchored on F1 (pool about 5 ft wide). Spot 14, 300 and 315 were re-aimed physically, and all four now land within a few inches of F1.

**Physical aim rule for the front bar:** tip DOWN = pool toward the speakers, UP = toward the ball, left/right = across the floor.

## Named positions
| Position | Target | Status |
|---|---|---|
| Floor Center | Pool on the centerline, leading edge under C3 (pool center about Y 155). The shared target for every mover. | Camera-checked, physically fine-tuned |
| Front of Floor | Centerline, roughly under C1 (Y about 251) | Camera-checked. Every mover lands within about a pool-width. |
| Back of Floor | Centerline, roughly under C4 (Y about 59) | Calculated from geometry, not checked yet |
| Cross | L Scan 110s throw to the R half and R Scan 110s to the L half, so the beams make an X. The front bar swings across too. | Calculated from geometry, not checked yet |
| Tiny Ball | The Pocket Beam on the tiny mirror ball | Pocket Beam aimed by Tony. The other movers are left at center. |
| Lanes, Ball | Planned | - |

The Pocket Beam is on the tiny ball (429, 509) in **every** position, so it always lights it.

## Crosshair values (Edit Positions grid, screen pixels)
These were read off the grid on the MacBook's screen. The grid center is about (510, 404), and the grid spans about ±164 px. Use them as starting points, not DMX values.

| Fixture | Floor Center | Front of Floor | Back of Floor | Cross |
|---|---|---|---|---|
| F1 Spot 1 (pan inv) | 522, 412 | 530, 395 | 519, 419 | 531, 412 |
| F5 Spot 14 (pan inv) | 484, 405 | 474, 388 | 487, 412 | 475, 405 |
| F2 Scan360 300 | 537, 383 | 537, 397 | 537, 368 | 560, 383 |
| F4 Scan360 315 | 503, 404 | 503, 418 | 503, 389 | 480, 404 |
| L1 / R1 (R pan inv) | 582, 345 | 495, 345 | 621, 345 | 582, 331 |
| L2 / R2 (R pan inv) | 528, 345 | 446, 345 | 597, 345 | 528, 331 |
| L3 / R3 (R pan inv) | 474, 345 | 414, 345 | 559, 345 | 474, 331 |
| F Vortex 405 | center | center | center | center |
| F Pocket Beam 27 | 429, 509 | 429, 509 | 429, 509 | 429, 509 |

## How the crosshair moves each fixture type
- **Scan 110 (mirror scanner, I-beams):**
  - **Tilt** sets how far across the floor the pool lands. The centerline is Y 345 for every Scan 110. Up = further across, toward the far side.
  - **Pan** moves the pool along the room, at about 2 px per degree of beam swing. The offset from 510 is 2 x atan((fixture Y - target Y) / 122). This predicted Front of Floor on the first try.
  - Each R fixture copies its L partner's values, with pan invert ON.
- **Spot 255 (moving head, front bar):**
  - Up = toward the speakers, at about 1.4 px per degree of tilt.
  - To keep the pair overlapped when aiming closer to the front, spread their pan apart: F1 right, F5 left.
- **Scan 360 (mirror scanner, front bar):**
  - Pan right sends the pool across to the bar side, and also a little toward the speakers.
  - Down = toward the speakers, up = toward the ball. It's sensitive: 20 px up throws the pool about 6 ft.
- **Pocket Beam (moving head, upright):**
  - Center = straight up.
  - Down on the grid tilts it toward the seating.
  - With that tilt, moving right swung it toward the back wall, so left swings it the other way.
- **Vortex (moonflower):** there's nothing to aim. Pan just turns the barrel.

## Autoloop position cues (Bank 1)
Added 2026-10-06. Before this, the stock Autoloops had no working position cues, so the movers never moved. Abbreviations: FC = Floor Center, Front = Front of Floor, Back = Back of Floor.

| Autoloop | Cues |
|---|---|
| 1 | every 2 bars: FC, Cross, Front, Back, FC, Cross, Front, Back |
| 2 | bars 1/5/9/13: FC, Cross, Front, Cross |
| 3 | bars 1/5/9/13: Back, Front, Back, Front |
| 4 | every 2 bars: Cross, FC, Cross, FC, Cross, Front, Cross, Back |
| 5 | bars 1/5/9/13: Front, Cross, Back, Cross |
| 6 | every 2 bars: FC, Front, FC, Back, FC, Cross, FC, Cross |
| 7 | bars 1/5/9/13: Cross, Back, Cross, Front |
| 8 | bars 1/5/9/13: Back, Cross, Front, FC |

Banks 2-4 have no position cues yet.

## Calibration and show looks (Static Looks, Bank 4)
- **CAL Test (slot 1):** includes every fixture. Used to isolate one fixture at a time. Last state: the Vortex at full with Barrel Rotation 65, everything else at 0.
- **Vortex Show (row 1, slot 4):** includes only the Vortex. Full brightness, Barrel Rotation 65 (medium spin), Show 134 (a built-in program). Tony likes it. Run it alongside the Autoloops.
