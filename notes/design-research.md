# Design research (2026-10-06 night)

Collected from Tony's references and a research pass. Use it with `stacks.md` and the rules in `CLAUDE.md`.

## From Tony
- **The orchestra (Facebook post Tony shared):** a rig is an orchestra, and the conductor doesn't have every musician play the whole concert. Use select instruments to build. The LD's best-received moment was a subtle wash, then half a dozen gobo spots sweeping slowly from the back of the house down to the conductor, stopping center at the height of the piece.
  - **Our version, "The Sweep":** a dim wash; the Scan 110s travel G3, G2, G1 (back to front), then all movers converge on Floor Center exactly at the drop.
- **Ultra Main Stage 2026 (Patrick Dierson, Chauvet post):** in each photo the whole stage is one coordinated palette: all fire-amber, all blue, or magenta + red. The architecture is drawn by the lights.
  - [Chauvet article](https://chauvetprofessional.com/news/tag-supplies-264-chauvet-professional-fixtures-for-patrick-diersons-ultra-main-stage-lighting-design/)
- **Mau P:** red + white, darkness between hits, the mirror-ball "mirrors" motif. **Carl Cox:** warm amber + white, long builds, spirals and fans only at the peak, and a cleaner, simpler look for big moments.

## Design rules (sources in the research report)
- **Palette:**
  - Two colors plus white at most per look.
  - Pairs that work: red + white, amber + magenta, congo blue + magenta, teal + magenta, amber + blue, deep blue + warm white, warm + cold white.
  - Change intensity rather than color within a song.
  - Avoid green washes and all-red on faces.
- **Haze:** saturated color goes on floor pools and walls (Tripars, Mega64). White or pale goes in the beams (Scan 110s, open-white Spots and Scan 360s).
- **Darkness is free.** "You can't have a light without a dark to stick it in" (Steve Lieberman, Carl Cox's Ultra designer). Don't reveal the whole rig early.
- **Layers:**
  - Wash: Tripars and Mega64
  - Beam: Scan 110s and Scan 360s
  - Texture: Spots with gobos
  - Sparkle: the balls
  - Effect: Vortex
  - Hit: Shocker
  - Use 1 lead and 1-2 supports per look. Everything else gets an explicit 0.
- **Tempo** (122-128 BPM, about 1.9 s per bar):
  - Groove: position changes every 4-8 bars with 1-2 bars of travel.
  - Peak: up to 1 movement cycle per bar.
  - Hold still in breakdowns.
  - Color changes only on 16/32-bar boundaries.
- **Strobe:**
  - Keep it at 4 flashes per second or fewer (UK HSE). At 128 BPM, 1/4-note strobe (2.1 Hz) is OK; 1/8 notes (4.3 Hz) is over the limit.
  - The Shocker faces the room at eye level, so keep it short and at peaks only.

## SoundSwitch technique
- **Track hierarchy:** the Main Track drives everything. Group and fixture tracks override it. **An empty track inherits the Main Track**, which is why the stock loops look all-on. For darkness, use an explicit intensity-0 override: right-click the selection > Create Intensity Override, which gives a flat 0 line. Confirmed 2026-10-06.
- **Wheel fixtures:** give them one solid color block for the whole loop. No color transitions or chases on them. If the color must change, do it on a phrase boundary while the light is at 0.
- **Slow color changes on RGB fixtures:** Apply Color Transition (Shift+T) across 8-32 bars.
- **Movement shapes** (Circle, H/V Scan, Ovals, Figure 8s, Square) ride between position cues. Give different groups different shapes for an organic ballyhoo.
- **Position cue at the loop wrap:** make the last cue match the bar-1 cue, so the movers don't snap.
- **Attribute cues are global presets.**
  - Gobo Change 1 = breakup (20)
  - Gobo Change 2 = swirl (28) with slow rotation
  - Gobo Change 3 = pink dot ring (12)
- **Lengths:**
  - 32 bars for most looks
  - 64 for builds
  - 16 for moments
- **Bank playback:** Sequential.
- **No crossfades between Autoloops:** build each handoff into the last bars of the loop.
- **Moments over the stack:** use Static Looks (One Beam, Mirror Ball, 841, Vortex Show).

## Sources
- [EDM.com, Ed Warren interview](https://edm.com/interviews/skrillex-fred-again-four-tet-msg-rave-how-ed-warren-designed-lighting-lasers/)
- [Chauvet, Chemistry of Color](https://chauvetprofessional.com/news/the-chemistry-of-color/)
- [Chauvet, Steve Lieberman](https://chauvetprofessional.com/news/steve-lieberman-inspired-light/)
- [Epilepsy Society, flicker limits](https://epilepsysociety.org.uk/node/3618)
- [SoundSwitch, Control Tracks](https://support.soundswitch.com/en/support/solutions/articles/69000847597-control-tracks-in-soundswitch)
- [Engine DJ forum, Autoloops all lights always on](https://community.enginedj.com/t/autoloops-all-lights-always-on/54542)
- [SoundSwitch, Color Transitions](https://support.soundswitch.com/en/support/solutions/articles/69000847584-soundswitch-utilizing-color-transitions)
- [SoundSwitch, Movement Shape Effects](https://support.soundswitch.com/en/support/solutions/articles/69000847396-soundswitch-movement-shape-effects)
- [SoundSwitch, Attribute Cues](https://support.soundswitch.com/en/support/solutions/articles/69000828942-soundswitch-controlling-gobo-prism-more-with-attribute-cues)
- [Ibiza Spotlight, Carl Cox at UNVRS](https://www.ibiza-spotlight.com/magazine/2025/06/carl-cox-raises-roof-his-unvrs-premiere)
- [Complex, Mau P Baddest Behaviour visuals](https://www.complex.com/music/a/complex/inside-the-visual-world-of-mau-p-baddest-behaviour-show-at-pacha)
