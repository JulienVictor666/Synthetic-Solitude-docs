# Synthetic Solitude - Documentation

Ce dossier contient la documentation de travail actuelle de Synthetic Solitude.

La documentation historique a ete conservee dans `old_documentation/`. Elle sert d'archive et ne doit plus etre consideree comme la source principale.

## Source de verite

- `GDD_MASTER.md` : vision consolidee du jeu.
- `00_vision/` : pitch, piliers et references.
- `01_game_design/` : boucle de jeu, runs, combat, missions et ennemis.
- `02_systems/` : systemes a specifier pour Unity.
- `03_content/` : catalogues de robots, equipements, blocs, ennemis et missions.
- `04_narrative/` : monde, protagoniste, progression narrative et themes.
- `05_art_audio_ui/` : direction artistique, audio, UI et hub.

## Regle de maintenance

Le `GDD_MASTER.md` donne la synthese. Les details vivants doivent aller dans les fichiers specialises.
Quand une decision devient stable, elle doit etre reportee dans le fichier specialise correspondant.

## Prochaine priorite

Avant de commencer la production Unity, il faut verrouiller :

1. Le rythme exact d'un combat automatique et sa duree cible.
2. La frequence de reevaluation des programmes de robots.
3. Le nombre d'interventions accorde selon la taille d'une mission.
4. Les ajustements autorises entre deux combats.
5. Le scope du premier prototype jouable.

## Historique de direction

Le tag Git `v0.1.0-pre-autobattler` conserve la documentation avant le recentrage du jeu sur des missions courtes en autobattle.
