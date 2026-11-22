# FAQ

[← Sommaire](index.md)

**Windows affiche « Windows a protégé votre ordinateur ». Est-ce dangereux ?**
Retrolith n'est pas encore signé numériquement ; Windows prévient pour tout programme récent et peu téléchargé. Cliquez
sur **Informations complémentaires**, puis **Exécuter quand même**. Pour vérifier le zip, comparez sa somme SHA-256
(`Get-FileHash Retrolith-<version>-win-x64.zip` dans PowerShell) au fichier `.sha256` publié à côté.

**Retrolith fournit-il des jeux ?**
Non. Il ne contient, ne télécharge et ne signale aucun site de jeux. Il gère les copies que vous possédez.

**Où trouver les DATs ?**
Sur les sites de [TOSEC](https://www.tosecdev.org/), [No-Intro](https://datomatic.no-intro.org/),
[Redump](http://redump.org/), [MAME](https://www.mamedev.org/) et [FinalBurn Neo](https://github.com/finalburnneo/FBNeo).

**Retrolith peut-il abîmer mes fichiers ?**
Il est fait pour l'éviter : rien n'est écrit sans aperçu, chaque zip est vérifié avant de remplacer l'ancien, toute
suppression passe par la corbeille (ou `_Retrolith Trash` sur un lecteur réseau), et chaque action est notée au journal
des fichiers. Gardez tout de même une sauvegarde de vos ROMs.

**Mes fichiers sont « à ranger ». Qu'est-ce que ça veut dire ?**
Ils sont reconnus, mais mal nommés ou mal placés. **Réparer la collection…** les range ; l'aperçu montre tout avant.

**Pourquoi tant de fichiers inconnus ?**
Ils ne correspondent à aucun DAT de cette collection : autre collection, autre version du pack, fichiers personnels. Un
clic sur la pastille en donne la liste. La réparation peut les mettre de côté dans `_Unknown`, ou ils peuvent rejoindre
un catalogue personnel.

**Le scan est lent.**
Le premier scan lit tout ; les suivants ne relisent que les fichiers changés. Sur un lecteur réseau, c'est surtout le
réseau qui compte. Pour aller vite, scannez seulement le dossier modifié (clic droit dans l'arborescence).

**Les actions CHD sont grisées.**
chdman est introuvable. Installez MAME et ajoutez son dossier au PATH, ou déclarez MAME dans LaunchBox ; voir
[Jeux sur disque et arcade](discs-and-arcade.md).

**ScreenScraper ne trouve rien.**
Vérifiez dans **Réglages ScreenScraper…** que l'icône montre une coche verte (compte reconnu) et que le quota du jour
n'est pas épuisé. Un jeu absent de la base de ScreenScraper n'aura pas d'infos ; vous pouvez ajouter vos propres images.

**Un jeu copié sur ma Recalbox ne s'affiche pas.**
Le système ne lit peut-être pas son format : l'aperçu de la synchronisation le signale. Pour l'arcade, vérifiez que le
jeu a son BIOS et ses CHD. Pensez à mettre à jour les listes de jeux de la Recalbox, ou à la relancer.

**Peut-on utiliser Retrolith sur deux PC ?**
Oui, pas en même temps : voir le dossier de données partagé dans [Données et réglages](data-and-settings.md).

**Comment signaler un problème ?**
Menu « ⋯ » › **Diagnostic** › **Copier le diagnostic**, puis ouvrez un
[ticket](https://github.com/TiticBE/Retrolith/issues) en le collant, avec ce que vous faisiez.

**Où poser une question ou proposer une idée ?**
Dans les [Discussions](https://github.com/TiticBE/Retrolith/discussions), en français ou en anglais.
