# Cours Lapalme

## 28 septembre

cf. http://www.iro.umontreal.ca/~lapalme/ift6282/RDF/

Nous avançons dans la pile des technologies sémantiques. Unicode, XML pour structurer l’information. Maintenant allons voir comment embarquer la sémantique à l’aide du modèle RDF. Ensuite, nous verrons comment introduire de la logique pour interroger les données représentées en RDF.

RDF est un modèle de données pour lequel il existe une stérilisation XML, on va l’utiliser comme une façon de coder le modèle de données même si on utilise de plus en plus d’autres notations plus proches du modèle d’interrogation. On aura donc deux grands types de sérialisation.

RDF est avant tout un modèle de données basées sur des arcs.

RDF a été inventé au cours des années 2000 dans l’idée de pouvoir disposer d’un modèle d’organisation des données. 

RDF signifie Resource Description Format. Resource ici est entendu de manière très très large, il peut s’agir d’un fichier, d’une image, d’une personne, d’un concept qui sont toutes des resources. L’idée sera de donner des identifiants à ces ressources afin de pouvoir les combiner sur le web.

Motivations pour la création du format

- L’idée générale de RDF n’est pas de remplacer XML qui code avant tout les données, mais pour **coder des métadonnées**, il s’agira d’associer des informations à la page web. Le format est donc d’abord destiné à faire du web métadata.
- On voulait également pouvoir **disposer d’un modèle ouvert**. Le format est entièrement connu et standardisé et pas sous forme binaire.
- L’idée était aussi de pouvoir avoir des **métadonnées traitables en dehors de leur environnement de création**.
- Il s’agissait aussi d’être capable de **combiner l’information entre les applications**
- Traitable par la machine

Buts de la conception

- On souhaitait pouvoir disposer d’un **modèle ouvert super simple de données**.
- On souhaitait également pouvoir disposer d’une **sémantique formelle qui permet des inférences**
- Disposer d’une sérialisation XML (même si on dispose aujourd’hui d’autres types de sérialisations) en intégrant les types XML
- Permettre à tous de créer des faits (des contenus)

Il est important de garder en perspective les règles que l’on s’était donné pour partir.

### Qu’est-ce que RDF ?

L’idée est de construire un graphe dans lequel on aura des neuds. Dans un graphe RDF on a deux nœuds et un arc orienté. Dans une déclaration RDF on a un sujet, un objet et un prédicat.

C’est la base du système.

L’astuce est que le sujet est ce qu’on appelle un URI. L’idée est ici de disposer d’un indicateur unique à travers le monde. Celui-ci prend souvent la forme d’une URL. Certains organismes pouvant s’organiser pour créer des URIs, par exemple Wikipédia.

Le sujet est un URI, l’objet est un URI, et le prédicat est un URI. Tout cela peut donc être nommé. L’objet peut toutefois aussi être une constante (un nombre, une chaîne, etc.).

Dans le modèle original RDF 1.0, une constante ne peut pas être sujet. Un choix initial qui a été modifié dans le dernier standard RDF 1.1 qui permet de mettre des constances dans les sujets, mais peu utilisé. Disposition prise car pensait que créerait des problèmes pour faire des inférences.

Quand on veut exprimer quelque chose, on va donc employer des URI pour les sujets et les objets, et avec le prédicat, une URI qui désigne la relation entre les deux.

On peut ainsi déclarer que Marie est l’épouse de Jeanne, sous la forme d’un triplet de trois URI. Comment fait-on ensuite pour créer un graphe ? et bien, le sujet ou l’objet peuvent aussi être le sujet d’autres relations.

C’est donc un modèle très très simple qui permet ainsi de construire les faits. On peut associer les objets à toute sorte de constantes pour des dates, etc. Ces constantes sont des littéraux.

Voici le modèle de base. Ce n’est pas RDF qui a inventé cela, car quelque chose qui est exprimé sous forme sujet prédicat objet, c’est ce qui s’écrit en logique p(S, O), dans le domaine des bases de données, on aura une table de prédicat avec le sujet et l’objet. (Dans la table EpouseDe, les couples dans chaque colonne).

### Les sérialisations

Cette relation de graphe, peut donc s’exprimer de plusieurs manières. 

Elle peut s’exprimer sous forme de graphes exprimés sous forme de prédicat binaires.

Il existe également une sérialisation XML. La description prendra la forme d’un arbre, mais ce que l’on décrit c’est un arc.

```xml
<rdf:Description rdf:about="sujet">
	<predicat>
		<rdf:Description rdf:about="objet"/>
	</predicat>
<rdf:Description>
```

