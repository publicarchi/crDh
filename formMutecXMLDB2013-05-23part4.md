Formation BaseX, speech n° 4, RESTXQ : Construire des Applications Web
===============

[cf. diapos "05 Web Applications.pdf]

### Les applications web

De plus en plus d’applications sont aujourd’hui entièrement basées sur les technologies du web. Précédemment sur le bureau, mais de plus en plus web, le plus souvent basées sur l'utilisation de JavaScript, HTML5. Il manque la possibilité de travailler directement avec XML.

Une telle approche présente plusieurs avantages, elle permet notamment de tirer parti de l'_ubiquité_ des navigateurs web qui fonctionnent sur la plupart des plate-formes modernes.

De nombreuses applications sont aussi construites sur des _sites web_ et des _services web_.
Les technologies populaires côté serveur sont plutôt PHP, Python, Ruby on Rails, ASP, JSP.

Ici l'utilisation de XQuery peut s'avérer pertinente. D'une part HTML c'est du XML. Les contenus textuels sont souvent _délivrés nativement_ en XML. Dans les langages de script et orientés objet, les données sont transformées de manière répétées depuis et vers XML.


### Le paradigme REST

REST : Representational State transfer

REST est un paradigme de programmation pour les applications web. Il est basé sur la [thèse de Roy Fielding de 2001](http://opikanoba.org/tr/fielding/rest/) (un des auteurs de la spécification http).

REST repose sur cinq principes
- Chaque service REST dispose d'une _adresse unique_ (qui est l’URI)
- Un service peut retourner _différentes représentations_ de la ressource adressée XML, JSON, etc.
- Les services REST sont dits _sans états_ (_statelesss_) : chaque requête contient toutes les informations qui permettent de comprendre un message.
- Les services doivent supporter _un ensemble défini d'opérations_ (HTTP: GET, POST, etc.)
- L'utilisation de l'hypermédia : on utilise les liens pour changer d'état l'application


### RESTXQ : Des applications RESTful avec XQuery

RESTXQ est une proposition de normalisation présentée en 2012 par Adam Retter à la conférence Prague XML.

Motivation
Pas de std pour XML et XQuery pour des services web (web capability)
Les extensions HTTP/web sont spécifiques aux vendeurs et de ce fait non portables

Solution
La solution proposée est inspirée de la stardisation de l'API JAX-RS
Elle utilise un ensemble prédéfini d'annotations faisant correspondre des fonctions XQuery à des requêtes HTTP
XQuery génère et retourne ainsi des réponses HTTP


### Les annotations RESTXQ

Les annotations RESTXQ utilisent l'espace de nom prédéfini : http://exquery.org/ns/restxq
Avec BaseX cet espace de nom est lié au préfixe 'restxq' et toutes les fonctions XQuery doivent être contenues dans un module de bibliothèque (_library module_)
cf. http://docs.basex.org/wiki/RESTXQ

#### Chemins

- Une fonction ressource RESXQ doit avoir une seule annotation de chemin qui reçoit une simple chaîne de caractères comme argument pouvant contenir des segments de chemin (_path segments_) et des motifs (_templates_)
- **un motif** ('template') contient une variable entre accolades ; ses valeurs sont assignées aux arguments correspondant de la fonction XQuery
- la fonction sera évaluée si une requête HTTP correspond au chemin

Cet exemple contient une annotation de chemin avec un simple segment de chemin :

```xquery
    module namespace _ = 'http://dbis.uni-konstanz.de/';
    declare %restxq:path("/main") function _:main() {
        <html>
            <h1>Welcome to this start page</h1>
        </html>
        };
```

L'exemple suivant utilise un segment et un motif :

```xquery
    (: ...omitting the module namespace... :)
    declare %restxq:path("/search/{$name}") function _:search($name) { "Specified name: " || $name
    };
```


### Méthodes http

Équivalent des méthodes de requête HTTP excepté pour TRACE et CONNECT :
GET, POST, PUT, DELETE, HEAD, OPTIONS

Une fonction ressource peut avoir _zéro ou plusieurs_ annotations de méthode :

```xquery
    declare %restxq:DELETE
            %restxq:path("/")
    function _:root($name) { "You have specified the root path and the DELETE method."
    };
```

Si aucune méthode n’est spécifiée, la fonction sera invoquée pour toutes les méthodes.
Les annotations de méthode POST et PUT peuvent prendre une chaîne optionnelle comme argument.

```xquery
    declare %restxq:PUT("{$data}")
            %restxq:path("/upload")
    function _:up($data as xs:base64Binary) {
        file:write-binary('/tmp/' || prof:current-ns(), $data), "Uploaded!"
    };
```


### Types de contenu (_content types_)

Une fonction peut être restreinte à un type de contenu ; elle ne sera invoquée que si le header _Content-Type_ de la requête correspond au type spécifié :

```xquery
    declare %restxq:consumes("application/xml", "text/xml")
            %restxq:path("/whatever")
    function _:_() {
        "The specified content type header is either application/xml or text/xml."
    };
```

### Accept

Une fonction peut être restreinte à une entête (_header_) Accept :

```xquery
    declare %restxq:produces("application/atom+xml")
            %restxq:path("/whatever")
    function _:_() {
        "The specified Accept header is application/atom+xml"
    };
```

### Paramètres de requête (_query parameters_)

L'URI d'une requête HTTP peut contenir une chaîne de requête (_query string_), qui est habituellement résolue sous forme de noms/valeurs. (e.g. www.bing.com/search?q=search+terms).

Une annotation de paramètre de recherche prend deux arguments ou plus :
- le premier argument contient le nom du paramètre de requête
- le second argument contient le nom de la variable à laquelle elle doit être liée
- les arguments restant seront liés à la variable si la requête HTTP ne contient pas de nom correspondants :

```xquery
    declare %restxq:query-param("q", "{$terms}")
            %restxq:path("/search")
    function _:_($terms as xs:string*) {
        "The following terms were specified in the query:" || $terms
    };
```

Remarquez que le nom d'une variable peut être spécifié plusieurs fois.


### Champs de formulaires HTML

Des paramètres de formulaires peuvent être passés lorsque la méthode POST est utilisée.
En RESXQ, leurs valeurs sont extraites aussi bien des requêtes GET que POST.
La syntaxe est la même que pour les paramètres de requête :

```xquery
    declare %restxq:form-param("q", "{$terms}")
            %restxq:path("/search")
    function _:_($terms as xs:string*) {
        "Specified query terms:" || $terms
    };
```

Un snippet HTML gèrant la requête pourrait prendre la forme suivante :

```xhtml
    <form action="http://localhost/search" method="post">
        <input type="text" name="q">
        <input type="submit" value="Suche">
    </form>
```

### HTTP Headers

Une requête HTTP peut également contenir des informations utiles qui peuvent être liées à des variables de la manière suivante :

```xquery
    declare %restxq:header-param("User-Agent","{$agent}")
            %restxq:path("/check-agent") function _:_($agent) {
                "You are using '" || $agent || "' as browser/crawler."
            };
```


### Paramètres de cookies.

Il est également possible de lier des cookies à des variables :

```xquery
    declare %restxq:cookie-param("User-Agent","{$agent}")
            %restxq:path("/check-agent")
    function _:_($agent) {
        "You are using '" || $agent || "' as browser/crawler."
    };
```

### Sorties (_Output_)

Par défaut tous les résultats sont retournés avec `application/xml` comme type de contenu (sononymes : mime type, media type).
Le type de contenu peut être surchargé au moyen de paramètres de sérialisation, qui seront liés au prefix `output` :

```xquery
    declare %output:media-type("text/plain")
            %restxq:path("")
    function _:_() {
        "KISS (or: keep it simple, stupid)"
    };
```

Le type peut aussi être modifié en spécifiant une autre méthode de sortie :

```xquery
    declare %output:method("html")
            %restxq:path("")
    function _:_() {
        <html><body>Finally.. Some HTML</body></html>
    };
```

On peut encore spécifier d'autres paramètres de sérialisation comme par exemple pour générer du XML et des déclarations de type de document :

```xquery
    declare %output:method("xhtml")
            %output:omit-xml-declaration("no")
            %output:doctype-public("-//W3C//DTD XHTML 1.0 Transitional//EN")
            %output:doctype-system("http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd")
            %restxq:path("")
    function _:_() {
        <html xmlns="http://www.w3.org/1999/xhtml">
            <body>You have just created some valid XHTML output!</body>
        </html>
    };
```

Fonctions pour le doctype, etc. qui ne peuvent être produits en XQUery


### Redirections

Quant on utilise des requêtes de mise à jour (_updating queries_, il est souvent utile de rediriger le navigateur vers une autre page qui indique que la mise à jour a bien été effectuée.

Ce mécanisme n'est pas prévu dans la norme, mais BaseX fournit deux solutions :
- si un élément `restxq:redirect` est retourné, un client sera redirigé vers l'URL spécifiée comme nœud texte. This usually triggers another
- si un élément `restxq:forward` est retourné, le serveur appellera directement la page demandée.

Le dernier exemple suivant génère donc une boucle sans fin :

```xquery
    declare %restxq:path("/loop")
    function _:loop() {
        <restxq:forward/>/loop</restxq:forward>
    };
```

### Divers

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
