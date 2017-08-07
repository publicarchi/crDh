# crAVdh2017

https://avindhsig.wordpress.com/workshop-2017-montreal/

SIG ADHO’s workshop, 2014 premier groupe rassemblé à Lausanne. Pas à Sydney, 2e workshop à Krakow où a décidé de se concentrer sur la question de la vision computationnelle. L’objet de ce SIG est de construire un réseau.

https://avindhsig.wordpress.com

Mailing list, lunch meeting on wednesday, 12h30, Leacock 232

Va se concentrer sur la manière dont la vision computationnelle peut être mobilisée dans les DH. C’est notamment la raison pour laquelle laisse beaucoup de place à la présentation de ce que vous faîtes avec ces techniques. Outre les présentations, plusieurs sessions pratiques auront lieu.

## Processing Pixels : Towards Visual Culture Computation 

[Lindsay King](https://resources.library.yale.edu/staffdirectory/detail.aspx?q=631) & [Peter Leonard](http://web.library.yale.edu/dhlab/peterleonard) (Yale University)

Évoquer les expériences conduites des plus simples aux plus complexes.

Comment en sommes venus à travailler avec les images ? une bibliothèque qui contient beaucoup d’images. Frappés par le fait que les journaux surtout textuels de même que les markup. Bibliothèque entièrement numérisée et encodée, possibilité de faire des expérimentations ProQuesr Vogue archive. 121 années, 1892-2013, 2 780 numéros, 440 000 images. 6 TB de données encodées. Articles, publicités, etc. Corpus qui rendait possible un grand nombre d’expérimentations possibles. Enjeux liés aux licences.

Premier expriment, classement par les métadonnées, N-gram search, et topic modeling. La durée de la publication permettant notamment d’analyser les changements au cours du temps.

Par exemple, travail sur la moyenne des couvertures du magazine dans le temps. Chaque pixel calculé à partir d‘une moyenne, pas de la vision computationnelle proprement dit, mais indique la manière dont les couvertures changent au cours du temps, décennies par décennies.

Cover browser, qui permet de naviguer parmi les images classées dans le temps, permet de visualiser la manière dont les patterns changent dans le temps, nombre de numéros par années, forme des couvertures. Il y a beaucoup de choses qui sont déjà visibles lorsque l’on peut zoom out / zoom in dans la collection. Les motifs sont d’emblée perceptibles, il s’agit déjà d’une certaine manière de distant viewing. Observation qui permet de voir comment les couvertures deviennent relativement uniformes dans les années 80. Diversités des années xx.. Dans les années 60, le design commence à devenir plus consistant. L’esthétique devient plus strict. Dans les années 70 uniformisation de la prise de vue. Rendre le magazine plus conforme aux femmes qui travaillent. Changement radical dans les années 90, 2000.

En zoomant on peut dont identifier des patterns, possibilité de regarder la manière dont certains patterns se déploient : comme le portrait américain, les couleurs douces, etc. et tracer leur apparition dans le magazine.

Toutes ces images peuvent également être comparées entre elles. En comparant les motifs ensemble, possible de visualiser les patterns dans des colonnes distinctes. Couvertures correspondantes illuminées dans chaque colonnes.

Image Analysis in RRV, sorting covers by color to enable browsing. Mesure de l’espace colorimétrique (colorimetric space) pour offrir une navigation à l’intérieur de tout ce matériel.

Statuation par année avec ImagePlot : les plus saturée, les plus haut. Voit qu’à partir des années 70, les images sont plus saturées. Si on regarde la saturation et hue par mois, s’aperçoit que les patterns sont plus divers que l’on aurait pu le penser.

Hue, saturation, and value avec D3 : une autre manière de naviguer dans l’ensemble de données. Peut passer de la prévalence d’une couleur à l’autre, etc. Permet de naviguer ç travers les différentes dimensions.

Le problème c’est que difficile d’isole une seule couleur par couverture, car souvent plusieurs couleurs. Exemple couverture avec 4 robes couleurs distinctes. Trouver des manière plus appropriée pour travailler sur cela.

Slices histograms (David Croquet ?) Idée que segmenter chaque couverture par couches afin d’obtenir des résultats beaucoup plus fins qui permettent de distinguer l’arrière plan du premier plan par exemple. Dans cette visualisation saturation / brillance. Depuis sa création s’oriente vers la saturation, probablement lié à l’amélioration des techniques d’impression. Sans doute factuel mais significatif.

K-means clustered colors : distribution by year. Prendre les couvertures et emploi d’un algorithme de clusterisation. Mean des plages moyennes de couleurs. Ici utilise spectromètre, couleurs ordonnées par fréquence. Pour chaque couleur, affiche les couvertures en fonction de la densité de la présence de ces couleurs. Fournit parfois des informations sur l’histoire de l’impression : par exemple pas possible de représenter le jaune avant… Diagramme radio pour représenter les périodes : on voit les choses apparaître de manière cycliques selon les années.

Face detection : technique de machine vision souvent employée. Expérimentation sur la photographie du gouvernement. Intéressant car localisation des clichés. Visualisation géographiques de ces dizaine de milliers de photos. Résulte en visualisation de l’espace américain. Ici pas particulièrement disruptif, seulement affichage des photographies en boîtes clivables sur la carte.

Christiana Wong, Analysis of Vogue Fashion photography implication about the female face. Calcul sur le delta de présence du visage. Ici on observe une énorme augmentation dans ce cadrage zoomant sur le visage dans les années 70. Or, cette évolution correspond exactement à celle que l’on observe avec augmentation de la saturation.

Visual Similarity : What if we could search for pictures that are visually similar to a given image ? Neural Neighbors, une technique dont entendu parler à Krakow. Convolution neural network conçu pour repérer des chats, etc. Entraîné sur des milliers des images, 1.2 millions images Image Net. Mais extrait le penultimate layer in the network (pool_310. Qui constant représentation plus abstraite de la vision artificielle, puis cherche voisin.

Resig John Aggrgating. 

Stahmer 

Lot pour lequel déjà des marquages. Mais pas de sémantique pour les images. Ici peut travailler sur ces objets, se déplacer sur ces objets avec la souris. Au fur et à mesure que se déplace au-dessus de ces images visualise les autres images qui sont dans l’espace de proximité. Plutôt performant.

Visual similarity : Face Cream. Une expérimentation intéressante. Permet de faire apparaître une sorte d’Historique de cette présentation. 

Puffed Sleeves, toutes différentes, mais similaires. Voit bien l’intérêt ici de ces techniques.

Aussi intéressant de noter que trouve les voitures.

Camouflages, ici repérées.



Obtenir et travailler sur des grandes collections d’images numériques.

- teenier compte des métadonnées intrinsèque disponibles dans les collections
- approche pour prendre en compte les restrictions liées aux copyrights, licences perpétuelles, usages transformation.
- collections de plus en plus importantes d’images numérisées, du gouvernement, collections, média sociaux.
- les dpts d’informatique computationnelle travaillent sur des dataset

Prochaines étapes pour une computation culture visuelle.

Focaliser sur les photographies du 19e. Compbiner signaux de pixels et ceux du textes. 

Prochaines étapes AVISG’s plans for Visual DH

Copyright comment gère le pb.  Qu’est-ce qui peut être équivalent à une citation, quids images partielles, quid des transformations comme histogrammes.



@pleonard

@mslindsaking

---

# Bertillonnage

consiste en une image et des champs. Une manière d’enregistrer des données corporelles sur les personnes.

Une exposition sur les différentes manières de représenter le corps. Mais aussi de gérer physiquement des données massives. Présentait dans l’exposition une machine de reconnaissance faciale.

Decimal Number Recognition, classification of handwritten decimal… 

Préparation du lot, segmentation, classification et reconnaissance des chiffres. Première étape pré-processing. Reconnaissance de caractères. Comme lettres cursives d’abord un problème de segmentation. Utilisation du Word Spotting DESCENT field.

Regional hard spots lorsque des marks, et des trous, etc. 

Problème de remplissage en dehors des champs.

Savoir si peut ou pas reconnaître l’écriture. Pas vraiment bien fonctionné.

Pour la reconnaissance des décimaux, pas suffisant même si plus de 70%. Les humanistes travaillent dans un espace ambigu. 

66% sur reconnaissance de caractères. Essai de réseaux neuronaux. Plus efficace quand entraîné, mais 70% sur autres champs.

Machanical Turk if public domain data and task is easy.

Toujours étonné à quel point la vision humaine est efficace comparée au travail fait par un ordinateur. Penser dans quelle mesure l’ordinateur peut faire le travail d’interprétation.

## Distant seeing TV

Comment passer à l’échelle pour les images mouvantes de la culture visuelle.

Comment traiter des corpus de millions d’images pour un seul et même plan.

Raison pour laquelle intéressant de pouvoir travailler avec des spécialistes en statistiques computationnelles. 

Voulait enseigner à l’ordinateur comment voir et extraire certains traits des images pour comprendre ce qui a lieu.

Création d’une taxonomie de traits. Objets, visages, textures, couleurs. Dès lors possibles d’extraire des choses plus abstraites un peu à la manière de topic modelling.

dliv, cvv, openCV, superbes librairies pour travailler sur des traits de bas niveaux.

Beaucoup de papiers et algo qui cherchent à identifier des traits de niveaux intermédiaire

- code souvent non existant ou pas public
- prototype ≠ librairie
- pas généralisable : black and white, low definition des exemples
- pas interopérables

pour les traits abstraits un territoire relativement nouveau.

Shot detection : détecte les plans. 

Face detection et face recognition

Exemple sur une vidéo

En live détecte les visages et reconnait mais aussi changement de caméras.

Pilot study : I dream of Jeannie vs Bewitches

Voir à quelle fréquence les personnages apparaissaient dans la saison. Présence des personnages féminins à travers la saison. Comment la visualisation peut nous informer sur la manière dont les personnages apparaissent. Étude des co-occurences des personnages.

voir distant.org

## match, compare, classify, annotate

VGG image Search engine VISE

...

Open source software BSD licence

Image matching : est-ce que toutes ces images représentent le même objet.

Extraction de traits dans des images, avec des prises de vues depuis des angles différents ce qui suppose un algorithme qui prend en compte la géométrie.

Classification suppose un concept de haut niveau de l’image. Exemple images avec plusieurs avions. Apprentissage depuis des lots images. Extraction de traits.

Annotation d’image sans doute moins remarquable, mais sans doute un champ directement associé à notre recherche.

Visual Geometry group

Extraction des vignettes, et clusgerisation visuelle. Sélection d’un détail de l’image et recherche dans d’autres pages. Méthodes pour visualiser les publications à travers le temps. Identification des copies et des réemplois. Identification du type d’insectes depuis les altération de ces blocs !

Moteur de classification. Une approche basée sur les réseaux neuronaux. Oxford painting retrieval : recherche trains, etc. Fonctionne assez bien pour donner un index. 

Bib : Elliot Crowley et andrew Zisserman : The state of the art : object retrieval in Paintings using Discrimitaive regions, 2014

Utilisation de Google Image pour apprentissage.

VIA for 15C printed Bookstrade project cd bookstrade.ox.ac.uk

https://goo.gl/GJgQcx

## Discussion

Sur le croisement entre approches culturelles et analyse automatisée. Exemple de la représentation des femmes dans les séries.

Question sur la matérialité des images, et ses implications méthodologiques. Si elle est faite de manière éthique, la numérisation vous oblige à considérer les différentes dimensions d’un objet. Sa matérialité mais aussi son usage.

## Divers

ERC sur les fils et la couleur

Voir goo.gl/nsbs7J

filmcolors.org/2015/06/15/erc/

zauberklang.ch/filmcolors/



NEURAL NEIGHBORS

 Pictorial Tropes in the Meserve-Kunhardt Collection

https://yaledhlab.github.io/neural-neighbors/

https://github.com/yaledhlab

## Hands on

Computer vision for DH handson

Goals

- from zero to convolutional neural networks
- Give intuitions
- very high level and hiding (not so unimportant) details
- deliberate tunneling (CV is nos just Deep learning)

Deep learning beaucoup de succès ces dernières années dans nombreux champs. Là pour rester, donc vaut la peine de prendre le temps de s’y consacrer.

Deux sessions

- HVS basics, convolution (necessary evil)
- Convolutional neural networks

Chaque session séparée théorie et pratique

Practice done in the browser

Utilisation de Python Numpy + Scipcy + Notebook

Basic image operations scikit-image

Face/object detection + identification : dlib

DL

### Qu’est-ce que la vision computationnelle

Auto-captioning, une tâche relativement difficile mais qui commence a avoir des résultats intéressants. 

Exemple : semantic segmentation. Une image donnée sur la gauche et identification des différents éléments.

Comment parvenir à une compréhension de haut niveau des images et des vidéos. Cherche à automatiser les taches que le système visuel de l’humain peut faire (Wikipedia).

Pour solutionner des questions, besoin d’une expérience du monde. Besoin de processus d’apprentissage et ses processus.

La vision humain (The Human Camera). Si travaille sur des images en biologie, pas forcément besoin de comprendre ce que les humains voient. Mais lorsque travaille sur des images faites pour les humains, alors besoin de comprendre comment fonctionne la vision humaine.

Dispositif optique qui achemine une image optique sur la rétine. 

Comment acquiert-on la couleur. Une distribution du spectre lumineux selon des fréquences. Information colorée projectée en système 3D peut distincte, souvent comprimée en trois valeurs.

à chaque niveau des processing qui interviennent. Au cours de ce processus nombreux filtres spatiaux, visualisation locale, etc. Des cellules spécialisées qui détectent, couleurs, etc. Information pré-processée acheminée au cortex visuelle où une compréhension à plus haut niveau intervient.

Visual cortex : séparé en couches (layers) qui traitent l’information à un niveau supérieur. 

Neurons are task-specific (color, motion, orientation, etc.)

Comment travaille-t-on dans un monde digital. Ici dispose d’une caméra qui se compose d’une arrays of photorécepteurs. Recepeteurs rouge-bleu-vert qui fournissent des images composées de arrays of pixels. Chaque pixel encode l’information colorée. 

Fantastique pour présentation, mais terrible pour l’analyse.

- 3D tensor (Height, Width, Channel)
- First 2-D : spatial
- Last dim : color

Digital vs HVS

Sensor | cones | CCD-sensor

Analysis l retinal processing | ?

Low-level difference example. Altère image, même nombre de pixels, du point de vue digital très peu de différence. Mais pour l’homme une configuration très distincte.

Différence de haut-niveau. Image de l’acropole d’Athènes. Mémoriser cette image dont peut acquérir une version mentale très haute. Pour autant incapable de répondre sur le nombre exact de colonnes. Pourquoi car une vision de très haut niveau, compressée en ne tenant pas compte du détail. Une représentation de haut niveau même si est capable de mémoriser les images.

### Une opération fondamentale : la convolution

Opération de base pour transformer une image

Cette transformation est définie par un kernel (filtre)

Elle peut produire un adoucissement, renforcer les angles, etc.

Convolution illustrée

http://setosa.io/ev/image-kernels

Comment prend en compte les pixels environnants pour computer le pixel lui-même.

Belles visualisation pour rendre cela plus clair. Version numérique d’une image une liste d’intensité de pixels. Peut jouer sur des niveaux de résolution différent. En circulant dans l’image prend la valeur et la combine avec des valeurs proximales calculées pour produire la nouvelle image.

Idée pas travailler avec mathématique, transformation de Fourier etc. mais seulement comprendre comment cette image fonctionne.

Gabor filters, detect orientation and scales of edges, good model pour le first part of V1 processing (brain)

Take Away messages : 

notre compréhension de la vision des images et sans doute plus complexe que les versions digitales (arrays of pixels). Ce qui rend le champ de la vision computationnelle si complexe. 

Digital images are a 3D stack

Convolution is an operation that transform images...

## Pratique

Buts se familiariser avec Jupiter

performer des opérations de base sur les images

jouer avec différente convolutions

https://cdh-dhlappc5.epfl

## What do art historian do ?

Projet depuis 2009

Computer vision formuler des questions de recherches qui soient pertinentes pour les deux champs. Savoir ce que nous définissons comme le style et définition des attributs du style.

Cam pcomputeres propel the understanding and reconstruction of drawing processes ?

étude du processus de dessin, puis modifications autres parties de l’image. Nous fournit des précisions sur les processus de production. Comparaison avec l’image originale.

Comment et quels gestes utilisés pour illustrer la communication légale. Quels gestes peut-on identifier. Image en deux dimensions et sans perspectives, pour autant challenge car des représentations de nature différentes selon les artistes.

Travail qui fournit des informations sur la communication gestuelles.

Projets qui montrent que possible d’analyser et explorer des corpus d’images numériques. Interface développée pour analyser des corpus plus larges. Algorithme de classification utilisé. Collection variée où peut sélectionner des objets d’intérêt. Sélection possible d’images pour identifier des motifs comparables dans le corpus. Interface qui permet de marquer jusqu’à 5 surfaces et lier ces surfaces entre elles. En tant qu’utilisateur, possible de donner du feedback au modèle pour marquer les exemples négatifs et positifs et relancer le processus.

Au moyen de ce genre d’interface possible de marquer et classifier grand corpus et trouver des similarités visuelles. Utilisation de DL méthodes et approches non supervisées pour étudier les similarités visuelles à différents niveau. Niveau de l’image, analyse globale, mais aussi séquences et aspects temporels.

Avec les développements du champs et de la numérisation de plus en plus confrontés à des grandes masses de données et se pose la question de savoir ce que l’on en fait.

Comment envisager les DH dans le futur, etc. 

Qu’est-ce qui manque en terme d’outils 

## The Media Ecology Project’s Semantic Annotation Tool and Knight Prototype Grant

https://news.dartmouth.edu/news/2015/12/mark-williams-and-media-ecology-project-receive-neh-grant

Digital curation university of Maine

Dimitrios Latsis pas pu être là, postdoc à Internet archive.

The Arclight, Media Ecology project. 

- Media thread
- Scalar
- Onomy.org pour faciliter la création de vocabulaires

Knight prototype grant. Équipe qui a beaucoup innovée dans l’analyse d cela vidéo. Possibilité de requêtes énormes dataset depuis Internet archive. Matériau publié.

Annotate Share Archive ! time based annotation. Pour annoter plusieurs sous clip. Une plateforme pour faire cela. Commencé à partir 100 aines de films éducatifs. Entraînement depuis Google Images.

[Waldorf.js](https://github.com/colejd/Waldorf) un plugin jquery, interface annotation. Annotation restent côté interface.

[Statler](https://github.com/VEMILab/Statler) server Ruby on Rails, Annotation aggregator, API-based interaction

## The mind of the Universe

https://www.vpro.nl/programmas/the-mind-of-the-universe.html

Navigation à travers les vidéos en "close reading".

Labellisation avec le thesaurus Unesco.

Modélisation des mouvements de camera dans les vidéo d’installation art. [Unfolded Cinematography](https://vimeo.com/210616907)

## CLARIAH Media Suite

http://mediasuite.clariah.nl

Un des workpackage, des outils que peut apporter au sein de l‘espace.

Outils qui supporte la critique de sources (quantités de sources, nb avec description, etc.), recherche, annotation, analysis, visualisation.

Possibilités de recherche quantitative mais aussi qualitatif.

AV player with annotation options connectable à diverses bases de connaissance : wikipédia, Unesco, possibilité créer son propre documentaire.

AV analysis services. Identification des locuteurs, détection des plans, extraction des éléments clefs des plans, reconnaissance faciale, reconnaissance des émotions, analyse des couleurs. Transcription du discours, etc.

## Using computer vision to describe material in the Graphic novel corpus

Plusieurs niveaux d’annotations. Subjective description. Objective description en relevant des aspects visuels. Reader-level description avec Eye tracking. Améliorer l'annotation automatique qui fonctionne bien pour le repérage des cases. Marquage du texte. Possible de 

## Mosaïc

Codé en pascal

http://mith.umd.edu/people/person/stephanie-sapienza/

## Aligning images and text in a Digital Library

Jack Hessel and David Mimno

Text and images, The British library corpus, why is this hard ?

Connection entre le texte et les images dans la production culturelle date de longtemps. Cf. vase grec avec inscription. Autre exemple Arp et poème.

Chercheurs qui cherchent à tracer la sémantique et l’esthétique à travers le temps et l’espace. Relever les influences et les allusions qui ne peuvent pas facilement être relevée. De même avec les images.

Prendre des images, toutes de la Nasa, navette, cosmonaute, logo. Toutes très différentes mais similaires car viennent toutes de la page wikipédia sur la Nasa. Le texte et l’image sont dont très différents.

De quelle couleur sont les moutons, un exemple classique pour le traitement automatique du langage. Pour Google Ngram Black. Mais si regarde les images sont plutôt blancs ou gris !

Previous multi-modal work

data sets 

- microsof common objects in contexte COCO : images labeled by anonymous workers on Amazon Mechanical Turk
- Flickr : Images with user-provided tags

Tasks

- boss modal information retrieval
- ..

Recent work

Pereira … voir dia

Exemple de la British Library. Avec numérisation de plus en plus de contenus mis en ligne. Contient aussi de plus en plus d’images. 

https://data.bl.uk/digbks/

texte scannés avec segmentation des image. Parfois problèmes d’orientation. Parfois cadres ronds ou ovales. Planches, vignettes, symboles, encadrements.

Pourquoi le traitement du lien entre l’image et le texte est-il si compliqué.

- variations dans la relation entre text et les images
- coco/flickr sont très alignés. Wikipedia moins
- les deux disponibles dans le patrimoine culturel mais alignement plus rare.

Exemple, image et légende. Veut que voit moi et la bibliothèque. Mais aussi l’arbre, les gens, etc. avec lesquels la machine va devoir faire.

Alignement texte et images. Utilisation des réseaux neuronaux.

utilisation de Resnet 50 et transforme en traits.

Pour les traits des textes, unigrams words, weighted unigram tfidf, etc. plusieurs méthodes.

LDA pour le texte, Resnet 50 pour les images. Comment les matcher ?

Volume-level holdout

Fait beaucoup mieux que random, etc.

Texte et topic générés. Plutôt du bon travail. 

Parfois moins bon !

## Visual trends in ads

Travail en cours à la bib des pays-bas.

Difficultés pour travailler sur les publicités. Rapport entre les publicités et les annonces.

Comment utiliser des aspects visuels des publicités pour les trouver dans un grand ensemble de journaux.

téléchargement par l’API gd nombre (1,6M) de pubs de deux journaux avec information sur leur localisation et contextes.Nb de pages qui augmente dans le temps. Journaux de plus en plus grands, et nombre de pub diminue en nombre. Dimension des publicités qui augmente dans le temps. Quelles position dans le journal. Mouvement du début vers l’arrière et de même.

Savoir le type de pub. Proposition des caractères en fonction de la pub. Permis de filtrer les annonces textuelles. Colonnes qui montrent que journaux très structurant (largeur des colones, etc.) Recherche de similarité.

Sur la pub mode, savoir si regarde l'évolution des annonce ou de la mode proprement dit.

Clusterisation par type d’image.

Travail sur l'analyse de topic. Langage très distinctif pour café, pour etc. mais difficile pour finance. Corrélation entre le visuel et le textuel qu’aimerait investiguer plus loin.

## Deep learning tools for foreground-aware analysis of film colors

Identifier l’innovation dans l’esthétique des fonds de couleurs dans les films.

numérisation et restauration.

Timeline of historical fils colors

db filemaker, mots-clefs, chaque segment analysé selon un protocole. Question des fonds très important pour l’analyse. Exemple robe rouge et fonds, très différent mur gris, ou fonds bleu. Mise en scène narrative de la star dans le film.

Semi-automati color scheme extraction

utilisation de TinEye Labs.

Yolo produit sélection de fenêtres sur les objets. Traitement de l'image comme un tout qui fournit meilleur contexte. Yolo très rapide. donc possible de penser détection en ligne.

Superpixel décomposition pour isoler les figures

## discussion

savoir si pas nécessaire d'avoir deux réseau parallèles, un pour la recherche l'autre pour la présentation; Car bien sûr contexte important mais pour le travail de reconnaissance, plus aisé de recadrer, etc. pour aller plus loin : ex visage avec type de moustache, etc.

rmq perso : en fait la stratégie pour les moteurs de recherche avec filtres et stemmatisation.



