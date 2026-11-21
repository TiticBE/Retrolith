# Infos et médias

[← Sommaire](index.md)

## ScreenScraper

[ScreenScraper](https://www.screenscraper.fr/) est une base collaborative d'infos et de médias de jeux rétro. Il faut
un compte, gratuit.

1. **Réglages ScreenScraper…** (barre d'outils) : entrez votre identifiant et votre mot de passe ScreenScraper, puis
   choisissez les médias voulus (écran titre, captures, mix, boîtes 2D et 3D, support, logo, manuel PDF…) et la langue
   des résumés. L'icône du bouton montre l'état du compte (coche verte si tout va bien).
2. **Infos ScreenScraper** sur un dossier ou une liste : chaque jeu est cherché par les sommes de ses ROMs, donc
   reconnu même mal nommé. La recherche tourne en tâche de fond ; vous pouvez continuer à utiliser Retrolith.

Sont récupérés : résumé, date, éditeur, développeur, genres et sous-genres, modes de jeu, série, nombre de joueurs,
note, et les médias choisis. Votre quota quotidien ScreenScraper s'applique.

**Compléter les genres des jeux déjà trouvés** va chercher les genres manquants sans retélécharger aucun média.

Les médias s'affichent en vignette à côté de chaque titre (trois tailles), en grand au survol, en galerie sur la fiche,
et partent sur vos appareils avec les jeux.

## Vos propres images

**Ajouter des images…** (clic droit sur un dossier) ou **Ajouter des images à la collection…** (menu de la collection),
sans ScreenScraper :

- choisissez un dossier où chaque image porte le nom exact d'un jeu (`Serenade #74.png`), à plat ou rangé comme la
  collection ;
- les captures d'écran vont à la racine ; les boîtes, écrans titres, logos et supports dans des dossiers `covers`,
  `titles`, `wheels`, `supports`.

Un média déjà récupéré sur ScreenScraper n'est pas remplacé, et ScreenScraper ne remplace jamais une image que vous avez
ajoutée. Le bilan compte les images sans jeu du même nom.

## Logos et photos des machines

Le logo et la photo de chaque machine s'affichent en haut du dossier choisi et dans la vue par machine. Les logos des
marques (Commodore, Nintendo, Sega…) sont pris sur Wikidata au premier affichage et gardés sur le disque. Une image
`media\brands\<marque>\logo.png` posée à la main reste prioritaire.

## Le dossier des médias

Les médias sont gardés dans `Data\media`. Ce dossier peut être déplacé (copie vérifiée) ou partagé avec un autre PC
(voir [Données et réglages](data-and-settings.md)).
