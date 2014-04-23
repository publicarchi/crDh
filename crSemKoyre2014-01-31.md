CR Séminaire volant du centre Koyé, 31 janvier 2014
=================

Introduction d'Alain Bernard
-----------------------

Séance qui prend place au sein d'un séminaire volant dont le but était d'acculturer des collègues du centre et des doctorants aux humanités numériques et aux enjeux en matière d'édition des corpus numériques en histoire des sciences. Peu de doctorants présents malheureusement.

Séance passée pas mal de succès à la fois avec des gens initiés et des étudiants du centre autour des enjeux d'annotation sémantique de corpus hétérogènes comme le corpus Ampère.

Invitation de Stéphane Lamassé qui travaille sur des approches linguistiques de corpus complexes.

Travaille sur l'histoire des mathématiques anciennes, pour lesquelles besoin de techniques d'encodage particulier.

Mercredi prochain 16h-18h, atelier de lecture du centre dans lequel présentation du Read Write Book 2, et ouvrage de McCarthy.


Tour de table
-----------------------

Houssay : Histoire des techniques depuis 2004. Doctorat avec Lilianne Hilaire Perez. Instruments.
Richard Walter : Item
Valérie Burgos : Société d'encouragement industrie nationale et conférences.
Anne-Laure Brisac : éditrice INHA, responsable d'édition numérique.
Emmanuel Chateau
Lou Burnard : Membre fondateur de la TEI. Intervient sur divers projets en France.
Henri Drisier : Paris 8, Maison des sciences de l'homme de Paris-Nord. Corpus oraux méditéranéeens.
Francis Huron ?
Violette Tameskievich ? : Philosophe, chercheur CNRS, épistémologie. Fonds d'archive de philosophie analytique d'Europe centrale que dirige. 60 000 pages scannées. Fonds inexploité pour des raisons géopolitiques et historiques, s'occupe de la numérisation et de la mise en ligne et depuis quelques années, encodage TEI. Travaille par ailleurs sur la problématique des ontologies dans les DH, IHPST
Marco Segala : membre de l'équipe Ampère, historien de la philosophie et histoire des sciences.
Christine Blondel : histoire des sciences.
Aude : ingénieur Ampère
Philippe Pons : Idem
Isabelle Versberger ? : du centre Koyré


Christine Blondel, Autour de l'encodage d'un corpus accessible en ligne, cas du corpus Ampère
-----------------------

### État des lieux du projet

Actuellement un site en ligne en deux parties, la correspondance et les archives, et une partie destinée à un public plus large sur l'histoire de l'électricité avec des vidéos.

Le corpus Ampère, un corpus important puisque les archives numérisées : 53 000 images. 53 publications plus les variantes. 12 000 lettres, et les archives. Documents divers.

Première ANR a permis la numérisation et l'édition de la correspondance aujourd'hui presque terminée avec un enrichissement de la correspondance par la production d'index, l'identification des ouvrages mentionnés, et renvoi sur les ouvrages s'ils existent en ligne. Un enrichissement qui reste encore limité.
Une partie des manuscrits transcrits mais avec un simple éditeur de texte.

L'étape qui vient consiste à exploiter le corpus. Bien sûr important de mettre à disposition des documents en ligne, mais plus important encore de pouvoir les exploiter. C'est là l'objectif de la Nouvelle ANR. Exploiter le corpus, mais aussi mettre au point des outils et des méthodes qui puissent être exploités pour d'autres corpus. Car une ANR beaucoup d'argent et important de pouvoir mutualiser les investissements, la raison pour laquelle aimerait beaucoup pouvoir travailler avec d'autres projets.

Ces outils devront pouvoir offrir des visualisations différentes, en ligne ou en papier des différents types de documents, permettre l'exploitation pour la recherche, ensuite l'enrichissement de ces documents bruts, enfin de pouvoir annoter ce corpus. Notre espoir c'est de pouvoir répondre à diverses questions auxquelles ne pourrait répondre sans avoir conduit ce travail préalable. Mais aussi de susciter de nouvelles questions de recherche. Enfin, de réfléchir à l'élaboration d'une nouvelle notion, de nouvelles modalités, d'édition critique.

Avec le numérique une notion ouverte, open ended. À la fois une chance, mais un danger dont il faut prendre conscience.

Les moyens techniques pour atteindre cet objectif :
- une nouvelle plate-forme
- des transcriptions avec un encodage des documents
- des fonctionnalités nouvelles avec implémentation d'un logiciel d'annotation (envisage utilisation de pundit)

