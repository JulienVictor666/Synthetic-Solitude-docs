
# Synthetic Solitude - Game Design Document

## 1. Présentation & Concept
Synthetic Solitude est un roguelite tactique en 3D isométrique au tour par tour. Le joueur incarne un humain augmenté, accompagné d’une escouade de robots de combat programmables. Les robots suivent des comportements définis via un système de programmation par blocs, mais le joueur peut intervenir directement pour donner des ordres contextuels.

L'objectif est de combiner planification stratégique et adaptation rapide en combat, tout en explorant les limites entre humanité et artificialité.

## 2. Pitch narratif
Dans un monde post-apocalyptique, un vaisseau de guerre écrasé sur une planète ennemie devient le dernier refuge du protagoniste. L’humain, gravement blessé et amélioré cybernétiquement, lutte pour survivre avec l’aide de robots produits par les usines endommagées du vaisseau.

Chaque run est une sortie hors du vaisseau pour remplir des missions, affronter différentes factions ennemies et récupérer des technologies. Entre les runs, le héros revient dans le hub (l'intérieur du vaisseau) pour programmer ses robots et améliorer son arsenal.

## 3. Atmosphère & style visuel
- **Tonalité :** sombre, mélancolique, introspective
- **Ambiance :** solitude, menace constante, technologie en ruine
- **Direction artistique :** 3D low-poly stylisée avec éclairages dramatiques, contrastes forts et effets de particules pour renforcer la tension

## 4. Boucle de gameplay
1. Choisir une mission dans le hub
2. Adapter l’équipement et la programmation des robots
3. Sortir pour une run courte et intense
4. Survivre, remplir des objectifs et récolter des ressources/technologies
5. Retour au hub pour méta-progression et narration

## 5. Structure des runs
- Runs courtes (10-20 minutes)
- Environnements variés : ruines, zones industrielles, territoires tribaux techno-barbares, zones mutantes
- Difficulté progressive : début avec ennemis faibles et peu nombreux → fin avec hordes massives et colosses

## 6. Système de programmation par blocs
- **Zone principale** : enchaînement libre de mouvements, actions mobiles ou immobiles
- **Zone d’interruption** : exécution prioritaire, 1 ligne au début, jusqu’à 3 lignes débloquées avec progression
- Déblocage progressif des blocs pour éviter surcharge cognitive
- Blocs disponibles : conditions (IF), actions, variables, arrêts de programme
- Possibilité de copier/coller, sauvegarder et dupliquer des scripts
- Mode “débogage” : visualisation ligne par ligne avant validation du tour

## 7. Équipements & progression des robots
Catégories d’équipement :
- **Bras** : armes, modules utilitaires
- **Jambes** : vitesse, franchissement d’obstacles
- **Torse** : défense, points de vie, vitesse de génération d’énergie
- **Capteurs** : précision, vision à travers fumée/murs, analyse de cibles
- **IA** : ajout de lignes de programmation, nouveaux blocs, meilleure détection
- **Armes** : primaires, secondaires, lourdes
- **Paquetage** : kits de soin, réparation, munitions lourdes

Différents types de robots ont des emplacements différents (ex. éclaireur : 2 capteurs, soutien : 2 paquetages, assaut : 2 armes).

## 8. Capacités du héros
- Don d’ordres contextuels (priorité, danger, position fixe)
- Mobilité améliorée (sauts impossibles pour un humain)
- Buff temporaire d’un robot (double vitesse)
- Défense limitée, héros fragile à protéger
- Vision anticipée des actions ennemies (grâce à augmentations)

## 9. Évolution et méta-progression
- Déblocage d’équipements et de blocs via découverte de technologies et réparation du vaisseau
- Progression narrative centrée sur les questionnements du héros
- Robots et héros gagnent en puissance, devenant surhumains

## 10. Ennemis & types de menaces
- **Humains redevenus sauvages** : agressifs mais peu organisés
- **Mutants intelligents** : rapides, imprévisibles
- **Tribus techno-barbares** : lourdement armés, vénèrent la technologie
- Variations de taille, résistance, vitesse, armement

## 11. Système de missions & variété stratégique
- Missions indiquent types de menaces dominantes (nombre, résistance, vitesse…)
- Incitation à varier programmation et équipement
- Types de missions : élimination, survie, récupération, assaut ciblé

## 12. Hub et menus immersifs
- Menu principal : vue extérieure du vaisseau, tirs automatiques, impacts sur bouclier
- Transition fluide vers l’intérieur du vaisseau
- Salle unique combinant programmation et équipement
- Interaction par clic sur éléments du décor pour ouvrir les menus

## 13. Interface, prévisualisation & mode débogage
- Prévisualisation des actions ennemies et alliées
- Mode débogage : lecture ligne par ligne des programmes des robots
- Validation du tour → exécution simultanée des actions

## 14. Ambiance sonore & musique
- Sons mécaniques, impacts métalliques, ambiance lourde
- Musique minimaliste avec nappes sombres
- Effets dynamiques pendant les combats
