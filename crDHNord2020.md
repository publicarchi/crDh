## Modeling

### Gonthier

Méthods

- Transfer Learning
- Feature visualization

Feature visualisation for art images

- from natural to art images
- training from scratch
- from one art dataset to another

Transfer learning of Deep Learning model trained on natural images has become a de facto method for art analysis applications.

- Replica (Seguin 2019) for visual siilarity search
- ArtPI (Artrendex 2018) for style artist and genre recognition
- Oxford Painting Search (Crowley et al 2018) for semantics recognition of arbritraty objects.

Whar are the effects of transfer learning

Input space, ouput space, a probability distribution entre l’input et l’ouput. Trouver la meilleure fonction prédictive.

Transfer learning, une source additionnelle qui diffère de l’input. Source dataset, nouvelles paires d’exemples d’images et de label.

Regression ou génération. Training set très importants dans ce genre d’approche. 

Image Net.

Rasta dataset, classification style 80 000 images. 1000 classes.

Paintings dataset. Classification 10 types objets classiques. 8 000.

IconArt dataSet 6000 images de différentes périodes. Gonthier et al. Nouveaux benchmarch pour sujets iconographie

Deep Convolutional Neural Network. Convolution layer, activation layer, pulling one. Apprentissage par backpropagation.

Besoin être entraînés sur des millions d’image. Raison pour laquelle utilise transfert learning.

- Off-the shelf feature extraction
- fine tuning
- training from scratch the same architecture

Off the shelf feature extraction, change seulement dernier layers pour avoir bon input. Seul élément qui sera modifié.

Fine tuning, modifie tous les poids. 

Même architecture mais random initialisation.

#### Feature visualization

Feature visualization, consiste à identifier quelles zones images utiles

- optimisation
- Maximal activation images

Images résultant le résultat. Permet comprendre comment forme représentation des images. Côtés, textures, etc.

Rasta car autres pas suffisamment gros pour modifier réseau.

FineTuning meilleures performances. Trainsing from scratch pas même performances.  Off the shelf mauvais résultats. Peut-être cas trop spécifiques, ...

Law levels are not modified. Certains détecteur sau milieu utiles. 

Détecteurs très changés.

High level layers, images optimisées difficiles à interprétées. Mais quand regarde maximul activation s’aperçoit que concentre images même style.

Training from scratch

Moins facile à interpréter. échelle pattern petit. Sans doute car grande capacité par rapport taille ensemble données. Fine tuning meilleurs résultats même sur petits coprus. même si la tâche pas la même.

Wilber et al 2017, Stezoski et Worning 2018 pour large scale dataset

## Circulation

#### BJP

Towards another narrative of  artistic modernities.

Shook the cliché. Notion influence.

Computational study => bdd et quanti est-ce computationnel ? quels algo ?

Circulation of a style doesn’t prouve an influence.

Center and periphery, question of the centrality of Paris.

Que faire pour exploiter les images digitalement. Study circulation of Visual motives themselfes. Printed periodicals, posters, etc. Collect collection in IIIF.

Identify images most reproduced. Challenge of their circulation.

Train machine learning (copies, etc.)

Pastiche, réappropriait. Diffusion challenge of motives.

All ingredients are there for a digital study of visual culture.

What it is, the where, when. A return to the old aristotellician categogies. Factual material turn. Plurality of methods can bring much in decentring and production of alternative to the canon.

### Columbia

Study slides library. Big collection missing a general catalog. Optical character recognition to extract textual informations. Exploitation Computational vision.

Media center for art history 1993

2016 projet de recherche pour déterminer comment collection pouvait participer mission institution. See how was a memory of art history in our dept.

Accessibility Neural network classifier to organise the collection in different categories. Basic categorisation desn’t need special competency. However identifcation reproduction special tuning. Utilisation transformation de fourier pour rendre motifs de trames plus manifeste pour le classificateur.

Comparaison des résultats de classification sur une preuve de concept.

Neural nets to Decision trees. XGBoost

As an Archive the slide library documents the development of art history across the time.

Subject matter documents the accroissemet of the field.

Notion of significance : images that are unique to the collection. Vendor sets, images produced by museums but without halftone. Photograph of a postcard.

8000 slides. Organised by subject and region. Tiff 4850x4850 avec image.

Tesserat. Label information a simplified VRA Core scheme in Filemaker. Manually cataloguing of 8000.

