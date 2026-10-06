# How SoundSwitch works (v2.11 on the MacBook)
Learned by driving it on 2026-10-05 and 2026-10-06. Screen positions assume the SoundSwitch window is on the left with Photo Booth beside it.

## Two modes
- **Edit mode** is for building. It has:
  - the full menu bar: File, Edit, Sound, Insert, View, Options, MIDI, Automation
  - the timeline, the Library panel, the toolbar, the DMX patch and the Autoloop editor
  - **File > Save Project. Edit mode is the only place you can save.**
- **Perform mode** is for running the show.
  - Its File menu is short: Open Project, Import from Control One, Switch Mode. **There's no Save.**
  - Tabs: Performance Mode, Autoloops, Static Looks, Edit Mode, External Mixer, Standalone. The Edit Mode tab has live Pan/Tilt dials and Hot Key Pulses.
  - The **Done** button at the bottom right drops you back to Edit mode.
- **To switch:** File > Switch Mode shows a big "Edit" / "Perform" chooser. Perform then asks for a venue. Pick the **left (drive icon) venue = the disk venue**. The right one (USB icon) is the Control One copy.
- **Usual loop:** edit Static Looks and positions in Perform. Then File > Switch Mode > Edit > File > Save Project. Then Switch Mode > Perform again.

## Edit mode layout
- **Toolbar, left to right:**
  - back, undo, redo, save, Q
  - grid icon: this opens the **Color Picker**, not the patch
  - dimmer bar, color wheel, ruler
  - link, add track, mixer, align, eye
  - **DMX: opens the DMX patch**
  - AUTO
  - zoom - / +
- **Library panel (left):**
  - Music: Local Files, iTunes, Virtual DJ
  - Effects: Intensity, Color, Chase, Color Palettes, Position, Strobe, Drops, Build Ups, Break Downs, Movement. Drag these onto tracks.
  - **Positions:** the named positions. **+** > Create Position Cue adds one. Double-click a position to open the Positions window.
  - Attribute Cues: Gobo Change 1-3, Custom Cue 1-5, smoke
- **Right column:** fixture tracks with M/S (mute/solo), plus the Main Track.
- **Bottom right:**
  - **A** opens the Autoloop banks: Bank 1 Dynamic, Bank 2 Upbeat, Bank 3 Smooth, Bank 4 Random, 8 Autoloops each, 16 bars long. **Double-click a slot to open it in the timeline.**
  - **S** is presumably scripted tracks.
  - Transport buttons.
- **Top bar:**
  - The top-left icon is Select Source: Ableton Link, BPM Detection, MIDI, PRO DJ Link, DJ Software (Virtual DJ).
  - BPM Detection toggle and BPM readout.
  - CONTROL ONE with a Connected badge.
  - **Gear = Preferences:** General, Library, Tempo Detection, Performance Mode, Hardware, User Account.
- **Options menu:** Lock Beatgrid, Scroll Wheel Zoom, Snap to Beatgrid, **Update Fixtures** (save first, it can crash to home), Reset Default Autoloops, Populate Empty Autoloops, Reset Track Names, Rebuild TrackMap.
- **Window:** if the window gets wider than the screen, **Option-click the green button** to fit it. A plain double-click on the title bar minimizes it.

## DMX patch (Edit mode > DMX)
- **Address grid:** universe tabs are on the left edge. The fixture list on the right shows each fixture's **type dropdown** and its **Group1-4 buttons**.
- **Adding a fixture:** the Fixture Library is at the bottom.
  1. Search the manufacturer, for example "American DJ".
  2. Search the fixture, for example "Pocket Beam".
  3. Click the mode row, then **Add Fixture**. It lands on the first free address. You can also drag it onto the grid at the right address.
- **Rename or re-address:** double-click a fixture's name in the right list. That opens a dialog with Name and DMX Address.
- The right list only scrolls with the mouse over its lower part. Its last rows can hide behind the Fixture Library, so scroll down hard. The Fixture Library divider can be dragged.
- **Done** closes the patch.

