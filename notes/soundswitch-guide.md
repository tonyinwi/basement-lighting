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
  - **A** opens the Autoloop panel. **There are 4 banks of 32 Autoloops each** (Bank 1 Dynamic, Bank 2 Upbeat, Bank 3 Smooth, Bank 4 Random), 128 in total (since 2.9). The panel shows the current bank's 32 slots in 4 columns of 8. **Click a bank's name to switch banks.** The column headers are easy to misread as four banks. The editor's top right confirms which bank you're in (for example "Bank 1 : Dynamic / 16 Bars"). **Double-click a slot to open it in the timeline.**
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
  - **Live preview:** while the Positions window is open, clicking a position in its list moves every mover to that position live, and dragging a dot moves that light live. Closing the window sends each fixture back to the position picked in its look's dropdown. So Tony may see lights jump around while positions are edited.
  - **Cancel doesn't undo +:** a position added with + stays in the list even if you Cancel the Positions window.
  - **Stacked dots:** a new position puts every fixture at grid center. A drag grabs the topmost dot there, whichever fixture row is selected. Move dots one at a time and check which fixture got selected.
  - The Position dropdown in a look lists THRU, the positions in creation order, and any new one at the bottom.
- **Typing an attribute value:** double-click the number next to an attribute slider (for example Gobo Wheel), press Cmd-A, type the value, then Return. That's more precise than the short slider, which runs 0-255.
- **Active Static Looks panel:** the eye icon toggles a look. **Clear all** turns every static look off. An active static look overrides the Autoloops on the fixtures it includes.

## How positions, looks and Autoloops fit together
- **A named position stores one aim for every mover**, like a snapshot. A new position starts every mover at grid center.
- **Static looks pick a position per fixture** (the Position dropdown on each row), and only the fixtures ticked in the look are touched. So looks can mix positions and be layered.
- **An active static look overrides the Autoloop only for the fixtures it includes.** Everything else keeps following the Autoloop. Example: "841" takes over Spot 1 while the Autoloop runs the rest.
- **An Autoloop position cue on the Main Track sends every mover to that position at once.** So any position an Autoloop uses needs a sensible aim for every mover. That's why the Pocket Beam sits on the tiny ball in Floor Center, Front, Back, Cross and Lanes.
- **Positions only used by static looks** (841 Logo, Tiny Ball) only need the lights in that look aimed. The rest can stay at center.
- Not yet checked: whether an Autoloop can give one fixture its own position cue.

## Building Autoloops by hand (learned 2026-10-06 night)
- **Open:** press A, then double-click a slot. The timeline shows the Main Track at the bottom and a track for every fixture or group on the right. Collapse groups with their folder icon so the list fits.
- **Wipe the stock loop:** right-click the Main Track > Select All, then Edit > Clear (Cmd-Backspace). Attribute cues (the small colored squares) stay; select one and press Backspace to remove it.
- **Color:** drag-select a range on a lane (the colored strip is the color lane), then right-click > Apply Color or Apply Color Transition. Type R/G/B in the picker, then Apply.
- **Intensity effects:** drag-select a range, then **double-click** the effect in Effects > Intensity. Dragging the effect onto the track is unreliable. A dialog asks for depth (minimum 10%) and beat length (1/32 to 1 bar).
  - **Smooth Pulse** is 0 on each beat and peaks between beats, so at 1/4 it lands on the **offbeat** (the hats).
  - **Flash And Fade** at 1/4 hits **on the beat** (the kick) and decays.
  - On a group track, a prompt asks "Selected Tracks" or "Group". **Group** writes the effect onto every member track.
