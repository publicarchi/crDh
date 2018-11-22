# Cours Lapalme 7 novembre 2017

Remonte la pile des technologies XML

Principe, un langage déclaratif pour exprimer des ontologies. Il ne s’agit pas d’un langage de schéma, et c’est un monde ouvert, ce qui change la façon de faire des preuves.

En OWL on se retrouve avec des axiomes, cad un ensemble d’énoncés de base supposés vrais. On a également des entités qui font référence à… Puis des expressions. L’ensemble formant une ontologique.

On y trouvera des énoncés de base. Et va parler de conséquences des énoncés. On exprime des relations entre des énoncés, ensuite pourra voir si un énoncé a est vrai si d’autres A le son. A entraîne (entails) a. Dira que A est consistant si une situation où tous ses énoncés sont vrais.

A est inconsistant si on ne peut trouver des situations..

Parle de logique formelle au sens où cherchera à trouver un ensemble … où tous les énoncés sont vrais.

Calcul automatique des conséquences d’un ensemble d’axiomes. Les outils sont appelés des *reasonners*. Pas toujours facile à contrôler ou à en comprendre les résultats. Comment fera pour trouver d’autres énoncés vrais, consistera à toujours ramener cela à un ensemble d’énoncés consistants. Ici comme dans la logique de premier ordre, quand a des preuves pour la résolution facile. Parfois plus compliqué de comprendre pourquoi lorsque l’on enchaîne des règles. Sera alors parfois difficile de comprendre ce qu’il faut changer pour que le système redevienne consistant.

Que retrouve-t-on dans le domaine de OWL ?

On parle d’individus (objet, personne, etc.) qui forment les atomes de base. Ces individus, seront catégorisés en classes. Les classes forment des regroupement. Ces classes sont essentiellement des regroupement des individus qui partagent un certain nombre de propriétés. On peut avoir par exemple des propriétés d’objet à objet (object properties) qui regrouperont deux classes de personnes : mariéA pèreDe. Mais aussi des objet-valeur comme âge, etc. sera alors une relation entre un individu et un littéral (data relation). Enfin des annotations, auteur, date de création, etc. Mais le raisonnement porte sur les individus, les classes et les propriétés.

Ensuite on va avoir des constructeurs qui constituent en quelque sorte notre langage comme en logique de premier ordre. En général il s’agit de constructeurs sur des classes. On va prendre la classe des femmes, celles des professeurs, et obtenir la classe des femmes professeures. Ici à la différence de RDFs le langage pour construire des classes est très riches. On va par exemple pouvoir faire la combinaison de classes (union, intersection). On pourra aussi combiner des propriétés mais cela est plus restreint, en fait pourra seulement composer les propriétés.

Structure de OWL-2. Il y a eu deux grandes versions du langage, OWL1 standardisé au milieu des années 2000, version 2 en 2009 puis récemment révisé. Structure de l’ontologie qui permet de définir des graphes RDF (définit syntaxes des modèles sur le graph RDF), sémantique directe de la structure et sémantique basée sur RDF. On va utiliser différentes syntaxes RDF/XML pour l’échange, obligatoires pour tous les outils. OWL/XML facilement traitable avec des outils XML. Fonctionnelle : fait ressortir la structure formelle. Manchester : ontologies plus faciles à lire/écrire. Généralement, on utilisera des outils.

Modélisation de base : être capable de définir des classes, des sous-classes, des propriétés et des sous-propriétés, des restrictions sur des propriétés, etc. Série d’éléments qui correspondent un peu à ce que peut faire avec RDFs mais plus riche

- classes et instances
- hiérarchies de classes
- propriétés d’objects
- hiérarchies de propriétés
- Restrictions sur les propriétés
- égalité des individus
- types des valeurs de propriétés

Ensuite relations avancées de classes : définition de classes complexes, restrictions de propriétés (ex famille nombreuse, plus de x individus enfants), mais aussi de cardinalice, énumérations d’individus. Choses qui s’expriment aussi en logique de premier ordre.

- classes complexes
- restrictions de propriétés
- restrictions de cardinalité
- énumérations d’individus

Utilisation avancée des propriétés

- caractéristiques des propriétés
- chaînes de propriétés
- clés

## Modélisation de base

