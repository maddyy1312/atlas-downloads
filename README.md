# Atlas

Atlas is a Subnautica companion with an interactive map, PDA encyclopedia, crafting calculator, base planner, and radio/story-event viewer.

**No Subnautica content is included.** You must own and install the original game, then import its data into Atlas. Below Zero is not supported. Atlas reads your game and save files without changing them.

## Download and set up

Choose a download for your computer:

| Platform | Download |
|---|---|
| macOS — Apple Silicon (M1 and newer) | [Download](https://github.com/maddyy1312/atlas-downloads/releases/latest/download/Atlas-osx-arm64.zip) |
| macOS — Intel | [Download](https://github.com/maddyy1312/atlas-downloads/releases/latest/download/Atlas-osx-x64.zip) |
| Windows — x64 | [Download](https://github.com/maddyy1312/atlas-downloads/releases/latest/download/Atlas-win-x64.zip) |
| Linux — x64 | [Download](https://github.com/maddyy1312/atlas-downloads/releases/latest/download/Atlas-linux-x64.zip) |

[All releases and checksums](https://github.com/maddyy1312/atlas-downloads/releases)

1. Download the ZIP for your computer.
2. Extract the entire ZIP. Open **Atlas.app** on macOS, **Atlas.exe** on Windows, or **Atlas** on Linux. Keep the application and its accompanying files together.
3. Select your installed Subnautica folder. On macOS, select the complete **Subnautica.app**, especially if you want to import audio.
4. Choose what to import and allow setup to download any required tools. Start with a lower-detail map for a quicker import.
5. Start the import. You can return to the other tabs while it runs; progress appears at the bottom of the window.

Initial setup needs an internet connection, free disk space, and time to process your game files. More detailed maps take longer and use more storage. After importing, Atlas can be used offline.

### Opening Atlas on macOS

Atlas is not notarized by Apple. If macOS says it cannot verify the app, first confirm you downloaded it from this page. Move it to Applications, then run this in Terminal:

```sh
xattr -dr com.apple.quarantine "/Applications/Atlas.app"
```

Then open Atlas again. If it is elsewhere, replace the path with its actual location. This removes the downloaded-file quarantine flag for that copy of Atlas; it does not sign or notarize it.

## Using Atlas

- **Map:** choose a biome or cave layer, search for objects, and enable the overlays you want. Possible spawn slots are not guaranteed object locations. Add personal markers or export a map as a PNG.
- **Encyclopedia:** browse collapsible PDA categories, read entries and view images. Game Reference adds available item properties and unlock information.
- **Crafting:** select items and quantities, then check off the required materials. The crafting-step list and material hierarchy stay in sync.
- **Events:** browse radio messages and story events, their requirements, and imported audio. Expect spoilers.
- **Saves:** load a save folder to see available progress, inventories and saved objects. Use **Load / Refresh** after saving in-game. Atlas never edits the save.
- **Settings:** adjust text and marker sizes, object labels, and the game-data storage folder.

## Manage imported data

Use **Game data** to import, replace or delete individual sections. Entries, images, recipes, icons and audio can be managed separately. Under **Map → Map imports**, manage each map detail and its textures. Imports and PNG exports can run in the background and be queued.

Choose **Settings → Game data storage** to use another storage folder. Changing this setting does not move existing files: copy your imported data to the new location first if you want to keep it.

By default, Atlas stores its files here, with imported content in the `data` subfolder:

- macOS: `~/Library/Application Support/Subnautica Atlas Distribution`
- Windows: `%LOCALAPPDATA%\Subnautica Atlas Distribution`
- Linux: `~/.local/share/Subnautica Atlas Distribution` (or your configured `XDG_DATA_HOME`)

**Keep imported data and saves private. Share the application download, not your generated game-content folder.**

## Unfinished features

These features are experimental and disabled by default. Enable them individually under **Settings → Unfinished**:

- **3D Map:** move around and rotate the terrain, including cave views. Choose Orbit or First person controls.
- **Encyclopedia Models:** preview imported models beside PDA images. Model geometry and textures can be imported or removed separately in Game data.
- **Object Renders:** display models of the Aurora, alien/Degasi bases, wrecks, lifepods and static props. Enabling this reveals **Map layer → Object Renders**. Import the matching models and textures in Game data first. The same options are available for PNG exports.
- **Alien Arches:** show arches and their links under **Map layer → Overlays**, after importing the relevant world data.

Rendering, textures and cave cutaways may be incomplete or incorrect, and these features can use substantial memory. The regular filled Aurora overlay does not require them. All models and textures must still come from your own game installation.


### Base Planning preview

The **Base Planning** tab is available directly. Import its data from **Game data → Base Planning**, then choose a piece from the catalog. Left-click to place, right-click to remove, and use **R** to rotate, **↑/↓** to change layer, and **Escape** to cancel placement and deselect. Base textures and transparency can be toggled in Options. Use Inspect mode or double-click a piece to manage its interior. The right panel tracks materials, depth-dependent integrity, and energy; adjust sunlight, individual thermal-plant temperatures, and charging/scanning switches there. Use **Base Components** to rename bases, select components (Shift-click for several), or remove them and their contents. **Charge all components** enables charging throughout the plan. Large-room partitions are currently disabled. Use **Base Plans** to save the whole plan, or **Save** beside a base in Base Components to save only that base. Saved plans can be added to your workspace or replace it, and you can choose an individual base from a saved plan. A 972-component performance example is included in the saves folder. Use **Cmd** on macOS or **Ctrl** on Windows/Linux with **Z / Shift+Z** for undo/redo and **C / X / V** for copy/cut/paste. Plans are saved automatically. Reimport Base Planning data after updating to obtain the new connection models and textures.

This is an early preview. Placement and power calculations may differ from the game, terrain is ignored, and free-standing furniture is counted rather than positioned. Models and data must be imported from your own game.

## Troubleshooting

If an import fails, open **Details** in the progress bar and check the log. Confirm you selected the installed game rather than a save folder, have enough free space, and can reach the download sites. Audio import needs the complete game installation for your operating system.

Windows and Linux packages are built on those platforms, but game imports and interactive use have not yet been verified there. Linux needs desktop graphics/OpenGL and audio libraries. Close older copies before opening an updated Atlas.

## Credits and third-party software

Subnautica belongs to Unknown Worlds Entertainment. Atlas is an unofficial companion. It does not include game files, extracted maps, models, textures, dialogue, music or saves.

Release packages include third-party licenses and dependency notices in **THIRD-PARTY**. Setup retains notices for separately downloaded tools. Keep these files with the application.
