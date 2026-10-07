# Fixes and open issues

## Fixes made
- **Shocker glowed at idle.** Its 5ch profile left ch 4-5 unmapped, which fired Auto Program. Fixed by moving it from 136 to 417 in 8ch Mode 3 (the unit was re-addressed).
- **F4 Scan360 315 did a slow strobe.** The profile's strobe range had R start 8. Changed it to 4 in Fixture Manager, since 4-7 = open. Then File > Save Workspace, then Options > Update Fixtures.
- **F4 lost its name and group** after that profile update. It was renamed "F4 Scan360 315" and set back to Mover Primary Group 2.
- **R1 182 lost its address and mode.** The fixture menu "Reset" was a factory reset. Re-entered 182 / 11CH.
- **L1 149's pool was fuzzy.** A fixture-menu reset fixed it, probably the gobo wheel position.
- **F2 300 was knocked.** Its mirror was hit, so it was reset and re-aimed.
- **Everything was lit with a purple tint.** Unplugging the Control One didn't help. Quitting and relaunching SoundSwitch did.
- **Stock Autoloops never moved the movers.** They had no working position cues. Bank 1 now has cues (see `calibration.md`).
- **Vortex was stuck on one look.** The "Vortex Show" static look runs its built-in program instead.

## Open issues
- **Black doesn't stop the Vortex (2026-10-06 demo).** With Vortex Show on, pressing Black on the Control One leaves the Vortex running. Likely cause: Vortex Show runs the fixture's built-in program (ch 7, Show 134), which seems to ignore the dimmer that Black pulls to 0. Ideas: once the Vortex has a color wheel in its profile, drive it from the Autoloops and Static Looks instead of its built-in show; or test whether Black also zeroes the shutter channel.
- **SoundSwitch froze after a save (2026-10-06 21:08)** with the Edit-mode File menu drawn open. Force Quit and relaunch fixed it, and nothing saved was lost.
- **The Vortex can't be colored by the Autoloops.** Its SoundSwitch profile exposes no color channels (the Color cell in Static Looks is blank). Barrel Rotation, Show and Reflector Rotation are attributes, and the Autoloops never animate them. To fix:
  - Map its color channels in Fixture Manager.
  - Add attribute cues in our own Autoloops.
  - Meanwhile, use Vortex Show.
- **Idle glow:** the Vortex 405 and the Scan 110s glow white at idle in Edit mode with nothing programmed. Their profiles are fully mapped. Next step is a DMX tester.
- **The hazer (141) doesn't respond to DMX.** Suspects are the wireless bridge and the DIP switches. Running it manually for now.
- **R3 204 is broken.** It's programmed and waiting for repair.
- **WiFLY name:** the WiFLY's name won't change in SoundSwitch.
- **Stray static looks:** "113" (twice) and "105" in Bank 4, "98" in Bank 4, and "1" in Bank 1.
- **QLC+** was looked at and ruled out (2026-10-07). See `qlcplus.md`.
