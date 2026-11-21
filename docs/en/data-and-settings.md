# Data and settings

[← Contents](index.md)

## Where your data is

In the portable version everything is in the `Data` folder next to `Retrolith.exe`: the database (`retrolith.db`),
settings, media (`media`), database backups (`backups`), game saves (`saves`) and logs (`logs`). Your ROMs stay in your
collections' root folders: Retrolith does not copy them into `Data`.

## Database

"⋯" menu › **Database**:

- **Back up the database…**: a full copy, even during an operation. The database is also backed up every week and
  before every update.
- **Restore a backup…**: replaces the database at the next start.
- **Compact the database…**: gives freed space back to the disk.
- **Export personal data (JSON)…**: what cannot be recalculated (lists, ratings, game info, devices, collection
  settings), in a readable file.
- **Open the backups folder**.

## Shared data folder

To use Retrolith on several PCs, **never at the same time**: "⋯" menu › **Shared data folder…**. Pick a folder on a
network share, OneDrive or Synology Drive. Lists, ratings, devices, collection settings, ScreenScraper info and personal
catalogs are written there; the database stays on each PC. A newer version is picked up at startup; in a conflict you
choose, and the other version is kept as a backup.

## Long operations

One writing operation at a time (scan, add, repair…). It can be cancelled, and you can keep browsing the collection
meanwhile. Background tasks (ScreenScraper, logos, backup, integrity) run alongside, in the tasks panel. The PC does not
go to sleep, progress shows on the taskbar icon, and a notification announces the end.

## Language

"⋯" menu › **Language / Langue…**: English or French, applied on restart. Until a language is chosen, Retrolith follows
Windows. File and folder names written to disk stay in English.

## Updates

At startup, at most once a day, Retrolith checks whether a new version is published. If so, a banner offers it:
**What's new** to read the changes, **Update** to download it. The zip is checked against its SHA-256 checksum and put in
place on restart. Nothing is installed without that click, and your data (`Data`) is never touched. Without a network
connection nothing is shown.

## Diagnostics

"⋯" menu › **Diagnostics**:

- **Copy the diagnostics**: puts the version, system, database state and the end of the log on the clipboard, to paste
  into an [issue](https://github.com/TiticBE/Retrolith/issues);
- **Open the diagnostic logs folder**: one log per day (operations, errors, interface freezes), kept 30 days.

The **File log** (toolbar) lists the latest copies, moves and deletions.
