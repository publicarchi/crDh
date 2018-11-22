# cr Lapalme 28 novembre 2017

## Outils Python du Web sémantique

Zakaria Bouchlih

https://github.com/RDFLib

https://rdflib.readthedocs.io/en/stable/

Python est un langage créé par Guido van Rossum, aujourd’hui développé par Python software foundation. Communauté dynamique, utilisé sur de nombreuses plateformes scientifique. Le langage est très utilisé pour le calcul scientifique à l’instar de R.

- large communauté
- syntaxe simple
- calcul scientifique
- grand nombre de librairies dans Python package Index PyPi

AllegroGraph, triple store destiné au linked data.

RDFlib librairie de Python pour travailler avec RDF, simple et puissante en terme de représentation d’information. Parse des fichiers RDF dans différents formats.

importation de données LOD, puis manipulation possible avec le langage.

Simple d’utilisation, namespace prédéfinis avec des raccourcis, plusieurs graphes sont manipulables avec des opérations de base comme l’ajout de triplets, etc.

Opérations de base, addition, union, intersection, etc.

Peut se limiter à des prédicats ou des objets.

Possibilité d’utiliser Jupiter pour travailler de manière interactive avec ces contenus.

Géonames dispose de nombreuses librairies client pour interroger d’une autre manière le webservice.

## Google Rich Snippets

Web de document, web social, web de données.

1998, Google a introduit le Snippets dans ses recherches. À partir de 2009, introduction des Rich Snippets proposant à l’utilisateur des contenus enrichis par des reviewing stars, des rappels du nom de la personne de la recherche, ou des événements. Pour les recettes, les reviewing stars, les votes, le temps de préparation ou les calories.

En tant que webmaster, il est possible de coder cela avec de simples balises qui sont ensuite reconnues par Google. Possible de fournir les informations avec JSON-LD (recommandé), Microdonnées, ou RDFa (sous forme de propriétés).

RDFa, une recommandation du W3C extension XHTML pour intégrer de riches métadonnées. exemple, sur une personne peut ajouter attribut property="v:name" en définissant sur l’élément parent le namespace.

Les microdonnées des propriétés.

