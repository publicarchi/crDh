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

Le GUI fournit une interface visuelle pour les différentes fonctionnalités de BaseX. On peut l'utiliser pour créer de nouvelles bases de données, réaliser des requêtes ou explorer interactivement ses données XML.

Après avoir téléchargé BaseX et lancé l'installation, l'interface graphique utilisateur (GUI) peut être lancée de la manière suivante :

- en double-cliquant sur l'icone `BaseX.jar` qui est une archive java exécutable.

D'autres options de démarrage sont également possibles :

- exécuter l'un des scripts `basexgui`ou `basexgui.bat` placés dans le répertoire `bin/`.
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

RMQ : Nota, il est possible d’utiliser le module de visualisation pour montrer les chemins XPath en direct (exploitation pédagogique possible).

Écrire les requêtes en XQuery, le système se charge de l'analyse abstraite des choses. Si on rencontre un problème, alors regarder les questions de performances et optimiser éventuellement la recherche.

Autre manière possible d'optimiser requête :

    `(//item)[1]`

### Script layout

Pour visualiser une sélection d’éléments.
Alors formuler une requête et filtrer les résultats.

Exemple : filtrer la population

    `//country[@population > 1000][name != "China"]`

Il est possible de personnaliser la visualisation, mais c'est compliqué car le module est écrit en java !

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

```xquery
    Module namespace _ = "http…" ;
    Declare function _:_() {
    <html/>
    } ;
```

```xquery
    Module namespace _ = "http…" ;
    declare function _:_() {
    %restxq:path('test')
    %output:method('html')
    <html>
        <form action="test">
            <input …
        </form>
    </html>
    } ;
```

```xquery
    Module namespace _ = "http…" ;
    declare function _:_() {
    %restxq :path(‘test’)
    %restxq :query-param("query", "{$query}")

    %output :method('html')
    <html>
        <form action="test">
            <input name="query" value="{ $query }" />
            <input type="submit" />
        </form>
    </html>
} ;
```

```xquery
    Module namespace _ ='http…" ;
    declare function _:_() {
    %restxq :path('test')
    %restxq :query-param("query", "{$query}")

    %output :method(‘html’)
    <html>
        <form action="test">
            <input name="query" value="{ $query }" />
            <input type="submit" />
        </form>
        <ul>
            for $c in doc('…
            return <li>{ $c/…
        }
        </ul>
    </html>
    } ;


Demo : Realtime Search in a Catalog Data

Propre moteur de recherche.
Intérêt d’implémenter la spécification XQuery full-text. Sans doute des choses pas possible avec XQuery full-text, mais plus proche de la structure des données.
