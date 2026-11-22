# FAQ

[← Contents](index.md)

**Windows shows "Windows protected your PC". Is it dangerous?**
Retrolith is not digitally signed yet; Windows warns about any new, rarely downloaded program. Click **More info**, then
**Run anyway**. To check the zip, compare its SHA-256 checksum (`Get-FileHash Retrolith-<version>-win-x64.zip` in
PowerShell) with the `.sha256` file published next to it.

**Does Retrolith provide games?**
No. It contains, downloads and points to no game site. It manages the copies you own.

**Where do I find DATs?**
On the [TOSEC](https://www.tosecdev.org/), [No-Intro](https://datomatic.no-intro.org/), [Redump](http://redump.org/),
[MAME](https://www.mamedev.org/) and [FinalBurn Neo](https://github.com/finalburnneo/FBNeo) websites.

**Can Retrolith damage my files?**
It is built to avoid it: nothing is written without a preview, every zip is verified before replacing the old one, every
deletion goes through the recycle bin (or `_Retrolith Trash` on a network drive), and every action is recorded in the
file log. Still, keep a backup of your ROMs.

**My files are "to be filed". What does it mean?**
They are recognised but misnamed or misplaced. **Repair the collection…** files them; the preview shows everything first.

**Why so many unknown files?**
They match no DAT of this collection: another collection, another pack version, personal files. Click the badge to get
the list. Repair can set them aside in `_Unknown`, or they can join a personal catalog.

**The scan is slow.**
The first scan reads everything; later ones only read changed files. On a network drive the network is what counts. To
go faster, scan only the folder you changed (right-click in the tree).

**The CHD actions are greyed out.**
chdman cannot be found. Install MAME and add its folder to the PATH, or declare MAME in LaunchBox; see
[Disc games and arcade](discs-and-arcade.md).

**ScreenScraper finds nothing.**
Check in **ScreenScraper settings…** that the icon shows a green tick (account recognised) and that today's quota is not
used up. A game missing from ScreenScraper's database will have no info; you can add your own images.

**A game copied to my Recalbox does not show up.**
The system may not read its format: the sync preview reports it. For arcade games, check the game has its BIOS and CHDs.
Remember to update the Recalbox game lists, or restart it.

**Can I use Retrolith on two PCs?**
Yes, not at the same time: see the shared data folder in [Data and settings](data-and-settings.md).

**How do I report a problem?**
"⋯" menu › **Diagnostics** › **Copy the diagnostics**, then open an [issue](https://github.com/TiticBE/Retrolith/issues),
paste it, and say what you were doing.

**Where can I ask a question or suggest an idea?**
In the [Discussions](https://github.com/TiticBE/Retrolith/discussions), in English or French.
