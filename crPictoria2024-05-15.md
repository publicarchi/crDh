# Journée de lancement du Consortium Pictoria, 15 mai 2024

https://pictoria.hypotheses.org/1520

## Introduction

### Julien Schuh

Choix d’un logo : Rendre compte de l’idée d’image numérique, jouer sur les pixels, avoir une identité forte et s’inscrire avec les autres logos d’Huma-Num.

Rappel sur le périmètre et les enjeux du consortium.

Fédération qui partage méthodes, etc. Pas toujours possible utiliser outils industrie en contexte de recherche. Interprétation d’images et modélisation du traitement d’images. Se former à ces outils mais aussi transformer la manière dont conçus pour qu’ils correspondent à nos enjeux patrimoniaux. Le faire collectivement

- Cartographie
  - identifier les outils pertinents
  - mettre en avant les lacunes
  - orienter le dév de nouvelles techno
- Protocoles, référentiels et tutoriels
  - dév proto partagé
  - créer base de tuto
  - aborder questions éthqiues et juridiques
  - pérenniser les données et modèles coûteux
- Formations et ateliers
  - Accompagner projets existants
  - stimuler la réflexion interdisplinaire
  - contribuer à la formation de jeunes chercheurs
- Prototypes

Labelisé pour un an. Bilan pour 3 années supplémentaires.

Des outils faciles à prendre en main. D’autres à repérer ou développer pour les proposer aux communautés.

Feuille de route de cette première année

- 15 mai, journée atelier IA et images en SHS
- 26 juin 1ère séance séminaire-atelier, IA et IIIF
- 11 septembre 3e séance
- 17 octobre 4e séanre
- 6-8 nov DHNord Lille

On remercie le DataLab de nous accueillir pour l’organisation de cette rencontre. Question du partage d’images, métadonnées et multimodalité.

Présentation du site.

### Catherine Éloi, présentation du DataLab

https://www.bnf.fr/fr/bnf-datalab

Se réjouit de cette collaboration, important de travailler ensemble mais aussi nécessité d’intégrer les outils IA pour améliorer l’accessibilité aux collections numériques. La BnF s’est dotée en 2021 d’une feuille de route IA à l’initiative d’Emmanuelle Bermès accessible sur le site de la Bnf qui se donne pour ambition de conduire diverses actions à la Bnf concernant l’infrastructure technique mais également l’amélioration de l’accès et l’éditorialisation des collections numériques.

Gallica Image, projet clef de la feuille de route de la Bnf en partenariat avec l’INHA. Création d’une base de données des illustrations de Gallica, extraire, annoter images. Proposer API de recherche. 3 ans, objectif analyse de 250M de pages. Mais pas le seul projet mené par la Bnf, travaux en lien avec Teklia, recherches sur l’HTR.

Le DataLab une porte d’entrée pour les chercheurs aux collections. Conventin avec Huma-Num. Installations qui proposent des salles de travail de groupe et une infrastructure de recherche. Un lieu de résidence (Obtic). Appel annuel à projet.

## Jean-Philippe Moreux, IIIF et IA

Envisager le protocole d’ëchange IIIF dans un contexte d’IA.

IIIF et workflows IA, pipeline et workflow

Boîte à outils IIIF

IIIF pour la dissémination des jeux de données

IIIF pour la dissémination des jeux de données enrichies

### IIIF et workflows IA, pipeline et workflow

Le PoC GallicaPix

Expérimentations à la Bnf au tournant 2017-2018 avec plusieurs prototypes qui ont permis d’identifier qu’il s’agissait d’un accélérateur d’idées en permettant d’accéder directement aux images à partir d’URL en partant des entrepôts institutionnels ou en utilisant des outils commerciaux. À l’époque indexation d’images.

Aujourd’hui flux complet d’iamges. Corpora sélection...

Méthodologie aujourd’hui classique. Exemple des collègues de la Sorbonne sur des Ms enlumminés. ex. Illumination Déterction in IIIF Medieval Manuscript... Sorbonne.

