# PictorIA

Une intiative sciences humaines et sociales. Cluster de recherche. Pas d’initiative comparable aux US.

Canada CRKN initiative.

Question disciplinaire. Actuellement essayent de relier communautés disciplinaires : archéologie et histoire de l’art. Certains intérêssés par annotations, autres géomatiques. 

Liens avec autres consortia : Ariane for text, Time machine, etc. 

## Léa Maronnet

Utilisation de Segment Anything 2 clusturing model pour accélerer le traitement. Personnalisation des annotations.

Production de masques multiples qui ont été évalués.

Mais pas de création de labels, seulement masques. Pour parvenir à régler ce pb, comparaison de similarité. 



Questions : 

- Comment fonctionne dynamiquement ?
- Question nb segment et réglage.
- Des possibilités pour améliorer pour les besoins du projet

Plus similarité que clustering non supervisé

Chaque segementation en réalité une interprétation des motifs que veut analyser. Besoin de conserver hypothèses et schemes cognitifs. 

## Ancient classical

Several areas of interest

Corpus où image est centrale. Intérêt dans les images et annotations.

Segmentation des figures sur vases grecs. Combinaison de personnages peut aider à la compréhension des narrations. Mais possible aussi que soit intéressant pour définir le style ou l’origine des images.

Postures et relations entre les personnages, enjeux de polysémies.

### Discussion

Avec les changeemnts sir réguliers du langage comment maintient 

## Yale Collections

What is LUX, cross-search collection system. 17M objets, 5M people, 546 948 places.

En production très peu d’information générée par ordinateur. Notes descriptives

Récupération du contexte pour fournir informations en traduction. Utilisation d’un modèle ouvert. Schema2 ? Essai d’autres. Pas de personnalisation particulière.

Images et IA. Un système image basé sur GPT4o. Pb usage interne. mais aussi Google Cloud avec Vertex API.

Digital collections IA.

N’importe qui peut traiter information. Extraire autant d’informations possibles pour localiser texte offensif. 

Version basique, utilisation GhatGPT et Claude 3 Haiku. Cheap mais noisy.

Donc exploré autres solutions. Modèles de Google. Vertex AI. Gemini 

Culture-heritage-project

Handwritten and printed text

Catalogues de ventes

Pb coût déterminer à quel modèle founi les documents en fonction des besoins. 

Pas encore en production.

Human in the loop dans le système de provenance. Pour valider l’information et baseline understanding. Sinon question de savoir où les ressources ou pas. Question good enough.

Utilisation du knowledge graph pour améliorer.

## Symposium

13 personnes en présence

En ligne : Peggy Davis et Kyrie Bouressa en plus d’Alice, Béatrice

### Facing Black Star and Beyond

Thierry Gervais. Nombreuses publications. Histoire de la photographie dans la presse.

Image Center avec photographies du Blac Star. Collection acquise par Ryerson en 2005, 6 000 photographies du 20e siècle. 292 000 imprimés NB. Quelques photographes très connus, Cappa, Cartier-Bresson, etc. Considérés comme les pères du photo-journalisme.

Bâtiment 72M, ouvert en septembre 2012. https://theimagecentre.ca

Collection qui réside au cœur de l’institution. IMC trois composants : Galerie, research and collection.

Pas seulement la collection BlackStar. Bérénice Abott Archive, Virginia Woolf archive, NY Times archive, etc. Aussi une collection de magazines comme Life complète. Collections de presses, etc. Picture post, Illustrated Weekly.

21 exposition chaque année. 

Facing Black Star, production du département de la recherche de l’institution. Existe rarement. Un essai d’avoir un secteur recherche à côté CPI Canadian Photography Institute à la Galerie nationale du Canada. Une manière de garder la collection vivante, d’autant plus que collection située sur le campus.

Student workshop. Symposium dédiés histoire-géographie de la photographie. Collection de série de livre IMC book serie publiée avec MIT Press.

Images différents formats, et exemplaires. Exemple image célèbre retournée. Différences dans l’impression. Question valeur vintage, etc. 

Chercheur capable de regarder 200 images par jour. Aurait besoin 146 jours pour parcourir la collection soit 8 mois plein-temps. Donne une indication du problème.

Enjeux pour naviguer ensemble des images. IA présenté comme solution pour naviguer ensemble du corpus.

Algorithme pour matcher presse dans la presse. Numérisation à grande échelle au cours des dernières années.

DataSet produit pour nbses années.

retouche photographique pas conçue pour être visibles. Retouches produites dans le cadre de travail. 

Ne pas seulement considérer les photographies comme sujets mais comme objets de l’histoire.

### Chantal

Automation an IA accroît efficacité du catalogage.

Connaissances Black Star. 77% numérisé. Nombreux de pb rencontrés sur les qualités de numérisation. Depuis 2005 changements normes et stds de numérisation. Nous a obligé à refaire grande partie du travail. Problème d’espaces de stockage, etc. Souvent retour original. Peut être frustrant pour accès.

