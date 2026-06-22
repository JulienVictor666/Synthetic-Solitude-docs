# Synthetic Solitude - GDD Master

## Identite

Synthetic Solitude est un roguelite tactique au tour par tour en 3D isometrique. Le joueur incarne un humain augmente, survivant d'un vaisseau de guerre ecrase sur une planete ennemie. Il combat avec une escouade de robots autonomes dont les comportements sont programmes par blocs.

Le coeur du jeu repose sur une tension simple : le joueur prepare ses robots comme des systemes autonomes, mais doit aussi intervenir en combat avec un heros fragile et limite.

## Pitch

Un humain augmente, seul survivant conscient d'un vaisseau ecrase, tente de survivre dans un monde hostile. Les robots du vaisseau sont reconstruits run apres run, equipes, programmes et envoyes en mission. Chaque expedition rapporte des technologies, des pieces, des donnees et des fragments de verite sur le monde, la guerre et la nature du protagoniste.

## Genre

- Tactique au tour par tour.
- Roguelite.
- Strategie programmable.
- 3D isometrique.
- Ambiance sombre, introspective et post-apocalyptique.

## Piliers

1. Programmer avant d'agir : les robots doivent etre preparables, testables et ameliorables.
2. Adapter pendant le combat : le heros peut donner des ordres contextuels sans remplacer toute la logique autonome.
3. Lire le futur proche : les intentions ennemies sont visibles, facon Into the Breach.
4. Construire une equipe asymetrique : chaque robot a des emplacements et roles differents.
5. Faire progresser le malaise narratif : la frontiere entre humain, machine, conscience et isolement devient floue.

## Boucle principale

1. Retourner au hub dans le vaisseau.
2. Choisir une mission.
3. Adapter les equipements et scripts des robots.
4. Sortir en run courte et intense.
5. Lire les intentions ennemies, valider le tour, observer l'execution.
6. Revenir au hub avec ressources, pertes, deblocages et narration.

## Combat

Le combat est tactique, au tour par tour, avec execution simultanee ou semi-simultanee apres validation. Les robots agissent selon leurs scripts. Le heros agit directement et peut fournir des ordres tactiques temporaires : cible prioritaire, zone dangereuse, position forcee, mode defensif, mode offensif ou evacuation.

Le heros est puissant mais fragile. Sa mort met fin a la run. Les robots sont des outils essentiels, mais leur comportement depend de la qualite de la programmation du joueur.

## Programmation des robots

Chaque robot dispose d'un programme compose de lignes. Une ligne contient des tests puis des actions. Si les tests sont vrais, les actions sont executees dans l'ordre. Sinon, le programme passe a la ligne suivante.

Le programme se divise en deux zones :

- Zone principale : lignes lues de haut en bas, puis boucle.
- Zone d'interruption : lignes prioritaires verifiees entre les lignes principales.

La complexite progresse avec le jeu : plus de lignes, plus de blocs, variables, cooperation, priorites et interruptions multiples.

## Progression

Les runs debloquent :

- Pieces de robots.
- Armes.
- Capteurs.
- Paquetages.
- Modules d'IA.
- Nouveaux blocs de logique.
- Nouveaux types de robots.
- Reparations et ameliorations du vaisseau.

La progression doit augmenter les options strategiques sans transformer le jeu en simple accumulation de puissance.

## Monde et narration

Le hub est l'interieur d'un vaisseau ecrase. Le protagoniste reapparait apres les runs dans une cuve de regeneration. Les robots sortent d'une ligne d'assemblage. Ces retours sont des moments narratifs : solitude, doute, perte de reperes, relation ambigue avec les robots et l'IA du vaisseau.

Le joueur doit progressivement douter de ce qu'il voit : les robots evoluent-ils vraiment, ou le heros projette-t-il une conscience sur eux ?

## Direction artistique

Le jeu vise une 3D low-poly stylisee, lisible, sombre et metallique. Le hub doit etre diegetique, avec des menus integres a l'environnement. Les combats doivent rester tres lisibles malgre l'ambiance : silhouettes nettes, intentions claires, feedback immediat.

## Premier prototype recommande

Le premier prototype Unity doit viser un seul combat vertical :

- Une grille tactique simple.
- Un heros jouable.
- Deux robots programmables.
- Trois ennemis.
- Un systeme minimal de lignes `conditions -> actions`.
- Une previsualisation des intentions ennemies.
- Un bouton de validation du tour.
- Un mode debug montrant quelle ligne de script est executee.
