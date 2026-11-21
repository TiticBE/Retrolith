# Disc games and arcade

[← Contents](index.md)

## Redump games with several tracks

A CD game is often a sheet (`.cue`, `.gdi`, `.ccd`, `.mds`) and its tracks (`.bin`, `.img`, `.sub`, `.mdf`). Retrolith
recognises them without any setting:

- inside the game's zip or as plain files;
- in the DAT's folder or in a subfolder named after the game.

Repair and "Add ROMs" file them like the rest of the collection. A `.cue` sheet naming old track names ("Track 01") is
rewritten with the DAT's names, if the tracks' checksums match exactly.

## Multi-disc games

"Final Fantasy VII (USA) (Disc 1)", "(Disc 2)"… are grouped into one game, like floppy disks: one tile in the grid,
"3 discs" or "2/3 discs". Two regions or two revisions stay two games. On a Recalbox or a Batocera, the game is launched
by an `.m3u` listing its discs.

## CHD

CHD is a compressed format from MAME, read by most CD console emulators (PlayStation, Saturn, Dreamcast, PC Engine CD,
Mega-CD…).

- **Recognition**: a `.chd` is recognised as the Redump game whose tracks it has exactly (count, order, size), read from
  its metadata without decompressing it. A DVD (PlayStation 2…) is compared with the DAT's ISO.
- A game is **complete** as CHD as well as cue/bin; one is not a duplicate of the other.
- **Layout**: `<game>.chd` in the DAT's folder (or in a subfolder named after the game).

### Converting with chdman

Conversion uses **chdman**, MAME's tool. Retrolith does not ship it: install [MAME](https://www.mamedev.org/) (chdman
sits next to `mame.exe`) and add its folder to the PATH, or declare MAME in LaunchBox. Retrolith finds it on its own;
otherwise the actions are greyed out and the tooltip says why.

- **Convert to CHD** (right-click a complete game) or a folder's **CHD** button ("Convert all to CHD");
- **Convert to cue/bin** (or **to ISO** for a DVD) to go back.

Tracks only go to the recycle bin once the CHD is recognised as the game; the CHD only once every extracted track has
been checked against the DAT. A failure leaves the game as it was. Each conversion is logged and can be cancelled.

## Arcade: MAME and FinalBurn Neo

MAME and FinalBurn Neo DATs (Logiqx XML, ClrMamePro, or `mame -listxml` output) load into a collection with the
**Other** format.

### Set types

| Type | A clone's zip |
|---|---|
| **Non-merged** | All its ROMs, including its parent's |
| **Split** | Only what differs from its parent |
| **Merged** | No zip: the clone is inside its parent's zip |

The type is recognised at every scan from your zips and shown in the header ("· split sets"). Correct it with
collection menu › **Arcade set type…**. **Repair never changes the set type** and never removes a ROM from an arcade zip.

### What Retrolith understands

- parents and clones, shared ROMs, BIOS and devices, CHD disks (`<game>\<disk>.chd`);
- a ROM marked `nodump` is never required;
- a game missing its BIOS, a device or a CHD is partial, and its row says which ("Missing neogeo");
- BIOS and devices are not games: they are counted separately, in the "BIOS and devices" badge.

### To a Recalbox

Each arcade collection goes to the core expecting its MAME version, recognised from the DAT: recent MAME →
`mame_latest`, MAME 0.78 or 2003-Plus → `mame2003_plus`, 0.139 → `mame2010`, FinalBurn Neo → `fbneo`… The core is
written in the folder's `.recalbox.conf`. A game takes along its BIOS, devices, parent (for split sets) and CHDs. A game
missing its BIOS or CHD is not copied, and the preview says so. A game present in two arcade collections is sent once
(FinalBurn Neo first, then the most recent MAME version).

Not handled yet: converting from one set type to another, software lists, sound samples.