Relation froter avec photographe propriétaire companie spécialiste de la numérisation de photographiques. Demande subvention avec eux. Idée développement outil IA pour mots-clefs à la fois en anglais et français.

Une table tournant avec zones de numérisation. Un système hydraulique pour maintenir les documents en position basse. Plusieurs caméras agissant sumyltanément. Tourne et flash. Une personne charge, une personne décharge, une autre monitore le système.

Manipulation des collections rend souvent les conservateurs nerveux. Le fait que monte et descende peut faciliter travail. Répétition pour économiser le temps.

Groupe travail pour spécification numérisations FADGI. Beaucoup pousser pour spécification.

Enjeux état de conservation, choix faire un seul côté de l’objet. Avec images de presse. Temps de traitement beaucoup sous-estimé. Traitement manuel.

Développer protocole IA.

Images avec marques de travail pour cadrage, etc. OCR qui extrait qqch d’étrange. Image de Apollo, etc. Pas encore cataloguée car besoin de réviser information.

Pour les collections. Commentaires des catalogueurs sur diffficultés.

Avec IA pas de line breaks, pas de localisation. Pas d’indication sur type écriture. Mais pas mauvais.

Gemini pro, questions modèle de langue utilisé. Pas parfait mais rend plus rapide processus pour le catalogueur.

Actuellement besoin de travailler avec un vendeur ou alors de développer nos propres outils. Accès recherche très spécifique, étude culture visuelle. Nouvelles manières de cataloguer que doit considérer. Possibilité d’ajouter des informations.

Comment ouvrir ces données largement alors que mots-clefs produits automatiquement. Quid éthique, biais, etc. Question colonialisme et catalogage.

Plus de questions que de réponses. 

### Discussion

Question dimensions parfois compliqué car plusieurs mesures. En réalité, automatise déjà cela en partie.

IA entraînés pour identifer le sujet plus que l’objet. Souvent images qui sont le mélange de différents médiums. Marques, etc. Image numérique que voit un peu dans le vide, en réalité utilisées de manière spécifiques : imprimées dans un format pour être manipulées, etc. Pinceau rouge très lié à la presse. Pourquoi retouche des photographies ? Pourquoi risque de mettre en cause authenticité à ce point ?

Pas de vocabulaire formel pour les matières. Souvent pas pertinent pour la photographies.

Qui créée les titres ? Dépend de comment été utilisé. Travail des catalogueurs mais aussi travail des curateurs pour définir titre. Devient un titre d’exposition.

Catalogage qui pose toujours difficultés. Difficile à utiliser pour la recherche. Car initialement conçu pour trouver images dans le stockage. Pas un outil de recherche. Bien sûr change, car accessibilité en ligne, etc.

- Comment distribuer les images pour traitement IA de manière pertinente ? Comment partager les résultats du travail déjà mené ?
- Collection Search

Ensemble des données corrigées, enregistrées dans un champ spécifique pour pouvoir repérer problèmes éventuels. Champs qui restent interrogeables même si pas présentés en tant que telle.

Pb attribution sur laquelle pourrait utiliser IA. Autorship souvent pas considérer à cette époque.

Event date et photography date. Pb vintage, etc. Aussi des photographies artistiques dans la collection, oblige à réfléchir à ces questions également. 

Contrat signé avec vendeur nous indiquant que pas le droit de partager l’information.

Encore nouveaux dans le domaine de la photographie. Pour le moment pas encore approchés par grands acteurs.

Problème d’échelle, institution relativement récente. Enjeu de dimensionnement.

## Béatrice Joyeux-Prunel

Université de Genève. Artlas depuis 2009. Postdigital 2016. 2019, Jean-Monnet excellent center...  Visual contasions.

Nombreuses publications.

A Corpus for the study artistic globalization

Artlas assurer que données utilisées pour thèse et publication puissent être utilisables pour d’autres. Catalogue exposition, et mise en commun. Penser nos jeux de données partagés pour analyse statistiques. Création de visualisations cartographiques pour autre analyses.

Bazart 2016, glbal database of artistic catalog. Transcrire le contenu des catalogues en bases de données. 

- Travail qui réclamait grand temps de travail et coordination internationale. 
- Difficultés pour inclure les images de ces catalogues

Deux objectifs, d’abord convertif images en texte. Ensuite indexer images. 

Enseignement des DH avec BasArt pour transcription des données et renvoi. Genève étudiants appréntissage à travers diverses étapes de travail. Principes FAIR, et recherche ouverte.

Sur extraction 2017, demande aide collègues extraire images. 2018-2019 tests sur les contenus visuels pour analyse culture visuelle. Exemple thèmes sur différentes œuvres très connues de l’histoire de l’art. Images de Venise.

André (collègue avec qui mené ces premières expérimentations) entré récemment en EHPAD en Belgique, espère que bien.

Nous a conduit à concevoir nouveau projet. Visual Contagions project. Objectif comprendre comment les images joué un rôle dans la globalisation des images. Ce que révèlent de la conversion du matériau culturel.

