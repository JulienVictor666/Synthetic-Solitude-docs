**Titre de travail : Synthetic Solitude**

---

## 1. Concept global

**Pitch :**
Un humain augmenté, seul survivant d’un vaisseau écrasé sur une base ennemie, doit survivre et comprendre sa nature en menant des robots de combat programmables. Chaque run permet d'améliorer la programmation de ses robots, de débloquer de nouveaux équipements et d'explorer les mystères d’un monde hostile.

**Genre :** Tactique au tour par tour, roguelite, stratégie programmable

**Vue :** 3D isométrique

**Références principales :** Final Fantasy XII (gambits), Into the Breach, The Last Remnant, Gladiabots

---

## 2. Structure de jeu

- **Hub central** : l’intérieur d’un vaisseau écrasé, servant d’interface pour toutes les fonctions hors combat (programmation, équipement, sélection des missions).
- **Runs** : sorties en terrain ennemi, combats tactiques à difficulté croissante avec mort permanente et retour au vaisseau.
- **Roguelite** : chaque échec permet de débloquer des blocs de logique, des capteurs, des pièces et d’améliorer la stratégie.

---

## 3. Gameplay principal

### 3.1 Le joueur (humain augmenté)

- Présent physiquement sur le terrain
- Peut se déplacer, attaquer, utiliser des modules spéciaux
- Peut changer le comportement des robots en combat (changer de "mode")
- Mort = fin de la run

### 3.2 Les robots

- Unité autonome basée sur une programmation visuelle modulaire
- Nombre initial : 2 (à définir), on pourra en débloquer plus ensuite 
- Types de robots : tireur, tank, éclaireur, soutien, assassin...
- Modules et capteurs modifient les comportements possibles
- Les robots disposent d’un certain nombre d’emplacements d’équipement (bras, jambes, torse, capteurs, IA, arme, paquetage), **variables selon leur type**. Exemple :
  - Éclaireur : 2 capteurs, mobilité accrue
  - Soutien : 2 paquetages
  - Robot d’assaut : 2 armes principales
- Cette asymétrie d’équipement favorise la spécialisation et la synergie d’équipe

- Unité autonome basée sur une programmation visuelle modulaire
- Nombre initial : 2 (à définir), on pourra en débloquer plus ensuite 
- Types de robots : tireur, tank, éclaireur, soutien, assassin...
- Modules et capteurs modifient les comportements possibles

### 3.3 Programmation visuelle

Le système de programmation repose sur une logique **visuelle par blocs**, conçue pour évoluer en complexité tout au long du jeu. Le joueur construit une **séquence de lignes** contenant chacune des tests et des actions. La programmation est divisée en deux zones principales :

- **Zone principale** : exécution ligne par ligne, de haut en bas
- **Zone d'interruption** : lignes prioritaires vérifiées entre chaque ligne principale (1 seule au départ, jusqu’à 2 ou 3 plus tard)

#### Fonctionnement d'une ligne
Chaque ligne suit cette structure :

- **Tests** : conditions à vérifier (ex : ennemi à portée, allié en danger, humain < 50% PV...)
- **Actions** : si tous les tests sont vrais, les actions sont exécutées dans l’ordre
- Si un test échoue, on passe directement à la ligne suivante
- Une fois toutes les lignes parcourues, on revient à la première (boucle automatique)

#### Types de blocs disponibles

- **Tests conditionnels** : visibilité, distance, points de vie, état d’un allié, possession d’une arme...
- **Actions** : déplacement, attaque, scan, lancer de grenade, tir de précision, etc. Aucune restriction sur leur enchaînement (actions mobiles ou fixes)
- **Blocs spéciaux** :
  - `Définir variable` : mémoriser une cible ou une position
  - `STOP` : interrompt la lecture après cette ligne
  - `RESET` : revient en début de séquence immédiatement

#### Interruptions

#### Commandes du personnage humain

Le joueur peut à tout moment émettre des **ordres tactiques directs** pendant une mission pour influencer temporairement les comportements des robots :

- **Définir une cible prioritaire** : les robots peuvent l'intégrer à leurs tests conditionnels pour adapter leur comportement offensif.
- **Marquer une zone dangereuse** : permet aux robots, s'ils sont programmés pour cela, d'éviter, contourner ou réagir différemment dans cette zone.
- **Ordre de déplacement forcé** : assigne un robot à un point spécifique. Toutes ses actions de mouvement sont suspendues ou redirigées vers ce point jusqu'à ce qu'il y soit arrivé ou que l'ordre soit annulé manuellement par le joueur.

Ces ordres sont des **variables temporaires ou prioritaires**, accessibles uniquement aux robots ayant une programmation adaptée à leur lecture. Ils permettent une forme d'override limité sans casser la logique programmée.

- Zone spéciale vérifiée entre chaque ligne principale
- Contient des lignes critiques : protéger l’humain, coopérer avec un autre robot, esquiver une explosion...
- Si la condition d’interruption est vraie, on exécute la ligne correspondante **avant de continuer la séquence**
- Au début, une seule ligne d’interruption ; on en débloque plus avec la progression

#### Interactions entre robots

- Certains blocs permettent de déclencher ou détecter des **actions coopératives** :
  - `Démarrer action synchronisée : arme lourde`
  - `Si robot A prépare arme lourde → se positionner pour assister`
- Ces actions offrent des **bonus** (précision, dégâts, rechargement assisté) mais demandent une bonne synchronisation dans les programmes

#### Évolution de la programmation

- **Début du jeu** : peu de blocs, logique simple, une seule ligne d’interruption
- **Milieu de jeu** : introduction des variables, tests plus complexes, priorités
- **Fin de jeu** : lignes longues, interactions entre robots, interruptions multiples, logique optimisée

