# Protocoles D'Intervention Du Joueur

## Objectif

Donner au joueur une prise rare sur un combat automatique sans lui permettre de corriger en permanence une mauvaise programmation.

## Preparation

Avant le depart, le joueur equipe un nombre limite de protocoles. Chaque protocole associe :

- Un declencheur observable.
- Une ou plusieurs actions autorisees.
- Une priorite si plusieurs protocoles se declenchent en meme temps.

Exemples de declencheurs :

- Un robot passe sous 20 % de vie.
- Un ennemi puissant entre dans le combat.
- Un robot subit une alteration d'etat.
- Un boss passe dans une nouvelle phase.
- Une cible de mission est menacee.

## Declenchement

Quand les conditions deviennent vraies, le combat se met en pause et presente la cause de l'interruption. Le joueur peut effectuer une action ou refuser. Le combat reprend immediatement apres la decision.

Le declenchement ne consomme pas de charge. Seule l'execution d'une action consomme une unite du budget de mission.

## Actions possibles

- Attaque ciblee.
- Reparation d'urgence.
- Bouclier ou reduction temporaire des degats.
- Cible prioritaire commune.
- Purge d'une alteration d'etat.
- Retraite d'urgence, si la mission l'autorise.

Toutes les actions ne sont pas disponibles des le debut. Certaines peuvent etre debloquees par des modules, des ameliorations du vaisseau ou des ressources rares.

## Budget par taille de mission

Le nombre exact sera equilibre par prototype. Regle de depart recommandee :

- Mission courte : 1 a 2 actions.
- Mission standard : 2 a 3 actions.
- Mission critique : 3 a 4 actions.

Le joueur connait son budget avant de composer l'escouade. Une mission plus longue donne davantage d'actions, mais aussi davantage de combats et d'inconnues.

## Protections contre les pauses repetitives

- Un seuil ne se declenche qu'au moment ou il est franchi.
- Un protocole refuse ne se repropose pas tant que son etat n'a pas ete reinitialise.
- Un delai minimal separe deux interruptions.
- Plusieurs evenements simultanes sont regroupes dans une seule pause.

## Questions a tester

- Le joueur choisit-il une action precise lors de la programmation ou un petit choix au declenchement ?
- Une intervention peut-elle modifier temporairement le programme d'un robot ?
- Le joueur peut-il provoquer manuellement une interruption en depensant plus de ressources ?
- Quel nombre de pauses reste satisfaisant dans un combat de moins de 90 secondes ?