Cropped slide to transparency.

True positive, true negative. False positive or negative.

\>40% de faux positifs Neural moins de True negative et false negative.

Decision tree plus efficace que neural net pour specificity (inverse pour sensitivité), --> Comment se l’expliquer ?

Ajoutant détection mots clef, améliore beaucoup résultat Décision tree. 

Implémentation en ligne de commande.

Projet encours, comment croiser possibilité automatiser tâches. Expérimentation toujours vitale. Amélioration des sorties. 

### Langlais

Stéréotypes viraux. Numapresse, nouvelle histoire culturelle.

Changement d’échelle, particulièrement observable dans le champ du journal et de la presse. Nombreux projets qui visent à créer des infra

- europeana
- oceanic exchannges
- NewsEye
- Impresso

S’intéresser à la presse pour la presse. Cultural analytics. Politique des supports, etc.

Viralité historique, quand infra techniqeu redéfinit l’objet de recherche. Analyse de circualtion. Constitution du corpus.

Tournant transnational études de presses. Nouveaux instruments scientfiques avec application outils de détection du plagiat, mettent en évidence circulation des textes.

Presse ancienne images pas encore en ligne pour recherche inversée

- Chronicling america
- Impresso

Accès aux fichiers de numérisation complet avec structure de la page. Corus XML, objets avec coordonnées => peut donc les récupérer automatiquement avec IIIF.

Développer de nouveaux outils basés sur le DL pour segmenter les pages à partir de différentes zonnes.

--> quelles techno ?

114000 images 7 hebdo illustrés 1850 à 1900.

Essor massif des images dans la plupart des quotidiens à partir de 1910.

Détecter les reprises d’images. Reprise de modèles pour classifier les images. Modèles classés à partir de classification contemporaines. Anachroniques par rapports aux corpus patrimoniaux.

Outils de transfer learning, bénéficier connaissances des modèles pour les réapliquer. Moins couteux que de développer à partir de rine.

Modèle qui intégre les normes de genre. Hommes femmes maquillés. Voitures, situations. Portraits médaillons qui disparaissent entre deux guerre.

Possibilité détourner outil pour chercher des images similaires. ou reconnaissance images. Impresso ou SIAMESE.

élargir approche viralité textuelle à la viralité des images. 

3e couche qui marchait le mieux. 

"l’inconscient du réseau de neurone"

Déterction de reprise. Comme 3e niveau, indépendant de la reconnaissance. Parfois erreurs mais intéressantes, circulation de codes visuels.

Quelques terraisn expérimentaux. 

Les pirates de l’image. Le voleur illustré le principal réutilisateur. Temps souvent courts. Qualifier ce qui a le plus de chance être piraté : portait et des scènes.

Arrivée massive image 1910-1914, où journaux mutualisent. Soit puisent même sources, et reportage. Images militaires et Paris-Match.

Processus de starification. Cinéma, avec vue de scène puis portraits. Parfois pour illustrer un concept.

Mémoire historique du journal qui recycle les mêmes portraits notamment pour les faits divers.

Nouvelles approches qui posent la question comment exploiter grands corpus et outils. Pas dépasser le qualitatif mais mettre le quanti au service du quali. Viralité qui nécessite retours critiques car phénomènes très différents. Objets que doit pouvoir requalifier.

Besoin infra pérenne pour naturaliser ces nouevaux outils.

### Isabella di Leonardo

Projet Replica fondation Cini Foundation

1M images.

Cardboard

Add historical knowledge regarding imagines 2 ways.

- photo as such
- photos as representation of other artworks

--> how enhanced knowledge of our collection.

Segmentation Sofia olivera et Benoit Seguin GitLab DHLab segment

https://github.com/dhlab-epfl/dhSegment

Similarity annotation établi sur a validated dataset.

Déterminer sous-hiérarchie d’éléments.

Reallignement as a process of re-documentation.

ULAN et Wikidata

Largest coverage and convergence

Système formel attribution

Learning model properly distinct close artworks

**What is the same as ?**

closeup, workshop paintings, restaurations, copy

Find machine logal descriptors

Choses pas détectées similaires alors que pour l’œil. Méthode de superposition.

Circulation motfis selon géométries ou appartenance même atelier.

--> **Morphographe** graph qui lie des peintures liées entre elles. Sous-graphe. Permet entrainer réseau neuronal qui peut claculer distance entre peintures.

