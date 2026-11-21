# Getting started

[← Contents](index.md)

## Install

1. Download `Retrolith-<version>-win-x64.zip` from the
   [releases page](https://github.com/TiticBE/Retrolith/releases/latest).
2. Unzip it into a folder you can write to (for example `C:\Retrolith`, not `C:\Program Files`).
3. Run `Retrolith.exe`. If Windows shows "Windows protected your PC", click **More info** then **Run anyway** (see the
   [FAQ](faq.md)).

The folder contains:

| Item | Role |
|---|---|
| `Retrolith.exe` | The launcher, to open. |
| `App\` | The application and its libraries. |
| `Data\` | Your data: database, settings, media, backups, logs. Created on first launch. |
| `portable.txt` | Keeps the data in `Data`. If deleted, Retrolith stores it in `%LOCALAPPDATA%\Retrolith`. |
| `LICENSE.txt`, `THIRD-PARTY-NOTICES.txt` | License of Retrolith and of third-party components. |

To move Retrolith, move the whole folder while Retrolith is closed.

## Create your first collection

On first launch the database is empty. The welcome screen offers two kinds of collections:

- **DAT collection**: to check your files against published DATs (TOSEC, No-Intro, Redump, MAME…).
- **Personal catalog**: for your own files, which no DAT lists (your dumps, your creations).

Pick one and give it a name; that's all. Other actions stay greyed out until a collection exists.

## Import the DATs

From the welcome screen, or later from the collection menu › **Import DATs**:

- **A file (zip, dat)…**: the pack as you downloaded it (zip), or a single DAT;
- **A folder of DATs…**: an unpacked pack, subfolders included.

Retrolith recognises the **naming format** (TOSEC, No-Intro or Other) and says so when the import ends. Re-importing a
newer pack only reads the DATs that changed; added, removed and renamed games are logged, and your lists and ratings
follow renamed games. An import never touches the collection's files.

Where to find DATs: the [TOSEC](https://www.tosecdev.org/), [No-Intro (Dat-o-Matic)](https://datomatic.no-intro.org/),
[Redump](http://redump.org/), [MAME](https://www.mamedev.org/) and
[FinalBurn Neo](https://github.com/finalburnneo/FBNeo) websites.

## Choose the root folder

**Choose the root folder of the collection…**: the folder holding your ROMs, or an empty folder where Retrolith will file
them. A network drive is fine; if it drops during an operation, Retrolith waits for it to come back and resumes.

## First scan

**Scan the collection** walks the root folder and matches every file against all the DATs. Then:

- the tree shows the percentage of titles owned, by machine or by DAT;
- the **badges** at the top right count titles owned, complete, to be filed, partial, unknown files and duplicates;
  click a badge to get its list.

Next: [file what needs filing](scanning-and-filing.md), [fetch info and media](info-and-media.md),
[make lists](browsing-and-lists.md) and [copy them to a device](devices.md).