Cultural analytics, souvent limitées à des corpus bien identifiés. Rôle globaliser recherche. Distant viewing, K Bender et Moretti, Impett.

Mais nous construire un corpus pertinent pour l’analyse de la circulation des images. Ne pouvait se contenter d’images issues de wikipédia ou des musées. Mais sources numérisées. Sources imprimées qui restent un réel challenge.

Capacité d’étudier images à grande échelle. Permet poursuite du travail. Idéal Corpus, illustrated periodicals. Assemblement corpus sur longue période alors possible.

Soutien du Fonds national Suisse.

18 723 périodiques. 3,6M IIIF documents. Nombreuux pays, etc.

Segmentation pour extraire les illustrations de chque magazine. Ne rentrera pas dans les détails. Mais convertis en images accessibles à travers protocoles interopérabilité.

Traiterment algorithmique ensemble du corpus et illustrations documentées avec coordonnées.

Ensemble projeté de manière vectorielle. Groupement statistiques pour identifer dans l’espace les différentes similarités dans le temps et l’espace.

15,4M illustrations extraites de 4,767 journaux, 1243 villes. Un corpus destiné à la machine. Faux positifs etc. comme tampons bibliothèques, etc.

Extraction images similarité : second corpus machine. Regroupé par similarité algorithmique. Groupement clusterisation. Provenance tracking, distinction provenance.

Images qui partage similarité (recadrage, etc). Images rassemblées par similarités car proches ou mise en page propre.

Développement d’une plateforme accèssible ouvert pour consulter ensemble des images qui peuvent être déployées en ordre chronologique, par proximité, etc. Données qui sont également téléchargeables. Utilisation explore pour étude du corpus. 

Collection de séries d’images nettoyées et étudiées. Possiblité de revenir à l’image et la source de chaque image.

2022 première présentation résultats dans une exposition et espace numérique. Les images dans la mondalisations. Publication de plusieurs articles. Art le type d’images qui traverses les frontières le plus facilement parmi les contenus visuels. Autre études sur circulation images de modes, publicités, etc.

Les images qui ont donné forme à l’Europe.

Corpus qui continue de grandir alors que ajoute contenu. En juin 2024, circulation image du Léopard.

Comme Warburg 100a utilise méthodes images. Adresser questions comment images circulent comment interpréte série. Comment construire séries qui ne réflète pas ...

Limitations de notre œuvre. Limité pour commencé en contenu, lié à la géopolitique des sources numérisées. Principalement européen et NordAm. Et même en Europe pas égal. Sans parler du sud global. Autres pays où les scans pas facilement accessibles ou pas dans des formats standard. 

Déployé une chaîne automatisation

*Visual Contagions IIIF Pipeline* notebook pour accroître corpus

https://www.unige.ch/visualcontagions/explore

Limites aussi chronologique. Blakhole.

An unbalanced social distribution aussi.

Problèmes de déséquilibre aussi dans le contexte de la nature du corpus. Homogénéisations, etc. Normal de poser question diachronique. Mais parfois mauavise réponse.

Dans l’art et histoire culturelle. Tentation diffusionniste. Vision difficile à contourner. Questions styles et influences. En cherchant simularités, approche computationnelle qui renforce ces tendances.

Chaînes de circulation qui renfoercent ce modèle généalogique. Chaînes de circulation chronologiques. Quid primitive image ? Notion influence ? Approches numériques qui suppose transition entre plusieurs états de reproduction, et pièces.

Questions points de départs et arrivée.

Souvent impression que Paris au centre. Arrive souvent au centre. Mais peut-on inférer premiere à produire ?

Mais parfois pas possible identifer liens qui justifierait influence de peintres français sur art allemand. Pourtant similarité visuelle.

Opposition domaine. Dominance impressionnisme. Dans les deux cas utilisation images. Réaction élitisme. Formalisme et construction automatique des données peut rendre obscure.

Diffusion des images fondées dans des facteurs humains et sociaux, quelque chose qui manque dans les corpus numérisés. Pour améliorer doit pouvoir ajouter autres paramètres : sociaux, économiques, etc.

Il n’existe pas un seul corpus. Ceux-ci évoluent constamment. Question interopérabilité. Celui produit par la machine ? Celui par clusterisation ? Celui produit par nos annotations. Rien fixé.

Nouveau corpus. Et méthodes.

Méthodes qui sont inhérentement trompeuses ou risquées. Cross references, méthodes, et formulation des hypothèses.

Plusieurs corpus disponibles. Comme question open access, login pour bénéfier autres corpus

https://visualcontagions.unige.ch/explore/

### Discussion

Projet fantastique qui a permis de réunir un corpus extraordinaire. Je me demandais à quelles utilisation secondaires vous aviez déjà pensé (même si pas à vous de le faire) ? Question de savoir comment mobilisable informatiquement ?

Fantastic project that has brought together an extraordinary corpus. I was wondering what secondary uses you had already thought of (even if it’s not up to you to do it)? Just curious to know how it could be mobilized digitally ?

Comment mobilisable informatiquement.

