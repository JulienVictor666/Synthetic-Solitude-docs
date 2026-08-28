# Combat

## Format

Combat tactique automatique dans un espace lisible en 3D isometrique. Apres le lancement, les robots se deplacent, choisissent leurs cibles et utilisent leurs capacites selon leurs programmes.

Le prototype doit tester un espace continu simple ou des positions discretes masquees sous le deplacement. Ce choix doit favoriser la lisibilite des comportements, pas la precision manuelle.

## Unites du joueur

- Robots : comportement autonome selon programme, equipement et capteurs.
- Protagoniste : absent des missions ordinaires. Sa presence dans certaines missions rares reste a valider.

## Intentions ennemies

Les attaques dangereuses doivent etre telegraphiees : zone d'effet, charge, cible verrouillee, renfort ou changement de phase. Le joueur ne valide pas chaque action, mais doit pouvoir comprendre le danger avant son execution.

## Execution

Chaque robot reevalue son programme lorsqu'il peut prendre une nouvelle decision. La premiere ligne valide determine son action. Les frequences exactes de decision, deplacement, attaque et reevaluation sont a verrouiller dans le prototype.

Le combat ne se met en pause que dans trois cas :

- Un protocole d'intervention programme se declenche.
- Le joueur ouvre volontairement le diagnostic, si cette fonction est conservee apres prototype.
- Le combat ou une phase de boss se termine.

## Interventions

Un declencheur valide ouvre une pause courte. Le joueur peut :

- Depenser une action pour une attaque ciblee.
- Effectuer une reparation d'urgence.
- Renforcer temporairement une defense.
- Imposer une cible commune.
- Refuser l'intervention et reprendre immediatement.

Le budget est commun a toute la mission et annonce avant le depart. Le declenchement seul ne consomme rien ; seule l'action choisie consomme une charge. Un meme etat ne doit pas provoquer des pauses repetitives.

## Conditions de defaite

- Destruction de toute l'escouade.
- Objectif critique echoue.
- Retraite ou extraction devenue impossible.

## Conditions de succes

- Dernier combat remporte.
- Objectif de mission accompli.
- Extraction de la ressource ou de la technologie reussie.