Outil pour l’utilisateur qui doit aussi permettre annoter et mofiier matchs.

Every photo library contains a partial network of knowlegde

 

## cr. Computationnal vison

### The image-theories behind computer vision

Every computer vision is a set of instruction how to decodes images. Chaque algorithme incorpore une manière de voir les images computer vision algorithm embodies some kind of explicit philosophies on image or philosohies.

Show how difficult to define procedure. Defining their own problem to some degree.

 OUblie parfois que doit être implémenter en instructions basiques. Texte correct car déjà en quelque sorte une technologies.

Quid des images ?

**So this paper is about that gap, it is about underline images theories of computer vision. But I aslo wanna suggest a new model for the use of computer vision in DH. Not only look for things in large things but rather a technical technology for implementing and explorating different ways of seeing things.** 

--> Modèle de la réalité

--> how much can we produce model we can work with ?

--> Question du travail images 2D, réalité artistique plus complexe. Objets 3D, etc. Passage obligé par image comme intermédiaire. En soit déjà une technologie.

--> Drucker qui dans son article de 2013, avançait déjà que digital surrogates a model. Quel lien avec propos de Leonardo. ++

*Shadows and enlightenment*, Michael Baxandall

**Not just a tool but a medium in witch processual processes can be modelised**

A conceptual apparatus. Crisis in AI.

Problem de Molyneux, problème du rôle de la vision et de la connaissance des choses.

Rule/space computer vision, vs neural network. NN more Condillac que Locke

**David Marr et Vision 1982**, modèle adopté par CV. Fonction pas modéliser vision physiologique. Marr comprend la vision physiologique en termes informatiques. Vision as information processing system.

**Computer vision not a simulation of human vision. Instead of understanding computing anthropomorphic. Does the opposite. Marr Technomorphic**

Marr innovation extend the metaphore not only to notation byt to metaphore : **vision as a information processing system**

--> Perceptron et **métaphore NN** quel sens en premier cf. Cardon

--> Histoire des sciences et **cybernétique**

psychologie de la vison Gombrich, logical space of any given expected painting Kittler. Mais Kittler complètement passé à côté computer vision.

Marr **vision as Inverse graphic** : **separation of Mesh and texture**

--> mesh vs structure et 3D ?

Vision as inverse graphics. Génération image synthétiques pour entraîner IA

Gibson ecological approach to visual perception. Pas décrire 3D externe mais servir des besoins spécifiques.

--> a-t-on forcément besoin passer par image 2D, doit-on penser de nouvelle manière de penser numérisation ?

--> biologie de l’historien de l’art

--> Question sur externalisation

// Panovsky

Perspective 3D geometry, coming from Marr, consist incapacity to deal with reality.

Marr paradigm, totalising 3D geometry inability to deal with the real ambiguities and consistancies of visual implications.

Sloman "Visual systems do not reprensent informations about 3-D structure in a 3-D model... but in collection of information fragments, all giving partial informatio. A model cannot be inconsistent. A collection of partial descriptions can."

--> disqualifie complètement le modèle ?

--> quel rapport avec la logique connexionnsiste ? autrement dit est-ce que pousser jusqu’au bout la logique connexionniste, ne pas abandonner complètement idée modèle abstrait, logique de la réalité.

--> succès pour le visuel des RN capacité à prendre en charge déformation, reconnaître. Si envisage manière proposée par Leonardo, ne quitte t on précisément pas la question de la reconnaissance. Finalement ne s’agit-il pas à proprement parler de modéliser la réalité, mais cette fois-ci pas d’après un modèle externe, mais depuis la réalité historique étudiée ? ++

--> would it still be computer vision ? or more simply real modelisation of cultural content +

écrire computational visual systems based on historical way to see ?

--> vision ? only, cf. composition architecture

Model vs collection de description partielles. Système visuel ne représente pas Information sur structure 3D.

Comment caractérise plis (cf. Texture)

It breaks the assomption we are seeing an actual ... of a model of objet.

Ambiguité, inconsistance. Calligraphie ? qualité non représentationnelle, qualités stylistiques. Temporal informations, line. Plus de paradigme inverse graphic. Détection des mains.

--> nouveaux modèles en retours pour CV ?

## Drucker AI and AI

Æesthetic intelligence vs Artificial Intelligence

Esthétique de John Dewey

