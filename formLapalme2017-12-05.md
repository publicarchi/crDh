# Cours Lapalme 5 décembre 2017 : Conclusion Linked Data - Topic Maps

## Linked Data ou Web of Data

### Qu’est-ce que le LOD

- Mise en relation de données sur le web
- À partir d’une donnée, on accède à d’autres

L’idée du Linked Data est de faire un web de données. Elle est partie de l’idée que l’on parle souvent de différents types de données, et de données ouvertes. 

Idée avancée par Tim Berners-Lee en 2006 qui associe une notation en étoile en fonction du type de données que publie.

Les qualités publiées sur le web peut être très différente :

- données sous licence libre
- données explicites et structurées
- format non-propriétaire
- URIs pour sujets et objets
- données liées à d’autres données

Les données présentes sur le web sont de toute sorte, mais pour que celles-ci soient utilisable, il faut respecter un certain nombre de critères. L’idéal étant d’avoir des données liées.

Le principe du Linked Open Data (LOD)

- URIs pour nommer les choses
- HTTP URIs pour y référer
- Lorsqu’on réfère à un HTTP URI, retourner de l’information utile en RDF
- Lier les données

Évolution du LOD depuis 2007

LOD qui a débuté par un ensemble de données publiées entre elles : DBPedia qui a constitué le centre, Geonames, projet Gutenberg, bases de données bibliographiques, FOAF, Musique. 

Ce nuage de données a connu une croissance considérable au point qu’aujourd’hui difficile à appréhender dans son ensemble. Il est dorénavant possible de les classer par domaine. Visualisation SVG qui permet d’afficher les liens entre les référentiels.

lod-cloud.net

Lien vers la description de la base de données dans Datahub, une bonne manière d’accéder à l’ensemble du LOD.

### Quoi faire avec le LOD ?

Il existe des browser spécifiques qui navigue le Linked Open Data

- ex Disco (un peu ancien)
- EUCLID un cours qui explique comment construire une application avec du LOD, et quelques exemples d’application

Les premiers à avoir utiliser le LOD de manière systématique, les organismes gouvernementaux car une bonne façon de partager l’information. Data.gov.uk a constitué un modèle dans ce domaine. De même data.gov aux EU. Des données gouvernementales liées et organisées sous forme d’application LOD. De même le Dynamic Semantic Publishing de la BBC qui a rendu toutes ses données disponible. Ou encore Research Space avec les données du British museum, les musées travaillant beaucoup à la publication de leurs données en utilisant ces standards.

LOD pas de programme, seulement des données, mais les personnes qui publient les données.

data.gc.ca existe mais peu de contenu par rapport aux autres pays. Environnement Canada essaye aussi de s’intégrer dans cet environnement.

L’idée évidemment pour utiliser le Linked Open Data consiste à combiner cela avec autre chose, c’est ce que l’on appelle des Linked Data Mashup.

- LDspider qui sert à découvrir de nouveaux liens à partir d’un URI
- il est encore possible de télécharger les données et conserveur leur provenance sur un serveur RDF local avec Jena TDB
- possible d’offrir un service web qui utilise SPARQL sur la base locale RDF

## Quelques idées reçues sur le web sémantique

cf. Le Web sémantique de Fabien Gandon

- WS est une nouvelle version du web
- WS est l’analyse et extraction sémantique du web
- WS se réduit à XML
- WS est l’Intelligence Artificielle sur le web
- Une application WS a forcément un moteur d’inférence
- WS suppose une ontologie universelle
- WS nécessite de grosses ontologies

Pas une nouvelle version du web car beaucoup plus que cela. Le web sémantique peut bénéficier de l’exaction sémantique mais pas nécessairement. Pas réductible à XML car plusieurs syntaxes. Pas de l’IA même si possible de mobiliser la technologie du WS de cette manière. Moteurs d’inférence optionnel. Pas forcément souhaitable d’avoir une ontologie universelle. En tous les cas possible de faire du web sémantique sans nécessairement disposer d’une universelle ni de grandes ontologies.

- Application du WS nécessite forcément une ontologie de ce domaine, pas obligé peut travailler avec RDF sans ontologie explicite
- Ontologie coûte cher, pas nécessairement
- Sur le WS les ontologies se gravent dans le marbre, pas nécessairement car modèle conçu pour des évolutions
- Web 2.0 et WS opposés, au contraire peuvent très bien se combiner
- WS est pour les académiques, oui mais beaucoup d’applications qui fonctionnent
- le WS devrait avoir déjà fait ses preuves, près de 15 ans qu’on en parle, plusieurs cas où déjà fait ses preuves, mais le meilleur reste à faire

## L’état actuel du WS

Quelque chose qui évolue constamment, les standards qui continuent à changer. Ce qui change c’est l’attitude à cet égard, les gens commencent à trouver cela plus naturel. Les industriels ont trouvés des astuces pour commencer à intégrer des idées développées dans le cadre du web sémantique (ex. Schema.org).

