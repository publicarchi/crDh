Formation Mutec jeudi 23 mai 2013, BaseX
=======================

Programme
-----------

Jeudi 23 mai 2013
Ma première application web avec BaseX
9h30-17h30 (enseignement en anglais)

### Formateurs :
- Christian Grün (Université de Constance, Société BaseX),
- Michael Seiferle (Société BaseX),
- Alexander Holupirek (Université de Constance, Société BaseX)

### 9h30-12h30
- Présentation de BaseX
- Les grandes fonctionnalités de BaseX
- Web Applications: RESTXQ, les services HTTP
- Installation et déploiement de BaseX pas à pas
### 12h30 : Pause repas
### 14h30-17h30
- BaseX Internals (Paramétrage des index, recherche full-text, …)
- Créer des formulaires : BaseX et les XForms
- Exercices pratiques sur les échantillons des stagiaires ou exercices encadrés dans BaseX

### Site web de travail
http://xml-basex.cbp.ens-lyon.fr:8984


Présentation de BaseX
-------------

Équipe de Université de Constance
Marc H. Scholl
Le projet a d’abord débuté comme un travail de recherche sur XSL, etc.
Plusieurs doctorants ont poursuivi leurs efforts de recherche dans le domaine de BaseX.
En 2005, furent écrites les  premières lignes de code Java. BaseX comme système de recherche.

BaseX est également un système open source. C’est quelque chose dont l’équipe est particulièrement fière. Dès les premières publications, il a été décidé de livrer sous licence libre, 100% open source. BSD Licenced XML DBMS. Libre de faire ce que l’on souhaite avec le code du moment qu’en cite la source, y compris l’inclure dans une distribution commerciale.

Il est également possible de rejoindre la communauté BaseX. Celle-ci comporte déjà 250 personnes, il s’agit d’une communauté relativement petite mais grandissante. Intéressant par ailleurs pour eux d’avoir du feed-back, non seulement sur les problèmes, mais également sur la diversité des usages. La communauté XML concerne des domaines très variables, ne pas hésiter à faire part de ses propres utilisations sur la mailing liste, ou même par mail privé.