Dit que ne veut pas placer en opposition. Mais montrer que AI laisser un espace occupé par l’expérience humaine telle qu’envisagée par Dewey qui a quelque chose à nous dire de notre existance augmentée par l’ordinateur et en ligne.

Engelbart : automation / augmentation (cd. McLuhan = extence capacity of human mind). Automation procédures pour devenir modèle du cerveau humain.

Feature recognition and description

Simulation capacité humaine

Model of human perception dependant on **feature description and classification**. Manière dont simule capacité humaine. 

--> Does this two poles could be put in relation with connexionist vs expert models ?

Generative

Elisa et contexte, espace d’expérience.

Program avec capacité émergente. Dinkins project.

--> Que peut-on apprendre de l’art numérique ? cf. Spratt. 

Automatisme : programmé, **pas besoin d’un humain**

Aestetic et génératif. Max Bense et Abraham a. Moles. Conviction que automatisme trop abstrait, espace de neutralité. Élimination catarthis, émotion. Procedural work (cf. Shanken)

--> Importance de la cybernétique

Si conçu par activité procédurale, serait purement abstraite sans potentiel de dommage potentiel. Sorte de neutralité, espace d’élimination catarcis effect, emotion.

--> Abstraction, universalisme et démocratie. Art concret.

Longue histoire des œuvres procédurales : Nake, Georges Nees, etc. 

**AI déplacé des activités procédurales à des activités émergentes** avec les réseaux neuronaux.

17’33 Détection, discerner feature et user comme inventaire, de l’autre classification.

--> classification/détection

Emerging system

Automatique, théorie de l’information.

**Tout cela pas pertinent.** Because utimatly aesthetic isn’t about either the objects (how it is produced, etc.) nor reside in the mind (détection). **Aesthetic is the capacity to experience with, understand.** **Hermeneutic space between and a procative object and what occurs between.** About the two, in relation. Related to experience, an event. 

Car esthétique a à voir seulement avec les objets. Capacité de comprendre et exister au sein d’une expérience. Dewey Art as Experience.

Espace herméneutique entre un sujet percevant et un objet. Espace entre les deux qui constitue l’esthétique. Pas du côté de l’esprit ou de l’objet.

Dewey marginalisé comme pragmatic

--> un point de vue de la médiation ?

Qu’est ce qui est génératif dans aesthetic. Adorno.

Esthétique générative Adorno, ne résolvent rien. Capacité de provocation, don’t resolve.

**Capacité de provoquer chez l’homme espace de l’expérience.** Lauren McCarthy

Aesthetic intelligence

--> Retourner le propos en quelque sorte : peut-on intelligibiliser l’aestetique ?

--> une critique de ce que peut nous apporter IA pour comprendre l’art ?

**pas question de savoir si peut être simulé ou procéduré car la question car expérience aesthetic au-delà de ces opérations**

is beside the point car au-delà des opérations procédurales

--> dans quelle mesure peut-on dire que pas impact sur esprit humain. En quoi un média.

## Dominique Cardon

Automates raisonneurs, intelligents, autonomes.

Sans doute nous trompons d’imaginaire. Nouveaux calculateurs qui ont énormément de propriétés intéressantes. Les machines sont inductives.

Tensions et disctinction épistémologique qui est au cœur de l’histoire de l’IA. Proposer une contre histoire de l’IA en opposant approche symbolique et connexionniste.

--> réconciliation possible symbolique et connexionniste ? En HA ?

--> Cybernétique (procédure, etc.) place de la cybernétique dans la compréhension Histoire de l’art

Perceptron de Rosenblatt et reconnaissance des images

logique pas la forme du raisonnement humain, ne tient pas compte formes plus perceptuelles, corporelles, liées à environnement et contexte

--> si suit Johanna question de la place de l’homme essentiel. Comment incorporer au-delà de la stricte visualité ?

-->Reconnaître les objets ? qu’est-ce qu’un pattern ? connoisseurship ?

--> comprendre ce que l’on fait. Boîte noire. Possibilité utiliser IA en recherche en HA.

--> métaphore physiologique

--> imprégniation = expérience esthétique. œil du quatrocento Baxandall qui projette ?

Peuvent aussi devenir générateurs d’images qui n’existent pas. GAN generative adversarial network

voir Michael Castelle

habitus, structure structurée agissant comme structure structurante. Incorporation externalité du monde. Internalisation représentation du monde, et externalisation.

