# cr Lapalme 23 novembre 2017

## FRED un lecteur machine pour le web sémantique

http://wit.istc.cnr.it/stlab-tools/fred

Grande quantité de documents textuels pouvant constituer une masse considérable d’information si pouvait extraire l’information en RDF. Une tâche dont parvient de mieux en mieux à s’acquitter. Mais l’apprentissage supervisé est une tâche spécifique à un domaine.

FRED est un outil développé par une équipe italienne, un assemblage d’outil de traitement automatique du langage NPL qui génère des OWL. Outil apprentissage supervisé.

Basé sur la théorie de la sémantique des cadres, Charles J. Fillmore, idée que ne peut comprendre le sens d’un mot isolé, mais nécessite le concept. Facile à comprendre pour des éléments terminologiques mais également applicable pour des verbes. Un cadre est donc un paquet de termes qui désignent le contexte. Des éléments obligatoires et d’autres facultatifs. Plusieurs mots ou verbes peuvent faire appel au même cadre, simplement les arguments vont alors changer de rôle. 

Un cadre contient toujours une définition, des unités lexicales (les mots qui font appel à ce cadre là), et les éléments du cadre (noyau et facultatifs). On a ensuite des phrases annotées avec chacun des éléments du cadre.

FRED emploie la base de données FrameNet qui est un répertoire de cadre sémantique lancé par Fillmore, lancé en 1997, 1200 cadres, 13 unités lexicales, 200 000 phrases annotées.

FRED est un outil multilingue, mais traduit vers l’anglais pour produire l’analyse. L’outil va donner une première formalisation avec une classe d’un terme donné, et une instance qui prendra les différents éléments.

Input Discourse Representation Structures DRS issues de la Théorie de la représentation du discours. Deux composants : les entités qui participent aux événements et leurs relations.

Premier outil de traitement du langage utilisé, BOXER qui est un passeur qui génère des DRS (sous formes de boîtes). À partir de cette boîte, le logiciel trace un premier graphe. Dans une première étape, on sépare les éléments du discours.

Deuxième étape pour faire des heuristiques, gommer les redondances, etc.

exemple simple. Pour la représentation du temps des verbes utilise l’algèbre des intervalles proposé par Allen en 1983. Plusieurs possibilités de relations 7 et leurs inverses.

Négation qui en logique pure est parfois problématique selon la situation de la négation. On l’inclue sans présumer quoi que ce soit sur la portée de la négation.

Modalité (verbes vouloir, pouvoir, aimer faire quelque chose) qui traduisent l’expression de la volonté du locuteur. Pas non plus d’éléments en OWL.

Composition sémantique, capable de décomposer en fonction de ce que le groupe de mots contient.

Représentation des adjectifs pour déterminer si la classe modifier l’instance ou la classe selon qu’il est intersectif ou subsectif.

Reconnaissance des entités nommées, les objets du monde réels. Intéressant car des éléments devant être reconnus comme des individus dans l’ontologie et non pas des instances de classe. Utilise ici un outil dédié Tagme et des bases de données pour les relier à d’autres entités documenter afin de pouvoir inférer qu’il s’agit de personne, etc.

Reconnaissance des entités nommées, détection et liaison qui sera réemployées plus tard.

Utilisation de plusieurs bases de données et de vocabulaires : FrameNet, VerbNet, WordNet, DBpedia, Schéma.org, etc. en plus de leur propre vocabulaire.

Évaluation de la performance par rapport à Sémaphore, à l’époque il y a 5 ans, le plus performant dans le domaine. Plus rapide, mais un score de taux de rappel un peu plus bas. Mais Sémaphore entraîné sur tout le corpus de Framenet, mais FRED non supervisé.

Au niveau des tâches, celui qui s’occupe du plan grand nombre de tâches, dans le plus de catégorie. Sans doute une des outils les plus complet actuellement.

Un logiciel proposé comme un middleware sémantique. Indépendant de domaine et utilisable par d’autres applications qui l’utiliserait : Sentilo, Tipalo, etc. Disponible en service REST ou en librairie Python démo web. Fonctionne en théorie en plusieurs langues.

## Frédéric Piedbœuf, Web sémantique et génération automatique de texte

GAT Génération automatique de texte, sous-discipline de la linguistique computationnelle qui vise à exprimer sous forme textuelle, syntaxique ment et sémantiquement correcte, une représentation formelle d’un contenu.

Cinq grandes tâches