## Fixture Manager (separate app)
- Profiles have attribute, channel and range, but **no default values**.
- After editing a profile:
  1. File > Save Workspace in Fixture Manager.
  2. Options > Update Fixtures in SoundSwitch. **Save the project first**, because this can crash to the home screen, and it can also reset fixture names and groups.

## Static Looks (Perform > Static Looks)
- **Banks:** 4 banks x 32 slots. **Bank 4 is Claude's.**
- **Creating a look:** clicking an empty "+" slot instantly creates a look named with a number (for example "121"). That's where the stray "113", "105", "98" and "1" looks came from.
- **Slot menu:** right-click a slot for Press Mode / Map / **Edit** / Copy / MIDI Output Color / Delete. Click a slot to switch it on or off.
- **Static Look Settings window:**
  - The name field is at the top left.
  - Rows are grouped by fixture model. The triangle collapses a group, which you'll need to reach the bottom rows.
  - Columns: include checkbox, **Color**, **Intensity** slider, **Position** dropdown, **Movement** dropdown, Strobe, plus an Attributes panel.
  - A new look includes no fixtures. Tick the ones you want.
  - **Color:** double-click the swatch to open the Color Picker. White is in the Recent swatches. Click Apply.
  - **Position:** THRU means no position control. Otherwise pick a named position.
  - **Attributes:** click a fixture's name to show them on the right, for example the Vortex's Barrel Rotation and Show.
- **Edit Positions** (button at the top right of the look settings):
  - Every mover appears as a dot on a grid. A hollow dot is the mirrored output of a pan-inverted fixture.
  - The fixture list has the P/T invert toggles. The Position list has **+** to add a position, and you double-click a position to rename it. A new position starts with every fixture at the grid center.
  - To aim: select the position, select the fixture, drag its dot, click **Apply**, then **OK**. **OK is what sends the move to the light.**
- **Active Static Looks panel:** the eye icon toggles a look. **Clear all** turns every static look off. An active static look overrides the Autoloops on the fixtures it includes.

## Autoloops
- **Perform > Autoloops:** banks 1-4 with 8 each, Play All Banks, Previous / Repeat / Next, Override Scripted Tracks, Sequential / Random. Click a bank header to play that bank, or click an Autoloop to start there.
- **They need a beat source:** music in Virtual DJ (OS2L), or the BPM Detection toggle (top left) listening to the room.
- **Editing (Edit mode):**
  1. Press A, then double-click a slot to open it in the timeline.
  2. The Main Track shows intensity pulses and the color bar.
  3. **Drag a position from the Positions panel onto the Main Track** at the bar you want. A small flag appears in the lane just above the bar ruler, and the movers go there at that bar.
  - The colored squares higher up in the Main Track are attribute cues, not positions.
  - From the official guide: select a range in the Main Track, then right-click > Change Color. Double-click to set the playhead, and press Space to play.

## Gotchas
- **Colors:** a Static Look's color defaults to 0,0,0, which is dark. **Always set white.**
- **Sliders:** a Static Look slider must be moved before a 0 actually sends. Push it up, then back down.
- **Black** on the Control One overrides everything.
- **Mirror scanners:** pan and tilt map to unexpected room axes, so check each model. The R side of a mirrored-mount pair needs pan invert.
- **Fixture "Reset":** the menu Reset on a Scan 110 can be a factory reset. **Re-check the address and mode after any reset.**
- **Finding a stray light:** deleting a fixture from the patch turns it off, which helps find what's driving a stray light.
- **Mac overlay:** the Mac's "Ring Light Helper" (Edge Light) overlay blocks clicks. Turn it off.
- **Focus:** if SoundSwitch isn't the focused window, the first click only focuses it, and the next click lands somewhere else. Verify that an editor actually opened before dragging, or the drags land on the look grid.
- **Perform File menu:** "Import from Control One" sits right where Save Project sits in Edit mode. A mis-click on 2026-10-05 probably triggered it. The only visible effect was an extra "113" look.
- **Photo Booth** pauses in the background. Bring it forward to refresh.