Cette description est plus verbeuse, mais on pourra décrire plusieurs arcs qui ressortent du sujet.

Au cours des dernières années d’autres sérialisations ont été normalisées comme ttl.

```ttl
sujet predicat objet.
```

### Les nœuds vides et relations n-aires

Quelles sont les limitations du modèle ? Pour le moment, les seules choses que l’on peut exprimer ce sont des relations entre deux choses. Or, dans la réalité il arrive que l’on doive exprimer des *relations n-aires*. On va donc faire comme en logique des prédicats, c’est-à-dire que l’on va binariser toutes les relations.

Supposons que nous avons le relatons adresse et que nous voulons indiquer que quelqu’un demeure à telle adresse.

Guy réside à une adresse, dans une province, un pays et un code postal. Il va falloir décomposer l’ensemble des éléments sous la forme de déclarations simples en conservant le lien entre les éléments de l’adresse. C’est ce que l’on appelle une relation n-aire.

On va alors créer des nœuds vides qui sont des nœuds intermédiaires destinés à regrouper des choses. Car la vraie relation est que Guy dispose d’une adresse et que l’ensemble des informations sur l’adresse forme une seule adresse. 

```
guy réside _.
_ aRue Saint-Laurent.
_ aProvince Québec.
_ aPays Canada.
```

Les *nœuds vides* vont être ajoutés au modèle pour être en mesure d’exprimer autre chose que des relations binaires. Les *nœuds blancs* seront des URIs locales au graphe de sorte que l’on puisse reconstruire le graphe. Personne de l’extérieur pourra y faire référence.

Les relations n-aires sont binarisées via des *nœuds vides (blank nodes)*.

### TP

Vous savez maintenant tout sur le modèle RDF qui n’est pas très compliqué. Mais évidemment le diable et dans les détails.

Exemple de graphe RDF pour ce cours.

http://www.umontreal.ca/cours/IFT6282

udem:professeur

foaf:homepage

http://www.diro.umontreal.ca/~Lapalme

foaf:name

Guy Lapalme

foaf:Organisation

Université de Montréal

dc:title

Web sémantique

dc:subject

RDF

dc:subject

ontologie

ajouter les URIs des vocabulaires pour FOAF et DC

On utilise des URIs, des espaces de nom avec des préfixes qui renvoient à des vocabulaires sur lesquels on s’entend pour désigner certaines choses.

FOAF Friend of a Friend, un vocabulaire destiné à faire des liens entre des personnes qui se connaissent. L’idée étant de pouvoir faire des réseaux entre des personnes qui se connaissent. Une version 0.1 restée comme telle.

Permet de coder le nom d’une personne, son organisation, sa page d’accueil, etc. pour décrire les personnes.

Un graphe très simple pour exemple, qui comprend un nœud vide car veut décrire le professeur. Il existe aussi un autre vocabulaire plus spécialisé qui s’appelle le Dublin Core et qui est destiné à coder des informations sur des documents. On retrouve diverses informations comme le titre, le sujet, etc.

Évidemment toutes ces choses là devraient être des URIs, mais voulait que rentre dans ce cadre simple.

Ici bien voir qu’il y a un seul sujet. Le professeur dispose d’un certain nombre de caractéristiques. Ici il y a une relation de sujet directe exprimée en RDF entre le cours et ses sujets. De même le prof dispose d’un certain nombre de caractéristiques.

Le même graphe peut s’exprimer dans une sérialisation XML. Afin de pouvoir être traitable par la machine, nous allons coder ce graphe en XML. On va donc coder tous les chemins à travers ce graphe là.

#### RDF correspondant aux chemins du graphe

On utilise des déclarations de préfixes pour les espaces de nom.

Un sujet commence toujours par Description, l’espace de nom réservé est RDF. Ici on doit construire l’URI au complet. La relation est udem:Professeur

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE rdf:RDF [
    <!ENTITY udem "http://www.umontreal.ca/">
]>
<?oxygen RNGSchema="rdfxml.rnc" type="compact"?>
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:dc="http://purl.org/dc/elements/1.1/"
         xmlns:foaf="http://xmlns.com/foaf/0.1/"
         xmlns:udem="&udem;">

    <!-- cinq chemins à travers le graphe -->
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <udem:professeur>
            <rdf:Description>
                <foaf:homepage>
                    <rdf:Description rdf:about="http://www.iro.umontreal.ca/~lapalme"/>
                </foaf:homepage>
            </rdf:Description>
        </udem:professeur>
    </rdf:Description>
    
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <udem:professeur>
            <rdf:Description>
                <foaf:name>Guy Lapalme</foaf:name>
            </rdf:Description>
        </udem:professeur>
    </rdf:Description>
    
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <udem:professeur>
            <rdf:Description>
                <foaf:Organization>Université de Montréal</foaf:Organization>
            </rdf:Description>
        </udem:professeur>
    </rdf:Description>
    
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <dc:title>Web sémantique</dc:title>
    </rdf:Description>

    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <dc:subject xml:lang="fr">Ontologie</dc:subject>
        <dc:subject>RDF</dc:subject>
    </rdf:Description>
