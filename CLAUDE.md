# Basement Nightclub - lighting

Tony's basement DJ room lighting, run with SoundSwitch 2.11 and a Control One. The sound system is a separate repo (`tonyinwi/basement-sound`).

## Working rules
- **Ask before anything risky or hard to undo.** That includes deleting fixtures or looks, Options > Update Fixtures, Reset Default Autoloops, and Export to Control One.
- **Save after every fixture:** press OK, then File > Save Project. **Saving only works in Edit mode.** In Perform mode the File menu has no Save, and "Import from Control One" sits where Save would be. Don't click it.
- **Static Look Bank 4 is Claude's** for tests and calibration. Bank 1 Autoloops can be overwritten, since Tony will rebuild all the Autoloops anyway.
- **Tony moves fixtures by hand, and only left/right and up/down.** Everything else is done in software.
- Give directions by **DMX address**. Number and list fixtures **from the front (speakers)**. Describe the room **as seen from the back**, facing the speakers.
- Use regular hyphens in writing, not em dashes.
- After each session, update the notes and `notes/session-log.md`, then commit.

## Current state (2026-10-06)
- **Patch:** validated and named. Groups are set: a pair shares a group, and a one-off gets its own. Full table in `notes/rig.md`.
- **Positions:**
  - Floor Center and Front of Floor are camera-checked.
  - Tiny Ball has only the Pocket Beam aimed.
  - Back of Floor and Cross were calculated from the geometry and haven't been checked yet.
  - The Pocket Beam sits on the tiny ball in every position.
- **Autoloops:**
  - All 8 in Bank 1 now have position cues, so their movers move.
  - Banks 2-4 still have no position cues.
  - The 32 Autoloops are still the stock "Dynamic" ones.
- **Static Look "Vortex Show"** (Bank 4) runs the Vortex's built-in program (Show 134) with a medium barrel spin. Switch it on alongside the Autoloops. The Autoloops can't change the Vortex by themselves.
- **Mac setup:**
  - Project file: `/Users/tonyw/Dropbox/SoundSwitch/Claude.ssproj`. Always use the **disk venue**. The USB venue is the Control One copy.
  - For calibration, an iPhone on a tripod behind C4 faces the speakers. Its Continuity Camera feed shows in Photo Booth (the image is mirrored).

## Next up
1. Check Back of Floor and Cross on camera, and fine-tune them.
2. Add the Lanes and Ball (big mirror ball) positions.
3. Map the Vortex's color channels in Fixture Manager, so Autoloops can color it. Try more Show program values.
4. Add position cues to the Bank 2-4 Autoloops, or build the custom "Groove" Autoloop:
   - Tripars on a slow color wash
   - Movers easing between Floor Center and Front of Floor
   - Vortex spinning
   - Pocket Beam on the tiny ball
   - Saber on the big ball
   - No strobe
5. Cleanup:
   - Delete the stray looks: "113" (twice) and "105" in Bank 4, "98" in Bank 4 and "1" in Bank 1.
   - Set every fixture's signal-loss behavior to Blackout.
   - File > Export to Control One.
6. Hardware:
   - Repair R3 204 (it's already programmed).
   - Fix the hazer's DMX.
   - Re-add one Pocket Roll.
   - Measure where the tiny ball and the Fog Fury are, and add them to the 3D model.
   - Track down the idle glow on the Vortex and the Scan 110s.
7. Back up `Claude.ssproj` and the custom Fixture Manager profile ("Intimidator Scan 360 Rev 2 tony") into this repo.

## Files
- `notes/rig.md` - room geometry, fixtures, positions in the room, patch, groups
- `notes/calibration.md` - method, camera setup, results, named positions, crosshair values, Autoloop cues
- `notes/soundswitch-guide.md` - how the app works, plus the gotchas
- `notes/fixes-and-issues.md` - fixes made and open issues
- `notes/session-log.md` - timeline
- `model/basement-rig-map.html` - 3D model (Three.js). Fixture data is in the `FX` array, in inches.
