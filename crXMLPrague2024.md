# XML Prague 2024

Diverses présentations sur IA et XML

Michael Kay, XSL 4.0

## Navigating, updating, transforming JSON

Version 3.0 parue 2017 introduit data array et maps. Support en XSLT en partie incomplet mais en réalité d’autres choses. Présentation sur les manques en 2016, avec cas d’usages qui ont servi au travail conduit dans le cadre du travail sur une version 4 de la spécification.

Les maps et arrays ont été introduits pour probablement trois raisons.

- d’abord lié au fait que XSLT devait supporter le streaming ce qui implique de ne pas pouvoir avoir accès à l’ensemble de la sortie
- ce qui implique d’avoir une structure de mémoire qui puisse efficacement être mettre à jour. Possibilité de produire des nouveaux maps à partir d’anciencs maps.
- alors réalisé que moitié du travail pour supporter JSON. Début de support pour arrays et maps, les deux structures de JSON

Covid qui a en partie limité l’avancée du projet. Arrivée de Norm a beaucoup accéléré le travail. 500 personnes intervenues sur le projet.

Les choses qui seront présentées aujourd’hui ne sont pas nécessairement des choses stabilisées, des changements pourront encore intervenir. Certaines choses implémentées, d’autres pas encore.

Six aspects

- navigation
- point update
- bulk transformation

Navigation : extraction de données d’arbres et de maps et d’array. Il faut se souvenir qu’il ne s’agit pas seulement de JSON car les maps peuvent contenir des nœuds ou d’autres structures. Il y a une généralisation entre les modèles XML et JSON.

Point update : faire des petits changements dans de grands arbres. Transformations basées sur XSLT impliquent 5 ou 6 phases alors que changement mineur dans la structrure. Question liée à l’identité des nœud et point update. En JSON pas le cas pour simplifier la question mais empêche de naviguer les arbres.

Bulk transformation : grouping, sorting, inversion, conversion dans d’autres formats. N’en parlera pas beaucoup pour des raisons de temps mais aussi car implémentation différente avec Saxon pour le moment. Recursive descent transformation.

### Navigation

Trois choses ont été faites

- ajout de `??` comme analogue de `//` pour naviguer arbres XML
- sélection d’items par leurs type
- et upwards navigation

Exemple avec l’outil Saxon Gizmo qui est un évaluateur interactif d’expression XPath.

```xquery
json-doc('books-and-bikes.json')
```

```xquery
show $in ? store ? bicycle
```

Noms en XML remplissent deux rôles : type d’objet. En JSON pas un nom. Mais les propriétés ont un noms. Les noms d’éléments en XML parfois types de chose ou relations au parent. Ici rôles différents. Ici les livres ne sont pas nommés, seulement l’ensemble de libre qui est un array d’objets anonymes en JSON.

Abréviation introduite

```xquery
show $in ?? bicycle
```

Utile pour plusieurs raisons, notamment parce que le chemin peut être relativement complexe, une abréviation efficace. Par ailleurs, il peut y avoir différents vélos à différents endroits dans la structure.

Différences entre XML et le modèle JSON

```xquery
show $in ?? price
```

Présente six prix. En XML pourrait naviguer entre les différents prix. Mais en JSON pas de navigation possible. Peut faire la moyenne, etc. mais ne peut pas dire que les vélos sont plus chers que les livres. Nous allons voir comment résolu le pb.

Évidemment opérateur compatible avec les fonctions introduites dans la version 3. Pour obtenir la moyenne : 

```xquery
show $in ?? price => avg()
```

```xquery
show $in ?? type ( record (title, author, *))
```

Les livres en JSON n’ont pas de nom. Au lieu de trouver le nom des objets, on peut les chercher par structure. On a donc introduit un pattern qui permet de sélectionner selon ce prédicat.

Bien sûr combinables avec d’autres choses. 

``` xquery
show $in ?? type (record (title, author, *)) => (: err chger opérateur :) map:filter(fn($key){$key = ('author', 'title', 'isbn')})
```

Construire nouveau map

```xquery
show $in ?? type (record (title, author, *) ! {'author':?author, 'title':?title})
```

etc.

Beaucoup plus de flexibilité pour traiter et filtrer les données.

Output navigation. Lorsque présenté le problème parent point. Pb identité dans les données. Mais se souvient que navigue de haut en bas, donc possible de se souvenir comment arrivé à ce résultat. Alors annote le résultat d’une expression avec chemin par lequel trouvé. Donc une annotation supplémentaire sur le résultat.

On peut donc qualifié les ?? dire que pas seulement les valeurs mais les entrées

