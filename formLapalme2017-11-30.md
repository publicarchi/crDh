# Lapalme 30 novembre 2017



IEML

Pierre Lévy, historien et chercheur en sciences des communications.

Une langue artificielle sur laquelle travaille depuis 20 ans. Écriture d’un dictionnaire et une grammaire de cette langue.

Langue naturelle, système symbolique sur lequel se met d’accord socialement pour communiquer. Une langue cet ensemble de symboles conventionnels

- Association entre le signifiant et un signifié qui est conventionnelle
- en général, il y a plusieurs signifiants différents pour un même signifié

Comment dans une langue naturelle on construit le sens. 

Au niveau cognitif

- Dictionnaire : sens des mots, ensemble de relations **paradigmatiques**
- Grammaire : Règles de compositions, relations **syntaxiques**

Au niveau social

- Pragmatique : sens que prennent les phrases dans un jeu social, ex. acte de langage, valeur de vérité

IEML langue naturelle

~ 5000 mots organisés en paradigmes

Nom/Verbe/Auxilliaire (trois classes)

Pour la grammaire, 3 types d’objets syntaxiques

- topic (sujet)
- fact (phrase)
- theory (texte structuré) un abre syntaxique de phrases pour construire un enchaînement logique de faits

Exemple de paradigme, les devenirs

Cette langue n’est pas conçue en copiant les relations sémantiques qui existent déjà dans les langues. Ici conçu comme des dimensions indépendantes pour chaque paradigme de sens.

Chaque mot reçoit une écriture en IEML, conçu de manière récursive. Part de 6 paradigmes de base, puis les multiplie ensemble pour obtenir des concepts de niveau supérieurs précis et particuliers.

Des briques que va ensuite utiliser partout dans le dictionnaire. Une notation polonaise inverse.

exemple M:M. devenirs

6 primitives | S signe (Sign) | B être (Being) | T chose (Thing)

Devenir du signe |  s. pensées | b. langage | t. mémoire

Devenir de l’être | k. société | m. affect | n. monde

Devenir de la chose | d. vérité | t. vie | l. espace

Résultat du dictionnaire une ensemble de paradigmes indépendants des autres.

Types de relations sémantiques du dictionnaire.

- relations paradigmatique
- relations germain : condition sur un couple de mots d’un même paradigme
- relation étymologique : les mots sont construits récursive ment à partir de mot...

Propriétés IEML

Dictionnaire composé de paradigmes avec des sens indépendants. 

=> Deux mots différents auront des sens différents

Normalisation de l’écriture des objets syntaxiques à l’aide de règle...

=>

Tous les signifiés ont un signifiant en IEML

IEML est un système de coordonnées de l’espace sémantique.

On appelle USL Uniforme Semantic Locator cette coordonnée

Librairie IEML développée en Python pour manipuler cette langue.

Une partie dictionnaire avec l’objet mot, cellule ou table. Un cellule de versioning.

Parseur pour créer graphe de relations sémantique entre les mots.

Grammaire et syntaxe.

Fonctionnalités sur la librairie, similarité sémantique, filtres, outils, path, USL

github

Exemple Intlekt

importation de collections de documents depuis les réseaux sociaux. Mapping #hashtags vers USL

Visualisation des collections

- quelles thématiques abordées, etc.
- quels hashtags significatifs

Collections importées de posts, pour un post donné peut voir les associations entre les mots clefs et les USL, traduit les mots clefs. Tables du dictionnaire pour identifier les mots-clefs.

Calcul de similarité, basé sur calcul de distance entre des USL. Fait une moyenne. Mais travailler le calcul car pour le moment les petits USL qui sont placés au centre.

Parallèle avec les technologies du web sémantique

Ensemble de formats de représentation et de validation des connaissances

- moteurs d’inférences
- beaucoup d’outils et de bases de données
- pas vraiment distribué au niveau du web car forte dépendance aux langues naturelles
- vocabulaires URI peuvent être redondants

IEML est une langue, on peut donc l’utiliser comme n’importe quelle langue avec les technologies du web sémantique. Par exemple pour remplacer des URIs pour désigner des concepts, ou pour traduire des facts en triplets d’inférence.