### Classes et instances

Notation Manchester (utilisée dans Protégé), Frame-based (.omn)

Marie est une personne

```
Individual: Mary
	Types: Person
```

On peut ici définir des individus. On indique que cet individu fait partie de la classe personne.

```
Individual: Mary
	Types: Women
```

Autres syntaxes

Fonctional-Style Syntax

```
ClassAssertion( :Woman :Mary )
```

voici une définition de classe et voici son individu

RDF/XML Syntax

```
<Woman rdf:about="Mary"/>
```

Turtle Syntax

```
:Mary rdf:type :Woman .
```

OWL/XML Synax

```
<ClassAssertion>
	<Class IRI='Woman'/>
	<NamedIndividual IRI='Mary'/>
</ClassAssertion>
```

Tout cela des sérialisations.

### Hiérarchies de classes

Sous-classes

```
Class: Woman
	SubClassOf: Person
```

également notion de EquivalentTo

```
Class: Mother
	SubClassOf: Woman
Class:Person
	EquivalentTo: Human
```

Aurait pu dire que Human classe Person et Person classe Human mais plus élégant

Classs disjointes que n’avait pas en RDFs

```
DisjointClasses: Woman, Man
```

Pratique mais souvent cause d’inconsistances, si définit des classes disjointe et dit ailleurs que appartient aux deux.

On a vu les classes, les individus, les sous-classes.

### Propriétés d’objet

On va également pouvoir avoir des Propriétés d’objets, qui sont les relations entre les individus

Relations positives comme en RDF

```
Individual: John
	Facts: hasWife Mary
```

Relations néagtives

```
Individual: Bill
	Facts: not hasWife Mary
```

Comme on est dans un système de monde ouvert, tout est possible à moins d’affirmer le contraire. Si n’exprime quelque chose, a priori tout est possible. On ne peut donc pas supposer que les choses que ne connaît pas sont fausses, à moins de l’exprimer explicitement.

### Hiérarchies de propriétés

Même principe que pour les classes

```
ObjectProperty: hasWife
	SubPropertyOf: hasSpouse
EquivalentProperties:
	hasChild, otherOnt:child
```

*otherOnt* serait ici le préfixe d’un autre espace de nom.

### Restrictions sur les propriétés

Un peu comme en RDFs, on peut spécifier le domaine et la portée

```
ObjectProperty: hasWife
	Domain: Human
	Range: Women
```

### Égalité et inégalité des individus

Par défaut, OWL ne suppose pas que deux individus sont différents. Toutefois, peut supposer que si des noms différents, des individus différents.

différent

```
Individual: John
	DifferentFrom: Bill
```

identique

```
Individual: James
	SameAs: Jim
```

Idée de OWL d’être capables de combiner des ontologies, or pour pouvoir les combiner doit pouvoir être capable de dire l’identité. Disponible pour les classes, pour les propriétés et évidemment pour les individus.

Souvent dit que tous les individus sont distincts.

### Types de valeurs de propriétés

On peut avoir des propriétés avec des valeurs (data properties)

positif

```
Individual: John
	Facts: hasAge "51"^^xsd:integer
```

Peut utiliser un type, même si normalement ne fait pas de calcul. Une data property car réuni un individu est un littéral

négatif

```
Individual: Jack
	Facts: not hasAge "53"^^xsd:integer
```

Domaine et portée des propriétés

```
DataProperty: hasAge
	Doamine: Person
	Range: ... #data property
```



Par rapport à RDFs, possibilité de mettre la négation, dire que les individus sont distincts les uns des autres. Mais essentiellement retrouve tout ce qu’était déjà capable de faire en RDFs.

## Relations avancées de classes

Mais OWL propose également des relations plus complexes au niveau des classes

- classes complexes
- restrictions de propriétés
- restrictions de cardinalités
- restrictions sur les individus

### Classes complexes

Intersection

```
Class: Mother
	EquivalentTo: Woman and Parent
```

Union

```
Class: Parent
	EquivalentTo: Mother or Father
```

La classe parent, l’ensemble des individus à la fois père et mère.

Complément

```
Class: ChildlessPerson
	EquivalentTo: Person and not Parent
```

