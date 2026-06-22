# Combat

## Format

Combat tactique au tour par tour sur une grille ou un espace discret equivalent. Le joueur observe, planifie, donne des ordres, puis valide.

## Unites du joueur

- Heros : controle direct, fragile, condition de defaite.
- Robots : comportement autonome selon script.

## Intentions ennemies

Les ennemis annoncent leurs intentions avant la validation du tour : attaque, deplacement, cible, zone d'effet ou action speciale.

## Execution

Decision a verrouiller pour Unity :

- Execution strictement simultanee.
- Execution par initiative.
- Execution par phases : interruptions, deplacements, attaques, effets.

Recommandation prototype : phases simples, afin de faciliter debug et lisibilite.

## Conditions de defaite

- Mort du heros.
- Objectif critique echoue.
- Extraction impossible.

## Conditions de succes

- Objectif rempli.
- Extraction reussie.
- Donnees ou technologies recuperees.