Dans IEML les relations ont aussi un nœud, donc pourrait aussi imaginer des traductions vers les formats du web sémantique.

Exemples d’applications et travail futur

- calcul sémantique : exploitation de la structure régulière d’IEML
- base de données avec un index sémantique
- synthèse/résumé de données non-structurées
- traduction LN -> IEML (algorithme de résumé de texte en IEML ou pour indexation)
- traduction IEML -> LN

https://github.com/IEMLdev

## Good Relations

Ontologie pour le commerce, Thibaut Bernard

- Contexte d’utilisation de l’ontologie
- Présentation des cas d’utilisation
- Avenir de l’ontologie et ce qui lui est arrivé depuis sa création

Martin Hepp, professeur de business Université Bundeswehr en Allemagne, travaille sur les structures de données partagées sur le web. Débuté ce vocabulaire en 2007 pour améliorer le commerce en ligne.

En 2007, e-commerce, possibilité de recherche sur des distributeurs ou des services, mais difficile de comparer des services ou des produits. Les informations pas interprétées par l’ordinateur mais devant être analysées par l’utilisateur manuellement. Dans ce contexte, volonté de créer une ontologie pour faciliter le e-commerce ou l’expérience utilisateur.

Une ontologie gratuite qui permet d’ajouter des informations concernant des produits. Spécifique au commerce en général, compatible avec les standards du W3C. Vise toutes les personnes qui offrent des produits ou du services, pour offrir visibilité.

Actuellement utilisée par Google, Yahoo! et BestBuy, ce qui lui a valu une forte pénétration.

Exemple d’utilisation avec Google pour un produit. Exemple recherche casque audio sur Google, résultas de recherche qui mettent en avant note, prix, présence en stock sur certains sites. Proche des Rich nippets de Google, car Good Relations utilisé dans les Rich Snippets.

Concrètement, ces informations sont codées sur le site web avec une référence à GoodRelation gr, puis peut définir diverses choses comme le nom du produit, sa description ou la relation du produit (vente, achat, etc.). Un identifiant pour le produit, normalement unique. Prix, mode de payements acceptés.

Exemple d’intégration pour un magasin. De même avec recherche Google, cherche le nom du magasin, affichage des informations issues de GoodRelations pour les horaires d’ouverture selon les jours, coordonnées, adresse, et description du magasin, etc.

Vcard pour les cartes de visites (car Yahoo!), spécification des horaires d’ouvertures avec GoodRelations.

Un outil développé pour créer des données à travers un formulaire qui permettait de renseigner les informations sur la société, le produit, etc.

Novembre 2012, GoodRelations a officiellement intégré Schema.org il en constitue actuellement la partie e-commerce. Mais désormais utilisable avec son namespace. On n’utilise plus de référence directe à GoodRelations même si reste compatible.

## Logique de description

ex. Preuve par tableau dans la logique de proposition

On a un langage très simplifié avec uniquement la négation et l’implication. Ce qui sera important savoir comment établir la négation d’un énoncé, et de passer chaque énoncé pour chaque construction.

Règles d’expansion, et conditions de fermeture, si contradiction.

Premier exemple, des implications et des négations. 

Savoir si cet énoncé est valide. Un énoncé est valide si pour toutes les affectations à X et Y c’est vrai. Ici facile car deux variables, celles-ci peuvent prendre vrai ou faux, pourrait tester chacune des quatre possibilités. Ici va plutôt utiliser la preuve par tableau.

On va prendre notre énoncé et ajouter le signe F à l’énoncé.

On va appliquer nos règles d’extension.

Dans l’approche par un tableau, une manière systématique de garder trace de toutes les dérivations possibles.

Genre de choses mieux faite par un ordinateur qu’un humain. Des solveurs qui sont capables de résoudre cela efficacement. Diverses stratégies pour ne pas exploser les branches, mais une façon systématique pour explorer la chose.

cf. ex diapos Bergeron

Lorsque l’on applique cela en logique de description, on va éliminer la TBox en remplaçant tous les termes par leur définition. Finalement se retrouve qu’avec la ABox.

Un peu comme pour la résolution va trouver une forme normale (pour la résolution s’appelait la forme clausale). Pour faciliter le travail, comme doit définir des règles d’expansion pour chaque élément de notre langage, on va remplacer les définitions de classes par ceci : grossi les termes mais systématique = moins de termes à faire.