Ce système favorise un **contrôle total** du comportement des robots, tout en laissant la place à des erreurs, de l’expérimentation et une amélioration progressive des stratégies.

- Pré-configurations stratégiques activables en combat
- Exemple : Mode défensif / offensif / évacuation

---

## 4. Progression & déblocage

- **Débloquables par run :**

  - Nouvelles pièces (armes, armures)
  - Nouveaux capteurs (infra-rouge, sonore, énergétique...)
  - Nouveaux blocs de logique
  - Nouveaux types de robots

- **Amélioration entre les runs :**

  - Modification du programme des robots
  - Évolution de l’équipement
  - Accès à des modes tactiques plus avancés

### 4.1 Équipements initiaux (exemples de base par catégorie)

**Capteurs :**
- Capteur optique standard : portée correcte, vision frontale, basique
- Radar circulaire : 360°, courte portée, flou
- Capteur thermique : détecte à travers la fumée, portée réduite

**IA :**
- IA basique : aucune ligne bonus
- IA de diagnostic : +1 ligne de script
- IA coopérative : débloque les blocs de coopération entre robots

**Paquetage :**
- Kit de réparation : permet de réparer un allié proche
- Munitions lourdes : permet d’assister un robot avec arme lourde
- Bouclier déployable : crée une zone défensive temporaire

**Bras :**
- Bras de tir classique : permet d’équiper une arme légère
- Bras stabilisateur : améliore la précision d’une arme lourde si robot immobile
- Bras outil : nécessaire pour réparation ou interaction complexe

**Jambes :**
- Jambes équilibrées : standard, aucun effet
- Jambes rapides : +1 case de déplacement
- Jambes lourdes : meilleure stabilité, moins de mobilité

**Torse :**
- Blindage standard : bonne défense
- Coque énergétique : +1 point d’énergie utilisable
- Système de refroidissement : réduit les temps de récupération de certaines actions

**Armes (principales) :**
- Mitrailleuse légère : tir en mouvement, dégâts faibles mais rapides
- Lance-flamme : zone courte, utile contre groupes
- Fusil de précision : longue portée, nécessite d’être immobile
- Canon lourd : nécessite un robot assistant avec munitions lourdes

Chaque robot commence avec une configuration simple, et les équipements sont débloqués, améliorés ou échangés au fil des runs.

- **Débloquables par run :**

  - Nouvelles pièces (armes, armures)
  - Nouveaux capteurs (infra-rouge, sonore, énergétique...)
  - Nouveaux blocs de logique
  - Nouveaux types de robots

- **Amélioration entre les runs :**

  - Modification du programme des robots
  - Évolution de l’équipement
  - Accès à des modes tactiques plus avancés

---

## 5. Direction artistique & ambiance

- **Ambiance** : sombre, introspective, questionnement sur l’identité humaine
- **Esthétique** : tons bleus, gris métalliques, flashes lumineux
- **Hub (vaisseau)** : diégétique, hublots donnant sur l’extérieur où des tirs ennemis et le bouclier du vaisseau sont visibles
- **Robots** : lisibles, anguleux, personnalisables visuellement par pièces

---

## 6. Thèmes narratifs

- Solitude prolongée et perte de repères humains
- Question de l’humanité persistante après l’augmentation (modification cérébrale)
- Dialogue intérieur ou avec une IA froide du vaisseau
- Possible révélation sur l’origine de la guerre, la nature réelle du héros, ou l’IA qui le maintient en vie
- **Avancement narratif** : après chaque run, à la réapparition dans le hub, le personnage semble sortir d’une cuve de régénération, tandis que les robots émergent d’une ligne d’assemblage. Ces moments servent à faire progresser les réflexions existentielles du protagoniste sur sa condition.
- **Dialogue intérieur** : se déroule uniquement après une run, dans la cuve ou en observant les robots. Progressivement, le personnage commence à entendre les robots lui parler — sans qu’on sache si c’est une **véritable évolution des IA** ou une **perte de repères mentaux**. À terme, il leur répond, installant un **malaise grandissant** autour de la frontière floue entre conscience, isolement et folie.
- **Anticipation des ennemis** : le joueur peut voir les intentions ennemies à l'avance (à la manière de *Into the Breach*), une capacité rendue possible par les **augmentations cérébrales du protagoniste**. Cette faculté devient un élément narratif : le héros perçoit de mieux en mieux les futurs probables, au prix de sa propre stabilité mentale.

- Solitude prolongée et perte de repères humains
- Question de l’humanité persistante après l’augmentation (modification cérébrale)
- Dialogue intérieur ou avec une IA froide du vaisseau
- Possible révélation sur l’origine de la guerre, la nature réelle du héros, ou l’IA qui le maintient en vie
- **Avancement narratif** : après chaque run, à la réapparition dans le hub, le personnage semble sortir d’une cuve de régénération, tandis que les robots émergent d’une ligne d’assemblage. Ces moments servent à faire progresser les réflexions existentielles du protagoniste sur sa condition.
- **Dialogue intérieur** : se déroule uniquement après une run, dans la cuve ou en observant les robots. Progressivement, le personnage commence à entendre les robots lui parler — sans qu’on sache si c’est une **véritable évolution des IA** ou une **perte de repères mentaux**. À terme, il leur répond, installant un **malaise grandissant** autour de la frontière floue entre conscience, isolement et folie.

---

## 7. Inspirations spécifiques

- *Final Fantasy XII* (programmation par conditions)
- *Into the Breach* (prévisualisation des actions ennemies)
- *Gladiabots* (programmation visuelle et logique IA)
- *The Last Remnant* (limitation volontaire des ordres disponibles)

---

> **Statut :** Prototype de concept en cours de développement. Ce GDD est amené à évoluer régulièrement.

