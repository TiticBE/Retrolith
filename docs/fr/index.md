# Guide de l'utilisateur de Retrolith

**[English](../en/index.md)** · Français

Retrolith gère des collections de jeux rétro : il compare vos fichiers aux catalogues de référence (les fichiers DAT),
range ce qui doit l'être, récupère les infos et les médias des jeux, et copie vos sélections sur vos appareils.

## Sommaire

1. **[Premiers pas](getting-started.md)** : installer, créer une collection, importer ses DATs, faire le premier scan.
2. **[Collections et DATs](collections.md)** : les formats de DATs, plusieurs collections, catalogues personnels,
   machines ignorées, rangement sur le disque.
3. **[Scanner et ranger](scanning-and-filing.md)** : scan rapide et complet, états des jeux, ajouter des ROMs, réparer,
   fixdat, intégrité, compléter depuis une autre collection.
4. **[Parcourir et faire des listes](browsing-and-lists.md)** : arborescence, liste et grille, noms décodés, filtres,
   recherche, fiche d'un jeu, notes, favoris et listes intelligentes.
5. **[Infos et médias](info-and-media.md)** : ScreenScraper, vos propres images, logos des machines.
6. **[Jeux sur disque et arcade](discs-and-arcade.md)** : Redump, jeux sur plusieurs disques, CHD et chdman, sets MAME
   et FinalBurn Neo.
7. **[Appareils](devices.md)** : Recalbox, Batocera, MiSTer, LaunchBox, carte SD ou clé USB ; BIOS, émulateurs,
   sauvegardes des jeux.
8. **[Données et réglages](data-and-settings.md)** : sauvegarde de la base, dossier partagé entre PC, langue, mises à
   jour, diagnostic.
9. **[FAQ](faq.md)** : questions courantes et problèmes connus.

## Les mots à connaître

| Mot | Sens |
|---|---|
| **DAT** | Fichier qui liste les jeux d'une machine avec, pour chaque fichier, sa taille et ses sommes (CRC32, MD5, SHA1). TOSEC, No-Intro, Redump, MAME et FinalBurn Neo publient les leurs. |
| **Pack** | Ensemble de DATs publié d'un coup (un zip ou un dossier). |
| **Collection** | Dans Retrolith : un pack de DATs (ou des catalogues personnels), un dossier racine où sont vos fichiers, ses listes et ses appareils. |
| **Titre / jeu** | Une entrée d'un DAT. Un jeu peut avoir plusieurs fichiers (disquettes, pistes, ROMs d'arcade). |
| **Complet** | Tous les fichiers du jeu sont présents, au bon nom et à la bonne place. |
| **À ranger** | Les fichiers sont là, mais mal nommés ou mal placés. La réparation les range. |
| **Partiel** | Une partie seulement des fichiers est présente. |
| **Inconnu** | Fichier du dossier racine qu'aucun DAT de la collection ne connaît. |
| **Fixdat** | DAT des seuls titres qui vous manquent, à donner à un autre outil. |

## Où trouver quoi

- **Barre d'outils** : scanner, ajouter des ROMs, réparer, synchroniser un appareil, copier sur une carte SD,
  ScreenScraper, journal des fichiers, et le menu **« ⋯ »** pour ce qui vaut pour toute l'application (base de données,
  dossier partagé, diagnostic, langue, à propos).
- **Menu de la collection** (le bouton à côté de son nom, en haut à gauche) : changer de collection, état de toutes
  les collections, vue par machine, importer des DATs, scan complet, fixdat, réglages de la collection.
- **Clic droit sur un dossier** de l'arborescence : scanner, réparer, exporter les manquants, ajouter des images,
  ignorer une machine.
- **Clic droit sur un jeu** : favoris et listes, conversion CHD, ajout à un catalogue ; **double-clic** : sa fiche.

Chaque bouton et chaque option a une infobulle : survolez-le pour savoir exactement ce qu'il fait.
