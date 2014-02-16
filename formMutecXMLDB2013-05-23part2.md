Formation BaseX, 2e Speech
===============

Lancer BaseX
---------------

BaseX peut être lancé de plusieurs manières :

- comme application autonome, en utilisant l'interface graphique utilisateur (GUI) ou l'interface en ligne de commande
- comme une application client/serveur, ou
- comme une application web, appellée depuis un serveur web


Démarrage de l'application (GUI)
---------------

Le GUI est l'inteface visuelle aux fonctionnalités de BaseX. On peut l'utiliser pour créer de nouvelles bases de données, réaliser des requêtes ou explorer interactivement vos données XML.

Après avoir téléchargé BaseX et lancé l'installation, l'interface graphique utilisateur (GUI) peut être lancée de la manière suivante :

- Double-cliquez sur l'icone `BaseX.jar` ou bien exécutez le script `basegxgui`.

D'autres options de démarrages sont également possibles :

- exécuter l'un des scripts `basexgui`ou `basexgui.bat`
- exécuter la commande `java -cp BaseX.jar org.basex.BasexGUI`

Notez que l'interface graphique utilisateur (GUI) n'interagit pas avec l'architecture client/serveur.


Présentation de l’interface
---------------

Chargement document dans l’application

    Ouvrir etc/factbook.xml

Fenêtre de requêtage XQuery
Visualisation des données

Plusieurs modes de visualisation sont disponibles, le mode de visualisation approprié dépend beaucoup de la structure des données. Dans l’exemple, ici des données plutôt plates. Mais affichage latitude, etc. et l'on peut produire une carte de points avec carte mondiale.

DataBase > Propriétés

Fournit des indications sur la base de données. Les ressources dans la base, les éléments nom, chemins,etc., index et full-text.
Avec full-text possibilité d’intégrer des stopwords, etc. stemming, etc.

On peut saisir une requête originale dans l’éditeur XQuery, celle-ci est réécrite en ayant recours aux index. Optimisation de requête, par exemple « // » remplacé avec adding/textStep… automatiquement réécrit par l’optimiseur.

On peut éditer ces étapes, pour optimiser le travail.
De même, on peut utiliser le texte des requêtes optimisées apparaissant dans le panneau "Query Info" pour faire le travail d’optimisation. Il est donc possible d'optimiser explicitement la requête. Ce sont ici des fonctions spécifiques à BaseX. Une documentation est disponible dans le wiki, sous "Module library".

    `//` = `descendant-or-self` `::node()/child` `::name`

    `//name` est optimisé en
    `db:open-pre("factbook",0)/descendant::*:name`

RMQ : Nota, il est possible d’utiliser le module de visualisation pour montrer les chemins XPath en direct. (exploitation pédagogique possible).

Écrire les requêtes en XQuery, le système se charge de l'analyse abstraite des choses. Si on rencontre un problème, alors regarder les questions de performances et optimiser éventuellement la recherche.

Autre manière possible d'optimiser requête :

    `(//item)[1]`

### Script layout

Pour visualiser une sélection d’éléments.
Alors formuler une requête et filtrer les résultats.

Exemple : filtrer la population

    `//country[@population > 1000][name != "China"]`

Possibilité de personnaliser ses visualisation, mais compliqué car le module est écrit en java !

