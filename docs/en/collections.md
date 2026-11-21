# Collections and DATs

[← Contents](index.md)

## Several collections

Retrolith handles as many collections as you like. Each has its DAT pack, its root folder, its lists and its devices.
The collection menu (next to its name) lets you:

- switch between collections;
- see the **Status of all collections…**: one card per collection, with the last scan, titles owned, complete, to be
  filed, partial, unknown files and duplicates;
- open the **View by machine…**: every title of a machine, across all collections;
- create a **New collection…**, rename or remove the current one (removing it deletes none of your files).

## Naming formats

All DAT collections work the same way; only the file naming format differs, recognised on the first import:

| Format | Recognised by | Layout on disk |
|---|---|---|
| **TOSEC** | `(TOSEC-v…)`, `TOSEC`, `TOSEC-ISO`, `TOSEC-PIX` branches | One folder per DAT (`Commodore Amiga - Games - [ADF]`), or the official tree (`Commodore\Amiga\Games\[ADF]`) |
| **No-Intro** | A date in the DAT name, "No-Intro" or "redump" in the header | One folder per system |
| **Other** | Everything else: MAME, FinalBurn Neo, GoodTools, personal DATs | One folder per DAT, named after it without its version |

If the recognised format is wrong: collection menu › **File name format…**. The DATs are read again in the new format,
lists and ratings follow, and no file is moved.

For TOSEC, **Layout on disk: one folder per DAT** (collection menu) chooses between one folder per DAT and the
official tree. Changing your mind moves no file: repair then files according to the new choice. Retrolith offers the
layout it recognises on disk. How the tree is displayed (by machine or by DAT) is chosen separately, above the tree.

## Decoded game names

Whatever the format, Retrolith reads from the game name: title, version, year, publisher, regions, languages,
translations, media, and flags such as `[!]` (verified dump), `[a]` (alternate), `[b]` (bad dump), `[cr]` (crack), `[h]`
(hack), `[t]` (trainer), `(Beta)`, `(Proto)`, `(Demo)`, `(Rev 1)`. They are shown as badges and used by the filters.
GoodTools names (`Game (U) [!]`) are read too.

A MAME or FinalBurn Neo game with a short name (`pacman`) is shown by its description ("Pac-Man (Midway)").

## Special DATs

- **Unzipped DATs** (Retroplay's WHDLoad…): a DAT that asks to keep its files unzipped is recognised on import. Each file
  (`.lha`…) is a title, kept as is.
- **Compilations** (Atari ST menu disks…): the list of games they contain, read from the DAT, is shown in the details;
  search finds a compilation by one of its games.
- **ROM headers** (NES, Famicom Disk System, Lynx, Atari 7800, SNES and PC Engine copiers): a headered file is
  recognised by DATs with and without headers, without being modified.
- **Disc games and arcade**: see [Disc games and arcade](discs-and-arcade.md).

## Personal catalogs

A personal catalog lists your own files, which no DAT knows.

1. Create a **Personal catalog** collection, then **New catalog…**: a machine, or a machine and a format
   (`Atari ST\[STX]`).
2. **Add games to the catalog**: files, or a whole folder (one game per file, per subfolder, or one for all).

Retrolith computes each file's size and checksums and writes the catalog as a real DAT, which you can reuse elsewhere.
Its games get everything the others have: details, ScreenScraper, ratings, lists, sync.

An **unknown file** from another collection can join a catalog too: right-click its row › **Add to a personal
catalog…**, or from the list of the "unknown files" badge.

## Ignored machines and branches

Right-click a folder in the tree › **Ignore this machine** (or **Ignore this branch**): its DATs stay visible but leave
the figures, exports and fixdats. Handy for a machine you don't care about. **Track again** puts it back.

## Folders with an old DAT name

When a pack renames a DAT, your folders keep the old name. Collection menu › **Rename folders under an old DAT name…**
finds them from the last scan and renames them in one go, without rewriting a single zip.