--> si médiation, comment l’IA agit sur notre compréhension du monde ?

Structure incorporée du modèle

--> quel statut peut on donner à cette structure incorporée

navigation qui n’est pas le fruit raisonnement mais liée à manière organisée et perceptuelle de reconnaître le monde avec ces technologies destinées à lire des images.

Système épistémologies et de compréhension et fonctionnement perception humaine, que pu trouver solution face à idée que raisonnons. Alors qu’engrammée en nous et utilisables sous des formes très diverses pour reconnaître l’espace de formes présenté à nos yeux.

--> quel espace de formes dans l’œil de l’HA ? de l’amateur, etc.

--> Pourrait-on engrammer la culture visuelle d’une époque ?





----

compte : GalPix password : 2020GALPIX_

Approches de transfert de style. GANs voir apparaître des approches scientifiques possible. Car possiblité de modéliser le style d’un artiste.

---

## docExtractor 

Méthode pour extraire automatiquement des éléments dans des documents historiques

Motivation relativement simple, un besoin crucial d’outils faciles dédiés à l’analyse d’image pour répondre à la numérisation massive.

Actuellement les principales méthodes pour extraire des éléments tels que du texte, des photos ou des dessins dans un document utilisent un système dédié à chaque tâche : pour l’ocr pour la détection de texte, de photos ou de dessins. Avec l’avènement des réseaux de neurones, la plupart de ces systèmes ont besoin pour la plus grande partie de ces méthodes d’annotation manuelle. Il s’agit de déterminer la région intéressante à extraire afin de générer une base de données où pour chaque image on dispose d’indication sur les zones intéressantes à extraire. Si on entraîne un algorithme sur une collection d’images dégradées, ses performances sur un autre jeu de données (en couleur par exemple) sont très faibles. Il devient donc important de pouvoir générer des algorithmes qui soient applicables à tout type de documents ou diverses tâches.

La méthode que l’on propose consiste à générer des documents synthétiques avec des annotation, d’entraîner la méthode avec ces données synthétiques pour faire la détection du texte mais aussi des illustrations en développant un système unique reposant sur des données synthétiques pour être applicable à tout type de données.

En générant des annotations synthétiques, il est possible de générer ces annotations gratuitement alors que l’annotation manuelle est extrêmement coûteuse en temps. Typiquement, pour entraîner une méthode, il faut un millier d’images. Ainsi, l’annotation synthétique nous permet de disposer de documents à la fois très génériques et de s’abstraire de l’annotation manuelle.

L’approche consiste à d’abord générer des documents synthétiques avec des annotations à l’échelle du pixel puis d’entraîner un réseau de neurone assez standard pour annoter ces régions. Pour générer ces documents synthétiques on a récupérer une collection d’arrière plan, de contenu wikipédia et de fontes de caractères. Composition de background + génération de contenu + ajout de bruit pour simuler des dégradations.

Pour la composition des arrières-plans, téléchargé 200 pages ainsi que des images de contexte (arrière plan, table, etc.). Traitement de doubles pages. Application de transformation de couleurs alléatoire (jaune).

Pour la génération du contenu. On génère alléatoirement une mise en page en quadrillant le document puis colle des éléments sur la page. Quatre grands types d’éléments sont définis : des images, des glyphes, des dessins, du texte. Mais on peut aussi ajouter toute sorte d’éléments. Pour le type d’éléments de texte, générer des types les plus différents possibles est crucial. Il faut avoir des images les plus génériques possibles et qui couvrent le plus d’ensemble possible de documents. Langues, légendres, transformations, etc. pour obtenir la plus grande diversité de document.

Enfin, on ajoute du bruit pour simuler flou, ajout de bruits avec lignes ou formes, ajout d’encre traversée de page, etc.

Exemple de document généré synthétiquement SynDoc qui contient une image, des tableaux où du contenu a été généré alléatoirement, des zones de textes manuscrites ou non manuscrites ou un gliphe. Synthèse d’image qui permet de générer autant d’images que l’on souhaite différentes les unes des autres. Puis possible d’entraîner un algorithme automatique.

Utilise un réseau de neurone destiné à déterminer la segmentation. Postprocessing en sortie très générique, il suffit de supprimer les régions un peu trop petites.

