# QLC+ as an alternative to SoundSwitch (researched 2026-10-07)

**Decision (Tony, 2026-10-07): not going there.** After reading up, he found it "kind of a hot mess". Studio 841 stays on SoundSwitch and the Control One. This page is kept for reference only.

## Facts
- **QLC+** is free and open source (Apache 2.0). Version 5.1.0 came out on 2026-01-05.
- 5.1 adds an experimental audio beat tracker, plus Virtual Console XY pad and audio-trigger widgets.
- 3D rendering on Intel Macs was restored in 5.1, but "performances might be bad".
- **DJ software sync:**
  - **OS2L:** only VirtualDJ sends it. It carries beats and pad/button commands, not BPM. Needs QLC+ 4.12.2 or later.
  - **MIDI beat clock** input (channels 530 and 531) has been supported since 4.5.0.
  - **No Ableton Link.** The developer has declined it over licensing.
  - **Engine DJ, Serato, rekordbox and djay** have no direct link. They'd need MIDI clock out or a Link-to-MIDI bridge.
- **Control One in QLC+:**
  - There's no native support. The Control One's USB DMX output is proprietary.
  - A community project, jloops412/qlcplus-soundswitch-integration, adds Control One and Micro DMX output, MIDI and LED feedback. It's **Windows x64 only**, alpha (V26), pinned to one QLC+ build, and the author says it is "not yet gig-qualified".
  - On the Mac, QLC+ needs its own supported interface, such as an Enttec DMX USB Pro, a DMXking ultraDMX or an Art-Net node.

## Sources
- [QLC+ OS2L plugin docs](https://docs.qlcplus.org/v4/plugins/os2l)
- [VirtualDJ wiki: QLC with OS2L](https://virtualdj.com/wiki/QLC%20with%20OS2L.html)
- [QLC+ MIDI plugin docs (beat clock)](https://docs.qlcplus.org/v5/plugins/midi)
- [QLC+ 5.1.0 release notes](https://qlcplus.org/news/qlc-5-1-0-release)
- [QLC+ forum: Ableton Link request](https://forum.qlcplus.org/viewtopic.php?p=55549)
- [qlcplus-soundswitch-integration (GitHub)](https://github.com/jloops412/qlcplus-soundswitch-integration)