Ex. Projet [rara magnetica](https://www.raramagnetica.de), Early modern magnetism image. Idem pipeline de traitement de l’image. Chaîne de traitement orientée sur la partie textuelle et une bdd compatible IIIF permettant de revenir à al collection pour déployer une activité scientifique.

Pipeline qui s’appuie souvent sur des outils existants, ici comme transkribus, Viskus pour visualisation IIIF. De plus en plus les pipelines s’appuient sur des outils existants.

2023, Utilising IIIF and IIIF and knowledge Bases for searching people within historical newspaper. Recherche patronimes.

Facilite les fonctionnalités offertes aux utilisateurs. 

Mais

- Pression sur les serveursSi les corpus sont massif, éviter les API.
- traitement d’images, si enchaînement d’étapes dans le workflow = faire une copie locale
- traitement du texte et des données : transformer les JSON IIIF

Projet [REMDM (Bnf)](https://remdm.hypotheses.org/le-projet-remdm), 2020. Identification de scripteurs de partitions imprimées. 

Workflow léger pour les HN Mezanno. Bnf, Epita, IGN, EHESS, 2024-2025. Préannotation automatique et annotation humaine collaborative dans un enviroenemnt léger.

https://www.bnf.fr/fr/plan-quadriennal-de-la-recherche

Workplow lourd : [PENSE](https://pense.inha.fr). Avoir à la fois un outils de travail et redéploiement et instanciation de la plateforme en fonction des contextes.

### Boîte à outils IIIF

IIIF aussi boîte à outils

- outils de transcription automatique, HTR et OCR : Transkribus, eScriptorium
- annotation : Mirado
- CMS pour les HN
- visualiseurs

### IIIF pour la dissémination des jeux de données et jeux de données enrichies

Corpus et jeux de données

- IIIF comme format de production et d’échange pour les jeux de donnée d’entraînement
- les collections IIIF et les annotations sont utilisées pour décrire les données
- les formats spécialisés deep learnin peuvent être dérivés (COCO, [Pascal VOC](http://host.robots.ox.ac.uk/pascal/VOC/), ...)

[Visual contagions](https://www.unige.ch/visualcontagions/) où annotations partagées en IIIF. Conservation du travail dans un format classique du patrimoine

[NewsEye](https://www.newseye.eu) projet de presse quotidienne. Jeu de données. Accès au dataset et corpus.

GallicaPix précurseur de Gallica Images. une fois les objets annotés, va avoir envie de fournir ces nouvelles métadonnées appuyées d’outils de consultation. Mais aussi laisser les utilisateurs valoriser ces données. IIIF permet de porter ces annotations.

Métadonnées consultables destinées à l’utilisateur du portail mais peuvent être utilisées par l’informaticien.

Possibilité de plus en plus utilisée : cf. [Biblissima+](https://projet.biblissima.fr/fr). Exemple requête sur la partie illustrée.

Vikus, visualiseur de collections IIIF. Déployé sur rara magnetica

Groupe de. travail au sein du consortium qui cherche à améliorer AIML https://iiif.io/community/groups/AIML/

Plupart des projets mentionnés éviqués dans

## Marion Charpier, Ontologie et annotation : bonnes pratiques et cas d’usage

https://www.linkedin.com/in/marion-charpier-033ba656/?original_referer=https%3A%2F%2Fwww%2Egoogle%2Ecom%2F&originalSubdomain=fr

Dans le cadre de la vision par ordinateur, l’ontologie un outil pratique pour définir les classes à annoter lers descriptions formelles explicites et précises de ces mêmes classes. 

Les propriétés de chaque classe décrivent leurs diverses caractéristiques et attributs ; les restrictions énoncent...

Conception du jeu de données en computer vision

- étape cruciale : conception doit répondre à la problématique initiale
- objectif : garantir la formationd ’un module robuste et adapté
- enjeux : 
- critères fondamentaux : diversité et varité, représentation équilibrée pour représentation optimale

Principes de l’ontologie en coputer vision

Restructurer l’approche pour pouvoir faire ressortir les concept qu’esssaye d’aborder. Doit concevoir approche rigoureuse qui va permettre annotation homogène et efficace.

- Transparence pour assurer homogénéité
- Transmissibilité
- Rigueur pour éviter les biais potentiels

Repenser l’ontologie et l’affiner.

- cohérence sémantique et cohérence dans l’annotation
- précision : réduction des erreurs
- exhaustivité : étiquetage de toutes les instances (qui des scènes complexes, etc.)

Processus long et chronophage, nécessite grande rigueur dans l’annotation.

Exemple du projet Royère au MAD. 18 000 documents.

Pb chevauchement des différentes classes. Définition première classe. Or, confusion entre objets. Ajouts parfois ajout de classes discriminantes pour éviter biais (confusion lampe et plantes).

Annotation un travail très long donc éviter aller-retour même si souvent difficile.

Classification faite par Jean-Royère lui-même de son archive. Besoin de recalibrer. Tables de salon, table basse ou guéridon que ne pouvait décliner avec un modèle.

## Christopher, Les outils open-source de Teklia

Une plateforme de traitement de documents dévelopée par Teklia depuis 2019 (début activité commerciale). Traitement numérique de documents. Utilisée pour 60aine de projets.

- traiter tout type de documents et personnalisation
- passage à l’échelle, traiter 1000 à 10M pages
- open-source diffusion et particiaption de la communauté

Pas un outil spécialisé.

Arkindex et Callico : un pari pour nous de les rendre open-source. Aspect opensource nouveau (avril). Communauté qui doit participer au développement de ces outils pour que fonctionne.

[Arkindex](https://teklia.com/our-solutions/arkindex/) stockage et gestion de documents : importation par interface web pour pt corpus, ou protocole de transfert de fichiers (Amazon S3) et support IIIF. Support de format simages et PDF. Structuration hiérarchique des corpus complèteemnt adaptable. Gestion des métadonnées à tous les niveaux. Visualisation, navigation.

[Callico](https://teklia.com/our-solutions/callico/) : Annotation et validation

Zonag, calssification, transcription, indexation clé-valeur (sans nécessairemnet localiser la valeur), entités nommées, groupement (groupement d’objet par exemple pour articles de presse)

Traitement en masse et industrialisation. Volonté de pouvoir traiter n’importe quel type d’algorithme et de pouvoir le déployer sur n’importe quelle plateforme. Communication avec ArkIndex par l’API.

Plusieurs projets menés

SOCFACE utilisation supercalculateur Jean Zay

Projet HikarIA, Musée Guimet 2023-2026

Tellement de modèles développés par des institutions qui ont plus de moyens de nous. Important de pouvoir développer l’infrastructure pour les évaluer ou les utiliser. Partie connaissance méteir sans doute la plus importante.

Teklya et l’Open-Source. Outils de Deep-learning. Ensemble des modèles développés que met sur Hugging Face.

Idée de dire que le plus important la plateforme et expertise (accopagnement de projet) qui fait que peut donner accès à tous ces éléments.

## Questions

-  Format Métadonnées IIIF
- Piste avancée par **Matthew Lincoln**, Carnegie Mellon University

Système souple de clef-valeurs. Mais pas de formalisation ni perspective d’intégration de standards préexistants. Chacun reste enfermé dans le formalisme qu’il a choisi.

JSON-LD pour Linked-art. Mais pour le moment seulement possible de lier.

Ontologies terme très polysémique. Bien explicité les classes mais quel formalisme allez-vous utiliser pour expliciter l’ontologie dans l’interprétation ou bien seulement limité aux classes.

R. ne va annoter que les classes. Simplement les informations en amont.

D’un point de vue terminologique plutôt un thesaurus. 

Modèle pas là pour intégrer toute la connaissance sémantique que l’on a des objets. Enjeu de la recherche.

Pas du tout la même définition de l’ontologie dans le monde du computer vision et du monde sémantique. Sans doute un enjeu ici pour poser des définitions.

Dans quelle mesure les stratégies d’annotation développées par les thesaurus iconographiques sont-elles réutilisables dans ce contexte. Ex. thesaurus Garnier, etc. Dans tous les cas, nécessaire de redévelopper une stratégie. Enjeu de spécificité liée à un corpus existant : mais risque de biais et d’erreur. Par exemple dans Mandragore des objets annotés comme dragons qui n’en sont pas. Dans la computer vision, peut être pas de sens de vouloir être générique. Concentré sur un projet en particulier plutôt qu’une volonté d’ouvrir de manière large.

Teklia, essayé d’utiliser des modèles de description iconographiques pour étiquettage textuel. Par contre pour définir scènes fonctionne assez bien. Alors possible de rentrer dans du détail.  Sans doute un grand intérêt à pouvoir réutiliser tout ce qui a été fait sur la structuration des vocabulaires iconographiques.

## L’IA dans les Sciences de l’information géographique, exemples d’application sur le cadastre napoléonien

En information géographique, la télédétection a constitué un moteur considérable avec la ce qui a été appelé la classification automatisée pour le traitement des images satellitaires.

Application de l’IA en cartographie IG

Ségemntation sémantique, utilisation IA dans une chaîne de production pour améliorer la classification du sol à grande échelle. Automatise la chaîne de production initiale pour l’amélioration des données.

Approche pas seulement développée en géographie mais aussi en agriculture ou métérologie. Ou encore pour la détection des piscines par les impôts.

L’IA arrive également dans les outils géomatiques. ArcGIS Pro propose ainsi de l’analyse automatique d’images : classification, détection d’œbjets, segmentation sémantique, d’instances ou d’objetss, segmentation panoptique, conversion d’images, etc.

QGIS package. R, etc.

Tous ces outils sont développés pour de l’image satellitaire ou de la photographie aérienne mais pas développés pour la cartographie ancienne qui reste le parent pauvre.

Ambittion du projet [Veccar](https://www.msh-vdl.fr/projet-veccar/) financé par le réseau des MSH, puis projet Canapé? (Tours).

Projetd e vectorsier le cadastre Napoléonnien. Pas exploitable sans interprétation pour traitement dans outils de gestion cartographique. Processus qu’appele vectorisation.

Cadastre Napoléon, beaucoup de variété de documents, de textures de documents. Supports de qualité variable, style graphique variable, qui pose la question de la généralisabilité du traitement.

L’objectif est d’extraire les limites cadastrales à partir de ces données vectorisées manuellement. MSH Sud-Est île-Rousse. Vérité terrain pour alimenter apprentissage des réseaux de neurones.

Deux solutions ont été développées inspirées de l’état de l’art et benchmarkées sur nos jeux de données.

Méthode 1 : détection de contours. Méthodes simples ancien temps avant le deep Learning.

Mais besoin adapter car pour un algo complet adjoindre algo de remplissage. Utilisation méthode développée dans SODUCO, méthode proposée par Chen, Chazalon, Mallet et al.

Architecture BDCN, alimentée par annotations.

Résultat : détection de limites de parcelles assez précises, lorsque choses bien définies. Mais des problèmes pour les parties fines : route sursegmentée, découpes problématiques. Mais globalement intéressant.

Sortie qui ne convient pas directement à l’utilisation d’un géomaticien. Posttraitement ou méthode différente à utiliser ? Se heurte au fait que la quantité de données difficile à obtenir car besoin de vérités de terrain.

Méthode 2 : Segmentation panoptique

Objectif rechercher les objets différents : zones et opbjets. Architecture du réseau Mask-RCNN Détectron 2, MetaAI.

Utilisation du formalisme COCO. Récupération des données. Détecter les instances de parcelles dans les images.

Résultats : on observe un bon niveau de confiance dans le modèle pour la prédiction. Tracés floux et non continuité des parcelles. Mais observe que des parcelles sont oubliées. Sur-segmentation (pour l’exemple de Ile-Rousse). Si veut compter les parcelles ok, pour déliminations, moins bon.

Fichiers sources qui posaient problèmes (artefacts de numérisation). Essai avec autres fodns de meilleure qualité.

Évaluation de la généricité. Application sur autre ville Féjus. Résultats intéressants.

Cas difficiles pour évaluation. Numéros de parcelles qui viennent géner la détection. Erreurs graphiques. Néanmoins des résultats intéressants avec des problématqiues dans les zones les plus contraintes.

Idée de pouvoir reprendre les données en SIG et de les coupler avec des informations différentes. Exemple couplaga avec LIDAR. Idée de pouvoir disposer de données enrichies pour autres analyses.

Continuer à travailler. Consortium PictorIA. ANR Communes. OpenHistorcial Map!

## Jean-Christophe Carrius, INHA

Trevor Paglen, The Treachery of Object Recognition, 2019. © Trevor Paglen, Courtesy of the Artist; Metro Pictures, New York; Altman Siegel, San Francisco.

INHA une institution de recherche mais aussi une collection, volonté de produire des données enrichies.

Projet qu’évoque pas né avec l’IA comme sujet principal. Voir comment un projet qui procède plutôt du web sémantique va entrer dans une nouvelle ère en se servant de ces outils.

Privilégie l’utilisation de l’appelation Intelligence machine à IA cf. Yann LeCun

Exemple document Lettre autographe de Félix Buhot. Document visou-textuel. Question multimodale importante.

Reconstitution numérique de la boîte d’archive enrichie par le travail de la recherche. ex. Papiers Barye.

Projet de design thinking. Pas beaucoup utilisé HTR, car plusieurs scripteurs. Mais aussi rendu compte qu’étape de transcription considérée utile pour les chercheurs. Temps d’imersion dans la source. D’autant que souvent les erreurs pas agréables à traiter. 

Collection Karbowsky. Image as a database.

Le fait que transcrive littéralement les documents ne correspondait pas à son usage. Transcription normalisée vs transcription automatique littérale. Interroge sur l’endroit où va utiliser intelligence machine.

Développer plusieurs niveaux de lecture d’une même source. Mener un travail sur la dimension restitutive et mise en scène, format d’édition important.

Travail sur l’intérgation d’une visionneuse IIIF à l’INHA. Projet PerVisum pour déveloper un format d’article visuel. Mettre l’image au cœur de la démonstration avec IIIF en gardant la notion multisulport. Peut présenter les choses de manière immersive. Mais veut aussi pouvoir en générer la version PDF interactive.

IIIF et open web annotation au centre du modèle. 

Penser l’annotation des images. Meta découpe la forme, la décontextualise complètement. Va devoir réfléchir à ça.

### Discussion

Comment des outils pourraient aller vers une représentation plus fine des objets mais aussi des classes. Avoir différents nievaux de conceptualisation et des objets, en ouvrant à la contextualisation.

Facettes d’observation d’un objet. Par le biais d’ontologie pouvoir raccrocher les wagons. Besoin de spécifique et classes définies pour faire apprendre le modèle.

Dans le projet présenté par JCh, idée de pouvoir réfléchir dans le contexte d’un corpus et de la manière dont va présenter la données dans un contexte spécifique. Rêve du web sémantique, que tout le monde va pouvoir parler avec tout le monde.

Tension entre un monde spécifique et monde général. Dans nos projets, il peut donc y avoir une tension entre le fait de répondre à un usage spécifique et de l’autre de se dire qu’on a un corpus à disposition et que les chercheurs puissent y mettre leur nez pour disposer de grandes masses de données.

En cartographie généralisation, un jeu d’échelle. Doit donner accès au jeu de données et à l’intérieur de l’ontologie donner accès à des données spécialisées.

Dès les années 2000, on appliquait des algorithmes pour la rectification topologique. Avez-vous pu développer des outils d’apprentissage profond pour pouvoir travailler sur la rectification topologique ?

Pour le moment limités à la reconnaissance des bordures mais apprès évidemment des méthodes différentes seront nécessaires. Des modèles qui évoluent rapidmenet. Ici choses testées il y a quelque temps. Doit continuer à tester d’autres modèles.

Graphiquement une parcelle, un chiffre, et une limite. À partir d’une définition sémantique, peut être possible de coupler ces informations pour éviter les erreurs. Mais en pratique compliqué à mettre en œuvre.

## Atelier DIY

Trois approches

- plateforme commerciale RoboFlow, pas d’enjeux en termes de développement. Charge images, entraîne un modèle et passe en production.
- scripts Python en environnement Collab

### RoboFlow

Détection d’objet et classification.

- préparer des images

Segmentation : Identifier des portions d‘images qui représentent des objets spécifiques.

### Similar images

https://gitlab.huma-num.fr/jschuh/pictoria

Comment télécharger notebook et l’installer localement ou sur un serveur à distance avec Google Colab

Un notebook qui sert à trouver des doublons ou de la similarité. Au départ graphiste ayant utilisé des fragments d’image sans garder la trace. Collection de 50 000 images. Une tâche de computer vision courante.

- représenter chaque affiche par un num 
- les représenter dans un espace vectoriel
- aller chercher les vecteurs les plus proches

Outil qui prend un dossier dans le Google Drive

En réalité pas vraiment besoin de savoir coder. Connaître les outils qui existent et savoir expliquer à la machine ce que l’on veut faire. Si vous pouvez expliquer de manière très précise ce que veut faire fonctionne vraiment très bien.

Utilisation de ChatGPT4 avec un prompt.

Montrer comment fonctionne, et comment dialogue avec ChatGPT pour corriger les choses jusqu’à ce que cela fonctionne. En anglais.

- écrit un script google colab à partir de ceci (renvoit à un outil google de reconnaissance faciale) pour vérifier... utiliser une interface Gradio (penser à faire attention à utliser dernière interface) et fichiers.
- le plus souvent ne fonctionne pas de suite

Quand on a une erreur, la renvoyer à ChatGPT

## Exploration

Valentin Chabaux, outil développé dont a décidé de faire une interface pour le rendre disponible à un public pas forcément programmeur. Fonction d’explorer un corpus d’images sémantiques et textuelles pour faire des requêtes textuelles sur un corpus.

L’idée est de pouvori comparer une chaîne de caractère et une image. Ex. Château. Intéressant car peut travailler pas que sur des images mais aussi des images tagguées ou légendes. Permet donc de gérer plusieurs cas de figure.

Compte Google pour avoir accès à un Google Drive et un Google Colab. Plusieurs opérations pour tester un corpus préparé. 

https://github.com/vchabaux/Smantic

Outil en cours de développement, afficher le ipynd et ouvrir dans Google colab

En haut, type de processeur. T4 processeur 

Pour créer les corpus, préférable d’avoir GPU. 1 minute par image, ridiculement long. Le faire tourner au départ ou personnelle avec GPU. Se connecter sans GPU car heure de pointe.

Possibilité d’entraîner sur gros corpus et ensuite partager avec d’autres les résultats car la recherche beaucoup moins coûteuse.

Plusieurs recherches possibles : images, texte et image. Modèle entraîné sur des termes anglais. Il peut y avoir des erreurs de traduction, d’où les options.

Ici meilleurs résultats si ne traduit pas. Sauf si recherche d’images.

Pas de la recherche lexicale mais de la recherche sémantique. On pourrait en combinant des termes créer du sens. En recherche d’image n’utilise pas la traduction.

Force du modèle, est qu’il est capable de lire du texte dans une image. 

Si on crée un corpus à partir non pas de fichiers locaux mais des adresses. Seulement à partager le lien du smantic pour faire le partage.

Créer un corpus, trois possibilités.

- utiliser un dossier d’image
- utiliser un identifiant ark (gallica + légendes)
- utiliser un fichier csv légende et images soit avec des images en local ou internet

Un bug, doit ajouter dossier TMP dans le répertoire Google pour travailler sur la création d’un corpus.

Utilisation de Blip2 pour l’analyse des images. Blip un modèle très installé pour la recherche de similarité texte et image. Version 2 sortie récemment, très efficace. Fonctionne mieux dans ce sens que dans l’autre. 

Un modèle qui peut fonctionner pour faire de la génération de texte à partir d’images mais ne fonctionnera jamais mieux. Un LLM entraîné en sortie pour générer les textes. On pourrait donc s’amuser à faire de la documentation automatique.



## Divers

Valentin Chabaux Gradio

https://www.parisnanterre.fr/valentin-chabaux-1

https://www.linkedin.com/in/valentin-chabaux-b021ba217/?originalSubdomain=fr

https://github.com/vchabaux

