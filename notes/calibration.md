# Calibration and positions

## Method (repeat for each fixture or pair)
1. In Perform mode, go to Static Looks > Bank 4. Right-click **CAL Test** and choose Edit.
2. Set the fixture(s) under test to full intensity, white, and the position being worked on. Set everything else to 0.
3. Click **Edit Positions**. Select the position, then the fixture's row, set P/T invert if needed, and drag its dot.
4. Click **Apply**, then **OK**. **OK is what moves the light.** Check the camera, allowing about 5 s of lag.
5. Repeat until it's close. Tony then fine-tunes physically (left/right, up/down only).
6. Switch to Edit mode and **File > Save Project**. Do this after every fixture.

## Camera setup
- **Since 2026-10-06: Ring "Dance floor" camera** on the back wall, facing the speakers. Not mirrored: the L I-beam is on image left. Wide fisheye, night vision (black and white in the dark). Live View ends after about 5 minutes.
- **Watch it in Claude's built-in browser** (account.ring.com, already signed in): find the "Dance floor" Go Live button and click it, then take screenshots of the browser pane. Claude can restart Live View itself there. In Chrome, Claude can only look, not click.
- Earlier: iPhone on a tripod on the centerline, about 1 ft behind C4, with the Continuity Camera feed in Photo Booth. That image is mirrored (bar side on image left). Photo Booth only refreshes while its window is visible.
- A phone photo from the back of the room is the best check for overlap; the Ring fisheye squashes the far end of the floor.
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
| Back of Floor | Centerline, roughly under C4 (Y about 59) | Checked on the Ring camera 2026-10-06. Scan 110 tilt lowered (the L/R pairs were crossing past each other); spots tilted toward the ball. Fine-tune by eye still worth doing. |
| Cross | L Scan 110s throw to the R half and R Scan 110s to the L half, so the beams make an X. The front bar swings across too. | Checked on the Ring camera 2026-10-06 and widened: Scan 110 tilt raised 17 px, Spot pan spread 25 px more each way. Every pair now makes a clear X with two separate pools. |
| Tiny Ball | The Pocket Beam on the tiny mirror ball | Pocket Beam aimed by Tony. The other movers are left at center. |
| Lanes | Each Scan 110 throws straight across a short way, so its pool stays on its own side and the pools make two lanes down the sides. The front bar points down the centerline. | Checked with Tony's phone photo 2026-10-06. The first try (Scan 110 tilt Y 369 old frame) landed too close to the centerline; lowered 25 px (L3/R3 35 px). |
| Ball | The big mirror ball at the back wall, by the left I-beam. Pocket Beam on the ball; the Saber (52) already lights it. Other movers stay at Floor Center. | Done 2026-10-06. Spot 255 beams are too wide for the ball (no iris, no tight-dot gobo), so the Spots stay at Floor Center. The first Pocket Beam aim was 180° off (it hit the block wall beside it); after swinging the pan 180°, Tony dragged it onto the ball himself. The little ball still lines up perfectly in the other positions. |
| 841 Logo | Spot 1 with the custom 841 gobo (value 36) on the white block wall behind the bar, spinning slowly (Gobo Rotation 10, about one turn every 9 s). | Done 2026-10-06; Tony: "Perfect." The plan was the floor in front of the speakers, but the logo wouldn't focus well on the floor, so Tony aimed it at the bar's back wall himself and focused it. Spot 1 crosshair: 578, 471 (old frame). The slow spin means it reads upright once per turn; to hold it still and upright, turn the gobo 180° in its holder. Only Spot 1 is aimed: every other mover sits at grid center in this position, so don't use it in an Autoloop. |
| (idea) Mini bar | A Spot on the mini bar. Tony may turn the mini bar into a DJ booth, which would change what this position should light. | Later |

The Pocket Beam is on the tiny ball (429, 509) in **every** position, so it always lights it.