Voici le résultat d’extraction de texte. En bleu cyan, la région de texte détectée par l’algorithme. En vert, la vérité terrain (ce que l’on voudrait extraire). Même si les données générées synthétiquement peuvent paraître génériques et peu réalistes, l’algorithme parvient à s’en servir pour extraire des lignes de textes de documents habituellement difficiles à traiter.

De même sur registres avec mise en page complexe. 

Idem avec documents où grande diversité d’images. Algorithme qui permet aussi directement d’extraire le texte et les illustrations au sein d’une grande diversité d’images.

Algorithme disponible sur GitHub en open source. Un lien ves une démo avec un Jupiter notebook pour réaliser pas à pas l’extraction avec notre algorithme.

- On télécharge le modèle déjà entraîné sur les données synthétiques
- on ouvre l’image dans l’interface
- on produit la segmentation sur l’image désirée

Sortie dans plusieurs formes : une image avec une couleur pour chaque objet. Une image pour évaluer. Possibilité extraire sur toutes les régions détectées (crop vers répertoire).

Coordonnées des zones pas vraiment fait.

https://github.com/monniert/docExtractor

### Comment développer une application web à partir de docExtractor

Un manifeste est un fichier JSON qui permet de rassembler toutes les données d’une collection d’images. Exemple https://iiif.biblissima.fr/collections

Mirador est un visualiseur qui permet, étant donné une sélection de manifeste, de visualiser des collections d’images et de naviguer dans ces collections.

Workflow de cette application web. Étant donné un utilisateur qui voudrait exploiter un manifeste IIIF, renseigner l’URL dans l’application web. 

inherit.inria.paris.fr

Envoie l’URL dans une application Flask qui va envoyer cette URL à docExtractor qui va télécharger toutes les images liées à ce manifeste, procéder à l’extraction puis renvoyer toutes les données liées à cette application web.

Démo. Un visualiseur mirador avec un serveur d’annotation SAS. Dans l’onglet extract, on peut renseigner l’URL recherchée pour lancer l’extraction automatique du document.

Une fois que la tâche est réalisée (400 images, 1 à 2 heures). Document qui devient disponible dans la page d’accueil de mirador, et possible d’aller directement dans le document qui nous intéresse et de directement visualiser les annotations générées de manière automatique avec docExtractor. Ensemble de régions de texte qui seront générées pour l’ensemble du document. C’est également le cas pour toutes les images des documents. Permet d’extraire de manière automatique les annotations et toutes les régions qui nous intéresse dans un document.

### Conclusion

docExtractor un premier algorithme qui permet l’extraction automatique d’illustrations et de textes. En ligne avec un notebook pour répliquer l’action.

Intégration avec IIIF et web application dans une application wbe pour visualiser des documents

https://enherit.paris.inria.fr (en ligne mais pas assez d’espace de stcokage) Code pour générer le serveur réplicable https://gitlab.inria.fr/dhai/SimpleAnnotationServer

### Discussion

Jean-Philippe Moreux commencé à l’utiliser, de même l’équipe de recherche de l’observatoire pour extraire des contenus de tables. Développé très récemment.

Quelles perspectives de développements ? Un étudiants qui exsaye de rafiner l’algorithme pour le spécialiser sur l’extraction de contenus dans des tables. Ou encore de pouvoir différentier extraction de dessins ou d’illustrations.

Annotations sous forme de boîtes englobantes dans IIIF et pas zones.

Est-ce que publie les annotations comme annotations IIIF. Enrichie la base de données d’annotations au sein de l’application web. Mais à l’époque SAS n’avait pas encore développé de méthode faciles pour récupérer les annotations. Aujourd’hui développements permettant de télécharger ensemble des annotations, mais la version sur laquelle on a travaillé ne le permettait pas.

Savoir si travaillent sur les lignes en vue de la HTR. Pour le moment pas du tout encore travaillé sur cela, un travail mené en amont.

Divers

- Universal viewer bonne opton car bien supporté et grande communauté, supporte plus de types de documents que Mirador notamment 3D et pdf et lecture de vidéo !
- Mirador très modulaire. Dernière version également vidéo et audios
- autres visualiseurs moins outillés et soutenu mais peuvent présenter des avantages dans des usages spécialisés. Tiffy moins répandu mais léger et bonne compatibilité mobile. Visualiseurs simples comme OpenSeaDragon et leaflet qui peuvent suffirent.