Fonctions XQuery pour fournir input, puis utiliser des fonctions de visualisation pour JSON avec un framework externe spécialement programmé pour connecter des données d’utilisateur pour des visualisation cools. Certaines personnalisables dynamiquement et leur effort principal. Sans doute un choix plus intelligent. Par exemple, utiliser [D3](https://github.com/mbostock/d3)

Pour des raisons de performances, actuellement la base est limitée à 500 Gigabytes.
Strong limitation.
Également limité à 2 millions de nœuds.

[les requêtes de démo sur factbook sont dans `/repo/demoFactbook`]

**ex1.xql** Afficher la liste des pays dont la population est supérieure à 10000, par ordre décroissant de population :

```xquery
    for $c in //country
    let $pop := number($c/@population)
    where $pop > 10000
    order by $pop descending
    return $c/name
```

**ex2.xql** Afficher la liste des villes dont la population est supérieure à 1000 dans les pays dont la population est supérieure à 10000 :

```xquery
    for $c in //country
    let $pop := number($c/@population)
    where $pop > 10000
    order by $pop descending
    let $name := $c/name
    for $city in $c/city
    where $city/population > 1000
    return $city/name
```

[[Voir
http://stackoverflow.com/questions/9407743/insertion-of-an-data-in-an-xml-using-basex]]

http serveur, qui est un serveur Jetty.
http://xml-basex.cbp.ens-lyon.fr:8984
http://docs.basex.org/wiki/Web_Application


Créér une requête

Module namespace _ =”http…” ;
Declare function _ :_() {
<html/>
} ;

Module namespace _ =”http…” ;
declare function _ :_() {
%restxq :path(‘test’)
%output :method(‘html’)
<html>
<form action=”test”>
<input …
</html>
} ;


Module namespace _ =”http…” ;
declare function _ :_() {
%restxq :path(‘test’)
%restxq :query-param(”query”, “{$query}”)

%output :method(‘html’)
<html>
<form action=”test”>
<input name=”query” value=”{ $query }” />
<input type=”submit” />
</form>
</html>
} ;

Module namespace _ =”http…” ;
declare function _ :_() {
%restxq :path(‘test’)
%restxq :query-param(”query”, “{$query}”)

%output :method(‘html’)
<html>
<form action=”test”>
<input name=”query” value=”{ $query }” />
<input type=”submit” />
</form>
<ul>
for $c in doc(‘…
return <li>{ $c/…
}</ul>
</html>
} ;

Demo : Realtime Search in a Catalog Data

Propre moteur de recherche.
Intérêt d’implémenter la spécification XQuery full-text. Sans doute des choses pas possible avec XQuery full-text, mais plus proche de la structure des données.


Information retrieval
IR retrouver l’information par les données.
Focus sur le full)texts, pas la structure ds documents

19th création premiers indices pour cat bib
$60-80 Boolean queries…
voir dia (très bien)

Monoculture de google.
XQuery full-text

Plusieurs fonctions qui peuvent être employées dans les requêtes
String, contains, lower case, uper case
Possibilité d’utiliser des expressions régulières avec matches

Declare variable $text := ”Find a or B” ;
Contains($text, ”a”) or contains($text, ”B”),
Matches($text, ”a|B),
Matches($text, ”a|b”, ”i”),
Matches($text, ”\Wa … …

Un std du W3C Actuellement version 3 en préparation.
http://www.w3.org/TR/xpath-full-text-10/
http://www.w3.org/TR/2013/WD-xpath-full-text-30-20130108/
Tokenization
Une chaîne est splitting en plus petites, significatives, unités normalisées (mots, phrases, symboles)
Peut par ex utiliser espaces comme délimiteurs, enlever caractères spéciaux, chager la case.
Conversion d’une expression en chaîne, tokenisation, test booléens, etc.
Pas de logique de scoring.

Techniques de tokenization
Case Folding
Réduire tt en bas de case
Le plus souvent peuvent être ignorés. Mais exceptions qui confirment la règle AIDS, etc.
Question spécifiques aux langues.
Case Folding in XQuery
Par défaut normalisation de la case
Mais peut demander ss normalisation
Définit les options pour indexer le texte.

diacritiques
Nbx diacritiques, etc.
Normalisation qui peut résoudre plusieurs caractères München -> Muenchen

Stop Words
Parfois contreproductif :
« to be, or not to be », « let it be »

Stemming
Très dépendant du langage avec lequel travaille.
Des aspects particulièrement challenging.
Très dépendant de la langue.
”Hauser

declare ft-option using stemming;
…


declare ft-option using stemming;
not(
  ft:tokenize("computer,computational,computation,compute")
  != "comput"
)

Utilisation du stemma de Lucene mais ici emploie XQuery full-text.


Thesaurus
Exemples qui montrent comment employer syntaxiquement un thesaurus
Groupes de mots ensemble d’après leurs similarités de signification
Différents champs d’intérêt.

Semistructured data
Challenge particulier contenu mixte dans le contexte TEI
Particulièrement vrai

string(<li><w>no</w>way</l>) contains text "no" ??

Recherche avancée
Recherche de Wildcard
Recherche approximative
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

Implémenté le std full text, plus en avance que eXist sur ce point.
Après la hype du XML, gens commencé à partir.
Techniques définies il y a 10 ans. Aujourd’hui gens qui reviennent dans le domaine, aujourd’hui pour utiliser des outils. Certains venant avec des choses traitées précédemment en perl, ou autre, et peuvent peut-être correctement prises en charge aujourd’hui par les outils XML.
Issus d’une communauté de Data, pas de contenu mixte. Vraiment en attente de projets avec du contenu mixte pour travailler. Actuellement seulement un projet de Basel de phraséologie sur des corpus TEI. Précédemment travaillaient en Perl. Besoin application des standards à niveau réel.
Si vous êtes ceux qui font le travail d’encodage, etc. et que vous avez des inspirations concernant l’implémentation, faites nous des retours. Besoin de contributeurs et de retours d’expérience sur cet aspect.



Web application
De plus en plus d’applications aujourd’hui directement basées sur le web. Précédemment sur le bureau, mais de plus en plus web. Avantage de ubiquité des navigateurs web.
Le plus souvent basées sur JavaScript, HTML5, XML.
Manque possibilité de travailler directement en XML.

REST Representational State transfer
Paradigme de programmation pour les applications web
Basé sur la thèse de Roy Fielding de 2001 (un des auteurs de la spécification http).

Chaque REST Service unique adresse (qui est l’URI)
Un service peut retourner différentes représentation de la ressource adressée XML, JSON
REST services sont statelesss : contiennent toutes les informations pour comprendre un message.
Services doivent supporter divers..

RESTXQ : RESTful Applications with XQuery
Présenté 2012 par Adam Retter à la conférence Prague XML.
Motivation
Pas de std pour XML XQuery no std web capacity
…

utiliser un namespace fixe
en BaseX restxq

Méthodes http
Équivalent des http request methods excepté pour TRACE et CONNECT
GET, POST, PUT, DELETE, HEAD, OPTIONS
Une ressource de fonction peut avoir zéro ou plusieurs méthodes d’annotations /

declare %restxq:DELETE %restxq:path(”/”) fucntion _:root($name) { "You have specified the root path and the DELETE method." };

Si aucune méthode n’est spécifiée la fonction sera invoquée pour toutes les méthodes.
POST et PUT annotations peuvent prendre une chaîne optionnelle comme argument.

declare %restxq:PUT %restxq:path(”/upload”) fucntion _:up(
  $data as xs:base64Binary) {
    file:write-binary('/tmp' || …

Types de contenu content types
Une fonction peut être restreinte à un type de contexte, …

Paramètres de requête (query parameters)
Une annotation de paramètre de recherche peut prendre un ou deux arguments.

HTML Form Fields
Paramètres de formulaires qui peuvent être passés quand POST est utilisé
Leurs valeurs sont extraintes en RESTXQ à la fois de POST ou de GET.
…
Paramètres de cookies.

Output prefix par défaut tous les résultats sont retournés avec application/xml comme type de contenu (synonyms : mime type, media type)
The content type peut être overriden via des paramètres de sérialisation
Le type peut être modifié en spécifiant une autre méthode de sortie.

Exemple de sortie XML
Fonctions pour le doctype, etc. qui ne peuvent être produits en XQUery

Redirections
Quand met à jour des requêtes souvent utile de rediriger le browser pour indiquer que l’update a été fait avec succès.
Pas prévu dans la norme.
Solution redirect ou forward implémentée dans BaseX restxq:redirect, restxq:forward

XQuery update permet de mettre à jour des données, mais n’amène pas de résultats.
Sans doute sera le cas dans 3.1, pour BaseX trouvé notre propre solution : db:output qui peut être utilisée avec XQuery update.

Documentation RESTXQ dans la documentation de BaseX
http://docs.basex.org/wiki/RESTXQ
Voir les liens :
Communication de Adam Retter :
http://www.adamretter.org.uk/papers/restful-xquery_january-2012.pdf
Diapositives :
http://www.adamretter.org.uk/presentations/restxq_mugl_20120308.pdf
Draft :
http://exquery.github.io/exquery/exquery-restxq-specification/restxq-1.0-specification.html


Web Application Development

Revenir à ces présentations lorsqu’aura besoin de construire application plus grande.
Maintenant essayer de produire de zéro, une page web en itérations différentes.

Pour cela, garder à l’esprit que RESTXQ seulement la chose qui connecte vos URLs et vos http request et vos requêtes.
Le serveur qui doit réagir à vos request, et lancer l’exécution des requêtes.

Blog example

Dézipper le dossier de travail
L’archive exécutable le fichier .jar
Le reste une présentation conventionnelle.
Etc. configuration
Bibliothèques dans lib
Dans bin que va travailler
Peut ici exécuter le client baseX dans bin en ligne de commande, différents lanceurs. Ici que se trouvent les différents scripts d’exécution des différentes incarnations de baseX, pour un serveur http, etc.
Ici un intermixe de web serveur et de servlet.
Quand besoin de mettre en œuvre un serveur, tout ici.

Le répertoire de données data est vide
Ici qu’allons charger les données. Ici peut mettre etc. modules, etc.
Dans etc que mettra les XSLT, etc.
Dans libraries que mettra plus tard les stemma

Répertoire repository actuellement vide, ici que pourra mettre les modules
Enfin le répertoire webapp
Ici la racine du serveur http
Quand démarrer le serveur http, ce répertoire qui est servi

Se placer à la racine du répertoire dézippé

ls –a pour fichiers cachés
retirer .basex
rm .basex

Créer un fichier vide de configuration .basex :
touch .basex

Maintenant avec cette configuration vide, nous allons démarrer BaseX dans sa version de console :
Exécuter le script de lancement du serveur avec la commande :
./bin/basexhttp

emmanuelchateau ~/Desktop/basex ./bin/basexhttp
Saving properties in "/Users/emmanuelchateau/Desktop/basex/.basex"...
BaseX 7.7 beta [Server]
Server was started.
HTTP Server was started.

[kill le serveur CtrC]

Aller sur le localhost.
Le serveur est accessible sur le port 8984

Pour ceux qui sont habitués aux bases de données, beaucoup de choses qui peuvent vous rendre la vie plus facile avec les GUI. Mais si vous devez réellement développer des choses, vous allez devoir entrer en contact avec le système. Or le système est un serveur sur une machine UNIX, il faut donc à un moment se confronter concrètement à cela à un moment ou un autre.

Nouvelle fenêtre de console
Aller dans bin et démarrer baseX :
./basex
On dispose directement du client en ligne de commande
Tapper xquery 1+4
Rapporte 5

La racine de votre répertoire est webapp
Nous avons démarré avec une base de données vide.
Rien n’a encore été configuré.
Pour ceux pas vraiment habitué au terminal, possibilité d’utiliser GUI.

Lister le répertoire data
ls –a data
Ne contient rien.

Première fonction à laquelle devons nous habituer.
Maintenant le serveur fonctionne
Démarrer l’interface graphique de BaseX avec le script « basexgui » :
./bin/basexgui

Nous avons maintenant un serveur http qui tourne
Un client GUI

Open file dans éditor
Aller dans webapp/restxq.blogv1.xq

Nous allons commencer par voir à quoi doit ressembler l’application.
Aller sur http://localhost:8984/restxq/blog-v1/

Créer la base de données
Regarder dans le code l’adresse créée

Fichier bloc_v1 qui contient du code XQuerry

(:~
 : Creates a new blog database.
 :)
declare %restxq:path("blog-v1/create-database")
        %restxq:GET
        updating function page:create-blog-database() {

  let $blogdb := <blog>
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

Maintenant peut voir qu’une base de données a bien été créée.
Voir dans le répertoire data
ls –a data

Sinon voir dans le GUI ouvrir bases de données
Il s’appelle my-blog
Fonction qui a créé la base de données.
Simplement une connexion par URL et requête qui créée la base de données.

De même option delete, etc.
Nous n’avons encore rien fait d’autre que de réaliser des tâches de base sur BaseX
Db :create() créée nouevlle base de données pour le blog
(db :drop() offre la possibilité d’effacer la base du blog)
Le fichier « blog.xml » n’existe pas réellement dans le système de fichier à la création de la base de données. Mais c’est le fichier qui existerait en sérialisant la représentation de la base de donnée pour un export.

Nous allons maintenant fournir du code pour insérer du texte, etc.

Aller voir la version 2
http://localhost:8984/restxq/blog-v2/
Va faire l’utilisation de fonctionnalités d’utilisation et de mise à jour de XQuery.
XQuery update langage de mise à jour de données.

Ici quand entre une donnée dans le formulaire. Retourne une page vide.
Se contente de mettre à jour la base de données.
Devons faire une combinaison de redirection et de update.

Doit augmenter cette fonction pour outputer…

Aller sur
http://localhost:8984/restxq/blog-complete/
Maintenant fonctionne
Aller voir le code

Allons créer maintenant une application de zéro
Donc Voulons créer une application sous l’adresse
localhost:8984/restxq/lyon
Pour le moment rien de servi.

Devons donc commencer.
Ouvrir le module restxq pour trouver des modèles d’inspiration

Première chose créer un nouveau fichier.
Première requête : 1+1

(: blog lyon :)
1 + 1

(: blog lyon :)
<h3>"hello Lyon" || 1 + 12 || "personne assistent" </h3>

Voulons faire de cela une fonction
L’encadre de { et déclare la fonction

(: blog lyon :)
declare function local:say-hello()
{
  <h3>{"hello Lyon" || 1 + 12 || "personne assistent"}</h3>
};

Le GUI nous dit qu’attend une expression

(: blog lyon :)
declare function local:say-hello()
{
  <h3>{"hello Lyon" || 1 + 12 || "personne assistent"}</h3>
};
local:say-hello(

créer un module :

module namespace page = 'http://basex.org/modules/web-page';

(: blog lyon :)
declare function local:say-hello()
{
  element h3 ("hello Lyon")
};
local:say-hello()

enregistrer sous le nom : Lyon.xqm dans restxq

[pb]

Pour que la page soit affichée :

module namespace lyon= 'http://basex.org/modules/web-page';
(: blog lyon :)
declare function
%testing:path('/lyon')
function lyon:say-hello()
{
  element h3 {"hello Lyon"}
};

Voir page
Nous avons maintenant connecté le code et la page.
http://localhost:8984/restxq/lyon

Créer une base de données
Aller chercher factbook dans etc

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
  function lyon:show-factbook()
{
  let $factdb := doc('factbook')
  return
    ($factdb//city)[1]
};

Comme c’est un module on ne peut l’exécuter directement
Mais comme c’est un module, on peut créer un nouveau fichier dans lequel importer ce module :

import module namespace lyon = 'http://basex.org/modules/web-page' at 'lyon.xqm';
lyon:show-factbook()


[[Voir fichiers credits.xml et payements dans le répertoire restxq pour des exemples d’implémentation de xforms]]

Cet exemple en html
Donc copier   %output:method('xhtml')

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
  %output:method('xhtml')
  function lyon:show-factbook()
{
  <html>
    {
    let $factdb := doc('factbook')
    return
      ($factdb//city)[1]

    }
  </html>
};


Voulons trouver quelque chose dans les données.
Créer un formulaire.

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

Créer une requête et besoin de fournir une variable avec paramètre et valeur sera évaluée
%restxq:query-param('query', '{$query}')
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


Créer après la requêet une loupe mettre ul

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

**En utilisant des litéraux :**

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
