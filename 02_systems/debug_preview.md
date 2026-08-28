# Debug Et Previsualisation

## Previsualisation ennemie

Le joueur voit les intentions dangereuses avant leur execution : cible, zone, charge, renfort ou action speciale.

## Previsualisation alliee

Avant la mission, le joueur doit pouvoir simuler des situations simples. Pendant le combat, il voit l'objectif actuel de chaque robot, la ligne active et la cible choisie.

## Mode debug

Le mode debug affiche :

- La ligne actuellement testee.
- Les tests vrais ou faux.
- L'action executee.
- Les interruptions declenchees.
- Les variables temporaires actives.

## Rapport d'apres-combat

Le diagnostic entre deux combats doit resumer :

- Les lignes les plus utilisees.
- Les lignes jamais validees.
- Les causes principales de degats et de destruction.
- Les protocoles declenches, acceptes ou ignores.
- Les moments ou aucun ordre valide n'etait disponible.

## Pourquoi c'est central

Sans debug clair, l'autobattle paraitra aleatoire. Le joueur doit pouvoir se dire : "j'ai compris pourquoi il a fait ca, et je sais quelle ligne essayer de changer".