## Crosshair values (Edit Positions grid, screen pixels)
These were read off the grid on the MacBook's screen. The grid center is about (510, 404), and the grid spans about ±164 px. Use them as starting points, not DMX values. They are relative to the dialog's position: if the SoundSwitch window moves, shift them by the same amount (on 2026-10-06 the window sat 25 px lower, so every Y was +25).

All values below are in the old frame (grid center about 510, 404). In the 2026-10-06 window position, add 25 to every Y.

| Fixture | Floor Center | Front of Floor | Back of Floor | Cross | Lanes |
|---|---|---|---|---|---|
| F1 Spot 1 (pan inv) | 522, 412 | 530, 395 | 519, 426 | 556, 411 | 498, 395 |
| F5 Spot 14 (pan inv) | 484, 405 | 474, 388 | 487, 419 | 449, 404 | 506, 388 |
| F2 Scan360 300 | 537, 383 | 537, 397 | 537, 368 | 560, 383 | 520, 397 |
| F4 Scan360 315 | 503, 404 | 503, 418 | 503, 389 | 480, 404 | 520, 418 |
| L1 / R1 (R pan inv) | 582, 345 | 495, 345 | 621, 363 | 582, 313 | 510, 393 |
| L2 / R2 (R pan inv) | 528, 345 | 446, 345 | 597, 357 | 528, 313 | 510, 393 |
| L3 / R3 (R pan inv) | 474, 345 | 414, 345 | 559, 349 | 474, 313 | 510, 403 |

Ball uses the Floor Center values for every mover except the Pocket Beam (first aim 561, 512, not yet confirmed on the ball).

Back of Floor lesson: the Scan 110 centerline tilt (Y 345) only holds for targets near the middle of the room. For targets far down the room the beam is longer, so the same tilt overshoots across the floor and the L and R pools pass each other. Lower the tilt the further along the room the target is (L1/R1 at Back of Floor needed about +18 px).
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
  - Pan is about 0.6 px per degree, so **108 px of pan = 180°**. With the head tilted down about 90° (Y about 108 px below center), right of center at X 561 pointed at the block wall beside it, and X 452 swung it around toward the big ball at the back wall.
  - Small physical or software tweaks barely move it on the little ball (close by) but decide whether it hits the big ball 28 ft away.
- **Positions vs physical aim:** a position stores pan/tilt relative to the fixture's mount. Turning a fixture by hand shifts every position for that light, and the far targets move most. Physical aiming is right for a light's first position and small trims, followed by a check of its other positions. Driving the dot in Edit Positions changes only that one position.
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

## Spot 255 gobo wheel (F1 Spot 1)
Identified 2026-10-06 from a slot-by-slot sweep Tony filmed, and matched to the Chauvet manual (13ch mode). The SoundSwitch Gobo Wheel attribute takes raw DMX (0-255). Each slot is 8 values wide, so use the middle of a range.

| DMX | Gobo | Tony's take |
|---|---|---|
| 0-7 (use 4) | Open | |
| 8-15 (use 12) | Gobo 1: pink dot ring (colored glass, 8 dots in a ring) | Useful, and it can overlap with the other spot |
| 16-23 (use 20) | Gobo 2: shattered / breakup | |
| 24-31 (use 28) | Gobo 3: swirl (3-arm galaxy) | |
| 32-39 (use 36) | Gobo 4: **841 logo** - custom, "841 STUDIO" with a triangle and swoosh. The basement's nickname. Spot 1 only. | Signature piece |
| 40-47 (use 44) | Gobo 5: rose / spiral rings | |
| 48-55 (use 52) | Gobo 6: diamond grid | |
| 56-63 (use 60) | Gobo 7: dense dot field | |
| 64-119 | Shake, gobo 7 down to gobo 1 (8 values each, slow to fast) | Not useful |
| 120-127 | Open | |
| 128-191 / 192-255 | Wheel cycle / reverse cycle, speeding up | |