Insister sur le fait que ce type de travail implique une logique de travail collectif, notamment avec les chercheurs.


### Présentation du site web (Maud et Philippe)

Site web qui mettait à disposition des facsimili des manuscrits et donnait accès à des transcriptions réalisées par les étudiants. 50 000 images, envisage transcription de 15 000, 5 000 de déjà transcrites.

Lorsque dispose d'un site avec des images, peut se poser la question de _pourquoi encoder_.

1. Un premier élément de réponse : pouvoir lier le document à l'image en produisant des métadonnées. Permet d'emblée de pouvoir bien documenter le texte que l'on édite et permet aussi de permettre de moissonner le fonds.

2. Le travail d'encodage est également une manière d'enrichir les documents sur lesquels on travaille en _réalisant une intervention éditoriale_ : par exemple pour signaler la structure du document, marquer les changements de ligne, etc. On peut également encoder différents changements éditoriaux, ratures, manques, remplacements, ajouts. Tout en pouvant qualifier ces différents types d'ajout et de bien les documenter. Une intervention éditoriale.

3. Enfin une manière _d'enrichir son document d'un point de vue sémantique_ en encodant des noms de personnes, des dates, etc. Un niveau plus interprétatif même si la frontière pas forcément très claire.

Ces trois exemples montrent que ce travail d'encodage implique de bien comprendre le texte. Exemple récent sur la liste TEI pour la qualification du texte marginal qui n'a pas nécessairement la même valeur et qu'il faut bien identifier pour pouvoir l'encoder. S'agit-il d'une maginalia, d'un ajout, etc.

Dans le numérique, une des perspective possible qui consiste pour les historiens à pouvoir se référer à des référentiels. Nombreux référentiels bibliothécaires, manque de référentiels historiques, les personnages historiques n'ayant pas forcément déjà publié, d'où l'intérêt d'une coalition sur ce sujet avec les archives. L'objectif en utilisant des référentiels avec la TEI consiste également à pouvoir qualifier cette relation et tracer la source.

Autre avantage de l'encodage : de permettre une exploitation du texte encodé. Il devient aisé de conduire des recherches simples ou multi-critères. À partir du moment où on a encodé correctement les noms de personnes, trivial de pouvoir trouver toutes les occurrences de cette personne dans le texte. De même pour définir des recherches multi-critères à partir du moment où s'appuie sur des éléments encodés.

Si une spéculation d'un chercheur sur une annotation interprétative. Est-ce que la recherche peut reposer sur cette note ?
R : Tout dépend de la nature de l'encodage mis en œuvre pour traiter cette annotation. Tout dépend des outils que l'on veut employer. 50 000 images à encoder, ne peut mener à bien l'encodage en utilisant toutes les dimensions de la TEI. Choix des outils à déterminer.

Lou : essentiel de comprendre que l'encodage TEI n'emploie qu'une seule technologie XML, avec un vocabulaire TEI. Les outils dont on se sert doivent seulement gérer cette technologie, permet donc de conduire n'importe quel type de recherche. Le premier commandement TEI, "You shall have no other encoding sheme beside me !".

Dissociation du fond et de la forme qui est importante également. Dans un traitement de texte, peut bien évidemment indiquer qu'un passage textuel est raturé. En TEI également mais le texte restera disponible et il sera toujours possible au besoin de donner accès à la fois au texte final de l'auteur, ou au texte initial en affichant les passages raturés. Avec le même encodage il est donc possible, selon les besoins du lecteur d'offrir un accès à plusieurs vues différentes du texte. La forme la représentation de l'information, le fond le maximum que peut avoir.

Qu'est-ce que l'encodage exactement ?
D'abord quand parle d'un encodage, définir ce qu'est un texte. Un "texte" est quelque chose d'abstrait : la construction d'une communauté de lecteurs. L'encodage explicite cette abstraction afin de la mieux gérer. (cf. Lou Burnard)
Tout document encodé doit respecter __une structuration du document__ qui permet l'interaction homme-machine. Par exemple on parlait tout à l'heure d'une liste d'index, on peut sortir cette liste d'index, parce que les éléments sont encodés. Dès lors que l'information est encodée, on peut lui appliquer toute sorte de traitement.
Un langage à balise permet d'attacher de l'information à une partie (...)
- physique
- éditoriale
- interprétative (sémantique)


#### Qu'est-ce que la TEI (TExt Encoding Initiative) ?

