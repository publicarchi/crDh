# Cours Guy Lapalme, 3 octobre 2017

## Rappels

RDF est un formalisme de graphe, ce que l’on définit c’est un sujet, un prédicat et un objet. On compose les contenus de cette manière, ce qui permet de créer des graphes car il y a des liens entre des propositions car on utilise des URI. Il y a différentes façons de présenter des graphes et il y a plusieurs stérilisation. Un système qui lit du RDF produit des constructions sous la forme d’un ensemble de triplets. Il n’y a pas de répétition, et il n’y a pas d'ordre.

Nous avions vu un ensemble de petits graphes où l’on indique un certain nombre de relations sur Shakespeare et des œuvres littéraires. On peut expliciter chacun des graphes sous la forme d’un tableau. Et cela peut être exprimé dans une stérilisation XML ou turtle.

cf. http://www.iro.umontreal.ca/~lapalme/ift6282/Shakespeare/index.html

La sérialisation XML débute par l’élément RDF dans l’espace de nom rdf qui est déclaré avec xmlns. Comme on emploie plusieurs espaces de noms pour séparer les triplets dans différentes catégories, on utilise des entités pour les décrire. Les URI existent dès lors que l’écrit, mais cela n’implique pas forcément qu’il y ait un fichier. L’URI est un espace de nom, pour construire notre graphe, la manière de dire que tous les arcs vont sur le même nom, c’est l’utilisation d’un identificateur unique. Il suffit que l’auteur soit consistant avec lui-même. Souvent, il serait intelligent que le lien ne débouche pas sur un 404. Mais comprendre qu’il s’agit d’abord d’une convention, un URI c’est une chaîne de caractère.

On les utilise comme catégorie un peu comme des préfixes. Car dans XML, on peut utiliser ces chaînes de deux manières, soit comme préfixe d’espace de nom soit comme le début d’un URI. On définit ainsi souvent des entités pour pouvoir les utiliser facilement. Ici deux cas de figure : l’emploi d’un préfixe d’espace de nom, d’autre part d’une entité pour les chaînes.

Le sujet rdf:about, ont dit quelque chose à propos de Shakespeare. Il y a plusieurs manières d’écrire les arcs, on pourra les écrire simplement les uns à la suite de l’autre, le système en les lisant recréée la structure. Mais il existe aussi des manières de grouper les déclarations. On peut utiliser les propriétés de XML pour que plusieurs triplets qui aient le même sujet partagent la même déclaration. Il y a plusieurs avantages à être dans XML, on peut bénéficier de l’espace de nom par défaut pour ne pas avoir à écrire certains préfixes. De plus, on peut spécifier une base. Habituellement les URIs relatives sont par rapport au fichier, mais on peut spécifier une base pour que celle-ci s’ajoute à la base. Attention, quand on utilise l’adresse, on place le dièse dans le pointeur. Habituellement on utilise un des deux systèmes mais ici, il s’agissait de vous démontrer plusieurs possibilités pour écrire du RDF en XML.

On peut également décrire le même graphe en turtle. De la même manière on va pouvoir spécifier les espaces de nom avec `@prefix prefix: <url...> .`, `@prefix :` correspond à base. Ici il est encore possible d’utiliser les préfixes dans les URIs ce que l’on ne pouvait pas faire en XML. Un littéral s’indique comme une chaîne, même lorsqu’il s’agit d’un chiffre. On peut également utiliser les types XML avec la syntaxe `"littéral"^^xsd:gDate`. De même on peut grouper les déclarations qui partagent des sujets avec `;` ou des objets avec `,`.

## Requêtage du graphe

Maintenant que l’on sait comment écrire un graphe, on va vouloir pouvoir extraire des graphes. On dispose de notre représentation du monde, on va rechercher des motifs qui correspondent à notre recherche.

forme simplifiée d’implication

SPARQL est une façon de fouiller dans le graphe et y rechercher des patterns de graphe, le système va nous ramener toutes les instanciation de ce graphe.

Le langage que l’on va utiliser est SPARQL qui est un acronyme à la mode des informaticiens, c’est à dire qu’il est autoréférentiel. SPARQL Protocol And RDF Query Language.

SPARQL est un genre de SQL, c’est un langage de requête mais aussi un protocole. L’idée que l’on se fait c’est que l’on aura des portails RDF qui sont de grosses bases RDF auxquelles on peut adresser des requêtes et qui nous répondent par l’intermédiaire d’un protocole.

### Structure d’une requête SPARQL

La structure d’une requête SPARQL est à peu près comme SQL sauf qu’il n’y a qu’un seul énoncé.

- Dans SPARQL en général on définira des préfixes (Prefix definittion)
- On va ensuite spécifier ce que l’on veut faire (Result ??)
- Puis on aura des Query Pattern

### Exemples

http://www.iro.umontreal.ca/~lapalme/ift6282/SparqlSyntaxe.html

L’idée est d’écrire des triplets. Un triplet est la même chose qu’en turtle, cad trois composantes terminées par un point. Un littéral est une chaîne ou une valeur typée. Il y a quelques raccourcis, on peut écrire une décimale ou un entier directement pour faciliter les requêtes, mais conceptuelle ment ce que va chercher le système c’est un type XML ce qui suppose que les triplets soient aussi écrits de cette manière.

