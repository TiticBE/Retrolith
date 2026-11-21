# Retrolith user guide

English · **[Français](../fr/index.md)**

Retrolith manages retro game collections: it checks your files against reference catalogs (DAT files), files what
needs filing, fetches game info and media, and copies your selections to your devices.

## Contents

1. **[Getting started](getting-started.md)**: install, create a collection, import its DATs, run the first scan.
2. **[Collections and DATs](collections.md)**: DAT formats, several collections, personal catalogs, ignored machines,
   layout on disk.
3. **[Scanning and filing](scanning-and-filing.md)**: quick and full scan, game states, adding ROMs, repairing, fixdat,
   integrity, completing from another collection.
4. **[Browsing and lists](browsing-and-lists.md)**: tree, list and grid, decoded names, filters, search, game details,
   ratings, favorites and smart lists.
5. **[Info and media](info-and-media.md)**: ScreenScraper, your own images, machine logos.
6. **[Disc games and arcade](discs-and-arcade.md)**: Redump, multi-disc games, CHD and chdman, MAME and FinalBurn Neo
   sets.
7. **[Devices](devices.md)**: Recalbox, Batocera, MiSTer, LaunchBox, SD card or USB drive; BIOS, emulators, game saves.
8. **[Data and settings](data-and-settings.md)**: database backup, data folder shared between PCs, language, updates,
   diagnostics.
9. **[FAQ](faq.md)**: common questions and known issues.

## Words to know

| Word | Meaning |
|---|---|
| **DAT** | A file listing a machine's games with, for each file, its size and checksums (CRC32, MD5, SHA1). TOSEC, No-Intro, Redump, MAME and FinalBurn Neo publish their own. |
| **Pack** | A set of DATs released together (a zip or a folder). |
| **Collection** | In Retrolith: a DAT pack (or personal catalogs), a root folder holding your files, its lists and its devices. |
| **Title / game** | An entry in a DAT. A game can have several files (disks, tracks, arcade ROMs). |
| **Complete** | Every file of the game is there, with the right name, in the right place. |
| **To be filed** | The files are there but misnamed or misplaced. Repair files them. |
| **Partial** | Only some of the files are there. |
| **Unknown** | A file in the root folder that no DAT of the collection knows. |
| **Fixdat** | A DAT of only the titles you are missing, to give to another tool. |

## Where things are

- **Toolbar**: scan, add ROMs, repair, sync a device, copy to an SD card, ScreenScraper, file log, and the **"⋯"** menu
  for application-wide things (database, shared data folder, diagnostics, language, about).
- **Collection menu** (the button next to its name, top left): switch collection, status of all collections, view by
  machine, import DATs, full scan, fixdat, collection settings.
- **Right-click a folder** in the tree: scan, repair, export missing titles, add images, ignore a machine.
- **Right-click a game**: favorites and lists, CHD conversion, add to a catalog; **double-click**: its details.

Every button and option has a tooltip: hover over it to see exactly what it does.