Laurent Romary : "Norme de balisage, de notation et d'échanges de corpus des documents électroniques. Elle s'est élaborée à partir des besoins de structuration, de conceptualisation et de mise en réseau des textes".

Un langage standard et international promu par les institutions (W3C, ANR, HumaNum). Sans doute car XML, bon candidat pour l'archivage pérenne car un fichier XML comme un fichier TEI n'est pas spécifiquement dépendant d'un logiciel particulier pour être ouvert.

Un langage qui est flexible. La TEI propose un jeu de balise étendu (500 éléments), un certain nombre constituant un noyau de base, d'autres à choisir en fonction des besoins. Il est donc possible de puiser dans l'ensemble de ce vocabulaire pour répondre spécifiquement aux besoins d'un projet.

Un cas particulier du langage XML.
XML un métalangage qui donne la grammaire. TEI un vocabulaire qui respecte la grammaire. Mais fait un peu plus que cela car donne une sémantique. Dès lors qu'une syntaxe et une sémantique = une grammaire.
Un certain flou Stéphane Lamassé qui revendiquait que puisse s'exprimer dans un certain code.
Lou : en principe la TEI n'est pas nécessairement exprimée en XML, peut tout à fait imaginer qu'elle soit exprimé dans un autre formalisme technique. En ce sens que constitue un langage, et une sémantique.

XML Un métalangage qui comprend diverses règles pour un langage à balises, tel que la TEI.
TEI précise avec un ensemble de vocabulaire une sémantique qui s'ajoute à ces règles.

Le Langage XML
Une Représentation arborescente
Une sérialisation textuelle
Texte qui doit être compris entre deux balises. Balise ouvrante, fermante.
Choix étiquette : exemple date = ordinateur peut comprendre que ce qui est compris entre les deux balises est une date.
Si ajoute un attribut, alors peut préciser cette date.

#### Du papier à la page

Transcription, etc.
Fac-simile
Travail d'analyse qui dépend de la définition préalable de ce que veut renseigner.
Conventions éditoriales fixées pour l'édition.
Structuration logique du document et éditorial
Aspects sémantiques

Visualisations possibles à partir de cet encodage.
Marquage de la rature
Autre visualisation plus riche, respectant les linebreaks. Feuille de travail pour visualiser les noms de personnes, etc. Plus confortable pour la lecture.

La TEI, un langage en évolution et à évaluer

Pour les mathématiques, encodage en MathML

Balisomanie
L'encodage, une relation étroite entre la taille du corpus, les moyens disponibles. Encodage qui peut paraître léger mais se mettre d'accord en fonction des moyens.

Discussion où se met d'accord sur l'emploi de certains aspects de la TEI. Souhaite contraindre l'utilisation de certains éléments. Cette discussion dans le cours même d'un projet est essentielle même si les choses peuvent être modifiées au cours du projet. Un processus continu d'amélioration des solutions pour baliser les éléments. Pour cela, la TEI propose un vocabulaire spécialisé pour documenter cette manière de baliser. Ce fichier, est un fichier XML, un ODD : "One document does it all". Un document qui fait tout, car fournit à la fois une documentation, un enregistrement de ce que vous avez choisi, et en même temps vous permet de produire un schéma avec lequel vous allez pouvoir valider votre document.

À côté du fichier ODD, peut avoir un manuel d'encodage en langage naturel. Il est possible de relier les deux.
Une étape qui permet d'optimiser le travail aux besoins du projet, et également de contrôler la production des fichiers.

Pour aller plus loin

Guide Pratique Marjorie Burghart
FormationTEI FC
Florence Clavaud, Introduction à l'édition scientifique numérique

Cours en ligne ENC et exemples d'édition

Communauté TEI
Eu besoin d'établir un inventaire sommaire pour établir ce qui correspond à un texte. Définition de l'unité textuelle. Dans une même chemise, des unités matérielles physiques qui ne posent pas de problème, parfois des sous-chemises, ou ensemble qui présentent une identité sémantique claire. Parfois moins évident.

Pour les publications, une liste de publication princeps, et des versions filles pour donner à la lecture uniquement les éditions mères. Mais transcrits seulement le texte princeps et pour le moment pas créé de relations entre le manuscrit et le texte imprimé, ou les différents états du texte.

Museum cas intéressant pour envisager le divorce entre les institutions patrimoniales et culturelles au sens où dépend du MESR. Pour autant, les programmes de numérisation mis en place n'ont pas nécessairement tout à fait pris en compte les enjeux de recherche.