Un des éléments d’un triplet peut être une variable qui peut être soit un identificateur, soit un nom préfixé par un ? ou un $. Toutes les occurrences seront alors les mêmes, c’est la manière dont on pourra créer des patrons un peu complexes de graphes. 

Les nœuds anonymes se trouvent comme en turtle avec _:id et [].

La même notation que turtle avec quelques raccourcis et la possibilité qu’un des éléments du triplet soit une variable.

Pour déclarer un préfixe on écrit `PREFIX identifier: <IRI> .` Quand on utilise les préfixes, d’un point de vue interne, seulement des URIs au complet.

La notation des triplets est la même qu’en turtle, triplets terminés par un ".". Il est possible d’utiliser des ";" ou des ",". Attention les parenthèses servent à signifier des collections. La notation des nœuds vides est la même. Attention l’emploi des nœuds blanc n’a l’air de rien mais est assez subtile.

Ces notations permettent de créer des patrons que l’on va chercher dans le graphe.

### Définition des modèles de graphe

Ce que l’on va définir c’est des modèles de graphe. Un modèle de graphe est fourni entre { }. Un modèle de graphe est une suite de triplets entre accolades. 

```
{?s gl:p "o". ?s gl:p "o1"}
```

Ici, on cherche tous les nœuds qui sont relations avec gl:p "o" et gl:p "o1"

### Requête

Lorsque l’on fait une requête on fait un SELECT qui identifie un certain nombre de variables qui vont être utilisées dans le modèle avec WHERE. [perso : les variables ne sont pas toujours nécessairement identifiées dans le SELECT]

On peut aussi créer des nouveaux triplets, ce qui ne les rajoute pas dans le graphe car a priori SPARQL est un langage d’interrogation, mais cela vous retourne la réponse sous la forme d’un modèle de triplet. Le plus souvent créée une nouvelle base avec ce que l’on a obtenu avec les CONSTRUCTs.

Néanmoins, il existe une version de SPARQL appelée SPARQL Update qui dispose d’instructions pour aller modifier le graphe.

Si tout ce qui vous intéresse est de savoir si un triplet existe, on utilise ASK

DESCRIBE permet de décrire un ressource ou une variable mais cette description est laissée au soin de l'implantation. Typiquement pour rendre un ensemble ensemble d’URI qui partagent un même sujet, mais pas standardisé.

### Modificateurs

Parfois intéressant de pouvoir trier un ensemble selon une même variable avec ORDER BY. Ou encore éviter les répétitions avec DISTINCT.

Les triplets étant considérés comme un ensemble, il est difficile de se fier sur l'ordre d'apparition des résultats. Il est toutefois possible de modifier la sortie avec les mots clés suivants:

- `ORDER BY *variables*` à la fin de la requête, trie les solutions en ordre croissant des variables; pour l'ordre décroissant, on indique `DESC(*variable*)`. On peut trier les solutions sur plusieurs clés.
- `DISTINCT` à placer immédiatement après le *verbe* (i.e. le premier mot) d'une requête pour garantir que chaque solution n'apparaîtra qu'une fois.

## TP

Il existe des SPARQL endpoint qui vous permettent d’interroger des bases de données de triplets. Avec Twinkle possible d’interroger des grandes bases. Ici interface pédagogique qui permet d’expérimenter facilement.

Quand fait file/open, ce que va chercher un fichier de requête. Pour charge les données aller dans data:url, File.

On commence par définir un certain nombre de préfixes.

On commence par la requête la plus simple.

Dièse sert aux commentaires.

La requête la plus simple à faire pour vérifier qu’a accès aux données.

```sparql
SELECT * WHERE { ?subjet ?predicat ?object . }
```

Ramène tous les sujets, prédicats, objets.

```sparql
# Show all predicates without repetition
SELECT DISTINCT ?predicate {?subject ?predicate ?object} 

```

Exemple d’utilisation de DISTINCT pour supprimer les répétitions.

```sparql
# Find an author whose work is set in the UK
SELECT ?author ?work { ?author lit:wrote ?work.
                       ?work lit:setIn ?place.
                       ?place geo:partOf geo:UK}
```

Ici on écrit la conjonction de ces trois triplets.

```SPARQL
# idem but using a blank node
SELECT ?author ?work { ?author lit:wrote ?work.
                       ?work lit:setIn [geo:partOf geo:UK]}
```

On peut aussi simplifier cette requête en considérant que le lieu est un nœud vide. On dit que c’est un nœud vide qui sera l’objet du premier triplet et qui se passera dans une partie du UK. Cette expression est le strict équivalent de la précédente.

 ```
# find a work containing the string "King"
SELECT ?work {[lit:wrote ?work].
              FILTER (contains(str(?work),"King")) # NB: regex must be applied on a string
             }
 ```

Ici possible de chercher des chaînes en employant des expressions régulières. Comme work est une URI, l’expression régulière ne donnera rien. Il va donc falloir aller chercher la chaîne correspondante, puis chercher si la chaîne "king" s’y trouve. Ici, à l’intérieur d’un modèle on peut en plus des conjonctions de triplets faire figurer des filtres qui restreignent un ensemble de résultats.