- sélection du contenu
- structure de l’information
- agrégation
- lexicalisation
- réalisation morphosyntaxique (regarder dépendance entre les mots) et linéarisation

Exécution en cascade

- planification du texte/document
- planification des phrases
- réalisation de surface

ex. Production rapports météorologiques comme concis, peut modifier l’ordre des tâches.

GAT Et Web sémantique. Plusieurs choses possibles comme 

- manipuler l’ontologie sans maîtriser son langage
- publier de l’information

Nécessite adaptation des techniques. Avantage du WS des standards, possibilité de réutiliser les technologies. Extensibilité pour des bdd très larges. Jusqu’à présent surtout des domaines restreints. Possibilité d’utiliser le web sémantique pour raisonner.

Réutilisation des ressources pour des générateurs.

Deux approches pour la sélection du contenu

- Planification fermée (SPARQL, sait ce qu’on veut)
- Planification ouverte

NaturalOWL, résume des individus ou des classes d’une ontologie. A été notamment employé dans le monde muséal pour donner des informations sur des objets à la demande des utilisateurs. Développé en anglais et en grec. Génération de texte à partir d’une ontologie.

Sélection du contenu, part d’un individu ou d’une classe, cherche toutes les expressions OWL concernant une classe ou un individu, en interdisant les éléments imbriqués (union et intersection). Pour une classe pas de distinction entre EquivalentClasses et SubClassOf. Cible de second niveau, parfois désirable d’aller chercher les individus et ses caractéristiques. Paramètres à spécifier.

Avec toutes ces expressions, va les transformer en triplets <S,P,O> où S est la cible, P une propriété ou un mot-clef ou une expression. O un objet.

Table de conversion entre les individus, idem pour les classes.

On va ensuite classer ces ensembles de triplets par score d’intérêt à partir d’informations concernant l’utilisateur (type d’utilisateur, historique de ses questions, etc.)

Chq triplet peut être exprimé dans une seule phrase, on va les ordonner selon le sujet qui doit avoir été entré dans l’ontologie. Triplets concernant les cibles de 2nd niveau immédiatement après.

Possible de partir de lexiques existants pour déterminer construction de la phrase et conjugaison. Des plans de phrases prédéterminés, mais souvent entrés par l’utilisateur de l’ontologie qui veut utiliser NaturalOWL. N’entrent pas en détail dans la référence au sujet pour éviter les répétition.

Plan par défaut puis agrégation des phrases. Règles pour éviter répétition du nom avec emploi adjectif. Restriction de cardinalice, emploi de classes et de phrases passives. Ensemble de règles qui servent à agréger les phrases tout en limitant le niveau.

Codifier information nécessaire pour le LN dans l’ontologie. Standardiser les interfaces GAT pour permettre la communication avec les modules. Adapter pour open data pour aller chercher du contexte. Imaginer la possibilité de formuler des questions en langage naturelle comme obtenir des réponses dans le même langage en cherchant à unifier les deux tâches.

## Logique de description

Un sous ensemble de la logique des prédicats, permet de faire des preuves et tout ce qu’il est possible de faire avec la logique des prédicats. Cela a été aussi une manière de pouvoir intégrer des éléments non logiques d’inspiration cognitive.

Combinant des approches logiques ou non logiques, au départ on les a appelé sous la dénomination de Terminological system. Il y a donc une très grande emphase sur l’établissement de la terminologie et de l’organisation du système de termes les uns par rapport aux autres. Puis reçu toute sorte de dénomination, concept langages, term subsumption language avant de ...

Logique description, consiste à définir les concepts pertinents d’un domaine. Utiliser ces concepts pour spécifier des propriétés des objets, des indidivus dans un domaine. Et une sémantique logique formelle pour déduire des connaissances implicites via la classification de concepts et d’individus.

### Composantes DL

Proches de OWL car ce langage a adapté des éléments qui étaient présents dans la logique de description.

On a des individus, puis des concepts atomiques qui sont des prédicats unaires. Enfin des rôles qui sont les propriétés que l’on a fait et qui sont des relations entre les objets. Réunit deux individus. Là encore prédicats binaires. Ce sont les concepts de base de la logique de description.

On va ensuite, comme dans les autres logiques, construire les relations avec des opérateurs qui ressemblent assez à ceux que l’on utilise en logique des prédicats.

Négation, intersection, union, sous-classe, ensemble, il existe

