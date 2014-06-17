Formation BaseX, speech n° 5, RESTXQ : Construire des Applications Web, Comment développer une application web basée sur RESTXQ
===============

[cf. diapos "2013-05-23-RESTXQ-WebApps-BaseX.pdf]


Web Application Development, introduction
-----

Revenir à ces présentations lorsqu’aura besoin de construire application plus grande.
On va maintenant, essayer de produire à partir de rien, une page web en itérations différentes.

Pour cela, garder à l’esprit que RESTXQ est seulement la chose qui connecte vos URLs et vos requêtes HTTP entre elles. Le serveur qui doit réagir à vos requêtes, et lancer l’exécution des requêtes.

Exemple de blog
--------

Dézipper le dossier de travail
L’archive exécutable est le fichier .jar
Le reste, une présentation conventionnelle.
Etc. configuration

Bibliothèques dans lib
Dans bin que va travailler
Peut ici exécuter le client baseX dans bin en ligne de commande, différents lanceurs. Ici que se trouvent les différents scripts d’exécution des différentes incarnations de baseX, pour un serveur http, etc.
Ici, un intermixe de web serveur et de servlet.
Quand besoin de mettre en œuvre un serveur, tout ici.

Le répertoire de données `data/` est vide
Ici qu’allons charger les données. Ici peut mettre etc. modules, etc.
Dans `etc/` que mettra les XSLT, etc.
Dans `lib/` libraries que mettra plus tard les stemma

Répertoire `repo/` repository actuellement vide, ici que pourra mettre les modules
Enfin le répertoire `webapp/`
Ici, la racine du serveur http : lorsque l'on démarre le serveur HTTP, c'est ce répertoire qui est servi.

Se placer à la racine du répertoire dézippé

`ls –a #pour afficher les fichiers cachés`

retirer .basex
`rm .basex`

Créer un fichier vide de configuration .basex :
`touch .basex`

Maintenant, avec cette configuration vide, nous allons démarrer BaseX dans sa version de console :
Exécuter le script de lancement du serveur avec la commande :
`./bin/basexhttp`

emmanuelchateau ~/Desktop/basex ./bin/basexhttp
Saving properties in "/Users/emmanuelchateau/Desktop/basex/.basex"...
BaseX 7.7 beta [Server]
Server was started.
HTTP Server was started.

[kill le serveur avec CtrC]

Aller sur le localhost, le serveur est accessible sur le port 8984

Pour ceux qui sont habitués aux bases de données il est possible d'interagir avec BaseX en ligne de commandes. Cependant, beaucoup de choses peuvent rendre la vie plus facile avec l'interface graphique utilisateur, GUI. Mais si vous devez réellement développer des choses, vous allez devoir entrer en contact avec le système. Or, le système est un serveur sur une machine UNIX, il faut donc à un moment se confronter concrètement à cela à un moment ou un autre.

Ouvrir une nouvelle fenêtre de console.
Aller dans bin et démarrer baseX :
`./basex`

On dispose maintenant directement du client en ligne de commande
Tapper 
`xquery 1+4`
Rapporte 5

La racine de votre répertoire est `webapp/`
Nous avons démarré avec une base de données vide.
Rien n’a encore été configuré.
Pour ceux pas vraiment habitué au terminal, possibilité d’utiliser GUI.

Lister le répertoire data
`ls –a data`
Ne contient rien.

Première fonction à laquelle devons nous habituer.
Maintenant le serveur fonctionne
Démarrer l’interface graphique de BaseX avec le script « basexgui » :
`./bin/basexgui`

Nous avons maintenant un serveur http qui tourne ainsi qu'un client graphique.

Open file dans éditor
Aller dans `webapp/restxq.blogv1.xq`

Nous allons commencer par voir à quoi doit ressembler l’application :
Aller sur http://localhost:8984/restxq/blog-v1/

Créer la base de données
Regarder dans le code l’adresse créée

Fichier bloc_v1 qui contient du code XQuerry
```xquery
    (:~
    : Creates a new blog database.
    :)
    declare %restxq:path("blog-v1/create-database")
            %restxq:GET
    updating function page:create-blog-database() {

    let $blogdb := 
    <blog>
        <blogname>The Weather Blog</blogname>
        <blogauthor>
            <name>John Doe</name>
        </blogauthor>
        <postings>
        </postings>
    </blog>

    (: Create the database. :)
    return
        db:create("my-blog", $blogdb, "blog.xml")
    };
```

Maintenant, on peut voir qu’une base de données a bien été créée.
Voir dans le répertoire data
`ls –a data`

Sinon, voir dans le GUI ouvrir bases de données
Il s’appelle `my-blog`
Fonction qui a créé la base de données.
Simplement une connexion par URL et requête qui créée la base de données.

De même option delete, etc.
Nous n’avons encore rien fait d’autre que de réaliser des tâches de base sur BaseX
`db:create()` créée nouvelle base de données pour le blog
(`db:drop()` offre la possibilité d’effacer la base du blog)
Le fichier `blog.xml` n’existe pas réellement dans le système de fichier à la création de la base de données. Mais c’est le fichier qui existerait en sérialisant la représentation de la base de données pour un export.

Nous allons maintenant fournir du code pour insérer du texte, etc.

Aller voir la version 2 :
`http://localhost:8984/restxq/blog-v2/`
Va faire l’utilisation de fonctionnalités d’utilisation et de mise à jour de XQuery.
XQuery update, un langage de mise à jour de données.

Ici, quand entre une donnée dans le formulaire. Retourne une page vide.
Se contente de mettre à jour la base de données.
Devons faire une combinaison de redirection et de update.

Doit augmenter cette fonction pour outputer…

Aller sur
`http://localhost:8984/restxq/blog-complete/`
Maintenant fonctionne
Aller voir le code

Allons créer maintenant une application de zéro
Donc Voulons créer une application sous l’adresse
[http://localhost:8984/restxq/lyon](http://localhost:8984/restxq/lyon)
Pour le moment rien de servi.

Devons donc commencer.
Ouvrir le module restxq pour trouver des modèles d’inspiration

Première chose créer un nouveau fichier.
Première requête : 1+1

```xquery
    (: blog lyon :)
    1 + 1
```
```xquery
    (: blog lyon :)
    <h3>"hello Lyon" || 1 + 12 || "personne assistent" </h3>
```

Voulons faire de cela une fonction
L’encadre de { et déclare la fonction

```xquery
    (: blog lyon :)
    declare function local:say-hello()
        {
        <h3>{"hello Lyon" || 1 + 12 || "personne assistent"}</h3>
        };
```

Le GUI nous dit qu’il attend une expression

```xquery
    (: blog lyon :)
    declare function local:say-hello()
    {
    <h3>{"hello Lyon" || 1 + 12 || "personne assistent"}</h3>
    };
    local:say-hello()
```

Il faut maintenant créer un module :

```xquery
    module namespace local = 'http://basex.org/modules/web-page';
    
    (: blog lyon :)
    declare function local:say-hello()
    {
    element h3 {"hello Lyon"}
    };
    local:say-hello()
```

enregistrer sous le nom : `lyon.xqm` dans restxq


Pour que la page soit affichée :

```xquery
    module namespace lyon= 'http://basex.org/modules/web-page';

    (: blog lyon :)
    declare %restxq:path('lyon')
    function lyon:say-hello(){
        element h3 {"hello Lyon"}
    };

```

Nous pouvons maintenant aller voir la page [http://localhost:8984/lyon](http://localhost:8984/lyon) : nous avons connecté le code et la page.

Créer une base de données
Aller chercher factbook dans etc/

```xquery
    module namespace lyon = 'http://basex.org/modules/web-page';
    
    (: blog lyon :)
    declare %restxq:path('lyon')
            %output:method('xhtml')
    function lyon:say-hello()
    {
        element h3 {"hello Lyon"}
    };
    
    (: show some facts about the fact book :)
    declare
    %restxq:path('factbook')
    function lyon:show-factbook()
    {
    let $factdb := doc('factbook')
    return ($factdb//city)[1]
    };
````

Comme c’est un module on ne peut l’exécuter directement
Mais comme c’est un module, on peut créer un nouveau fichier dans lequel importer ce module :

```xquery
    import module namespace lyon = 'http://basex.org/modules/web-page' at 'lyon.xqm';
    lyon:show-factbook()
```

[[Voir fichiers credits.xml et payements dans le répertoire restxq pour des exemples d’implémentation de xforms]]

Cet exemple en html
Donc copier   %output:method('xhtml')

```xquery
    module namespace lyon = 'http://basex.org/modules/web-page';
    (: blog lyon :)
    declare %restxq:path('/lyon')
            %output:method('xhtml')
    function lyon:say-hello()
    {
    element h3 {"hello Lyon"}
    };
    
    (: show some facts about the fact book :)
    declare %restxq:path('/factbook') 
            %output:method('xhtml')
    function lyon:show-factbook()
    {
    <html>
        {
        let $factdb := doc('factbook')
        return ($factdb//city)[1]
        }
    </html>
    };
```

Nous voulons trouver quelque chose dans les données.
Pour cela nous allons créer un formulaire.

```xquery
    module namespace lyon = 'http://basex.org/modules/web-page';
    (: blog lyon :)
    declare %restxq:path('/lyon')
            %output:method('xhtml')
    function lyon:say-hello()
    {
    element h3 {"hello Lyon"}
    };
    (: show some facts about the fact book :)
    declare %restxq:path('/factbook')
            %output:method('xhtml')
    function lyon:show-factbook()
    {
    <html>
        <form action="factbook">
            <input name="query"/>
            <sumit type="submit"/>
        </form>
    {
    let $factdb := doc('factbook')
    return
      ($factdb//city)[1]
    }
    </html>
    };
```

Créer une requête et besoin de fournir une variable avec paramètre et valeur sera évaluée
`%restxq:query-param('query', '{$query}')`
et modifie le formulaire

module namespace lyon = 'http://basex.org/modules/web-page';
(: blog lyon :)
declare
%restxq:path('/lyon')
%output:method('xhtml')
function lyon:say-hello()
{
  element h3 {"hello Lyon"}
};
(: show some facts about the fact book :)

declare
  %restxq:path('/factbook')
  %restxq:query-param('query', '{$query}')
  %output:method('xhtml')
  function lyon:show-factbook()
{
  <html>
  <form action="factbook">
    <input name="query" value="{ $query }"}/>
    <sumit type="submit"/>
  </form>
    {
    let $factdb := doc('factbook')
    return
      ($factdb//city)[1]

    }
  </html>
};


Créer après la requête une loupe mettre ul

module namespace lyon = 'http://basex.org/modules/web-page';
(: blog lyon :)
declare
%restxq:path('/lyon')
%output:method('xhtml')
function lyon:say-hello()
{
  element h3 {"hello Lyon"}
};
(: show some facts about the fact book :)

declare
  %restxq:path('/factbook')
  %restxq:query-param('query', '{$query}')
  %output:method('xhtml')
  function lyon:show-factbook($query)
  {
  <html>
  <form action="factbook">
    <input name="query" value="{ $query }"/>
    <sumit type="submit"/>
  </form>
  <ul>
  {
    for $factdb in db:open("factbook")
    return
      ($factdb//city)[1]
  }
  </ul>
  </html>
};

étape (ne pas oublier de fournir un argument entre parenthèses)

module namespace lyon = 'http://basex.org/modules/web-page';
(: blog lyon :)
declare
%restxq:path('/lyon')
%output:method('xhtml')
function lyon:say-hello()
{
  element h3 {"hello Lyon"}
};
(: show some facts about the fact book :)

declare
  %restxq:path('/factbook')
  %restxq:query-param('query', '{ $query }')
  %output:method('xhtml')
  function lyon:show-factbook($query as xs:string)
{
  <html>
  <form action="factbook">
    <input name="query" value="{ $query }"/>
    <sumit type="submit"/>
  </form>
  <ul>
  {
    for $city in db:open("factbook")//city/name
    where $city contains text {$query}
    return
      <li>{ $city/text() }</li>
  }
  </ul>
  </html>
};

Ajouter un count []

module namespace lyon = 'http://basex.org/modules/web-page';
(: blog lyon :)
declare
%restxq:path('/lyon')
%output:method('xhtml')
function lyon:say-hello()
{
  element h3 {"hello Lyon"}
};
(: show some facts about the fact book :)

declare
  %restxq:path('/factbook')
  %restxq:query-param('query', '{ $query }')
  %restxq:query-param('count', '{ $count }')
  %output:method('xhtml')
  function lyon:show-factbook($query as xs:string, $count)
{
  <html>
  <form action="factbook">
    <input name="query" value="{ $query }"/>
    <input name="query" value="{ $count }"/>
    <sumit type="submit"/>
  </form>
  <ul>
  {
    let $all :=
    for $city in db:open("factbook")//city/name
    where $city contains text {$query} using wildcards
    return <li>{city/text()}</li>
    return {
      $all[position() <= $count],
      <li>Number of total result : { count($all) }</li>}
  }
  </ul>
  </html>
};





XQuery
-------------
### Introduction

#### Qu’est-ce que XQuery 3.0 ?

XQuery plus qu’un langage de requête

Développé comme un « conterpart » de SQL, un langage fonctionnel
Extensible via des fonctions et des modules utilisateurs.

Un langage d’usage général ?

Plutôt un "langage de traitement de l’information" (Information Processing Language).

#### Les extensions

Extensions full text, update, scripting

#### Les alternatives

XSLT dispose de fonctionnalités comparables mais le langage est plus spécialisé pour les  transformations.
SQL 2005 a cherché à combiner SQL et XQuery.

Un langage dans le domaine spécifique des technologies XML et de requêtage de documents XML. Cependant, on peut faire plus que de requêter, on peut traiter les données, les analyser, et les manipuler.

Pour eux, avant tout un **langage de traitement informationnel** (« Information Processing Langage »).


### Un langage fonctionnel

Autres exemples proéminents de tels langages : Haskell, Sccheme, OCAML, R.

Basé sur l’évaluation de fonctions : une entrée, un résultat. Une entrée définie, et une sortie définie en résultat
Un langage dépourvu d’effet de bord (qui changerait l’état d’un programme)

Des fonctions d’ordre supérieur : fonctions comme arguments. [exemple tri d’une liste, peut renseigner une fonction pour le tri. Utilisation d’une fonction de comparaison. Une bonne manière d’abstraire.].

Il n'est pas possible de produire des _itération_, des boucles avec XQuerry. Cependant on dispose de la _récursion_ dans un langage fonctionnel.

XQuery 3.0 est un langage pleinement fonctionnel.
Si certaines choses peuvent paraître impératives, (come `for`, `if`) une conception tout à fait différente.


### Le modèle de données de XQuery

#### Les séquences

-L'évaluation des expressions ont pour résultat des _valeurs (values)_
- En XQuery, toutes les valeurs sont des _séquences_
- Les séquences sont des listes de zéro ou plusieurs _items_ :
`<H>U</H>, ("different", 2, <a/>), ()`
- Les séquences de zéro items sont appelées des _séquences vides (empty sequences_
- Les séquences sont ordonnées : (1,2) n'est pas équivalent à (2,1)
- Elles peuvent contenir des _duplications (duplicates)_ (à la différence de XPath)
- Elles ne peuvent pas être imbriquées, aussi elles sont automatiquement mises à plat :
`(1,(2,3),4) --> (1,2,3,4)`

#### Les types de données

- Les items sont des _valeurs atomiques_ ou des _noeuds_
- Les nœuds sont des constructions XML : éléments, attributs, etc.
- Les valeurs atomiques sont des booléens (booleans), entiers (integers), chaînes (strings), dates (dates)

#### Les types de nœuds XML

- nœuds document
- éléments
- attributs
- textes
- commentaires
- instructions de traitement

#### Valeurs atomiques

Cf. [XQuery Data Model, 2010](http://www.w3.org/TR/xpath-datamodel/)

En pratique travaillera principalement avec quelques types :

- xs:integer, xs:decimal, xs:double
- xs:string
- xs:boolean
- xs:date, xs:time, xs:duration

#### Créer des valeurs atomiques

**En utilisant des littéraux :**

`"string"`, `0.98`

**En les assignant explicitement :**

`"2000-12-31T23:59:59"`, `cast as xs:dateTime``

**Résulttante d'appels de fonction :**

`true()` --> xs:boolean, `max((1,2,5,10,20,50,100))` --> xs:integer

### Les expressions

Les expressions peuvent être de plusieurs type :

**Expressions primaires**

litéraux, variables, appels de fonction, parenthisées [??]

**Artithmétiques, de comparaison**

numériques et comparaisons de dates
comparaisons basées sur les valeurs ou l'ordre du document

**Logiques**

opérateurs booléens

**Conditionnelles**

if/then/else, switch, typeswitch

**Opérateurs de séquence**

opérations basées sur les ensemble

**Constructeurs**

construction de nœud directe et computée

**Expressions FLOWR**

Boucles spécifiques à XQuery


#### Expressions primaires

**litéraux**

chaîne (string) : `"example"`
entier (integer) : `1234`
décimal (decimal) : `12.34`
double (double) : `12.3e4`

**variables**

syntaxe dollar avec des préfixes ou des espaces de noms optionnels :
`$a`, `$pf:b`, `$Q{www}b`

**appels de fonction**

nom de la fonction, arguments :
`doc("input.xml")`, `local:function(99)`

**commentaires**

XQuery est un langage souriant ! Les commentaires sont compris dans  :
```(: smileys
    (: qui peuvent être imbriqués :)
 :)```

#### Expressions artithmétiques

**addition, soustraction**

- nombres : `1 + 2 - 3`
- dates : `date("2001-01-01") + xs:duration("P9Y")`
- chaînes : `"and " || "some " || "more"`

**multiplications, divisions d'entier, modulo**

- `(1 + 2) * 3`
- `4 * 5 div 6`
- `7 idiv 8`
- `9 mod 10`

#### Expressions de comparaison

**Comparaisons de valeurs**

- opérateurs disponibles : `eq`, `ne`, `lt`, `le`, `gt`, `ge`
- restreint à la comparison de _valeurs atomiques seules_
- les valeurs des deux opérandes doivent être du _même type_
- si _l'une des termes opérés_ contenait une séquence vide, () est retournée

Quels résultats attendre des expressions suivantes ?

- `3 gt 4`
- `"a" le "b"`
- `"123" eq 123`
- `<x>1</x> lt 2`
- `(1,2) gt (2,1)``
- `() eq ()`
- `() ne ()`

**Comparaisons générales**

- opérateurs disponibles : `<`, `<=`, `=`, `>=`, `>`, `!=`
- compare _tous les items_ d'une séquence les uns avec les autres
- retourne `true` si _au moins un des termes est **vrai**
- valeurs non typées...
-- _implicitement converties_ dans le type des autres items
-- si les deux items sont non typés, leurs valeurs sont comparées comme des _chaînes_

Quels résultats attendre es expressions suivantes ?

- `3 > 4`
- `"a" <= "b"`
- `"123" = 123`
- `<x>1</x> < 2`
- `(1,2) > (2,1)``
- `() = ()`
- `() != ()`

**Comparaisons de nœuds**

Expressions if/then/else

- syntaxe :
`if(test)`,
`then expr1 else expr2`

- syntaxe imbriquée :
`if(test1)`,
```then expr1
else if(test2)
then expr1
else expr2```

Valeur booléenne effective

Comme `boolean()`:

- strings --> string length > 0 ?
- numbers --> different to 0 ?
- boolean --> adopted as is
- empty sequence --> false
- sequence de nœuds --> true
- autres items/sequences --> absurde

#### Logiques

opérateurs booléens

.../...

#### Conditionnelles

if/then/else, switch, typeswitch

.../...

#### Opérateurs de séquence

opérations basées sur les ensemble

.../...

#### Filtres et Prédicats

Prédicats, Contexte item .

.../...

#### Constructeurs

construction de nœud directe et computée

.../...

#### Expressions FLOWR

Boucles spécifiques à XQuery

.../...

TIMTOWTDI (prononcez ”Tim Toady”, un motto de programmation Perl) There Is More Than One Way To Do It (Larry Wall)
