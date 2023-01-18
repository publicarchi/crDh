# Réunion métadonnées Béatrice Joyeux-Prunel, 5 février 2021

## Béatrice Joyeux-Prunel

- IIIF pour accéder images
- CIDOC pour documenter les imaegs

Pb appariements : algorithmes de comparaisons d’images, détection de répliques, détection de similarité des images, classification des images.

Voudrait pouvoir partager les données avec d’autres projets comme NumaPress qui ont déjà des segmentations effectives, etc.

Comment partager nos annotations ou segmentations d’images. Avec CIDOC possible de lier les images comme copies et de rendre des bases de données différentes interopérables. Il existe de nombreux thesaurus en histoire de l’art mais surtout dédié à la description des images mais ne permettent pas de décrire l’ensemble de l’image.

Voudrait pouvoir annoter une main, ou un détail représenté par plusieurs artistes à travers l’histoire de l’art. Quels outils et solution utiliser.

## MAthieu Aubry, école des Ponts ParisTech

Janbrueghe.net (Elizabeth Honig), ~1600 œuvres (petits) mais objectifs limités : voulait pouvoir reconnâitre des motifs.

Un algorithme qui permet de sélectionner un rectangle pour rechercher le détail dans l’ensemble de la base de données. Les détails identifiés peuvent présenter des différences stylistiques. On a déjà donc mis au point un algorithme pour analyser la manière dont le scopies ont été faites (copie précise ou ponctuelle, etc.)

Pourrait être intéressant de pouvoir donner un ensemble de données à l’ordinateur et demander à l’ordinateur ce qui a été répété dans le domaine. Pas une tâche facile à détailler et algorithmiquement pas trop complexe, problème disposer un jeu de données fiables pour travailler.

Papier des RSN, collecte image par hashtag. Groupées par identité visuelle. 

Essayent de transférer à d’autres cas.

Ce qui est plus fonctionnel, analyse documentaire. Reconnaissance de filigranes. Projet avec Shen, Pastorlin, Bounou, Gidaris, Smith, Poncet, Aubry, ICPR 2020.

Semi-succès car pas possible de maintenir l’outil et la bdd. Une application fonctionnelle qui permet de prendre une photo et reconnaître.

docExtractor projet de segmentation de documents. Un algorithmes de segmentation pouvant fonctionner sur n’importe quel type de documents comprendant des images ou des illustrations. Quelque chose qui peut être utile pour nombre d’application. Dévelopé un prototype sur Mirador.

Toujours pb de maintenance. Interface insuffisante.

Nous avons besoin de standards et outils pour pouvoir collaborer entre computer vision et histoire de l’art. IIIF est un bon départ, pas d’outils de visualisation idéal encore, pas de standard pour les groupes d’annotations (nécessaire pour les stocker, pour naviguer parmi ces annotations, pour les éditer avec des historiens de l’art).

## Jean-Philippe Moreux

Sharing Annotations with IIIF : from collections to researchers.

Manière dont IIIF pourrait aider les institutions patrimoniales et les chercheurs à interagir autour de IIIF. Chercheurs commencé à consommer les contenus de nos collections depuis plusieurs années. Fonctionne bien particulièrement dans la dynamique des DH. Beacuoup de réutilisation des contenus, en revanche partage des résultats des chercheurs reste difficile, particulièrement sur les données de transcriptions.

Nous pensons donc que IIIF peut aider les chercheurs à partager des transcriptions. Les bibliothèques peuvent donc exposer plus de métadonnées des métadonnées à travers IIIF. Bibliothèques qui peuvent bénéficier de ces contenus.

Quel type de métadonnées ?

Besoin de nous occuper de métadonnées. Dépend des sources. IIIF peut nous aider à décrire à propos de quoi sont les illustrations, dimensions, etc. Analyser les images à travers des commentaires de chercheurs. IIIF bien conçu pour ces cas avec canvas, layers, annotation list.

Gallicapix.bnf.fr, Deep Learning for Automatic Indexing

Data mining de Gallica, 100% APIs. Preuve de concept pour segmentation. Une webapp en premier et db pour partage des annotations. Utilisateurs de Mirador ou tout outil compliant avec IIIF peut utiliser ces contenus stockés dans GallicaPix.

## Matthew Lincoln

CAMPI : Computer-Aided Metadata for Photo Archives Initiative

Présentation focalisée sur la détection des duplicats.

## Memex, recognising obsects at not so sort distance

Stuart James

## Leonardo Impett, What Interoperability for Computer Vision Labels ? The Challenge of Annotation Standards

Iconclass AI Test Set Arkyves

https://labs.brill.com/ictestset/

Hertiana Buildings Dataset Category 61F (CAMPIDOGLIO)

12 000 images qui restent à nettoyer

Hacking Copyright (Hogarth)

Project avec Cynthia Roman (Yale), Stina Teilmann-Lock (Copenhagen BS), Isabella Alexander (UT Sydney)

Engraving Copyright Act 1734

Gillray d’après Hogarth

Multiplicité des états

## Mathieu Aubry

Computer visions standards et standards des humanités.

Beaucoup de question sur ce qui constitue de bons standards.

CIDOC-CRM venu plusieurs fois dans la discussion. Parfois affirme que difficile à utiliser. Mais Linked Art projet sur usabilité plutôt que complétude. Miriam Posner qui parlait enseignement avec les données, bien que mette à disposition API mes étudiants besoins de CSV. Être sûr que format puisse être fourni dans des formats divers pour l’utilisation.

