# Scanning and filing

[← Contents](index.md)

## Scanning

**Scan the collection** (toolbar) walks the root folder: plain files, `.zip` and `.7z`, recognised by SHA1, MD5 or CRC32
plus size. A scan modifies no file.

- **Quick scan** (default): zip CRC32s are read from their headers, a file whose size matches no ROM is not read, and an
  unchanged file (same size, same date) is not read again.
- **Full scan (SHA1)** (collection menu): unpacks and reads every file. Much slower, it also detects a damaged file. It
  resumes where it stopped.
- **Scan only this folder** and **Full scan of this folder (SHA1)**: right-click a folder in the tree.
- **Scan all collections** (collection menu): a quick scan of each, one after the other.
- An interrupted scan resumes with **Resume the interrupted scan** ("⋯" menu, only shown in that case).

## States

| State | Meaning | What to do |
|---|---|---|
| **Complete** | Every file of the game, right name, right place | Nothing |
| **To be filed** | The files are there, misnamed or misplaced | Repair |
| **Partial** | Some files are missing | Add ROMs, complete from another collection |
| **Missing** | No file | Same |

**Unknown files** (known by no DAT) and **duplicates** are counted in badges. Click a badge to get the list of what it
counts, ready to copy.

## Adding ROMs

**Add ROMs…** (toolbar, or drag and drop a folder onto the window): pick any folder. Each file is looked up in every
DAT of the collection.

1. **Preview**: titles completed or partial, files already there, unknown files, space needed. Nothing is written yet.
2. **Copy** or **move**: each ROM goes into its game's official zip (or unzipped, depending on the collection). Every
   zip is verified before it replaces the old one.

An interrupted add (network lost, application closed) is offered at the next start: **Resume** only writes the
remaining titles. A folder already analysed is analysed again quickly, even over the network.

## Repairing

**Repair the collection…** (toolbar), or **Repair this folder…** (right-click in the tree), based on the last scan:

- misnamed or misplaced ROMs are filed into their game's official zip;
- files no longer needed (duplicates, copies once filed) go to the recycle bin;
- unknown files can be set aside in `_Unknown`.

The same preview comes before any file is touched. Every deletion goes through the Windows recycle bin (or
`_Retrolith Trash` on a network drive, which has no recycle bin). Each action is recorded in the **File log** (toolbar).

## Completing from another collection

A game you own in another collection (No-Intro and TOSEC, for example) is flagged as owned elsewhere. **Complete from
the other collection** copies into this one the titles it is missing and the other owns. The other collection's files
are never moved.

## Fixdat

**Export missing titles (fixdat)…** (collection menu), or **Export this folder's missing titles (fixdat)…** (right-click a
folder): writes a DAT of only the missing or partial titles, for ClrMamePro, RomVault or another tool. Ignored machines
are left out.

## Checking integrity

At every start, a background task reads in full the files of one machine (the one checked least recently) and compares
their checksums to the last scan. A file damaged without changing size or date, which the quick scan cannot see, is
reported. Collection menu › **Check integrity (next machine)** runs it right away.

## Disks modified by a game

A game launched straight from its folder may write to its disk. Retrolith recognises it on scan ("Disk modified by the
game") instead of counting it as unknown. Repair keeps it as the game's save before putting back the right copy.