- **Gobo Rotation** (ch 8): 0-7 off, 8-119 spin, 120-231 reverse spin, 232-255 bounce. **There's no indexing** (no fixed angles), so the channel can't hold the logo upright.
- **Gobo Rotation 10** (near the slow end) turns the 841 logo about once every 9 s. Tony liked it.
- **The 841 logo projects upside down** on the bar's back wall when it isn't spinning (2026-10-06 photo). The fix is physical: unplug the fixture, open the gobo access cover, pull the 841 holder, and turn the gobo 180° in it. Turn it; don't flip it over, or the text mirrors. The full steps are in the Chauvet manual.
- An earlier quick pass seemed to show 10 = open. The slot-by-slot sweep and the manual are the ones to trust.
- None of the gobos gives a tight single dot, so the big ball needs the Pocket Beam, the Saber, or a new LED pinspot.
- Spot 14's wheel hasn't been checked; it doesn't have the 841 gobo.
- Source: [Intimidator Spot 255 IRC user manual, Rev. 4](https://www.chauvetdj.com/wp-content/uploads/2016/01/Intimidator_Spot_255_IRC_UM_Rev4.pdf)

## Calibration and show looks (Static Looks, Bank 4)
- **CAL Test (slot 1):** includes every fixture. Used to isolate one fixture at a time. Last state: the Vortex at full with Barrel Rotation 65, everything else at 0.
- **841 (row 2, slot 3):** Spot 1 only. White, full, 841 Logo position, Gobo Wheel 36 (841 logo), Gobo Rotation 10 (slow spin). Puts the spinning logo on the wall behind the bar. Switch it on over any Autoloop. Made 2026-10-06.
- **Mirror Ball (row 2, slot 4):** the Saber (52) on the big ball and the Pocket Beam (27) on the little ball (Tiny Ball position), both white at full. Tony: "perfect". Made 2026-10-06. Tony first tried the Pocket Beam on the big ball (Ball position), then chose the little ball for this look.
- **Vortex Show (row 1, slot 4):** includes only the Vortex. Full brightness, Barrel Rotation 65 (medium spin), Show 134 (a built-in program). Tony likes it. Run it alongside the Autoloops.
- **Vortex Slow / Medium / Fast (row 4, slots 1-3), made 2026-10-07:** copies of Vortex Show with the Vortex's **Show Speed** attribute ticked (it was already in the profile, so no Fixture Manager change was needed). Same Show 134 in all three.
  - Slow: Show Speed 10, Barrel Rotation 110 (slow CCW).
  - Medium: Show Speed 120, Barrel Rotation 65 (as Vortex Show).
  - Fast: Show Speed 230, Barrel Rotation 30 (fast CCW).
  - Manual: ch8 Show Speed runs slow to fast; barrel CCW 10-120 is fast to slow.
  - **Not yet seen on the light.** If Slow still looks busy, lower the barrel further (closer to 120) or try another Show value.
- **841 Fade (row 3, slot 2), made 2026-10-07:** a copy of "841" with Fade In 2 s and Fade Out 2 s, so the logo breathes on and off when switched instead of snapping. A static look can't pulse by itself (no pulse or intensity-effect option in the look editor), so the beat-synced **pulsing logo lives in Autoloop Bank 3 slot 7, "R2 7 841 Breakdown"**.
  - **Checked the Spot 255 IRC's own DMX (2026-10-08):** 13ch mode has ch10 Dimmer 0-255 and ch11 Shutter: 0-3 closed, 4-7 open, 8-215 strobe (slow to fast), 216-255 open. There's no pulse or ramp range, so the fixture can't pulse the logo by itself. The nearest is the slowest strobe (about 8), which is a hard blink, not a fade, and isn't tied to the beat. Source: [Spot 255 IRC Quick Reference Guide](https://www.fullcompass.com/common/files/32374-ChauvetIntimidatorSpot255IRCQuickReferenceGuide.pdf).