Précautions épidémiques débouchent sur quelles précautions dans la production des corpus.



## Remarques finales

Question de la création des corpus d’images pour l’IA.

Enjeux divers selon les mat2riaux que l’on traite

Enjeux de numérisation et matérialité des objets avec lesquels travail

à travers réduction à un plus petit dénominateur commun documentaire, IA qui peut être mobilisée pour réaccéder matérialité du corpus

Catalogage et IA. Cf. Human in the loop

## IIIF and Linked Art, Putting the AI in FAIR

Task force on AI. 

https://ai.yale

Principes et std. FAIR, LOUD, IIIF, Linked Art. Image Use Cases, cultural heritage and AI.

Putting the FAIR in AI. Fair data as necessary input.

Principes FAIR

- Findable
- accessible
- Interoperable
- Reusable

Ensemble de fonctionalités pour rendre les données plus facilement accessibles. Traiter les données de manière automatique. Besoin être interopérable. Réutilisable car provennace de données, comment créées et licence claire.

LOUD Linked Opend Udable Data. U for usability U qui a largement manqué dans la discussion sur le linked data au cours des dernières années.

À quel point les données utilisables sur le web. Si pas utilisable pourquoi fait-on ça.

LOUD’s Audience is Developers. Typiquement dit que les développeurs mais un état intermédiaire, les développeurs. Forte interaction avec les chercheurs. Usability notion cible développeurs qui construisent les systèmes où les chercheurs utilisent les données.

Des principes de dsign

- scope design through shared use cases
- design for international use
- make easy things easy, complex thing possible
- avoid dependency on speecific technologies
- uses REST / don‘t break the web / don’t fear the netwoer
- design for JSON-LD using LOD principles
- follow existing standards & best pratices, when possible
- define success, not failure
- separate concerns, keep APIs & systems loosely coupled
- adress concerns at the right level

IIIF d’abord et avant tout une communauté. Develope des APIs, application programming interfaçe. Aime les penser comme un argument qui précède une interaction. Formaliser des interactions entre deux ingénieurs logiciels pour échanger sans couplage. Implémente des logiciels et expose des contenus interopérables. Plusieurs millions images disponibles.

- Exemple hyperzoom.
- comparaison images dans organisation ou à travers des institutions en raisons de sa nature API
- annotation composant fondamental

Important pour IA aussi car annotation pas seulement commentaire humain. Peut utiliser ces annotations pour entraîner des modèles, ou produire les résultats.

Including for full text. Annotation aussi utilisées pour la transcription, les commentaires. Ensemble des contenus qui peuvent être encodés comme annotations pour être cherchées ou présentées à l’utilisateur. 4 APIs principales, Image, presentation, auth et search. Presentation API intrinsèquement pas sémantiquement, conçue pour l’utilisateur de manière à comprendre l’image plutôt que pour proposer des métadonnées.

Explicitement conçu pour cela. Sans doute une des raisons pour lesquelles succès car pas eu beosin entrer discussion dans quelle manière discussion comment décrir ms médiévaux, œuvres arts.

Néanmoins description reste nécessaire. Pour cela un autre std Linked Art.

Sémantic profile API conçu collaboratimvement pour la description objets, œuvres, personnes et lieux. Fournit stds métadonnées...

Linked Art : Usability vs Compleness. Pas cherché être maximum utilisable et complétion. Essayé de maximiser les deux.

Approche fondamentale ne pas être centré sur les objets mais sur des activités. Les activités qui produisent la culture. Alors facile de dire qui a fait quoi ou et quand. Et encore de classifier activités des acteurs.

D’æutres relations nécessaires pour rendre cela utilisable. Exemple exemplaires photographies. 

Linked Art APIs follow the FAIR and Loud design principles pour faire des choix sur efficacité pour gérer des interractions avec de grandes quantités de savoir dans un graph.

