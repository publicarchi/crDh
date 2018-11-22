# Cr RALI 6 septembre 2017

## Alfonso Hermelo, Concilier les triplets extraits à partir de texte et de bases de connaissances.

KB base de données faites pour contenir des faits vérifiés humainement (cad attestés)

Les OIE (Open Information Extraction) extracteur d’informations libre pour constituer des triplets non attestés (subjectifs)

On prend un texte en langage naturel et essaye d’extraire les informations en triplets qui correspond le mieux. Le résultat n’est pas toujours parfait et il peut y avoir du bruit.

À quoi cela sert ?

Les KB sont très utilisées en recherche et dans l’industrie car elles permettent la vérification informative, la production de résumés factuels, de l’annotation de textes bruts, ou apporter un semblant de valeur sémantique.

Les OIE sont des outils très différents, mais on va essayer des les concilier. Les OIE permettent de générer des Ntriplets et des représentations plus compréhensibles par la machine.

Dans un premier temps, nous avions à l’esprit un système qui permettait de désigner une entité, et d’aller chercher sous forme de triplets toute l’information comparable à partir des OIE.

Problématiques et hypothèse

Problématiques

- Manque d’analyses statistiques entre KB et OIE. 
- Les KB négligent les informations subjectives.

Hypothèses

- les informations des KB et des OIE sont complémentaires. Les deux produisent des triplets en sortie.
- est-il possible de réduire le bruit des sorties OIE en utilisant des heuristiques —> nettoyer les triplets de sortie OIE

Pour les questions de recherche principale

Les informations des KB et OIE sont-elles complémentaires, et dans l’affirmative, comment intégrer les triplets subjectifs des OIE aux triplets objectifs des KB ?

## Développements

### Analyse de l’état de l’art

Pas trouvé d’état de l’art, mais plusieurs projets comparables analysés.

KB : Yago, Yago2, DBpedia, Nell, Wikidata, Freebase, Knowledge Graph, Knowledge Vault

OIE : reVerb, OLLIE, ClausIE, PropS, CSD-IE, OpenIE-4, Standford Open IE, **Banc d’essai de Stanovsky et Dagan** (le banc d’essai est à la fois un corpus et un outil qui permet une comparaison statistique dans un schéma).

La Knowledge Vault est souvent considéré comme un état de l’art. Article publié par un groupe de recherche de Google. Si en lisant l’article peut avoir l’impression que c’est déjà distribué, en réalité pas mis en place. Rien depuis 2014. Toutefois, cela nous a permis d’avancer dans le domaine et la recherche s’approche beaucoup de nos préoccupations.

- ressource d’entraînement : Freebase, Knowledge Graph
- KB peuplée sans intervention humaine
- 1 600 000 de faits
- 1 fait = 1 score de confiance
- Mais aucune idée si les scores de confiance sont basés sur des faits subjectifs, etc.

### Étapes de travail

#### Benchmarking des IE

Sélection des KB les plus complètes. Pour les méthodes, observation empirique et analyse statistique.

Les trois meilleurs Wikidata, Freebase et le Knowledge google graph

Pour la recherche, a réduit à une 100aine entités + Chilly Gonzales ! 80% des entités des titres articles de Wikipédia. Au final 20 entités.

Nombre de faits correspondants pour une entité, parmi les 485 faits de Freebase, 13 d’entre eux correspondent en sujet et en objet (13 faits que l’on retrouve). On n’a pas tenu compte des propriétés car un protocole pour la production des bases de connaissance.

Quid des propriétés sur les propriétés dans Freebase, pas retirés, allé chercher les triplets les plus profonds (triplifié Freebase).

#### Choix de l’OIE

Benchmarking avec Stanovsky et Dagan. Comparaison des résultats en précision et rappel. Pour choisir les 6 meilleurs OIE, comme ce qui nous intéresse le plus la précision et pas vraiment le rappel.

Les trois meilleurs en précision au seuil minimum OpenIE-4, PropS ou OLLIE mais PropS ne prenant que du ASCII laissé tombé, choix de ClausIE.

Même évaluation pour identifier ce qui était en commun. Analyse ici sujet propriété et objet pour vérifier les points communs. Savoir si pas nécessaire d’en prendre un en commun si tous les trois les mêmes résultats.

En match exact, peu. Montre que leur périmètres sont très différents.

#### Comparaison triplets OIE et faits de KB

Pour Chilly Gonzales rien de commun ! Mais pour nos 20 entités, pas nombreuses mais tout de même des faits en commun. Ici seulement sujet et objet, pour voir si correspond. 

- <u>Chilly Gonzales</u> wasBornIn <u>Montreal</u>
- <u>Chilly</u> Gonzales bornIn <u>Montreal</u>

Bien sûr capte aussi si *dieIn*. Mais même avec des cas optimiste donne zéro. On comprend qu’il n’y ait pas vraiment de  comparaison statistique. Les attentes sont très grandes mais les résultas pas très concluants.

### Les heuristiques

Union et intersection, score de confiance, sujet exact, sujet entité-partielle (tokenize), sujet dit. Levenshtein, sujet dit. word emb., sujet alias, sujet pronom (ici très naïve, capturait pour voir)

Diagramme de Venn des triplets de sortie capturés par les heuristique pour un ex d’entité.

Chacune de ces heuristiques passées dans la banc d’essai de Stanovsky et Dagan pour avoir une mesure de la précision.

Montre que la comparaison d’heuristique qui fonctionne le mieux, mais avec un rappel terrible, mais qui en terme de précision est proche de l’humain. Meilleurs résultats intersection ClausIE et OpenIE-4 pour les sujets de proche distance (le cas quand utilisait Sujet alias de l’Entité). Ici parmi les 10 000 triplets du benchamark

Question de seuil sur le score embedding, entre 0,7 et 0,8

## Contributions

Offre une première analyse des complémentarités entre les KB et sorties OIE. Les faits de KB choisies et des tripless de sortie choisie.

Une petite comparaison des heuristiques des OIE. Avec ces heuristiques parvenu à supprimer une grande partie du bruit.

## Discussion

Tous les extracteurs ont des méthodes différentes, d’autant que très souvent les phrases ne se triplaient pas. Qu’ont fait Stanovsky et Dagan ?

Repris le corpus d’entraînement de… et posaient toutes les questions possibles à partir d’une phrase. Le fait que sépare ou pas la préposition a beaucoup d’importance dans l’évaluation. En fait Stanovsky compte 1 si les têtes matchent, donc flexibles sur les positions, mais avec le bruit que peut imaginer. De même pour le complément, et pareil pour la relation.



