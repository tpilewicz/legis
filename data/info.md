
<h1>Description du jeu de données</h1>

Le csv final à utiliser est merge.csv. Il contient également les résultats de 2017.

Chaque observation représente une des 577 circonscriptions une année donnée. En 2010, les circonscriptions législatives ont été redécoupées, et un couple département circonscription ne représente pas toujours le même endroit avant et après ce redécoupage. C'est pourquoi nous n'utiliserons pas les variables catégorielles indiquant département et circonscription dans la prédiction des scores de législatives.
Liées à chaque circonscription et pour chaque année, nous avons des variables d'entrée qui sont soit des scores de présidentielles, soit des données sociodémographiques. Malheureusement il n'est possible d'obtenir ces données qu'au niveau départemental.
Enfin les variables à prédire sont des scores de premier tour des législatives, cette fois bel et bien au niveau de la circonscription. Pour des modèles de classification, on aggrègera les scores en une variable catégorielle qui représente le groupe politique ayant rassemblé le plus de voix pour chaque circonscription.

Les variables :

<h2>Variables d'entrée</h2>

- dep : numéro de département. A noter que les français de l'étranger ont été exclus du jeu de données car de nombreuses données étaient manquantes à leur sujet.

- circ: numéro de circonscription

- year : année. Le jeu de données va des élections législatives de 93 à celles de 2017.

- pop : population du département.

- dens : densité de population du département.

- age_1, age_2, age_3, age_4 : proportion de chaque tranche d'âge dans la population du département. La tranche 1 correspond aux 0-20 ans, la tranche 2 20-40 ans, puis 40-60 ans puis 60 ans et plus.

- etud : proportion d'étudiants dans la population du département

- hf : ratio homme/femme dans la population du département.

- chom : taux de chômage dans le département.

- rev : revenu moyen dans le département.

- presid_... : ces variables contiennent les scores - au niveau départemental - aggrégés des 6 groupes politiques que nous avons dessiné : Centre (C), Droite (D), Extrême-Droite (ED), Gauche (G), Extrême-Gauche (EG), autres. L'attachement d'un candidat à un groupe politique a été déduit du parti pour lequel il se présentait. Pour consulter la façon dont nous avons fait le lien entre parti et groupe politique : data/attribution_groupes/presid. Voir le notebook python. Comme la logique de ce projet est de prédire des scores de législatives à partir des présidentielles les précédant, les lignes dont l'année est 1993 contiennent en réalité les scores de présidentielle de 88, les lignes dont l'année est 1997 contiennent en réalité les scores de présidentielles de 95.

<h2>Variables de sortie</h2>

(l_...)

Les variables à prédire sont des scores de législatives - au niveau circonscription cette fois - aggrégés des 6 groupes politiques que nous avons dessiné : Centre (C), Droite (D), Extrême-Droite (ED), Gauche (G), Extrême-Gauche (EG), autres. Les partis représentés sont plus nombreux au moment des législatives. Là aussi, il est possible de consulter l'attribution que nous avons fait de chaque parti à chaque groupe politique grâce aux notebooks python du dossier attribution_groupes/legis.

<h2>Sources</h2>

Les données sociodémographiques ont été téléchargées sur le site de l'INSEE.
Un petit script de scraping nous a permis de collecter les données de scores de présidentielles et de législatives sur le site du ministère de l'intérieur.