De même comme pour la forme clausale, les négations devront être collées sur le nom des classes.

Enfin, montrer que la négation de ce qu’on veut prouver est insatisfaisante.

Transformations en NNF, un exercice de calcul symbolique. Le plus compliqué c’est finalement d’aller coller les négations sur chacune des classes. Le fait également sur les choses existentielles.

On a ensuite des règles de tableau pour la logique de description. Comme tantôt des règles seulement pour la négation et l’implication. En logique de description, des règles pour les ET alors ajoute deux lignes dans le tableau, un OU ajoutera un branchement.

Pour les trucs existentiels, une règle où trouvera un certain individu et que va ajouter.

passe comme cela à travers chacune des règles.

Important de retenir le fait que l’on a défini pour chacun des éléments de notre langage de logique de description la règle d’expansion.

Application : mon TBox et mon ABox, peut-on prouver que Mary est une Grand-mère ? Va le faire avec la méthode de tableau.

Première chose à faire, éliminer la TBox. On va donc transformer le fait que tout se base sur Person et Female et la propriété hasChild. Reprend les définitions pour chacun en supposant pour les besoins de la cause qu’il n’y a pas de définitions récursives. Mais des solutions pour faire cela si c’est le cas.

Tout est défini en termes de Person / Female et hasChild. On explose toutes nos définitions de la TBox.

Ensuite prend cela et va appliquer les règles de transformation en NNF de manière systématique (remplacement systématique). Ici forme négative normal forme de ma définition originale. Se simplifie beaucoup.

Une fois que l’on a ça, on va appliquer nos règles. Dans notre ABox, avait utilisé que les relations de base donc commode, mais ferait la même chose avec des trucs plus compliqué.

Ici repart avec nos choses, transforme notre ABox ex Man(Peter) devient ¬Female(PETER) et va appliquer règle de transformation pour la relation.

Ensuite on ajoute la négation de ce qu’on veut prouver et transforme.

Maintenant va commencer à essayer de fermer des branches, partout où des OU des branches.

Lorsque des pour tout, une règle qui dit que si règle qui contient ∀R.C(x) pour tout RC de x, et que des relations R(x,y), signifie que pour tous les enfants de Mary, il ne faudrait pas que soit des personnes. Or sait que hasChild(Mary,Paul) et hasChild(MARY,PETER)

Pour que soit fait faudrait que Paul ne soit pas une personne et Peter non plus.

Comme Paul et Peter sont des personnes va pouvoir fermer.

Mécanisme des preuves par tableau, un mécanisme général de preuve que l’on peut appliquer dans toutes les logiques pour autant que capable d’établir des règles d’expansion et de négations. Doit pouvoir déterminer que toutes les règles de branchement que met et règles de déductions sont des choses valides.

Mais adapté pour les reasoners de DL.

La logique de description DL est un formalisme de représentation de connaissance combinant les graphes sémantiques et la logique. C’est donc une façon de représenter les connaissances essentiellement par la classification d’objets. 

Et que nos inférences sont faites par la *subsomption*. Essentiellement, tout se ramène à savoir si un élément est dans une classe ou pas.

La Logique de description DL est idépendante du web sémantique, mais elle a permis de constituer une bonne base théorique pour formaliser le langage OWL. Par la suite, comme souvent en informatique, l’application a nourri la théorie. Cela a forcé les gens à s’intéresser au domaine, beaucoup d’impact sur la logique de description en forçant des développements sans quoi serait probablement resté un système de logique un peu ésotérique. Du fait de cette base solide, sait que quand fait des déductions dans le web sémantique, peut avoir confiance dans le fait que soit solide.

Retenir l’idée de base qui est lié au fait que les preuves sont souvent détournées, mais dans Protégé peut construire une ontologie sans prêter garde, mais par ce mécanisme là peut déterminer la consistance par l’implémentation de la validation par la logique par tableau.

Doc de Gagnon

Bonne introduction en Français

Ouvrage de Hitzler bonne introduction aux mathématiques et à la théorie.

Baader, la vraie bible sur la théorie du sujet. Exemple tiré de là.

Site de ressources sur la Logique de description.

Implémentations.