Le Web sémantique commence à entrer dans les mœurs. Fait du WS souvent le savoir.

Mais le Réto-ingénierie difficile. Pendant longtemps avait pensé que pourrait prendre les pages web et les analyser mais s’est aperçu que ne fonctionnait pas bien. Lorsque créée les données s’organise pour y introduire de la sémantique au moment de la production.

## Topics Maps

D’autres approches sont cependant possible en dehors du web sémantique. Ne pas vous laisser sans vous signaler qu’il existe un compétiteur qui consiste en une autre façon d’envisager la sémantique que celle que nous avons envisagée tout au long du cours.

L’idée des Topics Maps est la métaphore de l’index de livre

- n’indexe pas tout
- liste des noms de *topiques*
- références aux *occurrences* de ces topiques

Index qui représente en quelque sorte le livre et permet d’accéder à l’information. Normalement si l’index bien fait pas seulement une recherche plein-texte avec l’occurence des mots mais identification des sujets. On a donc des topiques et des références à ces topiques.

Index Complexe comprend

- types de topiques
- types d’occurrences
- références entre les topiques
- sous-entrées

Peut avoir plusieurs types d’index

Les Topics Maps permettent de prendre une collection de documents sur un sujet et de faire des index à partir de ces documents.

C’est un standard international ISO/IEC 13250:2003 Il s’agit d’une extension du concept d’index au domaine de l’information numérique.

Le modèle a deux niveaux distincts

- une carte des connaissances (index)
- ensemble de ressources d’information (contenu)

Définit un espace multidimensionnel

- positions sont des topiques
- distances entre les topiques
- différents types de relations entre les topiques.

*Niveau des connaissances* (knowledge layer)

- **Topiques** : qui sont des sujets (typés?) de l’information
- **Associations** : relations entre les sujets

Dans l’exemple on a des topiques qui sont ici typés : des œuvres, des lieux géographiques et des personnes, ainsi que des associations.

On a ensuite le *niveau des documents*, et on va établir des liens avec les connaissances.

- **Occurrences** : relations (typées) entre eles topiques et les sources d’information.

Par rapport au web sémantique, on a deux niveaux, le niveau de la connaissance et celui des documents. Sur le même jeu de documents, on peut appliquer plusieurs topics maps différents qui pointeraient sur les mêmes ensembles de documents. Il y a donc une possibilité d’abstraire un niveau d’information par dessus les documents.

### Les types

Topics (relation typique de classe-instance)

- noms d’opéras, de lieu, de personnages

Associations

- géographiques, temporelles

Occurences

- articles, mentions, commentaire, image

### Séparation entre Topic Maps et les données

permet de faire :

- les mêmes Topic Maps sur différentes sources
- plusieurs Topic Maps sur les mêmes informations
- fusions de Topic Maps

Pour les fusionner des manières de les nommer.

### Notion de portée (scope)

Buts

- Tenir compte de la *subjectivité* des connaissances
- Exprimer plusieurs *points de vue*
- Donner des *vues* personnalisées pour certains usagers

Au moyen de caractéristiques valides selon un *contexte*

- nom : *Germany* désigne l’Allemagne en Français
- occurrence : dans une portée *technicien*
- association : vraie dans un certain *scope*

Dès lors que les données séparées de l’organisation, alors possible de jouer avec cela.

XML Topics Maps (XTM)

- sérialisation des Topic Maps
  - XTM - version 1.0
  - Standard ISO - Version 2.0
- Compatible avec XML et XLink
- Exemple de Topic Map

sur la musique

### RDF vs Topic Maps

Standards développés de façon indépendantes dans les années 90.

Topic Maps destinés à l’indexation de sources d’information (en Europe du N)

RDF métainformations structurées sur des ressources, base pour l’inférence (aux EU)

Familles de standards

TMCL contraintes cf. OWL pas des contraintes mais pour aider à faire de l’inférence

Topic Maps comme modèle de données plutôt que RDF

XTM, LTM syntaxes RDF/XML, N3

Correspondance avec RDF

Chose : resource en RDF, subject en TM

Symbole : nœuds en RDF, Topic en TM

Assertion : énoncé (statement) en RDF, Topic characteristic assignment

Identité : littéral, URI, Blank mode en RDF, String et URI (address vs id) en TM

Réification : rdf:statement, vs TAO name

Qualification : xml:lang, scope en ™ mais plus général

Types sous types, et merging

Comme guerre entre les deux, conversion ™-RDF

Modélisation de Topic Maps en RDF

- nœud RDF pour les noms, occurrences et associations
- statements pour les types et scopes

Modélisation de RDF en Topic Maps

- définit des Topics pour chaque élément RDF : resources, statement, property, subject, object… mais ne sert pas à grand chose

## Conclusion

RDF et ™ sont deux formalismes concurrents pour le WS avec une puissance d’expression semblable

Sauf que ™ a un peu perdu la guerre, plus grande monde qui l’utilise. Dernières conférences en Norvège.

TopicMaps.org











