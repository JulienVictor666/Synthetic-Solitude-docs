# Systeme De Programmation Par Blocs

## Objectif

Permettre au joueur de definir le comportement des robots sans ecrire de code. Le systeme doit etre visuel, testable et comprehensible pendant un combat automatique rapide.

## Structure d'un programme autonome

Un programme contient des lignes classees par priorite. Chaque ligne suit le format :

`SI conditions vraies -> executer une action`

Lorsqu'un robot peut prendre une nouvelle decision, il lit les lignes de haut en bas. La premiere ligne valide fournit l'action. Si aucune ligne n'est valide, le robot utilise un comportement de secours clairement affiche.

## Priorites reactives

Les urgences autonomes sont placees en haut du programme : esquiver une zone dangereuse, reparer un allie critique, reculer ou interrompre une attaque. Elles ne mettent jamais le combat en pause et ne demandent aucune action du joueur.

Les priorites reactives ne doivent pas etre confondues avec les protocoles d'intervention du joueur, decrits dans `player_interventions.md`.

## Blocs speciaux

- `Definir variable` : memoriser une cible, un allie ou une position.
- `Effacer variable` : oublier une valeur devenue inutile.
- `Attendre` : ne rien faire pendant une courte duree.
- `Mode` : lire un etat interne ou un mode temporaire accorde par une intervention.

`STOP` et `RESET` viennent de l'ancien modele sequentiel. Leur utilite dans un systeme reevalue a chaque decision doit etre validee avant de les conserver.

## Progression

- Debut : conditions simples, actions simples et peu de lignes.
- Milieu : variables, priorites, capteurs avances et cooperation.
- Fin : programmes plus longs, partage d'informations et comportements specialises.

## Points a specifier

- Frequence de reevaluation du programme.
- Duree et cout en energie de chaque action.
- Comportement si plusieurs cibles satisfont la meme ligne.
- Comportement de secours lorsqu'aucune ligne ne fonctionne.
- Possibilite ou non de corriger une ligne entre deux combats.
