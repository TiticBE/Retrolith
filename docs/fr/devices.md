# Appareils

[← Sommaire](index.md)

Retrolith copie vos jeux sur vos appareils et garde la trace de ce qu'il y a mis. **Synchroniser un appareil…**
(barre d'outils) ouvre la fenêtre des profils : un profil par appareil, avec son dossier ou son partage réseau, les
listes à y envoyer et ses options. La fenêtre n'affiche que les options que ce type d'appareil sait faire.

## Principes communs

- **Seuls les jeux complets** des listes choisies sont copiés.
- Un **aperçu** montre ce qui sera copié, remplacé ou retiré, et la place nécessaire.
- Retrolith ne retire **que ce qu'il a mis lui-même** ; les fichiers retirés vont dans `_Retrolith Trash` sur
  l'appareil.
- Une **réserve** de place (5 % du disque, entre 2 et 10 Go) est laissée à l'appareil pour son cache, ses sauvegardes et
  ses captures.
- **Ce qui change sur l'appareil revient** : un favori ajouté ou retiré sur l'appareil l'est aussi dans Retrolith ; le
  côté qui a changé depuis la dernière synchronisation l'emporte, et l'aperçu le montre. Les **statistiques de jeu**
  (parties, temps joué, dernière partie) sont relues et s'affichent sur la fiche.

## Recalbox

Dossier : la carte SD, un disque, ou le partage réseau `\\RECALBOX\share`.

- Chaque jeu va dans le dossier de sa machine ; `gamelist.xml` est complété (nom, année, éditeur, favoris, médias,
  résumé, manuel, genre) sans écraser ce que Recalbox a écrit.
- **Jeux sur plusieurs disquettes ou disques** : un `.m3u` les lance, les disquettes sont masquées.
- **Jeux sur plusieurs pistes** : copiés décompressés, feuille et pistes côte à côte ; un jeu possédé en `.chd` part en
  `.chd`.
- **Formats lisibles** : les jeux qu'un système de la Recalbox ne lit pas (d'après son `_readme.txt`) sont signalés et
  laissés de côté.
- **Émulateur par machine et par jeu** : dans le profil, chaque machine peut prendre un des émulateurs de Recalbox ;
  sur la fiche d'un jeu, un émulateur pour ce jeu. Le choix est écrit dans les fichiers `.recalbox.conf` à côté des ROMs ;
  une clé écrite à la main y est gardée, et signalée.
- **Options** du cœur (modèle de la machine : Atari ST, Amiga, Thomson, Atari 8 bits…), par machine ou par jeu, dans les
  fichiers `.core.cfg`.
- **BIOS** : vérification du dossier `bios` d'après la liste de Recalbox, et copie des BIOS manquants trouvés dans la
  collection.
- **État du disque…** : relu sans rien écrire, il montre les fichiers de Retrolith, les orphelins d'anciennes
  synchronisations, les copies faites à la main (à adopter dans une liste), les fichiers inconnus, manquants ou abîmés et
  la place par machine. Le ménage se choisit fichier par fichier. Les fichiers de Recalbox (`gamelist.xml`, sauvegardes,
  BIOS…) ne sont jamais touchés.
- Sur le réseau, EmulationStation peut être relancé à la fin.

## Batocera

Se règle comme une Recalbox : dossier `roms` ou partage `\\BATOCERA\share`, dossier de chaque machine sous son nom
Batocera, `.m3u`, `gamelist.xml` avec favoris et médias, BIOS manquants copiés. Les formats lus sont pris dans le
`_info.txt` de chaque système. Sur le réseau, Retrolith recharge les listes de jeux à la fin, une fois **Enable public
web access** activé dans les options développeur de Batocera.

## MiSTer

Copie dans `games\<cœur>` de la carte SD, d'une clé USB ou d'un partage (NES, SNES, MegaDrive, PSX, Amiga…), sans
liste de jeux. Les BIOS manquants sont posés dans le dossier du cœur sous le nom qu'il attend (`boot0.rom`…).

## LaunchBox

Un profil LaunchBox (Windows) copie les jeux dans le dossier de jeux de leur plateforme et les inscrit dans
`Data\Platforms\<plateforme>.xml` ; chaque liste devient une playlist, les favoris la case « Favori », les médias vont
dans les dossiers d'images, de vidéos et de manuels. Un jeu déjà dans LaunchBox est repris tel quel. Retrolith refuse
d'écrire pendant que LaunchBox ou Big Box tourne, et sauvegarde chaque fichier XML avant de le réécrire
(`Backups\Retrolith`).

## Carte SD ou clé USB

**Copier sur une carte SD ou une clé USB…** (barre d'outils) : les jeux complets d'un dossier, avec les mêmes filtres,
en zips ou décompressés. Relancer la copie met la carte à jour.

## Sauvegardes des jeux

À chaque synchronisation, Retrolith relève les sauvegardes des jeux sur l'appareil, sans jamais rien y modifier :

- **Recalbox** : sauvegardes de cartouche (`.srm`), instantanés (`.state`…) avec leur capture, disquettes de
  sauvegarde, instantanés d'Amiberry ;
- **Batocera** et **MiSTer** : sauvegardes et instantanés ;
- **LaunchBox** : sauvegardes de l'émulateur lancé pour chaque jeu (RetroArch, Hatari, Altirra, WinUAE, Amiga Forever).

Chaque sauvegarde garde ses 20 dernières versions (sauf celles marquées **Toujours garder**). La fiche du jeu les
montre ; **Restaurer sur…** remet une version sur un appareil où le jeu tourne avec le même cœur, le fichier en place
étant toujours gardé avant. Une sauvegarde peut ainsi passer d'une Recalbox à l'autre, ou de la Recalbox à LaunchBox.
La restauration vers Batocera et MiSTer n'est pas encore possible.
