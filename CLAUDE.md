# Basement Nightclub - lighting

Tony's basement DJ room lighting, run with SoundSwitch 2.11 and a Control One. The sound system is a separate repo (`tonyinwi/basement-sound`).

## Working rules
- **Ask before anything risky or hard to undo.** That includes deleting fixtures or looks, Options > Update Fixtures, Reset Default Autoloops, and Export to Control One.
- **Save after every fixture:** press OK, then File > Save Project. **Saving only works in Edit mode.** In Perform mode the File menu has no Save, and "Import from Control One" sits where Save would be. Don't click it.
- **Static Look Bank 4 is Claude's** for tests and calibration. Bank 1 Autoloops can be overwritten, since Tony will rebuild all the Autoloops anyway.
- **Tony moves fixtures by hand, and only left/right and up/down.** Everything else is done in software. When he says he'll "point it" or "move it", he usually means dragging the dot in SoundSwitch himself. Hand him the steps and keep off the Mac until he says done.
- Give directions by **DMX address**. Number and list fixtures **from the front (speakers)**. Describe the room **as seen from the back**, facing the speakers.
- Use regular hyphens in writing, not em dashes.
- After each session, update the notes and `notes/session-log.md`, then commit.

## Current state (2026-10-06)
- **Patch:** validated and named. Groups are set: a pair shares a group, and a one-off gets its own. Full table in `notes/rig.md`.
- **Positions:**
  - Floor Center and Front of Floor are camera-checked.
  - Tiny Ball has only the Pocket Beam aimed.
  - Back of Floor and Cross are camera-checked (2026-10-06). Cross is now a wide X with separate pools.
  - Lanes and Ball are done (2026-10-06). In Ball the Pocket Beam lights the big ball; it sits on the tiny ball in every other position.
  - "841 Logo" is done: Spot 1 throws the custom 841 gobo (value 36) onto the wall behind the bar, with a slow spin (Gobo Rotation 10). It aims Spot 1 only, so don't use it in Autoloops.
  - Spot 1 gobo map: `notes/calibration.md`.
- **Autoloops:**
  - All 8 in Bank 1 now have position cues, so their movers move.
  - Banks 2-4 still have no position cues.
  - The 32 Autoloops are still the stock "Dynamic" ones.
- **Static Look "841"** (Bank 4, row 2 slot 3) puts the spinning 841 logo on the wall behind the bar. Switch it on over any Autoloop.
- **Static Look "Mirror Ball"** (Bank 4, row 2 slot 4): Saber on the big ball, Pocket Beam on the little ball.
- **Static Look "Vortex Show"** (Bank 4) runs the Vortex's built-in program (Show 134) with a medium barrel spin. Switch it on alongside the Autoloops. The Autoloops can't change the Vortex by themselves.
- **Mac setup:**
  - Project file: `/Users/tonyw/Dropbox/SoundSwitch/Claude.ssproj`. Always use the **disk venue**. The USB venue is the Control One copy.
  - For calibration, the Ring "Dance floor" camera on the back wall faces the speakers. Claude watches its Live View in the Claude app's built-in browser (account.ring.com, signed in) and restarts it when it times out (about every 5 minutes). A phone photo from the back is best for checking overlap.

## Next up
0. **Tony's note:** pressing Black leaves the Vortex running when Vortex Show is on. See `notes/fixes-and-issues.md`.
1. Add Lanes and Ball cues to some Bank 1 Autoloops (they were cued before those positions existed).
2. **DJ booth:** now set up at the front of the dance floor, on the **left as seen from the back** (Tony's "stage right": his right when standing behind the front bar facing the room). Spot 1 can't aim at the booth (tried 2026-10-06). Tony will check whether he has a second 841 gobo; if so, it needs a fixture that can reach the booth (Spot 14 is worth testing first). An unused "DJ Booth" position and an empty look "99" (Bank 4, row 3 slot 1) are left over from the attempt and aren't saved yet.
3. Check L3 171 alone at Back of Floor and Cross.
4. Map the Vortex's color channels in Fixture Manager, so Autoloops can color it. Try more Show program values.
5. Add position cues to the Bank 2-4 Autoloops, or build the custom "Groove" Autoloop:
   - Tripars on a slow color wash
   - Movers easing between Floor Center and Front of Floor
   - Vortex spinning
   - Pocket Beam on the tiny ball
   - Saber on the big ball
   - No strobe
6. Cleanup:
   - Delete the stray looks: "113" (twice) and "105" in Bank 4, "98" in Bank 4 and "1" in Bank 1.
   - Set every fixture's signal-loss behavior to Blackout.
   - File > Export to Control One.
7. Hardware:
   - Repair R3 204 (it's already programmed).
   - Fix the hazer's DMX.
   - Re-add one Pocket Roll.
   - Consider another LED pinspot (or a pinhole gobo) for the big ball.
   - Measure where the tiny ball and the Fog Fury are, and add them to the 3D model.
   - Track down the idle glow on the Vortex and the Scan 110s.
8. Back up `Claude.ssproj` and the custom Fixture Manager profile ("Intimidator Scan 360 Rev 2 tony") into this repo.

## Files
- `notes/rig.md` - room geometry, fixtures, positions in the room, patch, groups
- `notes/calibration.md` - method, camera setup, results, named positions, crosshair values, Autoloop cues
- `notes/soundswitch-guide.md` - how the app works, plus the gotchas
- `notes/fixes-and-issues.md` - fixes made and open issues
- `notes/session-log.md` - timeline
- `model/basement-rig-map.html` - 3D model (Three.js). Fixture data is in the `FX` array, in inches.
