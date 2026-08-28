# Synthetic Solitude - GDD Master

## Identite

Synthetic Solitude est un roguelite autobattler de programmation en 3D isometrique. Depuis un vaisseau de guerre ecrase sur une planete ennemie, le joueur prepare une escouade de robots autonomes, programme leurs comportements, puis les envoie accomplir des missions courtes.

Le coeur du jeu repose sur une tension simple : transformer une intention en instructions, observer ce que les robots font reellement au contact de l'ennemi, puis corriger rapidement la programmation. Le joueur ne controle pas directement les robots pendant le combat, mais peut preparer un nombre limite de protocoles d'intervention.

## Pitch

Un humain augmente, seul survivant conscient d'un vaisseau ecrase, tente de survivre dans un monde hostile. Les robots du vaisseau sont reconstruits, equipes, programmes et envoyes en mission. Chaque expedition est une serie rapide de combats automatiques qui rapporte technologies, pieces, donnees et fragments de verite sur le monde, la guerre et la nature du protagoniste.

## Genre

- Autobattler tactique.
- Roguelite.
- Strategie programmable.
- 3D isometrique.
- Ambiance sombre, introspective et post-apocalyptique.

## Piliers

1. Programmer, observer, corriger : le resultat d'une modification doit etre visible rapidement.
2. Laisser agir sans perdre toute prise : les protocoles d'intervention offrent quelques actions rares et decisives.
3. Preparer avec une information imparfaite : les menaces principales sont annoncees, mais les missions avancees contiennent des inconnues.
4. Construire une equipe asymetrique : chaque robot possede des roles, equipements et capacites distincts.
5. Faire progresser le malaise narratif : la frontiere entre humain, machine, conscience et isolement devient floue.

## Boucle principale

1. Retourner au hub dans le vaisseau.
2. Choisir une mission en lisant ses risques, contraintes, inconnues et recompenses.
3. Composer, equiper et programmer l'escouade.
4. Choisir les protocoles d'intervention autorises.
5. Regarder les robots traverser trois ou quatre combats automatiques.
6. Entre les combats, choisir entre reparation, amelioration temporaire ou conservation des ressources.
7. Revenir au hub avec les ressources, pertes, deblocages et informations de diagnostic.

## Combat

Le combat se deroule automatiquement. Les robots avancent, choisissent leurs cibles et utilisent leurs capacites selon leur equipement et leur programme. Le joueur observe le comportement, les menaces et la ligne de programme active.

Avant la mission, le joueur programme aussi des declencheurs d'intervention : arrivee d'un ennemi puissant, robot sous un seuil de vie, alteration d'etat ou changement de phase d'un boss. Quand un declencheur valide survient, le combat se met brievement en pause. Le joueur peut depenser une action pour effectuer une reparation d'urgence, une attaque ciblee ou une autre action limitee, ou refuser et reprendre immediatement le combat.

Le budget d'actions est annonce avant le depart et depend de la taille de la mission. Il doit rester assez faible pour que la programmation soit la principale source de reussite.

## Programmation des robots

Chaque robot dispose d'un programme compose de lignes prioritaires. A chaque occasion de decision, il lit les lignes de haut en bas. La premiere ligne dont les conditions sont remplies fournit l'action a executer.

Le systeme distingue deux mecanismes :

- Programme autonome : logique executee par le robot sans arreter le combat.
- Protocoles d'intervention : declencheurs qui proposent au joueur de depenser une action limitee.

La complexite progresse avec le jeu : plus de lignes, plus de blocs, variables, cooperation et protocoles specialises.

## Progression

Les missions peuvent accorder comme recompense principale :

- Nouveaux blocs de programmation.
- Schemas d'armes.
- Nouveaux types de robots.
- Pieces et modules de robots.
- Capteurs.
- Paquetages.
- Modules d'IA.
- Reparations et ameliorations du vaisseau.

La progression doit augmenter les options strategiques sans transformer le jeu en simple accumulation de puissance.

Certaines missions imposent ou recommandent un type de robot ou une capacite precise. Ces contraintes servent a faire varier les equipes, mais doivent etre annoncees avant le depart.

## Monde et narration

Le hub est l'interieur d'un vaisseau ecrase. Les robots partent en mission et reviennent vers une ligne de maintenance ou d'assemblage. Ces retours sont des moments narratifs : solitude, doute, perte de reperes, relation ambigue avec les robots et l'IA du vaisseau.

La presence physique du protagoniste sur le terrain reste une question ouverte. Une piste est de la reserver a de rares missions a tres forte valeur, necessaires pour recuperer des ressources impossibles a manipuler a distance. Cette piste doit conserver les memes regles d'autobattle afin de ne pas creer un second jeu. La regeneration du protagoniste ne doit rester dans le concept que si ces missions rendent sa mort possible et significative.

Le joueur doit progressivement douter de ce qu'il voit : les robots evoluent-ils vraiment, ou le heros projette-t-il une conscience sur eux ?

## Direction artistique

Le jeu vise une 3D low-poly stylisee, lisible, sombre et metallique. Le hub doit etre diegetique, avec des menus integres a l'environnement. Les combats doivent rester tres lisibles malgre l'ambiance : silhouettes nettes, intentions claires, feedback immediat.

## Premier prototype recommande

Le premier prototype Unity doit tester une mission miniature :

- Deux robots programmables.
- Trois combats automatiques de moins d'une minute chacun.
- Trois familles ennemies aux comportements tres lisibles.
- Cinq a huit blocs de programmation.
- Deux choix de maintenance entre les combats.
- Deux protocoles d'intervention et un budget limite.
- Une fiche de mission annoncant menaces, recompense et une inconnue possible.
- Un mode debug montrant quelle ligne de script est executee.

Le critere principal du prototype est simple : apres un combat, le joueur doit vouloir modifier une ligne et relancer immediatement une mission.