</rdf:RDF>
```

etc. pour chaque relation

#### Combinaison de plusieurs propriétés sur le même nœud

Lorsque l’on a plusieurs relations identiques avec le même sujet comme on est en XML, il est possible d’ajouter plusieurs enfants à la description.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE rdf:RDF [
    <!ENTITY udem "http://www.umontreal.ca/">
]>
<?oxygen RNGSchema="rdfxml.rnc" type="compact"?>
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
    xmlns:dc="http://purl.org/dc/elements/1.1/"
    xmlns:foaf="http://xmlns.com/foaf/0.1/"
    xmlns:udem="&udem;">
    
    <!-- Simplification 1 : Plusieurs propriétés sur le même noeud -->
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <udem:professeur>
            <rdf:Description>
                <foaf:homepage>
                    <rdf:Description rdf:about="http://www.iro.umontreal.ca/~lapalme"/>
                </foaf:homepage>
                <foaf:name>Guy Lapalme</foaf:name>                            <!-- ** -->
                <foaf:Organization>Université de Montréal</foaf:Organization> <!-- ** -->
            </rdf:Description>
        </udem:professeur>
        <dc:title>Web Sémantique</dc:title>                  <!-- ** -->
        <dc:subject xml:lang="fr">Ontologie</dc:subject>     <!-- ** -->
        <dc:subject>RDF</dc:subject>                         <!-- ** -->
    </rdf:Description>
    
</rdf:RDF>

```

Élimination des propriétés vides

Mais écrit comme cela aurait deux nœuds anonymes. Ce que l’on va faire c’est plutôt regrouper toutes les propriétés qui dépendent du même sujet.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE rdf:RDF [
    <!ENTITY udem "http://www.umontreal.ca/">
]>
<?oxygen RNGSchema="rdfxml.rnc" type="compact"?>
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:dc="http://purl.org/dc/elements/1.1/"
         xmlns:foaf="http://xmlns.com/foaf/0.1/"
         xmlns:udem="&udem;">
    
    <!-- Simplification 2 : Enlever les propriétés vides -->
    <rdf:Description rdf:about="&udem;cours/IFT6282">
        <udem:professeur>
            <rdf:Description>
                <foaf:homepage rdf:resource="http://www.iro.umontreal.ca/~lapalme"/> <!-- ** -->
                <foaf:name>Guy Lapalme</foaf:name>
                <foaf:Organization>Université de Montréal</foaf:Organization>
            </rdf:Description>
        </udem:professeur>
        <dc:title>Web Sémantique</dc:title>
        <dc:subject xml:lang="fr">Ontologie</dc:subject>
        <dc:subject>RDF</dc:subject>
    </rdf:Description>
</rdf:RDF>
```

Des mécanismes pour nommer localement des nœuds blancs et y faire référence par la suite.

Intégration des valeurs chaînes comme attributs

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE rdf:RDF [
    <!ENTITY udem "http://www.umontreal.ca/">
]>
<?oxygen RNGSchema="rdfxml.rnc" type="compact"?>
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
    xmlns:dc="http://purl.org/dc/elements/1.1/"
    xmlns:foaf="http://xmlns.com/foaf/0.1/"
    xmlns:udem="&udem;">
    
    <!-- Simplification 3 : intégration des valeurs chaîne comme attributs -->
    <rdf:Description rdf:about="&udem;cours/IFT6282"
        dc:title="Web Sémantique"> <!-- ** -->
        <udem:professeur>
            <rdf:Description foaf:name="Guy Lapalme"><!-- ** -->
                <foaf:homepage rdf:resource="http://www.iro.umontreal.ca/~lapalme"/>
                <foaf:Organization>Université de Montréal</foaf:Organization>
            </rdf:Description>
        </udem:professeur>
        <dc:subject xml:lang="fr">Ontologie</dc:subject>
        <dc:subject>RDF</dc:subject>
    </rdf:Description>
</rdf:RDF>
```

Il existe encore une autre notation plus pratique pour regarder les fichiers RDF, mais c’est la même chose et le même modèle.