[L’adresse du projet](http://basex.org)
Le code source, écrit en Java, est quant à lui publié sur [GitHub]( https://github.com/BaseXdb/basex).
Nous-sommes invités à rejoindre [la mailing liste](https://mailman.uni-konstanz.de/mailman/listinfo/basex-talk)

3e domaine depuis 2011, un domaine commercial.
Celui-ci concerne principalement la fourniture de conseil et de formation en technologies XML et XQuery. Conventional software dev. Construire des applications web « in a pure X* technology stack ».

Amélioration de BaseX, sponsoring pour le développement. Évaluation du coût du développement et proposition de sponsoring avec condition de le placer dans le domaine open source. Très bons retours des clients sur cette logique.

BaseX c’est actuellement 3 employés temps plein, et 4 employés à temps partiel. Ils voudraient rester dans cette configuration pour les 5 prochaines années, veulent rester petit.


### Historique

BaseX research depuis 2005
BaseX open source depuis 2007
BaseX commercial depuis 2011

### Objectifs de développement

-	Haute compliance aux standards W3C
-	Implémanetation XPath et XQuery
-	Extensions XQuery Update, XQuery full-text
-	Haute utilisabilité et stabilité
-	Performance, performance, performance !


XQuery
-------------

### Qu’est-ce que XQuery 3.0 ?

- (plus qu'un) langage de **requête** pour des données XML
- (plus qu'un) « conterpart » de SQL
- un **langage fonctionnel**
- **extensible** via des fonctions et des modules utilisateurs.
- Un langage d’usage général ?

Plutôt un "langage de traitement de l’information" (Information Processing Language).

### Les Extensions

- Plein texte
- Fonctionnalités de mise à jour
- Extension de scriptage

### Les Alternatives

- XSLT : des fonctionnalités comparables mais spécialisé pour les transformations
- SQL2005 a tenté de combiner SQL et XQuery

### XQuery comme langage fonctionnel

- exemples prééminent : Haskell, Scheme, OCAMI, R
- basé sur l'**évaluation de fonctions** : une entrée, une sortie
- **fonctions de haut niveau** : fonctions comme arguments
- itération --> récursion

XQuery 3.0 est un langage fonctionnel complet

### Exemples

**Retrouver tous les items :**

    `//item/name`

**Retrouver les items avec l'id=0 :**

    `/item[@id = "0"]` (prédicat)

**Retourner les noms de tous les items, classés par leur date :**

```xquery
    for $i in //item
    order by $i/@date
    return $i/name
```

(on utilise une expression FLWOR)

**Requêtes imbriquées avec { }**

```xquery
    <hits>
        for $num in 1 to 100
        let $name := concat("doc", $i, ".xml")
        let $doc := doc($file)
        for $i in $doc//item
        where $i/price > 1000
        group by $i/city
        return <hit>{$i}</hit>
    </hits>
```

Intéressant car, tandis que l'on processe les données, on peut les retourner en HTML ou une autre construction ou dialecte XML.


Performances
-------------

Un test comme celui de Fibonacci permet d’aborder l’aspect fonctionnel du langage : on ne dit pas à l’ordinateur quelles étapes réliser pour calculer, mais plutôt la définition de ce que doit être un nombre de la courbe fibonacci :

```xquery
    declare function local:fib($n) {
    if ($n <2) the ($n) else (local:fib($n - 1) + local:fib($n - 2))}; local :fib(20)
```

Ce qui équivaut directement à la définition mathématique d’un nombre de fibonacci.

![graphique comparant les performances entre les différentes bases de données XML pour la résolution de problèmes courants en sciences de l'informatique]()

- Tour d’Hanoi (traiter informatiquement le problème de la tour d'Hanoi)
- Courbe Fibonacci (calcul des nombres de Fibonacci (n = 20) :
- Déplacement du cavalier (réaliser le déplacement d'un cavalier sur un échiquier. Author Michael Kay (11 kb)
- Unicode (retourner une liste formatée de tous les caractères Unicode 1.5kb)

Chaque système ses propres forces, rester prudent avec ces comparaisons. Il convient de connaître les aspects spécifiques de chaque système pour choisir entre eux. Par ailleurs, il existe des systèmes open source, des processeurs propriétaires, etc.
MarkLogic est un acteur prédominant. Le domaine open source est plus petit. Sans doute intérêt à se mettre ensemble dans le domaine de l’open source

[RESTXQ](http://docs.basex.org/wiki/RESTXQ), une proposition de spécification en 2012 à XML Prague sur la manière dont les implémenteurs pourraient baser leur implémentation de bases de données XML en REST. Une solution déjà implémentée dans BaseX ou eXist. Alors, pourrait passer d’un système à l’autre en conservant l’architecture générale du système.


Usability
-------------

### L'interface graphique utilisateur

Usability très importante pour BaseX. Marc H. Scholl initialement issu de la recherche sur les interactions homme/machine. Le projet de recherche consistait d'abord à montrer qu'il était possible de naviguer et d'explorer facilement de grandes masses de données XML.

D’abord conçu comme une fonctionnalité de démo, mais développé par la suite.

L'inferface graphique utilisateur (Graphic User Interface GUI) qui utilise la visualisation interactive, pour formuler des supposition et explorer la base de données.

Visualisation en arbre, en points, en tableau.
Mise en lumière des "matchs" lors de la formulation des requêtes, en temps réel

Un éditeur XQuery intégré

### La visualisation en arbre

Visualisation pour donner une meilleur perception des données.
Vue en arbre des données.
Une sensation spatiale, et une visualisation.
XML est une structure hiérarchique. Ici, chaque bloc affiche un nœud de l’arbre. Présentation de la structure des sous-arbres.

### L'éditeur  XQuery

Un éditeur XQuery intégré où l'on peut requêter ou programmer les données.

Ex. pour toutes les villes dans la base de données qui sont dans l’élément ville, retourner, etc.

On peut visualiser les "matchs" directement dans la visualisation. Et on peut accéder à la localisation directement en cliquant sur le nœud.

### Des extensions personnalisées

Ex. d’un projet de personnal management. Sur une machine possible de penser traiter les informations des métadonnées des fichiers sur un ordinateur. XML [FSML File Structure Markup Language](http://fsml.sourceforge.net). Écriture d’un outil, et représentation graphique avec thumbnails


La production d'applications
-------------

Situation de départ :
Il existe plein de manières différentes de produire des applications.
Mais si l'on dispose d'informations proprement encodées en XML,  avec une bonne sémantique, des contenus mixtes, alors c'est peut être une bonne idée de faire le choix d’utiliser des technologies XML pour traiter ces données.

Ici, un scénario de "personnal management". Nous avons un fichier de métadonnées pour chaque fichier vidéo.

Dès lors que toutes nos données sont encodées avec XML, alors, ce n'est pas seulement XML qui est disponible, mais également XForms, XSchema, XQuery, XSLT, XQuery pour supporter la construction de votre application. Pourquoi ne pas les utiliser ?

Nous allons voir ce que signifie ces technologies de domaines avec XQuery à partir de l’exemple de [XForms](http://www.w3.org/MarkUp/Forms/).

[XForms](http://www.w3.org/MarkUp/Forms/) est un standard pour la génération de formulaires électroniques.
Tous les widgets de formulaire fonctionnent sur le même modèle de données XML, de manière synchronisée et directement couplée avec le modèle de données.

C'est le modèle de données XML qui fournit des informations :

```xml
    <xf:model>
        <xf :instance>
            <... />
        </xf:instance>
    </xf:model>
```

On a alors la possibilité déclarer un formulaire de sortie qui serait connecté au modèle de donnée, de même pour le formulaire d’entrée.
Pré-remplis car directement connecté au modèle.
Possibilité d’updater directement le contenu dans le modèle de données. Cela, sans écrire une seule ligne de code en javascript.

**Modèle de données XML :**

```
    <xf:model>
        <xf:instance>
            <file name="05_Like_A_Rolling_Stone.mp3">
                <metadata>
                    <title>Like A Rolling Stone</title>
                    <artist>Bob Dylan</artist>
                    <composer>Bob Dylan</composer>
                    <album>Greatest Hits</album>
                    <track>5/10</track>
                    <recording_date>1965-06-21</recording_date>
                    <genre>Folk</genre>
                    <encodedby>iTunes 8.0.2</encodedby>
                </metadata>
            </file>
        </xf:instance>
    </xf:model>
```

**Formulaire de sortie :**

```
    <xf:output ref="//title">
        <xf:label>Le titre actuel est :</xf:label>
    <xf:output>
```

**Formulaire d'entrée :**

```
    <xf:input ref="//title">
        <xf:label>Changer le titre pour :</xf:label>
    <xf:input>
```

Ici, on se contente de décrire ses formulaires de manière déclarative : à quoi ils doivent ressembler et comment ils doivent coopérer. De même, pour les widgets d’entrée. Pas seulement les entrées textuelles, mais aussi les menus déroulant, les boites à cocher et le calendrier.

Passage au code source.
Tout en HTML (plain html) : un peu de javascript seulement pour le stylage. Cependant, ce sont des éléments xform spécifiques qui déterminent les données XML chargées par le formulaire, une déclaration de type à partir des types XML Schema, et une déclaration du comportement.

Le formulaire lui-même essentiellement du XML, hormis les éléments `xf:`  pour déterminer le rendu du champ.

On peut également switcher automatiquement d’un formulaire d’entrée à un formulaire de sortie. Ainsi, selon les droits d’un utilisateur on peut directement proposer l’accès à la mise à jour des données.

Question : Xform est une recommandation d’implémentation. Ce que vous montrez dans le browser, une implémentation du browser ou un rendu de votre application web qui implémente XForm ?

Réponse : Ici, pour la démonstration un fichier directement chargé dans le browser. Mais une XSLT qui renvoie à une implémentation qui est un moteur de rendu XForms (xsltforms). C'est ce moteur qui prend en entrée un dialecte XForms, et dans cette approche, laisse XSLT travailler dessus pour produire le HTML et le JavaScript qui sera ensuite interprété dans le browser.
C'est l'implémentation d’Alain Couthures (un français) qui est employée pour faire ce travail. Fondé sur le moteur de rendu XSLT 1.0 natif des browser, le traitement n'est donc pas forcément très rapide. Cela Oblige à faire des sous-formulaires pour les gros formulaires, ou à modérer la taille des formulaires. Nous montreront des trucs pour contourner ce problème.

[Liste des implémentations de XForms selon le W3C](http://www.w3.org/community/xformsusers/wiki/XForms_Implementations)

L’exemple de la démo présenté utilise [XSLTForms](http://www.agencexml.com/xsltforms) qui est une implémentation dans le browser (française), open source. Ici, le client qui fait la transformation.

[Une implémentation côté serveur par Marklogic](http://www.betterform.de/en/index.html) existe également.

Dans la démo rien n’est exécuté côté sur le serveur. Mais surtout ici, on reste dans son domaine XML : il est donc assez naturel d’utiliser Xforms plutôt que d’avoir à utiliser Javascript, etc.


### Une solution stratégique générale

**Une stratégie de solution générale qui consiste à utiliser les standards établis en se basant sur une pile technologique consistante et uniforme**

XML, XSLT, standardisés ISO, sont donc également ici pour durer.

```
   SQL
  NoSQL             persistence           XML
 XML Database           |                  |
    |                   |                  |
   PHP                  |               XQuery
   Ruby			  Business Logic       XML schema
    …                   |                  |
    |                   |                  |
   HTML	           Presentation		    XForms
                                         XHTML
```

[XRX (web application architecture)](http://en.wikipedia.org/wiki/XRX_(web_application_architecture))
" Dans le développement logiciel XRX est une architecture d'application absée sur XForms, REST et XQuery. Les applications XRX gèrent les données à la fois du côté du client web et du serveur web dans un format XML et ne nécessitent pas de conversions de formats de données. XRX est considéré comme une architecture d'application simple et élégante du fait du nombre minimal de conversion nécessaire pour transporter les données entre le client et le système serveur. L'architecture XRX est également très étroitement couplée aux standards du W3C (CSS, XHTML 2.0, XPath, XML Schema) pour assurer aux applications XRX une robustesse dans le temps. Comme les applications XRC sont basées sur des langages déclaratifs modernes côté client et des langages fonctionnels côté serveur, elles sont conçues pour être facilement appropriable par des non-dévelopeurs qui ne sont pas familiers des langages impératifs traditionnels tels que JavaScript ou .Net. "

L'utilisation de XForms et de XQuery avec une base de données XML native permet de réaliser toutes les opérations Create/Read/Update/Delete (CRUD) ainsi que la recherche, sans middleware. "The result is increased simplicity" (Erik Buchez, XForms and eXist : A Perfect Couple, novembre 2007)

**Références sur XRX :**

- [Dan McCreary. "XRX: Simple, Elegant, Disruptive". _XML.com_, 2008.](http://www.oreillynet.com/xml/blog/2008/05/xrx_a_simple_elegant_disruptiv_1.html)
- [Dan McCreary. "Introducing the XRX Architecture". _Dr. Data Dictionnary_, 14 décembre 2007](http://datadictionary.blogspot.fr/2007/12/introducing-xrx-architecture.html)
- [XRX Wikibooks](http://en.wikibooks.org/wiki/XRX)


**Références sur XForms :**

- [XForms pour les développeurs HTML (Version de travail)](http://www.xforms.fr/)
- [The Forms Working Group (W3C)](http://www.w3.org/MarkUp/Forms/)


Dans une architecture classique, passe des tuples vers php puis Html. Avec XML, on reste sur le même modèle de données. Il n'y a pas de conversion, de l’arrière à la visualisation, on deale avec le même modèle de données = "uniform technology stack".


### Le paradigme Model View Controller (MVC)

Le **modèle** qui est XML Schema,
Le **contrôleur** qui est XQuery,
La **présentation** qui est XHTML.

### Exemples de réalisations

[Lindau Nobel Laureate Meetings](http://www.lindau-nobel.org/) Réunion annuelle, rencontre entre nobel et jeunes chercheurs. Prospective. Conference de réseau.

[Alumni-Portal](http://www.alumniportal-deutschland.org) powered by XQuery. Une web Application implémentée avec tous ces standards.

Évidemment le site ressemble à une application conventionnelle. Mais dans la barre d’adresse, on peut déjà s'apercevoir que l’on utilise REST.

L'architecture générale consiste en une application web qui propose des services, des formulaires, etc. Côté serveur (servelt : cookies, sessions, templating), puis DB client BaseX

Le contrôleur prend en input une valeur déterminée par l’url. Prend un template comme input supplémentaire, traité par XQuery, puis le résultat renvoyé au client. Dans le principe, pas crucialement différent de PHP, simplement on utilise des langages différents. Et selon les cas, opérations XForms, soit côté serveur, soit côté client.


Client				Appli			Serveur
GET ou POST						BaseX
				+template


**à voir :**
- [RESTXQ](http://docs.basex.org/wiki/RESTXQ)
- [XRX (web application architecture)](http://en.wikipedia.org/wiki/XRX_(web_application_architecture))


