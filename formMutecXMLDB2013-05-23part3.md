Formation BaseX, 3e speech : XQuery Full Text
================

cf. [présentation "02 XQuery Full Text I.pdf"]


Information retrieval
----------------

L'Information Retrieval (IR) concerne la découverte d'information, pas des données.
Elle est centrée sur le plein texte, plutôt que sur la structure des documents.


#### Historique

XIXe siècle, création des premiers indices pour les catalogues de bibliothèques
1960-1970 : requêtes booléennes (Lockheed), Vector Space Model
1970-1990 : numérisation des données scientifiques et bibliothécaires (OPACs)
1990-2000 : émergence du web et des premiers moteurs de recherche
2000-2010 : web 2.0, recherche sémantique, réseaux sociaux
aujourd'hui : la recherche d'information en ligne est devenue l'_approche standard_ pour retrouver de l'information.


### La monoculture de google


XQuery full-text
----------------

### Recherches XQuery full-text

XQuery fournit plusieurs chaînes de fonctions qui peuvent être employées dans les requêtes plein-texte : `string`, `contains`, `lower case`, `uper case`,... Ainsi que des possibilités d'utilisation d'expressions régulières avec `matches`.

Exemple :

```xquery
    declare variable $text := "Find a or B";
    contains($text, "a") or contains($text, "B"),
    matches($text, "a|B"),
    matches($text, "a|b", "i"),
    matches($text, "\Wa\W|\Wb\W", "i"),
    matches($text, "(^|\W)a($|\W)|(^|\W)b($|\W)", "i"),
    analyze-string($text, "(^|\W)a($|\W)|(^|\W)b($|\W)", "i")
```

Ce genre de solution n'est pas sans présenter des inconvénients.

Solution avec XQuery full-text  :

    `"find a or B" contains text { "a","b" }`


### Le standard XQuery Full Text

XQuery full-text permet de réunir le monde de l'IR à XML.
Il permet l'écriture de requêtes pour des recherches full-text dans des données textuelles structurées. De telles requêtes peuvent être placées à peu près n'importe où. La syntaxe est simple.

Un standard du W3C actuellement en préparation pour la version 3.
http://www.w3.org/TR/xpath-full-text-10/
http://www.w3.org/TR/2013/WD-xpath-full-text-30-20130108/

Les étapes du traitement sont les suivantes :

1. _évaluer_ le texte et les expressions de la requête
2. _tokenizer_ les chaînes résultantes
3. _matcher_ les chaînes de la requête d'après (against) le texte d'entrée
4. retourner le résultat _booléen_ et (optionnellement) une _valeur de score_


### La tokenization

Une chaîne est splittée en plus petites chaînes, significatives, unités normalisées (mots, phrases, symboles)

On peut par exemple utiliser les espaces comme délimiteurs, enlever caractères spéciaux, changer la casse.

Conversion d’une expression en chaîne, tokenisation, test booléens, etc.
Pas de logique de scoring.

Techniques de tokenization

Changement de casse (Case Folding) en XQuery
Réduire tt en bas-de-casse
Le plus souvent peuvent être ignorés. Mais exceptions qui confirment la règle AIDS, etc.
Question spécifiques aux langues.
Case Folding in XQuery
Par défaut, normalisation de la casse
Mais peut demander sans normalisation
Définit les options pour indexer le texte.

### Diacritiques

Nbx diacritiques, etc.
Normalisation qui peut résoudre plusieurs caractères München -> Muenchen

### Stop Words

Parfois contreproductif :
« to be, or not to be », « let it be »

### Stemming

Très dépendant du langage avec lequel travaille.
Des aspects particulièrement challenging.
Très dépendant de la langue.

BaseX fournit une fonction `ft:tokenize(...)`pour tokeniser les chaînes.

**ex3.xql** Exemple de stemming :

```xquery
    declare ft-option using stemming;
    let $words := ("computer", "computational", "computation", "compute")
    let $stem := "comput"
    return every $word in $words satisfies ft:tokenize($word) = $stem
```

**ex4.xql** Version plus courte :

```xquery
    declare ft-option using stemming;
    not(
        ft:tokenize("computer,computational,computation,compute"         != "comput")
```

Utilisation du stemma de Lucene mais ici emploie XQuery full-text.


cf. [présentation "03 XQuery Full Text II.pdf"]


Utilisation de thesauri
------------

### Thesaurus

Exemples qui montrent comment employer syntaxiquement un thesaurus

Groupes de mots ensemble, d’après leurs _similarités de signification_
Différents _champs d’intérêt_ impliquent des sémantiques différentes.

### Thesaurus is XQuery

Attacher un thesaurus spécifié et trouver des _synonymes_ (UF = used for :

```xquery
    "word" contains text "term" using thesaurus at "thesaurus.xml" relationship "UF"
```

Utiliser un thesaurus par défaut (si disponible) et trouver des termes _plus précis_ (narrow term (NT)) :

```xquery
    "users" contains text "people" using thesaurus default relationship 'NT' at most 2 levels
```

Plusieurs thesauri spécialisés existent.

### Semistructured data

Un challenge particulier : contenu mixte dans le contexte TEI
particulièrement vrai.

string(<li><w><b>n</b>o</w>way</l>) contains text "no" ??

[Rmq : quelle solution proposée ? doit-on écrire les requêtes XQuery pour parer au problème]

### Recherche avancée

#### Recherche de Wildcard
Utilisation d'expressions régulières
cf. diapositive n° 5

#### Recherche approximative

… using fuzzy
Levenshtein distance
Vieux pb mathématique
Deux chaînes différentes dont veut définir formellement à quel point sont différentes.
Avantage de ne pas être dépendant du langage.

Indexing
La plupart des recherches sont réindexées depuis l’index.

Scoring
Autre option possible en XQuery full-text
Précision et rappel
TF-IDF Measure
Scoring sur longueur, profondeur, position, etc.
Exemple

Highlighting Results, etc.
Etc.

BaseX a complètement implémenté le standard XQuery full text, plus en avance que eXist sur ce point.

Après la hype du XML, les gens ont commencé à partir. Des techniques définies il y a 10 ans. Aujourd’hui des gens qui reviennent dans le domaine pour utiliser des outils. Certains venant avec des choses traitées précédemment en perl, ou autre, et peuvent peut-être correctement prises en charge aujourd’hui par les outils XML.

Développement de BaseX issu d’une communauté de Data, pas de contenu mixte. Ils sont vraiment en attente de projets avec du contenu mixte pour travailler. Actuellement, seulement un projet de Basel de phraséologie sur des corpus TEI. Précédemment travaillaient en Perl, besoin application des standards à niveau réel.

Si vous êtes ceux qui font le travail d’encodage, etc. et que vous avez des inspirations concernant l’implémentation, faites nous des retours. Besoin de contributeurs et de retours d’expérience sur cet aspect.