Une personne qui n’est pas parent. Partout où pouvait mettre une classe, peut mettre une expression de classe qui elle-même peut servir dans une autre expression plus loin.

Définition de sous-classes

```
Class: Grandfather
	EquivalentTo: Man and Parent
```

On peut même faire des expierions de sous-classes complexes. Si grand-père certain que parent et qu’un homme.

Expressions utilisable à la place d’un nom de classe. Partout où on avait une classe, on peut mettre une expression.

### Restrictions de propriétés

Quantification existentielle

```
Class: Parent
	EquivalentTo: hasChild some Person
```

On dit qu’un parent, c’est quelqu’un qui est en relation hasChild avec au moins une autre personne. Aussitôt qu’une personne a une relation hasChild avec une Person, alors cela désigne un Parent. Parmi les personnes, et pas les chiens.

Les parents sont les individus qui sont liés à une personne par le lien hasChild

Quantification universelle

```
Class: HappyPerson
	EquivalentTo: hasChild only HappyPerson
```

Une personne est heureuse, si tous ses enfants sont heureux.

Mais attention, trivialement vrai, si une personne n’a pas d’enfants, elle est heureuse selon cette définition là.

```
Class: HappyPerson
	EquivalentTo: hasChild only HappyPerson
	and hasChild some HappyPerson
```

Ne considère que la relation positive.

Ce qui est sans doute le plus inattendu dans OWL alors que tout le reste, classique UNION, etc.

### Restrictions de cardinalité

Cardinalité maximum

```
Individual: John
	Types: hasChild max 4 Parent
```

Ici exprime la relation avec mot-clef max et un chiffre, en spécifiant la classe des éléments enfants. John fait partie de la classe des gens ayant au plus quatre enfants qui sont parents, mais il pourrait avoir d’autres enfants qui ne sont pas parents.

Cardinalité minimum

```
Individual: John
	Types: hasChild min 2 Parent
```

Cardinalité exacte

```
Individual: John
	Types: hasChild exactly 3 Parent
```

Les restrictions de cardinalité se font sur les propriétés.

La spécification de la classe est alors optionnelle. On n’est pas obligé de donner des contraintes sur la classe des éléments en relation avec la propriété ici.

ex :

```
Individual: John
	Types: hasChild min 2
```

### Énumérations d’individus

```
Class: Elklkml
	EquivalentTo: { Bill, John, Mary}
```

On énumère tous ses individus.

## Utilisation avancée des propriétés

- caractéristiques des propriétés
- chaînes de propriétés
- clés

### Caractéristiques des propriétés

On peut déclarer des caractéristiques des propriétés. Simplifie en ajoutant un niveau d’abstraction.

Inverse

```
ObjectProperty: hasParent
	InverseOf: hasChild
```

Si dit qu’a une certaine propriété, peut la définir en fonction d’une autre propriété. Si a a comme parent b, alors b a comme enfant a.

Symétrie

```
ObjectProperty: hasSpouse
	Characteristics: Symmetric
```

Assymétrie

```
ObjectProperty: hasSpouse
	Characteristics: Assymetric
```

...

Réflexivité

```
ObjectProperty: hasRelative
	Characteristics: Relfexive
ObjectProperty: parentOf
	Characteristics: Irreflexive
```



Unité de valeur

```
ObjectProperty: hasHusband
	Characteristics: Functional
ObjectProperty: hasHusband   
	Characteristics: InverseFunctional
```

Transitivité

```
ObjectProperty: hasAncestor
	Characteristics: Transitive
```

Ensemble de déclarations qui vont nous simplifier la vie.

Pas de logique de défaut, tout cela s’exprime dans la logique de premier ordre. Toujours en logique du premier ordre, et même une restriction. Certaines choses de la logique de premier ordre que ne peut pas écrire ici, mais limitation du pouvoir de description qui permet de faire des reasoners plus efficaces.

### Chaînes des prorpiétés

permet de limiter la transitivité.

```
ObjectProperty: hasGrandparent
	SubPropertyChain: hasParent o hasParent
ObjectProperty: hasUncle
	SubPropertyChain: hasParent o hasBrother
```

On est ici capable d’exprimer cette composition de propriété.

### Clé

Il est également possible d’associer chaque instance de classe par une clef. Mais pas très utilisé.