- Woman ⊑ Person Woman est une sous-classe de personne
- Mother ≣ Woman ⊓ ∃hasChild.Person Woman équivalente à Mother et au moins une relation hasChild avec une autre personne. hasChild.Person signifie la portée de hasChild

Cela s’appelle la TBox, on y définit nos termes. Ici pas d’individus. Une forme d’ontologie mais comme en logique des définitions où définis un ensemble de termes avec des relations entre ces termes. Des rôles, des classes et des opérateurs pour définir de nouvelles expressions.

On a ensuite la ABox qui est l’assert box, celle des axiomes.

- Mary a comme enfant peter
- Mary est une femme
- Peter est une personne.

But sera de pouvoir déduire de nouveaux faits

- par exemple Mary est une personne car Mary est une femme et que femme est une sous-classe de personne
- de même une mère car au moins en relation hasChild avec Peter qui est une personne.

C’est ici le genre d’inférence que l’on va être capable de faire avec la logique de description.

Conceptuellement on a deux parties le TBox description du monde indépendamment des individus, et les assertions sur les individus.

### Inférences DL, TBox axiomes sur les concepts

Dès lors que dispose d’une TBox, peut déjà déduire des choses sans les individus, juste au niveau des concepts. Par exemple, lorsque créée un concept, peut-on garantir qu’il sera possible d’avoir une instance. Il s’agit ici de vérifier la **consistance**. La consistance, est indépendante des individus. On peut raisonner seulement sur le TBox.

La *Subsomption*, consiste à savoir si un concept peut être déduit d’un autre. voir ex. Là encore au niveau de la TBox, capables de faire un certain nombre de preuves.

### Inférences DL, ABox assertions sur les individus

On peut vérifier la consistance d’un certain nombre d’assertion.

- un individu déclaré comme instance d’une classe, répond-il à ses caractéristiques ?  

  p.e. une mère sans enfant 

- une relation déclarée entre deux individus est-elle possible ? 

  p.e. célibataire marié à un autre individu 

### Un contenu de TBox

Woman≡Person ⊓ Female

une femme est une personne qui est une femelle

Man≡Person ⊓ ¬Woman

Un homme est une personne qui n’est pas une femme

Mother≡Woman ⊓ ∃hasChild.Person

Father≡Man ⊓ ∃hasChild.Person

Parent≡Father ⊔ Mother

Grandmother≡Mother ⊓ ∃hasChild.Parent

MotherWithManyChildren ≡ Mother ⊓ ≥3 hasChild

MotherWithoutDaughter≡Mother ⊓ ∀hasChild.¬Woman

Wife≡Woman ⊓ ∃hasHusband.Man

### Contenu de Abox

```
MotherWithoutDaughter(MARY)
Father(PETER)
hasChild(MARY,PETER)
hasChild(MARY,PAUL)
hasChild(PETER,HARRY)

```

Définit des faits à partir de nos individus.

### Exemple de langage de description *AL*

La logique de description est très hiérarchisée en fonction de ce que l’on ajoute dans le langage d’opération et ses différents opérateurs. Plus de puissance, mais plus difficile de faire les preuves.

Attributive Language, le langage le plus simple, mais aussi le plus pratique. Et possible de faire certaines opérations non triviales.

Suppose qu’a un concept atomique A et un rôle atomique R.

On peut ensuite définir des concepts en fonction des concepts atomiques et des rôles.

Ici règle de grammaire informelle : on exprime deux concepts C et D, qui peuvent être une des choses suivantes, soit Concept atomique A, soit nothing, ou encore T top qui est  la surclasse de toute les classes, ou non un concept de base, ou encore l’intersection de deux concepts de base, encore pour tout d’une certaine relation avec un concept qui indique ici le domaine du concept, ou encore il existe R ou met T.

- Négation qui ne s’applique que sur les concepts atomiques
- seul ⊤ est utilisable dans l’existence

### Expressions

Toutes des expressions

Person ⊓ ∃hasChild.⊤

Des personnes avec le type d’un enfant, mais dans ce langage pas ne peut pas spécifier qu’une fille.

Person⊓∀hasChild.⊥

Tous ses enfants sont dans la classe Nothing.

Person ⊓ ∀hasChild.Female

Tous ses enfants sont des filles



### Interprétation des ensembles

Le i en exposant pour dire que l’on interprète.

Une façon d’interpréter ce que vient d’écrire sous forme d’ensemble.

Ici un exemple d’interprétation, mais pas la seul. Pourrait aussi avoir un exemple entièrement vide !





