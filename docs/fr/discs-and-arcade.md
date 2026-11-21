# Jeux sur disque et arcade

[← Sommaire](index.md)

## Jeux Redump sur plusieurs pistes

Un jeu sur CD est souvent une feuille (`.cue`, `.gdi`, `.ccd`, `.mds`) et ses pistes (`.bin`, `.img`, `.sub`, `.mdf`).
Retrolith les reconnaît sans réglage :

- dans le zip du jeu comme en fichiers simples ;
- dans le dossier du DAT ou dans un sous-dossier au nom du jeu.

La réparation et « Ajouter des ROMs » les rangent comme le reste de la collection. Une feuille `.cue` qui nomme
d'anciens noms de pistes (« Track 01 ») est refaite avec les noms du DAT, si les sommes des pistes correspondent
exactement.

## Jeux sur plusieurs disques

« Final Fantasy VII (USA) (Disc 1) », « (Disc 2) »… sont regroupés en un seul jeu, comme les disquettes : une case dans
la grille, « 3 disques » ou « 2/3 disques ». Deux régions ou deux révisions restent deux jeux. Sur une Recalbox ou une
Batocera, le jeu est lancé par un `.m3u` qui liste ses disques.

## CHD

Le CHD est un format compressé de MAME, lu par la plupart des émulateurs de consoles sur CD (PlayStation, Saturn,
Dreamcast, PC Engine CD, Mega-CD…).

- **Reconnaissance** : un `.chd` est reconnu comme le jeu Redump dont il a exactement les pistes (nombre, ordre, taille),
  lues dans ses métadonnées sans le décompresser. Un DVD (PlayStation 2…) est comparé à l'ISO du DAT.
- Un jeu est **complet** en CHD comme en cue/bin ; l'un n'est pas le doublon de l'autre.
- **Rangement** : `<jeu>.chd` dans le dossier du DAT (ou dans un sous-dossier au nom du jeu).

### Convertir avec chdman

La conversion utilise **chdman**, l'outil de MAME. Retrolith ne le fournit pas : installez [MAME](https://www.mamedev.org/)
(chdman est à côté de `mame.exe`) et ajoutez son dossier au PATH, ou déclarez MAME dans LaunchBox. Retrolith le trouve
seul ; sinon les actions sont grisées et l'infobulle dit pourquoi.

- **Convertir en CHD** (clic droit sur un jeu complet) ou le bouton **CHD** d'un dossier (« Tout convertir en CHD ») ;
- **Convertir en cue/bin** (ou **en ISO** pour un DVD) pour revenir en arrière.

Les pistes ne partent à la corbeille qu'une fois le CHD reconnu comme le jeu ; le CHD, qu'une fois chaque piste extraite
vérifiée face au DAT. Un échec laisse le jeu tel quel. Chaque conversion est notée au journal et peut être annulée.

## Arcade : MAME et FinalBurn Neo

Les DATs MAME et FinalBurn Neo (XML Logiqx, ClrMamePro, ou la sortie de `mame -listxml`) se chargent dans une collection
de format **Autre**.

### Types de sets

| Type | Zip d'un clone |
|---|---|
| **Non-merged** | Toutes ses ROMs, y compris celles du parent |
| **Split** | Seulement ce qui diffère de son parent |
| **Merged** | Pas de zip : le clone est dans le zip du parent |

Le type est reconnu à chaque scan d'après vos zips, et affiché dans l'en-tête (« · sets split »). Il se corrige par menu
de la collection › **Type de sets d'arcade…**. **La réparation ne change jamais le type de set** et ne retire jamais une
ROM d'un zip d'arcade.

### Ce que Retrolith comprend

- parents et clones, ROMs partagées, BIOS et périphériques, disques CHD (`<jeu>\<disque>.chd`) ;
- une ROM marquée `nodump` n'est jamais exigée ;
- un jeu à qui il manque son BIOS, un périphérique ou un CHD est partiel, et sa ligne dit lequel (« Il manque
  neogeo ») ;
- les BIOS et périphériques ne sont pas des jeux : ils sont comptés à part, dans la pastille « BIOS et devices ».

### Vers une Recalbox

Chaque collection d'arcade va au cœur qui attend sa version de MAME, reconnu d'après le DAT : MAME récent →
`mame_latest`, MAME 0.78 ou 2003-Plus → `mame2003_plus`, 0.139 → `mame2010`, FinalBurn Neo → `fbneo`… Le cœur est écrit
dans le `.recalbox.conf` du dossier. Un jeu emmène son BIOS, ses périphériques, son parent (en split) et ses CHD. Un jeu
à qui il manque son BIOS ou son CHD n'est pas copié, et l'aperçu le dit. Un même jeu présent dans deux collections
d'arcade n'est envoyé qu'une fois (FinalBurn Neo d'abord, puis la version de MAME la plus récente).

Pas encore gérés : conversion d'un type de set à l'autre, software lists, échantillons sonores.