Comment repérer premier corpus sur lequel travailler pour identifier des ressources disponibles en IIIF. Discussion au sein du consortium pour travailler sur un moteur de recherche. Mais ne s’orientera probablement pas dans cette direction car question centrale des métadonnées, question que IIIF évacue de manière relativement habile faute de pouvoir disposer d’un modèle suffisamment générique pour tout type d’objets. En tous les cas consortium travaille activement sur le développement de mécanismes qui permettent de le faire sans s’attaquer frontalement à la question des standards de métadonnées. API change (chain ?) directory sensé répondre à des agrégateurs spécialisés. Plusieurs prototypes développé comme par OCLC. Biblissima avec IIIF collections, ms numérisés agrégateur spécialisé et pour lequel essaye de s’attaquer à la question des métadonnées avec agrégation et réconciliation pour offrir système robuste de recherche avec facettes pour recherche. 

Europeana qui peut être une bonne porte d’entrée pour travailler en masse, agrégateur OCLC, métamoteur IIIF au Japon et un autre pour objets d’origine japonaise où qu’ils soient conservés dans le monde.

Modulo, version 3 de Nakala en développement. Prévue en décembre. API image dans Nakala, très bien et pratique. Présente l’avantage d’avoir des DOI automatiquement. Permet de s’affranchir de la gestion du serveur d’image qui sera géré en humanum. Mais pas encore l’API présentation dans la première version. Donc devra s’affranchir de Nakala pour produire les manifestes. Pour les annotations, peut-être plus judicieux de prévoir un hébergement sur Nakala avec un serveur d’annotation. Voir comment Nakala pourrait être utilisé comme serveur d’annotation. Question de granularité posée également avec Nakala. Comment ont-ils prévu la création des manifestes : savoir comment 

Serveur d’image Loris utilisé par Nakala, l’un des serveurs d’images les plus utilisé dans la communauté. Bon logiciel qui implémente l’API image au niveau 2. Beaucoup d’installation de Cantaloupe sur Huma-Num, possible que passe à cela par la suite.

https://cantaloupe-project.github.io/



## Question table ronde circulation

Atelier IIIF

comment savoir si une institution utilise l'IIIF? 

si une institution est sur Europeana, elle utilise forcément IIIF? 

geo:  https://www.georeferencer.com/ permet de relier les cartes anciens avec les cartse actuelles via IIIF

**Question de Alix Chagué**

Une question concernant l'articulation IIIF + TEI : existe-t-il des projets qui lient les deux (via l'API Presentation ?) ? Est-ce faisable ? Ou trouver des recommendations ou des exemples ? 

**Question d'Alexandra**

Pourriez-vous donner quelques précisions et exemples pour IIIF et la cartographie ?

**Question générale sur l'OpenScience**

Utiliser iiif garantit-il la compatibilité avec les principes FAIR ?

comment faire pour installer mirador pour mon propre corpus ?

un chercheur a un corpus d'images. il souhiate l'annoter, l'augmenter avec des corpus extérieurs puis publier sa recherche en citant les images très précisément. par quoi doit-il commencer ?

usages en distant reading ?

quid des corpus contemporains ?

exemples sur les arts de la scène ?

**Cas de la génération de sites web**

Quand on édite un Manifest iiif pour générer un site web : est-ce adapté au responsive design ? Comment le manifest résiste-t-il / gère-t-il les redimensionnements dus aux différents écrans possibles pour afficher la page ? 

La page web correspond-elle à un canevas ?

**Cas des collections d'images**

La gestion éditoriale d'une collection d'images peut-elle se faire aussi dans un seul manifeste (avec un canevas qui mobilise plusieurs images) ? (expliciter la différence et la pertinence d'utiliser une collection, notamment pour le cas d'un site web)

**Cas de l'annotation des objets audiovisuels**

Existe-t-il des outils déjà partagés et "labellisés" iiif pour faire de l'annotation / chapitrage vidéo avec interfaces de navigation ? iiif peut donc gérer des "segments" de time-code ?

**Cas API recherche**

des moteurs de recherche généralistes peuvent-ils facilement interroger des API recherche pour afficher en résultats des annotations et/ou extraits d'images numérisées et compatibles iiif ?

**Ressources audio et vidéo:**

  possible d'importer des flux youtube et vimeo ?

  Memorekall ?

  synchronisation avec des partitions ?

  comment fait-on pour choisir le logiciel/viewer qui nous convient le mieux? 

