# cr Guy Lapalme 12 octobre 2017

## Classes de RDFS et RDF

Classes fondamentales

- rdfs:Resource
- rdfs:Class
- rdfs:Literal, rdf:XMLLiteral
- rdfs:Property
- rdf:Statement

Relations

- rdf:type
- rdfs:subClassOf
- rdfs:subPropertyOf

Type et liens entre les propriétés et des classes

Pour les propriétés

- rdfs:domain
- rdfs:range

Propriétés pour la réification  Statement, subject, prédicateur, object

Container

- rdf:Bag, rdf:Seq, rdf:Alt
- rdf:List, rdf:first, rdf:rest
- rdfs:Container, rdfs:ContainerMembershipProperty, rdfs:member

Autres propriétés auxiliaires (documentation pour les humains, pas de sémantique associée)

- rdf:seeAlso (lien vers une autre propriété qui l’expliqque
- rdfs:isDefinedBy
- rdfs:comment
- rdfs:label

## D’où viennent les URIs ?

Les **URIs devraient être non ambigues**. C’est-à-dire qu’elles devraient toutes être utilisées de manière unique. De manière à pouvoir faire des liens entre les choses, concepts définis une seule fois. Mais ce principe est assez difficile à appliquer.

**URIs, de vocabulaires prédéfinis**. Il existe des vocabulaires qui ont été définis et que tout le monde réutilise.

Par exemple ce qui a été défini dans RDF, c’est un vocabulaire prédéfini. 

http://www.w3.org/1999/12/22-rdf-syntax-ns#Description

Mais aussi FOAF, un des premiers définis (milieu des années 90)

http://xmlns.com/foaf/0.1#homepage

- définie des relations entre personnes
- pas un vrai standard mais très utilisé
- assez commun pour éviter la confusion

Dans un fichier on renseignait un certain nombre de champs. 

## Comment créer de bons URIs ?

Si existe déjà des vocabulaires, réutiliser des choses existantes. Mais sinon, on peut créer des URIs. Une URI ce n’est qu’une chaîne de caractères

- Utiliser un schème existant http: tel: isbn: issn:
- Utiliser un URI inutilisé ailleurs en se basant sur la structure hiérarchique des URLs. Par exemple en choisissant un domaine qui vous appartient et en essayant d’être consistant avec soi-même. C’est ce qui explique que souvent les URI ressemblent à des URLs.
- Distinction entre une page Web et ressources abstraites
  - qui est l’auteur de http://en.wikipedia.org/wiki/Othello

Un URL est toujours une chose concrète. Supposons que nous avons cette page Wikipédia. Si demande qui en est l’auteur, parle-t-on de la page web ou de la pièce Othello. Il faut donc distinguer les sujet dont parle la page web de l’auteur.

Pour s’en tirer, il peut être commode d’avoir des URIs concrets. Pour séparer les choses, on va tenter d’avoir deux URIs apparentés qui différentie la page web et ce dont va parler la page web.

### Utilisation de fragments

Une manière de faire est de rajouter des fragments #xxx

Le concept l’ensemble de l’URIs, mais permet d’indiquer la page où est décrit le concept.

Une autre façon, donner une page et décrire des fragments qui n’existent pas dans la page. Pas d’ambiguïté car des chaînes de caractères uniques. L’avantage de fournir si on veut une description. Les URIs sont arbitraires mais intelligent que l’URI puisse être résolvable.

Voilà une des façons de décrire la page et de séparer le concept de la page.

Une autre manière de faire, plus compliquée car elle nécessite d’avis accès à la configuration du serveur, cette façon de faire consiste à pouvoir faire des redirections en fonction du client.

### Redirection d’RUL dans un serveur

L’agent va s’identifier, et le serveur, en fonction de l’information va retourner de l’information différente. Par exemple pour un concept dans DBPedia, celui-ci est accessible à un URI qui parle de la ressource. Lorsque demande de l’information sur la ressource, le serveur s’il identifie que la requête vient d’un browser web, renvoie la page HTML. Si s’aperçoit qu’une requête d’un client informatique, renverra du RDF.

- http://dbpedia.org/resource/Montreal
- http://dbpedia.org/page/Montreal
- http://dbpedia.org/data/Montreal

## Applications de RDF

### Dublin Core

Dublin Core est en quelque sorte la métaphore des bibliothèques. L’idée est de décrire des documents en vue de leur indexation. Plusieurs versions. La première définit 15 propriétés.

Dublin Ohio, conférence à laquelle on a définit les bases de ce vocabulaire. L’idée était de s’entendre sur 15 propriétés génériques suffisantes pour décrire toute sorte de contenus sur le web.

Le Dublin Core peut s’exprimer en RDF.

L’espace de nom de Dublin Core, souvent préfixé dc est http://purl.org/dc/elements1.1/

Une application simple de RDF qui a l’avantage de pouvoir être utilisée pour l’interopérabilité sur le web.

Ensuite ajouté dcterms qui offrent une description plus fine. http://purl.org/dc/terms/

Un cas où l’on décrit une ressource, remarquer que le document ici n’est pas présent, il s’agit seulement de métadonnées.

### DBPedia

Extraction de l’information structurée de Wikipédia (infobox)

Disponibilité de la communauté

exprimée sous forme de triplets.

- 13G triplets RDF dans la version d’avril 2017 (donnée d’octobre 2016)
  - 1,7 G extraits de wikipédia anglais
  - 6,6 G extraits de wikipdédia autre langues
  - 4,8G extraits de Wikipedia commons et Wikidata


- 9G triplets en NLP Interchange Format (NIF)
- 128 versions localisées
- 25M liens à des images
- 30M liens à des pages web externes
- 50M liens à d’autres sources RDF

Wikidata des données directement produites sous forme de données, pas une extraction.

Les triplets NLP sont des triplets extraits du texte des pages à partir d’un moissonnage du texte. Mais du texte brut. Effort de normalisation pour faciliter le traitement.

Seulement pour l’anglais, 6,6M d’entités dont 1,9 avec des coordonnées géographiques, 1,5 personnes, 840 000 endroits, 139 000 albums de musique, etc.

Particularité, couvre tous les domaines, évolue automatiquement avec Wikipédia. Multilingue, Interrogeable avec SPARQL comme par ex trouver toutes les villes au New-Jersey de plus de 10 000 habitants, trouver les musiciens italiens du 18e siècle.

Organisé par la Universität de Leipzig puis Freie Universität Berlin. OpenLink Software (Burlington, USA). Supporté par la CEE Aligned-Software and Data Engineering.

Infobox : information structurée exemple Montréal. Surtout l’information qui se trouve dans les infobox.

La production de DBPedia n’est donc pas un travail trivial.

DBpedia data set identification des information.

Le principe de base est qu’il y a une correspondance directe entre les URIs du wiki et l’information correspondante dans DBpedia.

Y trouve des informations de base fournies sous la forme de triplets, comme des étiquettes, un résumé (souvent en anglais) long et cours, un lien à la page Wikipédia, et un lien à une image.

Pour les autres informations, on utilise diverse classifications

- catégories Wikipédia (vocabulaire SKOS)
- classification Yago (combine WordNet et WP)
- liens vers les Synsets de WordNet (dictionnaire où mots liées à des synonymes)
- aujourd’hui nouvelle ontologie dbo (DBpedia ontology)
- Données des Infobox
- liens externes
  - faon:homepage
  - noms de lieux géographiques, de livres, publications
  - coordonnées géographiques

Exemple de description pour la ville de Montréal.

Ontologie DBO

Accès avec SPARQ?person dbo:almaMater dbo:université de montréal

Plusieurs interfaces pour interroger le SPARQL endpoint 

- SNORQL
- Interactive query builder
- etc.
- fonction dessin du graph

des applications construites par dessus DBPedia pour interroger les données.

Création de banques de données de triplets et point d’accès à partir desquels va pouvoir faire diverses choses.

Jeu de données, ou même framework pour extraire l’information de Wikipédia ou contribuer à DBpedia. Infrastructure impressionnante mise en place pour travailler avec ça.

Des applications possibles cf. plateforme LinkedData, des triplets dans de très nombreux domaines qui seront reliés entre eux.

## Comparaison RDF et XML

- RDF est construit par-dessus XML
- XML est un abre, RDF ensemble de triplets
- XML est ordonné, RDF sans ordre
- RDF permet de ne comprendre qu’un sous-ensemble
- RDF est plus facile à interroger
- XML est syntaxique, RDF est sémantique
- RDF permet de déduire
- RDF et Ontologies permettent aux programmes de déduire
- RDF permet de s’abstraire de la syntaxe des documenst
- RDF est plus compliqué et demande une planification
- Pas tous les projets ont besoin de RDF

## Outils de traitement de RDF

Java: Jena (issu des travaux du HP Labs UK, aujourd’hui Apache) souvent la source de nombreux produits (comme Twinkle)

Redland, une librairie qui permet de manipuler du RDF en C, avec interface pour Perl, PHP, Python, Ruby

Semantic Web Development Tools

- http://www.w3.org/2001/sw/wiki/Tools

Voir références dia

#Création d’un vocabulaire RDF

Voir Practical RDF (livre pas bon mais bel exemple)

## Différence entre vocabulaires RDF et XML

L’idée est d’avoir une situation et voudra organiser des données dans RDF

## PostCon

Gestion de contenu annoncé (posted) sur le web pour suivre la vie d’un document.

- titre, auteur, copyright, mots clés (HTML)
- destruction et sa motivation
- remplacement ou déplacement
- durée de vie attendue
- ...

Définition des éléments du domaine et leurs propriétés.

Il s’agit de définir de quoi on va parler, quels seront les éléments et ce que voudra avoir sur cette situation donnée.

La resource de base sera la page web que l’on pourra regarder selon diverses perspectives. Pour chacune des perspectives, va les regarder comment les classer.

- *bio* auteur, propriétaire, date, sujet
- *relevancy* mis à jour, périmé, ?
- *presentation* agent de présentation spécial
- *related* remplacé ? dépend-il d’autres ?
- *history* détruit ? déplacé

On indentifie les éléments du domaine et on les classes.

Ceci fait, va donner des noms. Formalisation des éléments du domaine et des propriétés. 

bio

​	title abstract description dateCreated author owner

Maintenant va pouvoir formaliser cela. Définit des préfixes. Et commence

Dit que page web de type ressource, puis prépare les autres informations avec des propriétés correspondant la formalisation que l’on a faite.

Ensuite va préciser les choses.

Peut commencer à ajouter des choses dans le RDF. Aura ici recours à des propriétés tirées de Dublin Core.

Pour certaines propriétés on peut avoir plusieurs objets.

Pour l’historique en revanche, on s’attend à avoir un certain ordre. Ici on utilisera un Seq.

Une fois qu’on est parvenu à copuler notre système. Va pouvoir formaliser le vocabulaire avec un schéma RDFS.

Pas strictement requis, mais cela garantit qu’un document RDF soit syntaxiquement et sémantiquement consistant à travers les implantations. Ici que définit les éléments du vocabulaires, les Classes, les propriétés, leur portée, domaine.

Lorsque l’on créée un vocabulaire RDFS le plus difficile de penser quelles seront les relations entre nos objets. Pas de meilleure solution, demande une réflexion sur les buts et les objets.

Le plus possible, cherchera à réutiliser des vocabulaires existants.

Possibilité de "validation" avec schéma. Verra mieux ce que cela apporte lorsque l’on ajoutera les mécanismes d’inférence.















