# Données et réglages

[← Sommaire](index.md)

## Où sont vos données

Dans la version portable, tout est dans le dossier `Data`, à côté de `Retrolith.exe` : la base (`retrolith.db`), les
réglages, les médias (`media`), les sauvegardes de la base (`backups`), les sauvegardes des jeux (`saves`) et les
journaux (`logs`). Vos ROMs restent dans les dossiers racines de vos collections : Retrolith ne les copie pas dans
`Data`.

## Base de données

Menu « ⋯ » › **Base de données** :

- **Sauvegarder la base…** : une copie complète, même pendant une opération. La base est aussi sauvegardée chaque
  semaine et avant chaque mise à jour.
- **Restaurer une sauvegarde…** : remplace la base au prochain démarrage.
- **Compacter la base…** : rend au disque la place libérée.
- **Exporter les données personnelles (JSON)…** : ce qui ne se recalcule pas (listes, notes, infos des jeux,
  appareils, réglages des collections), dans un fichier lisible.
- **Ouvrir le dossier des sauvegardes**.

## Dossier de données partagé

Pour utiliser Retrolith sur plusieurs PC, **jamais en même temps** : menu « ⋯ » › **Dossier de données partagé…**.
Choisissez un dossier sur un partage réseau, OneDrive ou Synology Drive. Listes, notes, appareils, réglages des
collections, infos ScreenScraper et catalogues personnels y sont écrits ; la base reste sur chaque PC. Une version plus
récente est reprise au démarrage ; en cas de conflit, vous choisissez, et l'autre version est gardée en sauvegarde.

## Opérations longues

Une seule opération d'écriture à la fois (scan, ajout, réparation…). Elle s'annule, et vous pouvez continuer à consulter
la collection pendant ce temps. Les tâches de fond (ScreenScraper, logos, sauvegarde, intégrité) tournent à côté, dans
le panneau des tâches. Le PC ne se met pas en veille, l'avancement s'affiche sur l'icône de la barre des tâches, et une
notification annonce la fin.

## Langue

Menu « ⋯ » › **Langue / Language…** : français ou anglais, appliqué au redémarrage. Tant qu'aucune langue n'est
choisie, Retrolith suit celle de Windows. Les noms de fichiers et de dossiers écrits sur le disque restent en anglais.

## Mises à jour

Au démarrage, au plus une fois par jour, Retrolith regarde si une nouvelle version est publiée. Si oui, un bandeau la
propose : **Nouveautés** pour lire ce qui change, **Mettre à jour** pour la télécharger. Le zip est vérifié par sa
somme SHA-256 et mis en place au redémarrage. Rien ne s'installe sans ce clic, et vos données (`Data`) ne sont jamais
touchées. Sans réseau, rien ne s'affiche.

## Diagnostic

Menu « ⋯ » › **Diagnostic** :

- **Copier le diagnostic** : met dans le presse-papiers la version, le système, l'état de la base et la fin du journal,
  à coller dans un [ticket](https://github.com/TiticBE/Retrolith/issues) ;
- **Ouvrir le dossier des journaux de diagnostic** : un journal par jour (opérations, erreurs, gels de l'interface), gardé 30 jours.

Le **Journal des fichiers** (barre d'outils) liste les dernières copies, déplacements et suppressions.
