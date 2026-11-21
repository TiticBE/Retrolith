# Parcourir et faire des listes

[← Sommaire](index.md)

## Arborescence, liste et grille

À gauche, l'**arborescence** de la collection, avec le pourcentage de titres possédés à chaque niveau. Au-dessus :
l'affichage (par machine ou par DAT) et un filtre (tous les dossiers, incomplets…). Sa largeur se règle à la souris.

À droite, les titres du dossier choisi :

- **en liste**, une ligne par titre, avec ses pastilles et son état ;
- **en grille**, une case par jeu avec sa jaquette (boîte, sinon support, sinon écran titre), comme dans LaunchBox ; un
  curseur règle la taille des cases. Un jeu sans image est dessiné sur son support (disquette, cassette, cartouche, CD).

En grille, les disquettes, faces, cassettes ou disques d'un même jeu tiennent dans une seule case (« 4 disquettes »,
« 3/4 disquettes » s'il en manque). Un bouton à côté repasse à une case par disquette.

Un dossier qui n'est pas un DAT (« Atari › ST ») montre les titres de tous ses DATs. Au-delà de 100 000 titres, rien
n'est chargé : choisissez un sous-dossier ou cherchez.

## Filtres

- **Versions originales seulement** : sans cracks, hacks, trainers, traductions…
- **Une version par titre** : garde la meilleure version de chaque jeu (dump vérifié, puis original, version finale,
  votre langue préférée, version possédée, la plus récente).
- Possession, note, types de version : seuls ceux que portent les noms de la collection sont proposés.

## Recherche

Le champ de recherche en haut à droite cherche dans toute la collection : par nom (ou par un jeu d'une compilation), ou
par somme (CRC32, MD5 ou SHA1 collé). La recherche se filtre par machine, type de version, possession, note, genre.
**En faire une liste intelligente…** garde la recherche comme liste.

## Fiche d'un jeu

Double-clic sur un jeu : sa fiche. Elle montre les fichiers et leur état, les infos et les médias, les autres versions
et collections où il est, vos notes, ses étiquettes, ses statistiques de jeu sur vos appareils, ses sauvegardes, et
l'émulateur choisi pour lui.

## Notes et étiquettes

- **Note** : la vôtre, sur 20, ou celle de ScreenScraper. Elle vaut pour toutes les versions du titre, dans toutes les
  collections, et sert au tri et aux filtres.
- **Notes personnelles** : un texte libre sur la fiche.
- **Étiquettes** (« À deux », « Enfants »…) : sur la fiche, pour toutes les versions du jeu ; elles servent aux listes
  intelligentes.

## Favoris et listes

Onglet **Listes**, à côté de l'arborescence, et clic droit sur un jeu.

- **Favoris** : clic droit › **Ajouter aux favoris**.
- **Listes personnelles** : **Nouvelle liste…**, puis clic droit sur un jeu › **Ajouter à une liste**. Les listes suivent
  les jeux d'un pack à l'autre, même renommés.
- **Listes intelligentes** : **Liste intelligente (par règles)…**. Des règles sur la machine, le dossier, le nom, le type
  de version, la possession, la note, les genres, les modes de jeu, la série, vos étiquettes, les parties jouées sur
  vos appareils (« jamais joués », « joués ces 30 derniers jours »), une version par titre. La liste se recalcule après
  chaque scan et chaque synchronisation.
- **Place maximale** : une règle de liste intelligente qui garde les titres les mieux notés tant qu'ils tiennent dans une
  taille donnée. **Lire la place de l'appareil** la remplit d'après un appareil, en laissant une réserve pour son cache
  et ses sauvegardes.

Un jeu sur plusieurs disquettes ou disques entre dans une liste avec tous ses morceaux.