**Circulations**

**Moderator: Nuria Rodríguez Ortega, University of Málaga**

**ALL :**

Criteria for an ideal corpus ? (see BJP)

scaling : Next steps: Aggregate other collections ?

#### form or style

would you say that Computer vision approaches are more adapted to the analyse of visual culture more than to stylistic analysis in art ? Do you think art history is necessarly switching to visual culture using this technics ? How and where "circulation studies" would differentiate themselves from Visual culture ?

What is a form (Leonardo) ? if this techniques are more conceived to recognise details or particular agregators of patterns. Where does style starts ? How should we think back this question 

**Béatrice Joyeux-Prunel, University of Geneva**

What are the specific difficulties you encounterd working with contemporary corpus

What is the nature of collaboration with artist Gregory Chatonsky ? ++

"Not possible to survive in art history without a computer "

**Stefaan Van Liefferinge, Columbia University**

Have you already identified interest among other art history slides collections accross the world to apply your approach ?

How much could you employ the metadata extracted from the OCR to help the training of computer vision model in this project ?

I**sabella di Lenardo**

Mutualisation : alignment for names (Getty, Wikidata) + to redo the work periodically (when does it ends ?) 

The tool you’ve developped around this project is really amazing. In a way, it’s a general tool usable for art history research. As you said "Every photo library contains a partial network of knowlegde." Are you planning to make it accessible more broadly for other corpora ?

**Pierre-Carl Langlais**

which technologies did you use for segmentation of the corpus ?

next step : multimodal analysis ? until now, a silo approach (image / text). How about image-text analysis ? 

In your presentation you use the expression the "inconscient of the neural network" (l’inconscient du réseau de neurone) Beyond the naturalistic metaphor, how far do you think we can talk about an unconscious?

de Victoria:Pour Langlais qui évoquait une library avec différents modèles utilisés qui pourrait être réutiliser: quel serait le niveau de granularité des infos à partager? le modèle en entier ou alors aussi les données, comme un data paper?

take away:

  need more than just these approaches, they're a complement not replacement to traditional art history

––––– Ce texte est à effacer (après lecture si c’est votre première visite) ou à conserver en bas de votre pad –––––

Bienvenue sur Framapad ! 

Ce service s’inscrit dans le réseau associatif Framasoft qui propose un ensemble de sites et de projets autour du logiciel libre, sa culture et son état d’esprit.

➡ Comment commencer ?

• Renseignez votre nom ou pseudo, en cliquant sur l’icône « utilisateur » en haut à droite.

• Choisissez votre couleur d'écriture au même endroit.

• Lancez-vous : écrivez sur votre pad !

• Les contributions de chacun se synchronisent « en temps réel » sous leur propre couleur.

➡ Comment partager / collaborer ?

• Sélectionnez et copiez l'URL (l'adresse web dans la grande barre en haut à gauche du navigateur)

• Partagez-là à vos collaborateurs et collaboratrices (email, messagerie, etc.)

• Attention : toute personne ayant cette adresse d'accès peut modifier le pad à sa convenance.

• Utilisez l'onglet chat (en bas à droite) pour séparer les discussions du texte sur lequel vous travaillez.

➡ Comment sauvegarder ?

• Il n'y a rien à faire : le texte est automatiquement sauvegardé, à chaque caractère tapé.

• Marquez une version (un état du pad) en cliquant sur l’icône « étoile ».

• Retrouvez toute l'évolution du pad et vos versions marquées d'une étoile dans l’historique (icône « horloge »).

• Importez et exportez votre texte avec l'icône « double flèche » (formats HTML, texte brut, PDF, ODF…) ou avec un copier/coller.

Important ! N’oubliez pas de conserver quelque part l’adresse web (URL) de votre pad.

Bon travail collaboratif :)

Merci pour votre attention et votre confiance.

––––– Ce texte est à effacer (après lecture si c’est votre première visite) –––––

**ATTENTION**

CETTE INSTANCE PROPOSE DES PADS À EFFACEMENT AUTOMATIQUE !

VOS PADS SERONT AUTOMATIQUEMENT SUPPRIMÉS AU BOUT DE 183 JOURS (6 MOIS) SANS ÉDITION !

Si le contenu de votre pad semestriel a été effacé, c'est qu'il n'avait pas été modifié depuis plus de 183 jours (6 mois) consécutifs.



















