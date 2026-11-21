# Info and media

[← Contents](index.md)

## ScreenScraper

[ScreenScraper](https://www.screenscraper.fr/) is a community database of retro game info and media. You need an
account; it is free.

1. **ScreenScraper settings…** (toolbar): enter your ScreenScraper login and password, then choose the media you want
   (title screen, screenshots, mix, 2D and 3D boxes, media, logo, PDF manual…) and the language of summaries. The
   button's icon shows the account state (a green tick when all is well).
2. **ScreenScraper info** on a folder or a list: each game is looked up by its ROM checksums, so it is found even when
   misnamed. The lookup runs in the background; you can keep using Retrolith.

Fetched: summary, date, publisher, developer, genres and sub-genres, game modes, series, number of players, rating, and
the chosen media. Your daily ScreenScraper quota applies.

**Complete the genres of games already found** fetches missing genres without downloading any media again.

Media show as a thumbnail next to each title (three sizes), full size on hover, as a gallery in the details, and go to
your devices with the games.

## Your own images

**Add images…** (right-click a folder) or **Add images to the collection…** (collection menu), without ScreenScraper:

- pick a folder where each image has the exact name of a game (`Serenade #74.png`), flat or laid out like the
  collection;
- screenshots go at the top level; boxes, title screens, logos and media go in `covers`, `titles`, `wheels`, `supports`
  folders.

Media already fetched from ScreenScraper are not replaced, and ScreenScraper never replaces an image you added. The
summary counts images with no game of the same name.

## Machine logos and photos

Each machine's logo and photo appear at the top of the chosen folder and in the view by machine. Brand logos
(Commodore, Nintendo, Sega…) are taken from Wikidata the first time they are shown and kept on disk. An image placed by
hand at `media\brands\<brand>\logo.png` takes priority.

## The media folder

Media are kept in `Data\media`. This folder can be moved (verified copy) or shared with another PC (see
[Data and settings](data-and-settings.md)).
