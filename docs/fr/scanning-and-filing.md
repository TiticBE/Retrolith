# Scanner et ranger

[← Sommaire](index.md)

## Scanner

**Scanner la collection** (barre d'outils) parcourt le dossier racine : fichiers simples, `.zip` et `.7z`, reconnus par
leur SHA1, leur MD5 ou leur CRC32 et leur taille. Un scan ne modifie aucun fichier.

- **Scan rapide** (par défaut) : le CRC32 des zips est lu dans leur en-tête, un fichier dont la taille ne correspond à
  aucune ROM n'est pas lu, et un fichier inchangé (même taille, même date) n'est pas relu.
- **Scan complet (SHA1)** (menu de la collection) : décompresse et relit chaque fichier. Bien plus long, il détecte
  aussi un fichier abîmé. Il reprend là où il s'était arrêté.
- **Scanner seulement ce dossier** et **Scan complet de ce dossier (SHA1)** : clic droit sur un dossier de
  l'arborescence.
- **Scanner toutes les collections** (menu de la collection) : un scan rapide de chacune, l'une après l'autre.
- Un scan interrompu se reprend par **Reprendre le scan interrompu** (menu « ⋯ », présent seulement dans ce cas).

## Les états

| État | Sens | Que faire |
|---|---|---|
| **Complet** | Tous les fichiers du jeu, au bon nom et à la bonne place | Rien |
| **À ranger** | Les fichiers sont là, mal nommés ou mal placés | Réparer |
| **Partiel** | Une partie des fichiers manque | Ajouter des ROMs, compléter depuis une autre collection |
| **Manquant** | Aucun fichier | Idem |

Les **fichiers inconnus** (qu'aucun DAT ne connaît) et les **doublons** sont comptés en pastilles. Un clic sur une
pastille donne la liste de ce qu'elle compte, à copier.

## Ajouter des ROMs

**Ajouter des ROMs…** (barre d'outils, ou glisser-déposer un dossier sur la fenêtre) : choisissez n'importe quel dossier.
Chaque fichier y est cherché dans tous les DATs de la collection.

1. **Aperçu** : titres complétés ou partiels, fichiers déjà présents, inconnus, place nécessaire. Rien n'est encore
   écrit.
2. **Copier** ou **déplacer** : chaque ROM va dans le zip officiel de son jeu (ou à sa place sans zip, selon la
   collection). Chaque zip est vérifié avant de remplacer l'ancien.

Un ajout interrompu (réseau coupé, application fermée) est proposé au démarrage suivant : **Reprendre** n'écrit que les
titres restants. Un dossier déjà analysé se réanalyse vite, même sur le réseau.

## Réparer

**Réparer la collection…** (barre d'outils), ou **Réparer ce dossier…** (clic droit dans l'arborescence), d'après le
dernier scan :

- les ROMs mal nommées ou mal placées sont rangées dans le zip officiel de leur jeu ;
- les fichiers devenus inutiles (doublons, copies une fois rangées) vont à la corbeille ;
- les fichiers inconnus peuvent être mis de côté dans `_Unknown`.

Même aperçu avant de toucher au moindre fichier. Toute suppression passe par la corbeille de Windows (ou par
`_Retrolith Trash` sur un lecteur réseau, qui n'a pas de corbeille). Chaque action est notée dans le **Journal des
fichiers** (barre d'outils).

## Compléter depuis une autre collection

Un jeu que vous possédez dans une autre collection (par exemple No-Intro et TOSEC) est signalé « possédé ailleurs ».
**Compléter depuis l'autre collection** copie dans celle-ci les titres qui lui manquent et que l'autre possède. Les
fichiers de l'autre collection ne sont jamais déplacés.

## Fixdat

**Exporter les manquants (fixdat)…** (menu de la collection), ou **Exporter les manquants de ce dossier (fixdat)…**
(clic droit sur un dossier) : écrit un DAT des seuls titres manquants ou partiels, à donner à ClrMamePro, RomVault
ou un autre outil. Les machines ignorées en sont exclues.

## Vérifier l'intégrité

À chaque démarrage, une tâche de fond relit en entier les fichiers d'une machine (celle vérifiée le moins récemment) et
compare leurs sommes à celles du dernier scan. Un fichier abîmé sans changer de taille ni de date, que le scan rapide
ne voit pas, est signalé. Menu de la collection › **Vérifier l'intégrité (machine suivante)** la lance tout de suite.

## Disquettes modifiées par un jeu

Un jeu lancé directement depuis son dossier peut écrire sur sa disquette. Retrolith la reconnaît au scan (« Disquette
modifiée par le jeu ») au lieu de la compter parmi les inconnus. La réparation la garde comme sauvegarde du jeu avant de
remettre la bonne copie.
