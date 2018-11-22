# SKOS

But de SKOS de pouvoir récupérer des données produites dans différents contextes, et de les unifier pour pouvoir les réemployer dans le contexte du web sémantique.

Le langage respecte de formalisme des ontologies avec choses développées dans d’autres contextes.

Il s’agit d’un standard de W3C.

On y trouve :

- des concepts identifiés par des URI
- des étiquettes avec des chaînes dans plusieurs langues
- des relations informelles entre les concepts
- ...

Cela s’exprime sous forme de triplets. Il existe donc une notation Turtle ou RDF.

voir les exemples.

On va ainsi faire des liens entre différentes ressources. Simplement, un certain nombre de propriétés et de termes auront ici un sens particulier et permettront d’unifier des ressources hétéroclites.

Plusieurs espaces de noms sont utilisés, celui spécifique de SKOS, mais également rdf, rdfs, oïl, dit, faon, ex, ex1, etc.

## Concepts

Plutôt que de parler de classe, on parle ici de concepts. Ce qu’on appelle un concept est ce qu’on appelle une classe ailleurs, mais le terme est plus général. Il peut s’agir d’unité de sens, de choses, etc. qui existent indépendamment de leur étiquette.

On peut ensuite associer à un concept, une manière d’y référer dans différentes langues naturelles.

skos:prefLabel un seul

skos:altLabel synonyme ou abréviation

skos:hiddenLabel pour la machine seulement.

Pas quelque chose qui va permettre de faire des preuves mais plutôt quelque chose pour fédérer des ressources. C’est la raison pour laquelle beaucoup de soin a été mis sur les différentes manières de de désigner un même concept.

## Relation

### Liens hiérarchiques

skos:broader

- du particulier au général
- de la partie vers le tout

Exemple des mammifères en relation avec un autre concept plus général. Pourrait dire que ceci est une sous-classe de cela, mais ici ne parle pas de sous-classe car pas les mêmes contraintes. On sait tout de même que certains concepts sont plus précis que d’autres.

skos:narrower

### Liens associatifs

Il existe aussi des liens associatifs. Mais les liens seront relativement flou.

skos:related

## Documentation

De nombreux éléments définis par SKOS concernent la documentation.

skos:scopeNote

skos:definition

skos:example

skos:historyNote

...

## Schème d’agrégation

Plusieurs utilisations

- représenter un vocabulaire traditionnel

- intégrer des thésaurus ou classification existants

- déclaration skos:ConceptScheme

  ex.

- liaison avec les concepts avec la relation skos:inScheme

ex définit les mammifères les vaches et les poissons et les place dans le schéma thesaurus des animaux.

### Relations entre les schèmes

- correspondance entre schèmes semblables aux relations entre propriétés

skos:exactMatch, skos:closeMatch, skos:broadMatch, skos:narrowMatch, skos:relatedMatch

Peu strict, le 

- réutilisation et extension des schèmes

skos:inScheme

- indexation via d’autres vocabulaires

dc:subject

ex.

SKOS essentiellement des concepts, des relations de concepts, des schèmes qui regroupent des relations et des relations entre les schèmes. Ce qui forme la base de SKOS

## SKOS Advanced

Collections, relations..

## SKOS en action

Modélise les standards de représentation de thesaurus, termes et concepts et leurs relations.

Exemples d’utilisation

- Nations Unies SKOS pour lier information du AGROVOC (UN) et du National Agriculture Library (NAL) des USA. Ne contraint pas à utiliser tel ou tel vocabulaire, comme un dictionnaire entre vocabulaires et une façon de coder les liens entre les deux. Raison pour laquelle les liens ne sont pas très formels.
- Semantic Web Environmental Directory (ancien)

## FOAF (Friend of a Friend)

http://www.foaf-project.org

Ancêtre des réseaux sociaux. Idée de pouvoir regrouper les gens. Hypothèse du petit monde : les 6 degrés de séparation

- la longueur des chemins entre deux personnes dans un réseau social est courte
- expérience classique de Milgram en 1967
- idée qui se retrouve dans plusieurs autres travaux en sociologie, mathématique
- variation sur le même thème 
  - six degrees of Kevin Bacon
  - Erdös number

Approche évolutive pour l’extension d’information. Facilement extensible par n’importe qui.

SKOS approche plus organisée, standardisée par le W3C.