Pour les Webmasters, Google fournit un outil pour tester les structures de données le [Structured Data Testing Tool](https://search.google.com/structured-data/testing-tool?hl=fr)

Doit utiliser vocabulaire schema.org En effet, depuis 2011, Google Yahoo et Bing ont développé un vocabulaire spécifique pour les extraits. Contraint de suivre ce vocabulaire prédéfini. Mais avec ces propriétés, reconnaissance des propriétés.

Avantages des extraits enrichis, permettent d’ajouter des informations utiles sur une page web afin que Google puisse traiter les métadonnées de la page afin de proposer des résultats plus intéressants pour les utilisateurs. Les pages qui l’emploient apparaissent mieux sur les recherches ce qui génère un trafic supplémentaire.

On pourrait souhaiter des extraits plus enrichis pour avoir des résultats de recherche plus pertinent pour les contenus multimédias, ou pour joindre de l’information provenant de plusieurs sources de données.

http://www.oclc.org/research/themes/data-science/linkeddata.html

## Logique de description

Individus objets, concepts, rôles et constructeurs

TBox et ABox

A est un concept dans la logique de description, en OWL une classe

négation ¬C

Rôles existentiels ∃R.C et universels ∀R.C owl:allValuesFrom, owl:someValuesFrom

Nothing ⊥ et Thing, owl:Thing et owl:Nothing 

Combinaisons de classes avec des expression  C ⊓ D | C ⊔ D, inclusion, disjonction et équivalence de classes

Il existe une hiérarchie de logiques de description en fonction de leur complexité. Nous allons maintenant regarder ce que l’on peut faire avec ces langages.

Person ⊓ (<=1 hasChild ⊔ (>=3 hasChild ⊓ ∃hasChild.Female ) )

les personnes avec au plus un enfant ou avec 3 enfants et au moins une fille

DL peut aussi être traduit en logique des prédicats, alors il est intéressant de voir comment on fait le lien avec la logique de prédicat.

Ici π exprime le processus de traduction

### Pour les classes

πx(A) = A(x) on traduit l’expression pour x = Concept prédicat unaires

Relation, une relation entre deux individus. Considère que la relation R entre deux individus x,y sera la Relation x, y. Rôles prédicats binaires.

Expression inclusion de classe :

πx(C⊑D) = ∀x (πx(C) → πx(D))  pour tout x C de x implique D de x. Implique que pour tout x, qui est un élément de C alors un élément de D.

Logique de description est donc un sous ensemble de la logique de premier ordre car peut traiter toutes nos expressions.

⊓, ⊔ , ¬ ≡ interprétation ensembliste habituelle 

Union, intersection, négation dont les traductions sont à peu près directes.

### Pour les rôles

πx(∀R.C) = ∀x’(R(x,x’)→πx’(C))  Pour tout R.C, pour tous les x’ qui sont entrealation avec R, implique que l’élément x’ sera élément de C. S’il est en relation avec l’élément recherché, alors doit absolument être de cette classe là.

πx(∃R.C) = ∃x’(R(x,x’)⋀ πx’(C)) S’il existe alors en relation avec x’ qui lui est dans la classe qu’on cherche.

πx(≥nS.C) =  ∃x1...xn (Λi≠j (xi≠xj) ⋀ Λi(s(x,xi) ⋀ πxi(C)) Sans doute le moins intuitif. Remarquons qu’ici on a des constantes, pas un *n* quelconque. Cherche à ce que au minimum en ait un, va regarder tous les couples S avec C en considérant toutes les possibilités. Il faut donc qu’il en existe au moins n variables, toutes différentes, et toutes en relations avec la bonne classe.

Il existe de X1 à Xn car doit générer tous les couples, il un ET logique car des expressions booléennes. Si j’en veux au moins n, va devoir trouver n variables de X1 à Xn qui sont toutes vraies en même temps. Il faut qu’il existe une combinaison de n variables, de telles sortes que toutes les possibilités de la relation tienne, qu’ils soient différents, que la relation existe, et qu’ils soit de la bonne classe.

πx(≤nS.C) =  ¬∃x1...xn+1 (Λi≠j (xi≠xj) ⋀ Λi(s(x,xi) ⋀ πxi(C))) Ici ne veut pas en avoir plus que *n*. On ne veut pas qu’il existe de Xn de plus que 1, et il ne faut pas que tout cela soit vrai en même temps.

ex : Exam ⊑ ≤2hasExaminer 

On peut aussi regarder les propriétés sur les rôles.

π(R1⊑R2) = ∀x∀y(πx,y(R1)→πx,y(R2))  Si on a des surrôles, la même chose que pour les classes. Si R1 pour x, y et qu’une sous propriété, alors la relation tient pour R2

πx,y(S) = S(y,x) 

πx,y(R-) = πy,x(R)  relation

πx,y(R1•...•Rn) = ∃x1...xn-1  (πx,x1(R1) ⋀ Λi=1..n-2 πxi,xi+1(Ri+1) ⋀ πxn-1,y(Rn))  De même, il existe, une série de X1 à Xn pour lesquelles...

Propriété réflexive π(Ref(R)) = ∀xπx,x(R) 

asymétrique, dissymétrique

On a donc ce qu’il faut pour faire des preuves, mais comme une restriction sur la logique des prédicats, pas de variables, etc. Certains on découvert des algorithmes beaucoup plus efficaces de résolution.

## Quelques exemples de traduction

Professor ⊑ FacultyMember 

∀x(Professor(x)→FacultyMember(x)) 

Quand on a une sous-classe, tout professeur est membre de la faculté. Alors pour tout x Professeur(x) implique qu’il est membre de la Faculté.

Professor ⊑ (Person ⨅ FacultyMember)   ⨆ (Person ⨅ ¬PhDStudent) 
∀x(Professor(x) → (Person(x) ∧ FacultyMember(x))  ∨ (Person(x) ∧ ¬PhDStudent(x))) 

Pour tout x Professeur(x) cela implique que soit x est une personne, ou un membre de la faculté, ou encore que c’est une personne et qu’il n’est pas candidat au doctorat.

Exam ⊑ ∀hasExaminer.Professor 
∀x (Exam(x) → ∀y(hasExaminer(x,y)→Professor(y)))

Pour les rôles, pour tout x qui est un examen, alors un examinateur, et cet examinateur un professeur.

Exam ⊑ ≤2hasExaminer 

∀x (Exam(x) → ¬∃x1,x2,x3 (x1≠x2)∧(x2≠x3)∧(x1≠x3) 
⋀ hasExaminer(x,x1) ⋀ hasExaminer(x,x2)  
⋀ hasExaminer(x,x3))

pour tout x examen(x) alors ne doit jamais trouver 3 x, tous différents identiques, qui ont examineurs...

hasParent • hasBrother ⊑ hasUncle ∀x∀y(∃x’ hasParent(x,x’) ⋀ hasBrother(x’,y)  

→ hasUncle(x,y))

Pour tout y, pour tout y, s’il existe x’ en relation avec x hasParnet et hasBrother x’ avec y, alors hasUncle(x,y)

### Inférences sur la TBox

Ici pas d’individus, on regarde seulement les expressions sur les classes.

Première chose à voir savoir s’il existe un modèle pour la classe, savoir si la définition des classes est consistante. Est-ce qu’elles peuvent au moins avoir une instance, cad être satisfiable.

Est-ce que C⊑D? (C est subsumé par D), peut-on le prouver ? 

Équivalence de classes ( C ≡ D)  

Classes disjointes ( C ⊓ D ⊑ ⊥ )

Inférences que peut faire sans tenir compte des individus. Toutes ces choses là se ramènent à la question de la satisfiabilité.

- C ⊑ D ⬄ C ⊓ ¬D insatisfaisable

  signifie impossible qu’un élément D qui ne soit pas dans C

- C ≡ D ⬄ C ⊓ ¬D et ¬C ⊓ D il faut que les deux expressions soient insatisfaisables 

  pour savoir si deux classes sont équivalentes, vérifier que C est sous-classe de D et D sous-classe de C. C ≡ D ⬄ C ⊑ D et D ⊑ C Mais peut les prendre à l’envers

- C ⊓ D ⊑ ⊥ ⬄ C ⊓ D insatisfaisable

  pour des classes disjointes, il n’y a pas d’élément qui soit à la fois dans C et dans D, alors il ne faut pas que puisse trouver des éléments dans la classe C ⊓ D

Attention, en logique descriptive : Les propriétés sont des choses qui unissent les individus, ensuite pense les classes en fonction des individus.

Ce sont des inférences typiques que l’on peut faire dans la TBox, ici a montré que si capable de résoudre la première question de la satisfiabilité, alors peut tout ramener à cela.

### Inférences sur la ABox

La ABox signifie que l’on introduit nos individus, alors regarder ce que l’on peut faire. Ici va avoir nos définitions de classes.

Le but est de classes nos individus.

On a affirmé que a était dans la classe C. Alors vérifier qu’effectivement a appartient bien à cette classe là. C’est une vérification d’instance.

On pourrait trouver tous les éléments qui appartiennent à la classe C

Trouver des classes correspondants à des individus.

Détermination de la taxonomie de classe (même si normalement l’a déjà défini)

Il y a donc des inférences que l’on peut faire avec la TBox, mais peut aussi introduire des inférences avec la ABox.

### Preuve par tableau

Pour réussir à faire cela, le mécanisme de preuve est un mécanisme générique. Il existe plusieurs façons de faire des preuves, en logique des prédicats on a vue la méthode de résolution, ici la méthode par tableau.

Une méthode de preuve dite par tableau. Voir document de J. Bergeron. Une méthode systématique pour explorer toutes les possibilités et faire une preuve par réfutation pour y parvenir.

cf. document Bergeron, méthode intuitive

Méthode des tableaux sémantiques qui ressemble assez à la résolution. On va essayer de prouver que sa négation est impossible.

On a un énoncé, et l’idée est que la méthode des tableaux sémantiques s’applique sur n‘importe quelle logique pour lesquelles capables de définir les opérateurs et de faire les extensions.

On va donc procéder à la négation d’un énoncé, puis faire l’expansion du tableau en branche, essaye de fermer toutes les branches, si arrive à toutes les fermer alors pu prouver que c’est impossible. Quand dans une branche une contradiction, ferme la branche.

Si on réussit à fermer toutes les branches, alors la négation de l’énoncé est impossible, donc notre truc est vrai. Si à la fin nous reste une branche ouverte, alors nous donne un exemple pourquoi ce n’est pas bon.

Si un contre-exemple, alors négation pas possible, puisqu’à trouvé un exemple.

Quand on veut appliquer la méthode des tableaux sémantiques sur une certaine logique, il va falloir trouver un certain nombre de choses.

- savoir comment créer la négation d’un énoncé
- ensuite, définir les règles d’expansion relatives à chaque constructeur
- définir les règles de fermeture des branches
- prouver la complétude et la validité de ces règles en regard de la logique concernée

Doit être au moins démontré une fois pour une logique déterminée (règles monotones décroissantes). Pour la logique des prédicats, ne fonctionne pas car des choses que ne peut pas prouver. Mais marche dans beaucoup de cas. Une bonne façon de faire les preuves pour la logique descriptive, fastidieux, mais permet d’avoir une bonne intuition sur ce qu’il se passe. Il existe des applications pour le faire.

Une logique super simple :

- Negation : ¬A avec signification habituelle

  Une chose qui peut être vraie ou fausse

- Implication : A => B avec signification habituelle

  Dans mon langage, un seul opérateur qui est l’implication

Avec ce langage de logique très simple, pour faire la négation de l’énoncé, on va simplement ajouter le signe T ou F selon que c’est vrai ou faux.

FX alors exprime que X est faux.

I T¬A |- FA i.e.T¬A eq T¬A^FA

Si T de non a, alors remplace par FA