Rijksdata as an example of providing multiple formats with varying granularity (https://data.rijksmuseum.nl/object-metadata/download/)

Nicola Carboni, des limitations avec Linked Art. Distinguer rôle d’une institution et d’un chercheur. Chercheur ne pourra jamais créer graph à la hauteur de ce qu’une grande institution peut faire. Doit pouvoir penser des manières d’annoter les contenus, et voir comment peuvent être enrichies. Pb conservation, mais préfère quelque-chose plutôt que rien. Web annotation data model très basique (trois partie).

https://www.w3.org/TR/annotation-model/

Stuart beaucoup de dataset competition, Wikidata, dbPedia en CSV. Chercheurs plus besoin de CSV que d’apprendre SPARQL.

Faciliter les cycles de travail pour ramener métadonnées dans des collections. Peut-être pas aux gens du computer vision de ramener des informations muséales. Besoin d’établir les métadonnées pour pouvoir être utilisées proprement.

Nanne contrer le narratif de la simplicité. Fait CV pendant longtemps, vu personnes faire du scrapping, labelling, etc. Un problème de visibilité. Raison pourquoi Wikiart dataset beaucoup utilisé car plus facile à trouver. Travail sur le standard, ne va pas permettre de différentier les modèles.

Pas important avoir modèle de métadonnées si dépôt où met les données à disponibilités sur GitHub.

ICCV tous les deux ans même discussion sur concours. Le plus souvent dataset qui n’est pas public.

HCR aussi besoin de format de métadonnées et de définition de standards pour partage de ground facts. Métadonnées pas forcément plus compliqué, simplifie les choses parfois car pas besoin de se poser la question de comment les données sont structurées.

Thoms Smits : Que voulons-nous que les gens de Computer vision solutionnent comme problème. Humanities people plus servis par solutions qu’ils peuvent appliquer eux-même que de travailler sur des datasets compliquées. Computer vision dataset should be simple et pas aussi compliqué que ce que les gens des DH ont besoin.

Modèle intéressant, celui où met des données quelque part et quelqu’un fait quelque chose. Mais projets les plus intéressant, celui où des chercheurs. 

Intérêt d’avoir un standard simplement possible de pouvoir dire qu’a un problème et proposer à d’æutres de travailler avec. 

Fabian Offert, between et middle ground. Personnes venant différantes communauté. Souvent progrès dans la communauté utilsation choses nouvelles. 

Peter Bell : Bien sûr Matthieu combiner des recherches multidisciplinaires serait gold standard. Mais grande communauté computer vision, et nombre de personnes que peut adresser avec des grands corpus annotés. Nous avons des problèmes très sofistiqués et nous pouvons seuelemnt solutionner quand contrôle gens CV. Responsable d’ouvrir nos données dans nombre de directions et annoter nombre de questions qui peuvent intéresser des gens avec des vues très différentes. Pour comprendre iconographie à plus haut niveau, important de pouvoir amener ces éléments.

Thomas Smits : standardiser les pratiques pas seulement les annotations. Datasheets for dataset qui argumente standardisation des datasets en CV. Aussi ce qu’annote dans un contenu.

## Quel besoin satisfaire

Format spécifique, lieux pour partager.

ML Plein de standards et de formats disponibles, pas besoin ajouter. Ce qui pourrait être utile développer le vocabulaires plutôt que la grammaire. Par exemple pour pouvoir déterminer de quel type d’annotation il s’agit.

Nicolas Carboni. Pb de vocabulaire, enjeu diversité linguistique. Mais nous avons à mon avis d’abord besoin d’une structure.

Benoît aucun des outils annotation fait pour ça. Si pb retrouver visuel, etc. Pb simple, est-ce le même endroit et la même tâche; Opérationalisable.

Besoin de penser à ce que les gens vont faire après. Type information que reçoit différent de ce que peut présenter. Une chose que ne fait pas différentier entraînement de dataset et tester des datasets.

Approches très centrées sur les tâches sont marginales. Trouvera toujours des choses qui ne fonctionnent pas. Mais choses décrites par Leo fonctionne vraiment très bien. Bien sûr questions majeures comme ImageNet, et besoin de corpus art. Mais différence en qualité devient plus petite en fonction du type de tâche que veut solutionner.

paperswithcode https://paperswithcode.com/

Nanne image detection tâche générique. Même pour cette question des distinctions importantes possibles : même images, plusieurs photographies d’une même images, gravue et états, etc.

Leonardo Impett avoir un test set bien défini. Avoir un ensemble de dataset, pouvoir évaluer algorithme sur plusieurs datasets. Quelque chose qui manque pour les DH.

Fabian human in the loop pb, pas des pb qui peuvent être directement solutionnés par les humains.

Matthew Lincoln beaucoup de cela peut être adressé par de meilleures interfaces. Mais système bibliothèque pas de système pour gérer cela.

Image Net 3000 classes différentes, pas seulement millions images. Pour pouvoir travailler besoin d’un coprus.

Stuart James, CV ne définiront pas questions Art history et inversement. Mais peut trouver terrains communs.

Travail challenge sur collections du MET (Nanne)

## Réflexions

Deux comunautés qui n’ont pas les mêmes objectifs. Préférence

Eva Cetinic

