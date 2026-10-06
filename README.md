# Basement Nightclub - Lighting

Notes, calibration data and a 3D model for the lighting rig in a basement DJ room. The rig is run with **SoundSwitch 2.11** and a **Control One**, using about 20 DMX fixtures on one universe.

The rebuild started 2026-10-05. It works in this order:
1. **Map the room** and place every light in 3D. Done.
2. **Validate fixtures and DMX addresses.** Done.
3. **Calibrate the movers** to shared named positions, so they aim where you expect. In progress.
4. **Build the looks and Autoloops.** Next.

## The rig at a glance
| Where | Fixtures |
|---|---|
| Front bar, by the speakers | 2x Intimidator Spot 255 IRC, 2x Intimidator Scan 360, Mega 64 Profile Par (washes the speaker wall) |
| In front of the front bar | Eliminator Vortex moonflower, ADJ Inno Pocket Beam Q4 (lights a tiny mirror ball) |
| Ceiling, on the centerline | 4x Mega Tripar Profile Plus |
| Along both I-beams | 6x Intimidator Scan 110 (one is broken) |
| Back wall | Saber Spot Go on a 16" mirror ball |
| Speaker wall | Shocker Panel 180 strobe, Z-350 hazer |
| Lounge, behind the back wall | WiFLY Bar QA5 lighting the fireplace |

## Files
| Path | What it is |
|---|---|
| `CLAUDE.md` | Working rules, current state and the to-do list. Start here. |
| `notes/rig.md` | Room geometry, every fixture's position and DMX address, and the groups |
| `notes/calibration.md` | Named positions, crosshair values, Autoloop position cues, and how each fixture type aims |
| `notes/soundswitch-guide.md` | How SoundSwitch 2.11 actually works, plus the gotchas |
| `notes/fixes-and-issues.md` | Fixes made so far and open problems |
| `notes/session-log.md` | What happened, session by session |
| `model/basement-rig-map.html` | Interactive 3D model of the room and fixtures. Open it in a browser. It loads Three.js from a CDN. |

## Conventions
- **Viewpoint:** stand at the back (mirror-ball wall), facing the speakers. Left and right are from there.
- **Numbering starts at the front, by the speakers.**
- **Units:** inches. X is measured from the left I-beam, Y from the mirror-ball wall, and Z is height off the floor.
- **Fixture names:** prefix plus DMX start address. F = front bar, C = ceiling Tripar (C1 is nearest the speakers), L/R = left/right I-beam, W = speaker wall. Example: "L2 Scan 160".