```xquery
show $in ?? (: incomplet :)
```

Recherche les tris, valeurs et propriétés. Avec information ancestors et root pour revenir à l’arbre

```xquery
show $in ?? entry::price [?parent()?isbn]
```

Filtre le fait que le parent un objet avec isbn

```xquery
show $in ?? entry::price [?parent()?isbn] ? value
```

### Updates

Premier usecase de 2016 difficile, prendre ensemble similaire de données JSON et voir comment augmenter les valeurs de 10%. Solution la plus simple, transformer les données en XML, faire la requête en XML et mettre à jour. Très long en réalité à opérer.

La solution de la spécification 4 est la suivante. Nouvelle expression update

```xquery
show update array [0, 1, 2, 3, 4] replace ?2 with 10
```

Bien sûr devient plus intéressant avec deep-updating. Syntaxe facile à comprendre mais sémantique en réalité complexe. Car pour que fonctionne nombreuses choses qui doivent être faites : consolider, donner, mettre à jour feuilles individuelles, et garder de la trace de ce qui a été fait avant de propager.

La spécification exprimée en top-down descent mais implémentation différente.

```xquery
set $in = json-doc('price.json')
```

```xquery
set $out = update array $in replace ??type(record(tags, prices, *))[?tags= (: ... :)e']?price with .*1.1
```

Listes de cours des étduiants. Requête hiérarchique inversée. Solution structurer un array et pour tout email, groupé par la valeur du courriel, ordonné par la clef, et retourne un map qui contient adresse et ensemble de cours de l’ancêtre.

Solution XSLT similaire. 

Résumé : voir article pour détail.

### Discussion

Langage mélange de différentes capacités adressant différentes parties des langages plutôt qu’unification. Mais s’explique par le fait que les langages sont très différents. Résulte du fait que le modèle de données manque l’ordonalité qu’il aurait été idéal qu’il ait. 

Les arbres XML ont toujours un pointeur. Rien d’intrinsèque qui devrait faire que XML et JSON soit si différents. Mais XML focalisé sur le texte qui est récursif, nécessite navigation qui n’est pas nécessaire dans le monde des données.

## JSONPath : an IETF Proposed Standard, with compparisons to XPath

Alan Painter

Stefan Gössner proposé en 2007

https://cburgmer.github.io/json-path-comparison montré que différentes implémentations.

Implémenté dans différents outils Kubernetes, etc.

2024 un groupe de travail IETF arrivé avec un nouveau standard RFC9535. Vidéo et page Wikipédia

Voir les communalité avec la création de XML. Pas seulement dans le format mais data-interchange et media-type. 99 internet standards W3C. Près de 25 ans pour avoir un standard après spécification de JSON...

Modèle de données. Standard très simple et basique.

RFC9535 objectif simple extraire valeurs de JSON. Pas créer un langage qui fait tout (pas XPath) mais tâche très simple extraire valeurs.

Environnement d’exécution. Simple query argument, et produit output values. Liste de valeurs, presque séquence, une liste de chose. Toujours une paire : une valeur et indication où se trouve. Normalize path.

Expression : identifier segment et sélecteur.

- `$` source document la racine de l’argument `/` en XPath
- `@` qui correspond au nœud contexte `.` en XPath
- [(selectors])] child
- ..[(selectors)] descendant

Mais ne peut pas sélecter les keys en JSON

Liste de sélecteur, name avec valeur de key. Wildcard, index, array slice, filtre introduit par ?

Plusieurs fonctions, expression régulière. Filtre peuvent être comparaison ou existence.

XPath vs JSONPath

Nombreuses différences.  JSONPath, beaucoup plus simple.

Page Wikipédia qui n’évoquait pas XPath comme alternative. Seulement JSONiq. L’a ajouté. Montre que pas XPath 3.1 pas connu dans la communauté que très bonnes requêtes possibles.

JSONPath et XPath 3 expression souvent similaires.

JSONPath ne peut pas remplacer XPath transformations

JSON est partour, faire savoir que XPath excellent poru traiter JSON

JSONPath maintenant standard proposé, importantes divergences. Est-ce qu’il y aura alignement des différentes implémentations ?

Note de bas de page. Question localisation. Dans implémentation originale, peut lister objets ou localisation. 

### discussion

Bray expliqué que si JSON a réussi selon lui car pu implémenter en un we. Souvent une manière de rendre les choses efficaces. Pour XPath 3, implémentation difficiles à produire.

## Single source

IDML format format échange.

Introduit en 2008 avec Adobe CS4, pas le format de travail.

Pas de documentation publicaque.

Version 8 depuis 2012

Spreads, double page contient différent type d’objets