```sparql
# Who is the spouse of the author of King Lear
SELECT ?spouse {?spouse bio:married ?author.
               ?author lit:wrote lit:KingLear}
# SELECT ?spouse {?author bio:married ?spouse.   #does not return anything...
              ?author lit:wrote lit:KingLear}
```

On chercher quelqu’un qui est marié à un auteur et que cet auteur est celui du Roi Lear.

Dans le deuxième cas, aucun résultat car la relation n’est pas réflexive. Les arcs sont orientés, et il n’y a pas de relation inverse exprimée dans mon arc.

```sparql
##  create a bidirectional relation for bio:married
SELECT ?spouse ?author {{?spouse bio:married ?author} UNION {?author bio:married ?spouse}.
                        ?author lit:wrote lit:KingLear} 
```

Plutôt que de modifier le graph, peut aussi dire que recherche une épouse et un auteur, ou bien un auteur est marié à l’épouse. Nous donne un ensemble de triplets qui est soit l’un soit l’autre, et on trouve la relation de l’autre côté. Une manière de faire des disjonctions. Ici l’union avec un ensemble vide. Le résultat de cette expression est un ensemble de triplets, ici fait la conjonction des ensembles de triplets à moins de faire UNION.

```sparql
# Who wrote King Lear and where in England does he live ?
SELECT ?who ?where {?who bio:liveIn ?where. 
                   ?where  geo:isIn geo:England.
                   ?who lit:wrote lit:KingLear}
```

```sparql
SELECT ?who ?where {?who bio:liveIn ?where; lit:wrote lit:KingLear.
                    ?where  geo:isIn geo:England.}
```

Comme le sujet est le même, on peut les combiner. On peut également utiliser la notation avec les ; et les , dans les modèles.

```sparql
# Show a work and the place it is set in if known
SELECT ?work ?place {[lit:wrote ?work]. 
                      optional {?work lit:setIn ?place} }
```

Ici va écrire chaque œuvre et quand connaît l’endroit où se passe va l’écrire. Ici plutôt que de dire si pas de lieu l’éliminer, ici dit qu’est optionnel. La variole n’est simplement pas instanciée pour ce triplet là.

Avec SPARQL on écrit donc des modèles de graphe que le système va essayer d’instancier sur le graphe dont on dispose. Bien comprendre que l’on travaille sur le graphe et non pas la sérialisation ou turtle. On a donc des variables qu’on réussit plus ou moins à instancier.

FROM permet de combiner plusieurs SPARQL endpoint et regrouper les résultats.

Comme en SQL des group by, order by, offset, etc.

Présentation de l’Aide mémoire et autres fonctionnalités.

SPARQL vous permet ainsi d’interroger un graph RDF et d’extraire des données, de faire des traitements non triviaux et les regrouper. Cela sert essentiellement à regrouper des éléments et faire des choses avec. Ce n’est pas un langage de programmation mais une façon d’aller interroger vos triplets et de retourner des résultats qui seront typiquement adressés à d’autres programmes.

---

# RDF Schema

Quelque chose de bâti par dessus RDF.

Vous a toujours vendu l’idée que le web sémantique nous permettrait de faire des déductions, mais jusqu’ici on n’a pas fait grand chose.

On a combiner des requêtes, etc. seules déduction qu’on ait faite interroger que si x marié a y, etc.

On a besoin de pouvoir intégrer un peu de sémantique, ce que l’on va pouvoir faire avec RDFs. On va pouvoir introduire des classes et des propriétés.

Représentation des connaissances en RDF

- Toute information est encodée comme un triplet
- un fait complexe est encodé comme une conjonction de triplets élémentaires
- on ne peut exprimer la négation ou la disjonction
- on peut déduire des nouvelles informations à l’aide d’un processus d’implication (*entailment*)

Exemple de typage, rappel utilisation des types XML Schema

On peut aussi construire par dessus RDF un certain nombre de structures avec les *containers*. Ici reste dans RDF. Pour le moment, on se contentait de dire que l’on avait des rations entre a et b. Mais si veut dire que l’on a un cours et que des étudiants qui font partie de ce cours là, donc que ce cours là, c’est l’ensemble de ses étudiants. Comme il s’agit de cas de figure courants, on a défini en RDF des containers pour prendre en charge ces cas là.

Un type prédéfini destiné à exprimer le fait qu’on ait un ensemble d’étudiants. Ce qui dit que c’est un container, c’est que son type, l’URI de RDF bag.

http://www.w3c.org/1999/02/22-rdf-syntax-ns#Bag

en fait on a un nœud vide, et son type, le type prédéfini de bag.

Les éléments du bag sont codés à la suite en étant numérotés.

Pour accéder à tous les étudiants de ce bag, possibilité de faire des expressions régulière sur la valeur. Mais il existe ici un rdfs:member qui est un prédicat spécial interprété par l’interprète SPARQL.

Notation qui emploie des noms internes.

également les containers alt, collection, etc.