Syntaxe RDF Turtle, la traduction du fichier RDF montré tantôt. Ce que l’on écrit ici ce sont des triplets. On a à chaque fois, un URI, la relation et l’objet et ainsi de suite. L’indentation est seulement choisie pour faciliter la lecture.

En insérant un ";" au lieu de terminer par un point, on va pouvoir partager un sujet. Les crochets servent à désigner les nœuds vides. La bonne façon pour partager les nœuds vides consiste à les regrouper.

```ttl
@prefix dc:      <http://purl.org/dc/elements/1.1/> .
@prefix foaf:    <http://xmlns.com/foaf/0.1/> .
@prefix rdf:     <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix udem:    <http://www.umontreal.ca/> .

<http://www.umontreal.ca/cours/IFT6281>
      udem:professeur
              [ foaf:homepage <http://www.iro.umontreal.ca/~lapalme> ;
                foaf:name "Guy Lapalme";
                foaf:Organization "Université de Montréal"
              ] ;
      dc:title "Web Sémantique" ;
      dc:subject "Ontologie"@fr, "RDF" .

# même définition pour toutes les simplifications RDF/XML
```

Virgule qui partage prédicat et plusieurs objets.

Du RDF dans tous les cas, simplement différentes façons de le nommer.

## Éléments de syntaxe Turtle

Turtle (Terse RDF Triple Language), abrégé ttl.

L’avantage de cette notation est qu’elle est plus proche de celle employée dans le langage d’interrogation.

On exprime des triplets, puisqu’un graphe est un paquet de triplet.

La notation la plus longue se compose donc de trois *termes* séparés par des espaces et terminées par un ".".

#### Termes

- Un *terme* pourra être un URI noté entre chevrons `<uri>`
- Un *terme* pourra aussi être un QName (nom qualifié en XML), cad un nom, qualifié par un préfixe : `prefix:nom` où le préfixe a été prédéfini avec une instruction @prefix
- Un *terme* peut encore être un littéral qui est écrit entre guillemets auquel on peut aussi ajouter un type XML. `"littéral"`, ou encore `"2017-09-29"^^xsd:gDate`

On peut aussi exprimer un nœud vide soit avec un préfixe underscore et un id local au fichier _id mais plus souvent en utilisant des crochets ouvrant et fermants.

L’instruction préfixe

`@prefix nomPrefix: <URI> .`

#### Raccourcis

Il existe plusieurs abréviations. Il arrive assez souvent qu’on a des relations qui partagent des prédicats ou des objets.

- La virgule permet de répéter le sujet et le prédicat précédent (on écrit toujours des triplets).

  par exemple : `ex:a ex:b ex:c, ex:d.` ⇒ 

  ​	`ex:a ex:b ex:c.`

  ​	`ex:a ex:b ex:d.`

- Le point-virgule permet de répéter le sujet précédent

  par exemple : `ex:a ex:b ex:c; ex:d ex:e.` ⇒

  ​	`ex:a ex:b ex:c.`

  ​	`ex:a ex:d ex:e.`

Les nœuds vides sont notés avec [ ]

exemple `[ ] gl:p "o" .` peut aussi s’écrire `_:b1 gl:p "o" .`

mais encore `[gl:p "o"]`

#### Exemple shakespearien

Lorsque l’on fait un graph RDF, la première chose à penser, c’est la manière dont on va structurer ce que l’on veut dire.

Ici placé dans des espaces de nom différents ce qui a rapport à la biographie, à la littérature et aux lieux. La structuration des URIs fait partie du processus de conception et traduit la manière dont va construire son monde. Ce faisant, on impose sa vision du monde.

Quand on fait du RDF la première des choses consiste à essayer d’imaginer le graph d’ensemble et de le dessiner pour identifier l’organisation des choses.

Le monde que je veux représenter peut-être codé sous la forme de triplets. On emploie ici des couleurs pour distinguer ce qui a rapport à la littérature, la biographie et la géographie.

On peut encore les noter sous la forme de triplets, les systèmes utilisent ce genre de représentation RDF. La première chose que fait un système c’est représenter les choses dans un format dans lequel peut travailler et créer ses index.

On peut encore sérialiser cet exemple en XML qui est une autre façon de coder la même information.

Regardons maintenant la notation turtle = une codification du graphe que l’on a à côté. On définit un ensemble de préfixe.

Il existe un langage d’interrogation dédié qui s’appelle SPARQL dont l’objet est essentiellement de trouver des motifs de triplets. Pour la pratique, un module de base pour apprendre, twinkle. Choisir celui qui est accessible depuis ma page pour faciliter son utilisation. Ajout de plusieurs éléments.

Aller chercher un fichier RDF et s’assurer que l’on charge le bon graph.