- **Make a light go dark:** select a range on its track, then press **Shift+O** (Create Intensity Override). That gives a flat 0 line, which overrides the Main Track. An empty track inherits the Main Track, which is why stock loops look all-on.
- **Remove an override:** select the range and press **Shift+Cmd+Delete**. That clears the track's data and overrides, so it inherits again.
- **Positions:** drag a position from the Positions panel onto the lane just above the bar ruler.
- **Rename / Delete / Duplicate:** right-click the Autoloop slot. Duplicate fails when all 128 slots are full, so delete a stock loop first. Deleting shifts every later loop up one slot across banks. A duplicate lands in the last slot; drag it to where you want it.
- **Save:** Cmd-S saves the project in Edit mode, and the "Saving Project / Completed" dialog confirms it.
- **The Main Track needs its own color.** A loop copied after clearing can end up with no Main Track color at all; then lights without their own color get no defined color. Fix: right-click the Main Track color lane (just above the position lane) > Select Color Track, then right-click > Apply Color.
- **Delete Override:** right-click a selection on a track that has an override; the menu shows **Delete Override**.
- **Movement effects:** select a range on a mover track, right-click > Apply Movement Effect. Shapes: Circle, Scan Horizontal/Vertical, Oval Horizontal/Vertical, Figure 8 Horizontal/Vertical, Square, Triple 8 Horizontal/Vertical. Size and Speed each have a start and end handle (ramps). **Reverse** flips the direction, so a pair can circle against each other.
- **Group scope:** a zero override on a collapsed group header blacks out the whole group, and a member track with its own data overrides the group.
- **Position cue at bar 1:** drag the position onto the lane just above the bar ruler, at bar 1 (x about 244 with the current window).
- **Still to figure out:** setting a steady, non-pulsing level (the override line wouldn't drag).

## More Autoloop technique (learned 2026-10-07 night)
- **Autoloop panel layout (confirmed):** the header row "Bank 1 : Dynamic | Bank 2 : Upbeat | Bank 3 : Smooth | Bank 4 : Random" is the **bank selector**. Below it are the selected bank's 32 slots in 8 columns of 4, so slots 9-16 sit under the "Bank 2" header even when Bank 1 is selected. The editor's top right ("Bank 3 : Smooth / 16 Bars") names the real bank.
- **Rename a slot:** right-click it > Rename, then Cmd-A, type, Return. The first time after opening a loop, the menu sometimes appears without the field going into edit; open the menu again.
- **Autoscript dialog:** the AUTO button. See `autoscript.md`. In the Positions and Attribute Cues tables, **clicking a Main 1 / Main 2 number cycles it** (0 = unused, then 1, 2 ...). It remembers the last loop's settings.
- **Position Override for one fixture (Shift+P):** select a range on the fixture's track, right-click > Create Position Override, then drag a position from the Positions panel onto that track. That fixture follows its own position while the rest follow the Main Track. Used for Spot 1 on 841 Logo.
- **New attribute cue:** the + next to "Attribute Cues" > Create Attribute Cue adds "New Attributes Cue" at the bottom of the list. Right-click > Rename Attributes Cue. Double-click it to edit: pick a fixture on the left, tick an attribute, double-click its number to type a value, then Apply. Cues are global presets; drag one onto the Main Track's cue lane (just above the color lane, y about 709) at the bar you want.
  - Created tonight: **Prism Spots + 360s**, **841 Logo Gobo**, **Spots Clean** (see `stacks.md`).
  - Gotcha: a drag from the cue list sometimes drops the cue that was **already selected** in the list, not the one under the mouse. Click the cue in the list first, then drag it.
- **Intensity effect at bar 1:** the first Flash And Fade at the very start of a track sometimes doesn't take. Apply it a second time.
- **Selecting a whole track:** drag left to right from just inside bar 1 to just inside bar 17. Starting the drag on an existing envelope point moves that point instead (undo with Cmd-Z).
- **Track list scrolling:** the scroll wheel over the right-hand track names scrolls the list.
- **Static Look Fade In / Fade Out:** checkboxes with seconds at the top of the look editor. They fade the look in and out when it's switched; a look can't pulse on its own.

## Freezes
- **2026-10-07, about 21:30:** SoundSwitch froze after scrolling the Autoscript preset dropdown with the mouse wheel. Force-quit (Activity Monitor) and reopen; everything saved came back. Pick presets with single clicks and save before opening that dialog.

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
- **Frozen after save (2026-10-06):** right after a save, SoundSwitch once stopped responding with the Edit-mode File menu drawn on screen. Don't click around in that menu blind: Export to Control One and Import from Control One are in it.
