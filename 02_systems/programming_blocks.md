# Systeme De Programmation Par Blocs

## Objectif

Permettre au joueur de definir le comportement des robots sans ecrire de code. Le systeme doit etre visuel, testable et comprehensible en combat.

## Structure d'un programme

Un programme contient :

- Une zone principale.
- Une zone d'interruption.
- Des lignes composees de tests et d'actions.

## Structure d'une ligne

Une ligne suit le format :

`SI tests vrais -> executer actions dans l'ordre`

Si un test echoue, la ligne est ignoree et le programme passe a la suivante.

## Interruptions

Les interruptions sont verifiees entre les lignes principales. Elles servent aux cas critiques : proteger le heros, esquiver une explosion, reparer un allie, assister une arme lourde.

## Blocs speciaux

- `Definir variable` : memoriser une cible ou position.
- `STOP` : arreter la lecture apres cette ligne.
- `RESET` : revenir immediatement au debut.
- `Mode` : lire l'ordre tactique actif du heros.

## Progression

- Debut : conditions simples, actions simples, une interruption.
- Milieu : variables, priorites, capteurs avances.
- Fin : cooperation, interruptions multiples, scripts longs.

## Point a specifier

Il faut definir le cout exact des actions : une ligne peut-elle executer plusieurs actions dans un meme tour, ou chaque action consomme-t-elle une ressource ?