- En particulier JSON-LD, usabilité alors que LInked Data
- [W3C Activity Sreams](https://www.w3.org/TR/activitystreams-core/) / [IIIF Discovery API](https://iiif.io/api/discovery/1.0/) pour moissonnage et lister les résultats
- pas de langage de requête mandataire

Exemple jeune stagiaire, appropriation très rapide.

### Images and AI

Interagîr avec AI. Comment envisage interactions avec IA. Nombreuses images, mais aussi documents, données structurées et audio. Données générées. 

Tâche plus utile, transcription du contenu. Description des entités, résumés, classification, traduction et reconnaissance entité nommées.

En même temps souhiate que le système soit prédictible, reliable, performant, affordable, ethical, explainable, multilingue.

Impact environnemental dans le fait de faire tourner machine. Tâches que les humains peuvent mener.

Exemples de cas d’usage

- transcription écritures ms, dans plusieurs langages
- créer web accessibility text pour une image, ou pour une partie de l’image sélectionnée par un utilisateur
- catégorisation
- etc.
- créer linked data description, etc.
- répondre questions
- extraire données

Sans doute bientôt idem pour vidéos et modèles 3D.

AI requires accurate, relevant & big data. Pas d’institution qui possède ensemble du savoir vous. En utilisant les principes FAIR, et LOUD, peut combiner entre institutions approches qui produisent de la valeur internement plutôt que cout. Takeaway slide, celle là.

we must publish and use FAIR and LOUD data to fully leverage this technology to provide value to our community.

Exemple Béatrice Joyeux-Prunel, LUX layer sur GPT4o. Quel artiste Béatrice utilisa...

LUX CH Knowledge Graph, lieu de naissance, occupation, nationalité, etc. Titres etc. d’où viennent informations ? de diverses sources sur le web. Œuvres de la bibliothèque du congrès. Wikidata et national Library.  LOC. liens qui permettent de consulter plus info.

Graph Retrieval Augmented Generation pour overcome informations manquantes du graphe de connaissance. exemple catalogue exposition. demande même question mais en amenant information contextuelle du graph à l’agent...

Suggéré plusieurs artistes sur lesquesl publicés. Pourquoi Kusama ? Un livre à paraître aujourd’hui.

Quid des images ? Connaît choses à propos des artistes. Montrer objets concernés. Très rapide avec IIIF et Linked Art. En mettant les données FAIR dans l’AI peut rendre choses très...

no single organization have all inforamtion about Picasso. But together, we do !

Putting the AI in FAIR

AI-powered knowledge enhancement. We can use modal AI to extract knowledge form images. But the What ?

Actuellement extraire provenance objets à Yale.

Handwritten and Printed Text. Exemple catalogue de vente en français. Écritures au 

Single operations, 100% correct

Autre exemple reçu de Matisse pour 4 peintures. Transcriptions. Très petits nombre d’erreurs. Surpris que pu lire ligne difficile.

Information extraction

Can FAIR-in-AI improve AI-in-FAIR ?

Human Readbel Provenance. Description dans le catalogue. Dans Lux les organisations mais pas liées au peintre encore.

Alors possibilité de marquer les contenus. Cercle vertueux qui permet de collecter contenus. Peut imaginer faire cela à l’échelle pour le projet sur les expositions de Béatrice. 

Près demi million de lieux. Place Description enrichment. Sujet du livre, histoire de Notre-Dame. Donner une description courte et formelle. Présentation dans les enregistrements. Bon travail à partir du contexte.

Expérimentation

Deux préocupations à discuter. Technocal model Collapse.

Dès lors que contenus AI augmente, entraînement sur ce contenu. 

Conclusion. OXford closed look. Stanford n’arrive pas. Data to AI to data peut devenir dangereux mais sans doute pas à cette échelle.

Question plus importante. Bias amplification. Grande majorité des coprus entraînement issu du web et terrible. S’assurer que communauté ait contribué.

Conclusions principes FAIR et LOUD et APIs, AIs comprenne le context des questions. EN particulier IIIF images and Linke Art semantics. AI can accurately extract knwoledge from imaegs. AI generated data peuvent enrich sparse data. The amplification of baisi in AI loops doivent être 

## Julien Schuh, Operationalizing Panofsky On Artificial Iconology

Emprunt titre Impett et Moreti

Question meilleur modèle possible. Comprendre ce qu’est une image et relation entre image et ses annotations. Question de ce que nous faisons lorsque nous annotons des images, des catalogue pour entraîner des modèles. En fait toutes les informations que fournit pour entraîner des modèles en apportant des données sur l’image : qu’il s’agisse du temps, de tags, etc. technique utilisées pour produire image. Idée que le lien entre image et annotation est essentielle logique et qu’il existe une relation d’équivalence entre l’image et les annotations.

Sans doute ce que devons critiquer. En réalité toutes les données reposent sur des interprétations. Produites dans un contexte sémantiques. Donc autant du producteur que de la métadonnées. Toutes interprétation située. Toujours imparfait, biais, partiel. Au détriment autres aspects oubliés.

Pour pouvoir travailler pourquoi fait ce travail, qu’est-on supposer faire. Pour rendre compte évolution motif, circulation des formes. Établir le cadre dans lequel ces éléments seront mobilisés. Considérer ces images non pas comme un objet stable, etc.

Programmer attention visuelle dans le temps. Une image tjrs changeante et dynamique et change dans le temps. Girl with the pearl earing. Attention loop. Picture works car fonctionne dans le temps. Si ne tient pas compte de ce processus loupe les choses. Pas quelque chose que capable de traiter aujourd’hui.

Autres modèles possibles, gaze analysis. 

Paper.mage modèle montrer que pas seulement du texte

https://aclanthology.org/2023.emnlp-demo.45.pdf

Dans quelle mesure pourrait-on utiliser méthodologie proposée de Panovsky. Une manière exploratoire pour penser des objets. Nouvelle manière de penser qui pourrait être opérationnalisé. Différents niveaux opérartionnalisations. Possibilité de produire une lecture plus complexe.

Pré-iconographic level, basic representation. Niveaux formes primitives, identifier structures formelles. Formes dynamiques. Quand voit ces formes et segmente, une interprétation et plusieurs autres manière de représenter les choses. Lorsque essaye de voir choses masques. Peut representer même objet à deux niveaux différents. Et ces représentations toutes deu cohérentes.

Différents cadre interprétatifs, segmentation ddiférents objets. Et image résultat de ce processus interprétatif. Extraction poses. Principes Gestalt.

Demandé ChatGPT4o.

Iconographic level, reconnaissance des sysmboles et conventions culturelles. Problème du modèle de controle pour s’assurer que ce que produit soit cohérent.

Niveau iconologique

Compréhension plus profonde. Où l’image connecte avec d’autres questions. Comment pointe vers série d’objets autres époques. Estimation des poses, lien sentiment plus profond. Cf. Pathos formel.

Comment implémenter multilevel interprétation scheme. Sans doute compliqué mais possible de produire iconologie numérique. 

Ne pas comprendre image comme entité fermée, auto-efficiente. Comprendre comme qqchose vivant.

Nouveaux agents pour manager le visible avec lesquels pourrait dialogue. Comment accéder mémoire visuelle créée par l’humanité, alors agents qui

### Question

Question lien entre IA et web sémantiques.

Pour le moment dans exemple Beatrice. Toute information provient ontologie et balance au prompt. Pourrait penser environnement plus riche. Ou verbalise relations dans l’ontologie pour fournir des phrases. Et relancer le processus. Expliciter dans la manière où modèle de langue peut comprendre et garantir consistance. Quelque chose que voudrait explorer à travers multistep.

Microsoft derive RAG dérivé de ontologie sans doute avenue. Pour le moment pas suffisamment exploré. Mais ce faisant pourra produire réponse plus facilement possible de proposer réponses.

Alix et intégration transcription dans IIIF. Quel point de vue par rapport à cette représentation versus Alto ou Page. N’utilisent pas directement Alto et Page. Notion de transcription pas celle de TEI, mais que peut on voir dans l’image plutôt que le langage qui peut être exprimé dans l’image. Par exemple pour du texte entre deux pages aucune manière de les connecter. XML structure donc possible adopter modèle TEI. Ne pense pas que lossy. Image centric. Ce que plusieurs organisations ont fait, récupérer le fichier Alto et transformer pour exploration et interface. Question comment aligne matérialité de la page avec le texte contenu de manière à ce que ne rompe pas. Approche IIIF valable car la même technologie pour toutes les annotations. Ce que IIIF fait qui serait valable, comment préserve la sémantiques de la vue. Si enseigne cours paléologie et veut voir transcription et texte même moment. Viewer ne sachant pas ce que veut faire, alors viewer devant, ou derrière.

Clarisse terminé présentation à propos du partage. Comment convainct les gens d’utiliser une telle solution. gros travail, beaucoup de participation colloques et parler. Successivement IIIF par le fait d’avoir fait plutôt que dit. Essayé de le mettre en pratique à travers les organisations. Sémantique et présentation layer. Montrer que possible à l’échelle. Actuellement travaille projet pour produire stack complètement ouvert. Actuellement moteur de recherche propriétaire pour des raisons d’échelle. Mais pense que faisable. Pas pu financer, essayer de le faire. 10aine viewer, qq serveurs. Mais partage argument. Si parvient à comprendre que implémentant telle chose possible faire tellement de chose.

Question de comment opérationalise. Dans le processus de collecte information système entièrement automatisé. Github et project locks. Architecture publique. Réutilisable. Coût, sitting up the système et attendre que nombres soient crunchés. Pb délais requêtes multiples sur sources données. Besoin de cacher les données lourdement pour éviter délais de requêtes. Après pb de stockage.

Modèle que vient de présenter devrait reposer sur une infrastructure comme celle présentée. Car besoin des données sur les objets mais aussi représentation distribuée. 

Analyse Serment des Horaces, analyse composition traditionnelle pas du tout prise en compte : phrise de l’architecture. Pyramidage des groupes. cf. madone.

Frappé que dans l’exemple donné, le niveau iconographique passe par le texte.

Si vivant, alors question du partage des annotations humaines et production des annotations.

Acteurs privés et utilisation systéme technique.



Une des raisons pour lesquelles porte approche IIIF. Une communauté qui porte les choses. W3C une communauté qui produit des stds mais personne pour les porter. Une des questions. Spécifications au cœur du web. Pas de sustainability ou maintenance. Doit convaincre consortium qu’il y a un besoin pour suppoter nouvelle version. Besoin vote favorable pour création. Nb pourcentage doit voter. Très dur d’obtenir nouveau groupe de travail pour spécification de niche. Un autre step. Baseline plutôt bonne.

Mais communauté besoin que quelqu’un autre prenne main pour dire comment utiliser les choses. Pour utilisation entraînement, etc. pourrait être IIIF mais focalisé d’abord sur image et présentation plutôt que sémantique.

Nathalie fait remarquer deux fantaisies. Global knowledge graph. Au moins bibliographiques ou données structurées. Bib congrès, etc. Getty vocabularies. 

Pb droit auteur et IIIF. Pb Authentiication API.

Question vampirisation des contenus annotés réunis par des commuanutés sur des œuvres libres. Plutôt question comment contrôle que sa propre culture est représentée.

14H30 pause

- 3pm-4pm *Panel Discussion* : **“Enriching Metadata with AI”** – moderated by Emmanuel Château-Dutier (Université de Montréal); Panelists: Léa Maronet et Alice Truc (Université de Montréal) on « Annotating collections of heritage images: format issues and feedback »; Clarisse Bardiot, Emmanuel Château-Dutier, Robert Sanderson, Julien Schuh, and Anne-Violaine Szabados (CNRS).



## Discussion

In the context of using artificial intelligence for data production, which involves an annotation stage.

Several formats have emerged in the field of image annotation. These are often directly derived from research conducted for the development of models by major companies or GAFAM.

Annotation tools built on these models are relatively limited.

Online discussion organized in 2021 by Béatrice to attempt to address annotation

- Idea of being able to share data with NumaPress

IIIF Working Group on AI and ML primarily interested in rights statements.

Within PictorIA, there is a desire to establish a working group on this annotation issue.

Multimodal issues, specific context of HAR research and culture. The need to capitalize on research and to be able to share well-documented data.

The heritage and cultural sector is used to working on structured data documented by metadata schemas. There is real expertise in this area.

Culture info

- Identify and analyze the existing formats and their potential limitations
- Propose solutions to improve the quality of these formats for AI and visual content usage
- Plan conversion systems and …

Let me know if any adjustments are needed!

Le terme vérité lui-même est compliqué. Parle-t-on véritablement de vérités ? Pour pouvoir reproduire les choses peut sans doute produire meilleurs schémas pour l’annotation. Dans PictorIA et autres projets. Parfois annotation par nous même, parfois récupération de données pas produites pour entraîner des modèles. Aperçu que parfois reproduit les biais mais parfois meilleurs résultats que certains buts.

Exemple eyevision. Grand dataset d’images annotées crées à travers captions, etc. Demandé internet

Kyrie Bourrassa.

Partage annotation difficile. Personnellement ne réutilise jamais les annotations d’un autre projet. Préfère plutôt de pouvoir récupérer des informations basiques et aller chercher archives. 

From my perspective la question syntaxique est réglée. Open Web Annotation. Implementée récemment dans IIIF. Récemment implémentée dans Chromium. Dès lors que annotation ailleurs que dans Kobo alors OWA.

Question sémantiques de l’interprétation est difficile. Polygones arbitraires en SVG, ou 3D modèles de IIIF WK3 pour derscription plus appropriée d’une zone plutôt que d’une région. Permet de réduire dimensions, etc.

Catégorisation qui suppose tagging. Aussi linked data donc peut sémantiquement dire que telle partie qui annote solution. Pixels, etc. Si images change alors possible de réaligner image. Pense qu’un problème réglé syntaxiquement.

En termes d’échelle, toutes ces spécifications dans un modèle interopérabilité et non database structure. Welcome trust. Utilisation open web annotation modèle pas possible. Outils peuvent utiliser mais pas de stockage des annotations web.

Part of speech. Annotation. Stocker format le plus utile et diffusion. 

Besoin d’informations descriptives fournissant des informations sur le contexte de production des annotations en vue du partage. HTR United.

Les annotations correspondent à des questions de recherche. Une loop entre les questions et les annotations. Quand travaille avec équipe d’annotateurs devient encore plus complexe.

Travailler avec des medium corpora. Pas très facile de travailler dans ce contexte. 

Ne résoudra pas toutes les questions sémantiques

Mais possible d’avoir véhicule commun pour partager



Peut être pas avoir un seul modèle. Mais peut être avoir un modèle unifié de ce que les modèles peuvent faire. Dire ce que le modèle peut produire. Pouvoir décrire audience modèle.

Question sur les processus dans lesquelles les annotations ont été génerées, la véritable question à résoudre. Si ne croit pas la provenance de l’annotation, ne va pas croire le dataset. Doit donc pouvoir documenter le processus pour produire ces annotations pour que puissent être réutilisées dans certains contextes.

Annotations souvent fautives. Ce que croit c’est l’archive. Actuellement rassemble les données d’instructions que l’on considère trustfull. Autorités. 

HTR-United une initiative très importante. Car annoter un dataset très coûteux. Pas tant de subsentions pour le faire. Dès lors que reçoit argent important de pouvoir le publier et de le mettre en ligne. Car petite communauté. Exemple théâtre quand commencé pas de jeu de données. 

Lien avec les biblio

---

Pour engager la discussion, peut-être pourrions-nous discuter de. Quand a-t-on besoin de format d’annotation ? Pour quels usages ?



Plusieurs outils sont destinés à l’annotation de corpus d’images sont à la disposition des chercheurs. Quels sont ces outils, leurs avantages et leurs limites ?



Dans quelle mesure ces limites sont-elles attribuables au modèles documentaires utilisés; Comment peut-on les améliorer ?

Plusieurs chercheurs proposent de travailler avec des annotations plus riches. Par exemple sémantiques ?

Annotation multimodales et sémantiques ?



VAleur des standards. Quelles condition pour fonctionner ? Format pivot plus expressif et ses conversions.



IIIF et les metadonnees ? Groupe de travail ML et IA

https://iiif.io/community/groups/AIML/

[Kyrie Bouressa](https://www.linkedin.com/in/kyrie-bouressa-03a1a6265/overlay/about-this-profile/)

## Clarisse Bardiot, Exploring the visual digital traces of performing art

Clarisse Bardiot, études théâtrales Rennes. ERC grant.

Début recherche

Depuis quelques années, traces du théâtre de plus en plus devenues numériques. Avignon, mais seulement étude du Canon et pas du festival dans son entier. Point de départ de cette recherche. Va présenter les challenges du point de vue de l’IA.

Sources principales les programmes du festival. Deux types de programmes : programmes géneraux et programmes de salle souvent plus développés parfois avec résumés et commentaire du metteur en scène. S’y ajoute corpus de photographies.

Programs. Souligner interactions entre individuels, et contexte créatif du temps. Pour faire cela programmes source sous exploitée.

Exemple récent et anciens. Nombreuses variations graphiques entre les deux, volonté directeur. Mais aussi périodes.

Décision retourner à la source. Bases de données existantes. Base en ligne du festival, Bnf, etc. Nombreux choix possibles. Mais pas si simple, souvent pas des bases ouvertes, modèles pas documentés, et pas API. Souvent quand historiens convertissent sources en données, obligé de rendre explicite ce qui est implicite. Aussi souvent ce qui résiste à la catégorisation ou à l’indexation est exclu.

Exemple pb : création nouveau champ pris 8ans. Mais pas de réindexation rétrospective. Ainsi décidé retourné aux sources.

Exemple de pq si important pour ma recherche. Programme Avignon 80. Comparaison avec Bnf. Programme aux archives de la Maison Jean-Vilar d’Avignon.

Changement s

Analyse des programmes.

Photographies et enregistrements vidéos. Sources majeures des arts de la scène. Athmosphère, et étude évolution esthétique pratiques performatives.

[Pix Plot](https://dhlab.yale.edu/projects/pixplot/)

Idée de savoir comment pourrait construire une iconologie des arts de la scène. Pose détection qui transforme toujours images animées en images fixes. Or phrases et gestuelles phénomène temporel qui doit s’analyser comme tel.

Cour d’honneur qui impose des manières de jouer aux acteurs.

Est-il possible de capturer le fantôme de la Cour d’honneur, son imaginaire. Car lorsque joue dans cet espace, pas possible ignorer ce qui s’est joué avant.

Peter Browdwell et al. étude de la K-pop. Distant viewing pour l’étude des chorégraphies K-pop. Comment définir leur vocabulaire. Flow chorégraphiques.

Heugebaert, PHD. Visualisation du rythme

Troisième thème, comment étudier les processus de création et transformer en données. Comment idée présentée en image, passe en texte, etc. comment trace idée vers document multimodale.

Nombreux documents. Archives numériques, documents numérisés. RSN. Comment mieux comprendre comment des contributeurs différents produisent œuvre. Observer ce qui intervient, interactions directeur et acteur. 

Souvent débuté bien avant. Collection des traces numériques, une manière de dire qu’un processus. Traiter l’entre deux.

Multimodal turn. Actuellement approche par Silo. Actuellement sépare texte et imaegs pas de réelles manières d’avoir un outil permettant de passer du texte à un fichier excel. Une des difficultés qu’a pour étudier ce type de corpus.

Pb du contexte des données. Éléphant dans la pièce.

Arvest, alpha en décembre.

IIIF un support parfait. 

Ce que produit, manifeste de manifeste.

### Discussion

Très important de garder les choses simples. Plupart des collègues en art de la performance, ne veulent pas faire cela et ne le feront pas. Donc besoin d’une manière entrée simple. Mais aussi besoin avoir les deux. Evolutions très rapides, donc souvent difficile à maintenir. Belle équipe mais 2028 sera alone. Comment rendre ce genre de projet mainable.

Question manière dont pourrait rendre aux bdd Bnf contenus. Travail en collaboration étroite. 66 000 enregistrements et inconsistances. Choqués quand pointé les erreurs. Possibilité de travailler

Différence entre gestion information et histoire dans des champs disciplinaires. Est-ce que fait les deux en même temps ou bien déjà modélisation de l’information en fonction de la recherche et déjà une analyse du contenu.

IIIF ontological agnostic, n’aime pas pour cela non plus. Mais une liberté. Pb avec ontologies dans le domaine des études théâtrales. Milieu très conservateur et peu collaboratif. Comme gros financement, responsabilité de construire des outils qui puissent bénéficier non pas seulement à ma propre recherche mais aussi collaborateurs. Pour l’histoire que veut réaliser, besoin de collaboration.

Plugin, etc.