## Annotation

Ne décrit pas le domaine, mais parle de la description. Associe une paire propriété-valeur à une partie de l’ontologie. Ne fait pas partie de la logique de l’ontologie.

```
Class: Person
	Annotations:
		rdfs:comment "Represents the set of all people."
```

Partout où a une classe peut ajouter une annotation avec des commentaires. Des choses qui vont suivre l‘ontologie, intégration dans le code. Mais les reasoners ne s’occupent pas du contenu de ces annotations là. Plutôt pour les humains et l’affichage.

## Gestion de l’ontologie

Comme OWL a été organisé pour pouvoir combiner des ontologies, il y a tout un langage pour définir des préfixes et combiner des ontologies.

Possible d‘importer d’autres ontologies, lui donne alors un espace de nom.

Puis utiliser les SameIndividual, et EquivalentClasses, EquivalentProperties

Permet de combiner des ontologies et traiter les différents éléments dans une seule ontologie.

## Sémantiques des ontologies

Il y a deux sortes de sémantique, une qui correspond au modèles en logique de description, et l’autre qui est une extension de RDFs. On transfère la sémantique écrite en logique de description en un graphe RDF et on considère l’ontologie comme un graph RDF. Souvent indécidable, donc dans beaucoup de cas ne pose pas de problèmes.

OWL 2 DL

- *direct model semantics*
- correspond au modèle en logique de description

OWL 2 RDF

- extension sémantique RDF
- ...
- indécidable

...

## Profils

Plusieurs syntaxes, nous avons vu celle de Manchester.

Ensuite, on a défini des profils qui sont en quelque sorte des sous-langages de OWL qui restreignent le langage mais peuvent rendre les raisonnements plus rapides

- Compromis entre expressivité et calculabilité.
- sous-langages de OWL2
  - propriétés computationnelles
  - et ...

### Profil EL

Plusieurs profils, le plus limité EL ne permet pas la quantification universelle. On peut seulement dire qu’il existe un truc, sans donner des règles génériques. Bien sûr limite le genre d’expression que peut faire, mais dans beaucoup de cas, notamment les grandes ontologies où des listes pas besoin de donner des règles spécifiques et si en a besoin pourra les ajouter. On se contentera alors de descriptions structurales complexes, avec grand nombre de classes et grandes quantités de données.

Correspond à la famille de la logique de description EL (ne permet que la quantification existentielle).

Dès lors le processus de preuve beaucoup simplifié. En particulier car peut avoir des algorithmes polynomiaux pour vérifier la satisfiabilité, classification, vérification d’instances.

Ne peut utiliser :

- owl:allValuesFrom, wol:unionOf, owl:complementOf
- xdd:int, xsd:byte, xsd:double

### Profil QL

QL pour Query Language

Vise des ontologies relativement simples, où les classifications ne sont pas trop compliquées. Pas trop de combinaisons de classes, mais un grand nombre d’entité. (p.e. thesaurus)

Pouvoir d’expression similaire à celle des schémas entités-relations ou UML

Intégration possible avec les BD relationnelles, raisonnement à l’aide de réécritures de requêtes SQL relativement efficace. Ce qui est la force de ce modèle là.

### RL

RL pour Rules Langage

Une sorte de RDF enrichi avec des règles. Pourra alors faire un raisonnement avec des systèmes de règles, permet alors d’exprimer des choses.

Le plus expressif des profils existants. Quelques 

...

## Outils

OWL-API: interface Java

Outils qui vont permettre de fouiller et construire les classes puis de travailler sur les structures de données qui correspondent à la structure de l’ontologie. Ici l’outil de bas niveau, à partir du quel ont été construit des éditeurs d’ontologie.

Éditeurs d’ontologie

- Protégé, SWOOP
- TopBraid Composer (Commercial)

Protégé qui existe depuis plusieurs années, débuté dans les années 80, d’abord LISP, puis s’est adapté à la technologie du web sémantique. Aujourd’hui bâti au-dessus de OWL-API.

Raisonneurs

- Fact++ (Manchester)
- Pellet
- RacerPro (un peu l’ancêtre car avait été développé pour faire des preuves en logique de description. De même adapté au fil du temps aux technologies du websem. D’abord écrit en LISP.)

