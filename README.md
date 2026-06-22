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

1. Le format exact d'un tour de combat.
2. L'ordre d'execution des scripts de robots.
3. La difference entre ordres directs du heros et programmation autonome.
4. Le scope du premier prototype jouable.
