# Reimagining Annotation for Multimodal Cultural Heritage

7-9 Feb 2024 Rennes (France)

https://reimagining-amch.sciencesconf.org

## Workshops

### SCENE

Clarisse Bardiot, Jacob Hart, David Rouquet, Université Rennes 2 (France)

https://scene.tetras-libre.fr

MemoRekall https://memorekall.com and Rekall, travail d’artistes, et proximité avec la production artistique.

- 2006, début travail recherche et documentation de la performance. DOCAM, fondation Daniel Langlois. Langlois demande de s’intéresser à la préservation. Travail sur production de Michel Noiret. Dès la première présentation obsolète. Besoin de solutions de préservation pour la performance théâtrale. Commencer par l’enregistrement vidéo, car première solution facile. Début de YouTube. Publication ArtPress pensant que quelqu’un ferait le développement... ce qui n’arriva pas. Où attendait une solution ou commençait à travailler avec des développeurs. Début de son parcours en DH.
- 2013, développement une version pro. 2 dévelopeurs : Guillaume Jacquemin et Guillaume Marais et consultâtes Thierry Coduys (un des premiers à s’occuper de real time sensors pour les arts de la scène).
- Novembre 2014 : v0
- October 2016 : v1
- January 2017 : v1.1

Rekall objectifs

- aider les artistes à documenter leur travail et permettre recréation en luttant contre obsolescence technique
- aider les chercheurs à étudier le travail d’un point dans une perspective génétique dans le contexte de documents big data nativement numérique

Premier prototype Rekall, premier environnement multimodal pour réunir dans un même espace, vidéo, métadonnées, texte pour acquérir une vue générale d’un ensemble complexe.

MemoRekall, demande solution plus simple par le MCC, plus accessible pour les institutions thépatrales. Annotation de timeframe, expliquer la scène ou repérer la scène. Rendre explicite ce qui est implicite dans l’enregistrement vidéo. 

5 000 utilisateurs qui crééent des capsules.

SCENE

- Janvier 2023, Jacob Hart joint l’équipe. 
- Prototypage Q1 2023
- Présentation juin 2023 conférence IIIF de Naples
- Novembre 2023, développement version beta, financement SATT Ouest valorisation
- Juillet 2024 : relase beta version

Transition d’un modèle centré sur la vidéo à une perspective de réseau de document. Basé sur le viewer IIIF. Une manière de gérer et distribuer les médias. Presentation API pour la vidéo récemment. Manifests pour décrire les médias/documents composites.

IIIF viewers, app pour rendre contenus fondés sur IIIF.

Développements OpenSource

Développement très alpha. 

- Annotation images et vidéos (visuellement et sémantiquement). 
- liens et navitation à travers els documents

SCENE Architecture

- plugins pour mirador
- pas encore multi-user portal. 
- FrontEnd in react
- Django app. (Proxy et API) -> services externes Peerturbe, IA, etc.
- Backend

IIIF supporte la vidéo mais pas le streaming car pas le standard. On a donc besoin de services externes pour stocker les flux mais aussi d’autres outils techniques.

COESO Project

Cas d’usage https://coeso.hypotheses.org projet en science citoyenne. Documenter processus créatif entre artiste et philosophe.

Approche multimodale.

Espace de travail principal de Mirador qui va pouvoir être alimenté avec des documents. Pour le moment ce que propose Mirador par défaut. Aujourd’hui vidéo dans Mirador.

Possibilité de copier l’adresse d’un manifeste IIIF

Chorégraphe travaillant beaucoup avec cinétographie Laban (laban notation). Donc intéressant de prendre ces documents et de les présenter en regard de la vidéo. Des esquisses sur les mouvements par les danseurs.

Liste d’annotations sur la gauche qui sont reliées à un document. Celles-ci sont liées à des timestamp. Interaction possible avec la vidéo. Une manière simple mais puissante de montrer comment ces annotations peuvent fonctionner dans cet environnement.

Possibilité fournir détails et lier autres ressources RDF. Montre comment peut s’orienter vers un réel réseau de document.

Annotation que l’on peut insérer sur un timestamp.

Comparaison entre pièce et partition. Comparaison avec autre vidéo. Possibilités de pouvoir faire des études comparatives de performances. Ensemble des documents dans le même espace et possibilité de visualiser les documents dans le même espace. Comme IIIF aussi possible d’ajouter autres documents.

Possibilité de sauver l’espace de travail mais peut être aussi stories (séquences d’actions)

Presentation API 4 pas encore disponible. Mais ajout à Canvas scènes 3D. Timeline. Nouveaux formats de médias qui vont entrer dans le modèle.

Question sur limites éventuelles du modèle de IIIF pour décrire.

Canvas qui peuvent avoir une dimension temporelle. Sur la vidéo peut définir des zones qui seraient liées à d’autres documents. Cible qui peut être une forme complexe et une dimension variable. Possibiliét de créer des documents composites. 

Sans doute besoin de définir des informations sur la manière dont les choses devraient être présentées, ou leur statut. Mais choses qui dépendent du contexte de l’utilisateur. Car si veut que soit interactif dépend normalement de l’utilisateur.

LinkedArt expliqué comme pattern modèle pour intégrer IIIF in LinkedArt. Julien Antoine Remy déjà expérimentation pour intégrer LinkedArt in IIIF.

Dans IIIF ne modifier pas le document original. Dans le format présentation possibilité d’avoir un champ pour annotation. Besoin ajouter UI pour cela. Dans IIIF ce que manipule a besoin d’être référencé par des URI, mais également possible d’utiliser un dataURI.

Important pour nous d’amener IIIF dans la communauté. Car très orienté vers le patrimoine. Car besoin de ressources pour la recheche. Mais lorsque besoin de publier les choses en ligne, notamment pour rendre compte du parcours de travail et articulation des documents les uns avec les autres.

Comment faire de la recherche dans un environnement numérique en jouant avec un standard. Voir comment pourrait utiliser des documents que n’utilise pas alors que disponibles en IIIF. Conversation qui a lieu avec la communauté de Mirador pour voir comment peut adapter l’API pour amener le standard à la communauté.

Une nouvelle version de Mirador qui va bientôt arriver. Gros enjeux car important de suivre les changements. Annotation plugins populaire, mais cassé. Le premier plugin annotation mis à disposition de la communauté.

https://github.com/dbmdz/mirador-plugins

En IIIF un modèle de story.

Standardisation vient de l’usage, ne pas hésiter à avoir des projets qui poussent les limites de IIIF. Amener de nouvelels idées ou de nouveaux besoins est également une manière d’amener des contributions à la communautés.

Jacob, exemple où probablement poussé le format traditionnel. Ex dans COESO. Exemple de réseau. Annotation des nœuds pour pouvoir proposer interactivité avec le document.

Exemple de visualisation de données. Très important de toujours pouvoir avoir le contexte des données lorsque l’on fait une visualisation de données. Ici bien sûr le traitement est réalisé de manière externe, mais possible de conncter les points. Pour l’historien très important de pouvoir lier les choses.

Juin à septembre

- Multi-user env
- collaborative projects
- UI design
- stocking multimedia content
- peertube instance
- streaming support
- ontologies
- manifest in a manifest = alors possibilité de naviguer dans un réseau
- RESTful API

Besoin de testeurs

### Distant Viewing Toolkit

*Lauren Tilton, Taylor Arnold, University of Richmond (USA)*

https://www.distantviewing.org

https://github.com/distant-viewing/dvt

Richmond University

Travaillé depuis des années sur les médias basés sur le temps, rendre disponible cela dans IIIF, une contribution énorme à l’égard de ce que nous sommes en train de faire.

Développe techniques computationnelles pour étudier la culture visuelle à grande échelle. Comment utiliser des méthodes computationnelles pour travailler sur des ressources.

Digital topic modeling, objets et images. Trouver images similaires dans le corpus.

Travailler sur le front-end pour faciliter le travail sur des contenus photographiques, etc.

Logiciel qui informe un logiciel.

Explorer les données pour poser des questions. Exploratoire / confirmateur

https://colab.research.google.com/drive/1xvy-nFcj8Bzi2J2zYpQADDuqYi5SAgVZ?usp=sharing

## Ouverture

Colloque qui fera probablement date. Mémoire du geste créatif

Annotation et enjeux. Première talk ouverture.

### Scott Delahunta (Coventry University)

http://www.sdela.dds.nl

Contribution arts de la performance. Écrivain, curator, prof danse. Motion Bank

https://medium.com/motion-bank/motion-bank-at-hochschule-mainz-c89ef4a61643

Collaboration artistes et numériques.

Question de la source, or dans les arts de la performance éphémère.

Digital traces of dance... What is missiong ?

Impliqué depuis 30 ans dans l’étude des traces numériques des performances contemporaines et particulièrement de la danse. Projet 2006. Toujours préoccupé de ce qui manque quand numérisation.

Modélisation et algo et IA, ouvrent nouvel espace pour répondre à ces questions. Partager des réflexions. Explicite, standardisé et simplifié de l’implicite de la danse. DataDriven et non data-driven quand considère multi-sensory sense.

80s 90s immergé dans la communauté de la danse contemporaine. À cette époque à Boston, Montréal, communauté influencée par diverses pratiques dont le Butô japonais. Première fois où essayé de communiquer ce qui était communiqué dans cette pratique. En dehors du studio. Important de comprendre ce qui se joue dans le fait de danser et pas seulement le voir.

Lorsque déménagé à NY pour enseigner à Amsterdam. Champ émergeant danse et technologie. S’intéressait à ce qui se passer entre la danse et ordinateur. Organisation premier symposium : 1996, Connecting Bodies.  Question de life form (cf. Cunningham). Real time interaction avec les performer. Première version de performance internet. Première version de Frothyte collabroation avec le Center for media art in Carlsruhe formalisé en 1999 sous la forme d’un CD Rom. Aujourd’hui un web site. *Parallel Sheer* and Room Writing.

Conçu pour nouveaux danseurs rejoignant la compagnie. Déjà relation au mouvement. Très populaire, notamment parmi les architectes. Question de savoir comment les danseurs peuvent communiquer ce que savent de l’intérieur depuis leur pratique.

Software for Dancers, sept/oct 2002.

Inventer concept d’outils conçus pour les danseurs et le travail en studio. TRavail avec Zach Lieberman (à l’époque moins connu) http://zach.li aujourd’hui auteur [openFrameworks](https://openframeworks.cc)

Focalisation sur le fait de supporter le travail de danse. Overlapping project 2001-2002. Nombreux projets plus en ligne car en Flash. Choreographic objects : traces and artifacts of physical intelligence (2008). Penser conservation à long terme de ces projets pour que durent et puissent se disséminer.

Projets qui cherchaient à connecter d’autres disciplines. Dans quelle mesure possible de proposer une contribution à d’autres champs. Une expérience de savoir qui peut être utilise pour d’autres champs. Intelligence dans la danse contemporaine, comment peut être formalisée ou rendue explicite pour d’autres. Exploiter la technologie de différentes manières pour interactions avec vidéos, etc. Documenter le travail et disséminer le savoirs à des non-praticiens de la danse.

Une question critique émergea qui a été très importante pour moi. 2008 financé pour une étude de réseaux. Alors étude comparative. Nous amène à la question de savoir ce que signifie amener les danseurs dans la production de savoir. 

« Knowlegde forms that cannot and or perhaps should not be separated from the bodies and processes fo their production » James Leach.  Ownership and transmission in contemporary dance and beyond. International Journal of Cultural Property, sepcial issue, July 2022.

Rendre visite l’implicite. Question du langage visuel. 

*Motion bank* project. Vision de Forthyte pour un environnement en ligne apprentissage danse. Pédagogie et accessible en ligne. An online interdiscplinary research environment for danse, 2010-2014 (phase 1). Question de la langue.

https://motionbank.org

Artiste logiciel, voulait beaucoup plus utiliser des données et travail en real time pour obtenir plus de contribution des artites.

Ros Warby, Janine Durning, Juliette Mapp. Approche rédaction score très unique. Réponse au mouvement des danseurs. Langage métaphorique et poétique. Pour son projet donné une partition à trois danseurs qui savent comment travaille. Expérience de perception choregraphique. Pratique 3 mois journalière. Performance adaptation.

Extraction de chemins 3D avec computer vision. Consistance mais différentes.

Theatre data

https://datatheatre.eu

Adopter une approche plus datadriven. Video rekall pour demander autuers nous expliquer chaque section.

À bien des égards échoué à rendre datadriven. Pour les artistes réduction, tendance abstraction.

La question du langage cruciale. Chrorégraphe pour qui langage cenrtal dans le travail.

cf. Language in use practical danse vocabulary and knowing : Biblioteca teatrale. 2020. 

Autres langues qui inflitrent le champ de la dance (ex jardinage). Mais compréhensible. Parfois déclanche les choses. Parfois encore utilisation poétique pour évoquer les choses.

Piecemaker développé par David Kern. Projet Motion Bank qui hérita de la structure. Problème de droits sur l’archive. Plusieurs versions. PM2, etc.

Goût particulier exploration espace de création.

Pratique qui résitent à la classifaction.

*International journal of Perfromance arts and digital media*. Contributions qui n’évoquent généralemnt pas la documentation. Mais réflexions qui donnent une idée implicite des annotation.

Questions ouvertes qui relèvent d’une méthode d’annotation liée à la pratique. Lorsque se déploie face à nous. Pas de répertoire de codage.

Propositions pour rejoindre le monde de la danse et le monde de l’analyse des données. Danse pratiques collaboratives, importante de qualification, etc. Challenge les savoirs et les hiérarchies. Mais peuvent proposer nouvelles méthodes pour la recherche future. Doit donc réflexivement, car possibilité recherche plus analytique, et pratique. Essayer de co-author les papiers. Mais besoin d’un code de conduite, intérêt mutuel dans le projet et ses résultats, considérer aussi que les choses changent, donc prévoir que puisse renégocier. Rechercher petits point, où peut voir travail collaborative émerger, pour développer nouveaux standards qui incluent les pratiques corporelles et choses qui risquent de disparaître. Pas la question de l’éphémère des arts de la performance. Mais ne veut pas êrte effacés. Honorer ces mémoires et le patrimoine de ces pratiques performatives.

Florian Jenett

## Audiovisual Documents Analytics

### Advene, 20 years of vido annotation

Olivier Aubert, www.olivieraubert.net

https://www.advene.org

20 ans que maintient ce logiciel. Question de sa maintenance à long terme.

Annotations en recherche, un aspect fondateur du travail de la recherche. Exemple manuscrit avec annotations marginales. Ici le medium de l’annotation celui du document original. Avec post-it, séparation du medium original de celui de l’annotation. Couleur qui permet la catégorisation. 

Plusieurs communautés d’annotation vidéo. 

- Media studies : Advene, VIAN, Mediascope, Lignes de temps, pan.do/ra
- Enseignement : CoCoNotes, Travis-go
- etc.

Ecology of hypertext annotation, taxonomie de système d’annotation.

https://dl.acm.org/doi/pdf/10.1145/276627.276632

Advene project, lancé en 2001 avec Yannick Prié et Pierre-Antoine Champin. Environneemnt d’édition et de diffusion. Annotate Digital Video Exchange on the Net.

Travail sur Mulholland Drive. Active reading and close-reading de vidéo. Compagnion pour recherche exploratoire.

Travail avec Bernard Stiegler, utilisation dans les écoles d’art, etc. Nombreuses expérimenations. 

Travaux plus récents avec ADA Project, https://projectada.github.io Annotation très intensive (jusqu’à 20 000) avec des structures basées sur des ontologies. Financement de la pérennisation du logiciel car à l’époque plusieurs librairies en fin de vies.

Leçons de ce projet. La technologie est un pharmakon (Stiegler). Enjeux de maintenance et de sustainability. Réaliser que la technologie est formidable, mais mouvante et fragile. À la fois le remède et la maladie. Repose sur choses que ne peut pas nécessairement comprendre ou maintenir. Les dettes technologiques peuvent s’accumuler et vous conduire à l’écroulement.

Pour la vidéo, pendant longtemps n’existait pas pour le web, besoin d’une librairie externe ou plugin. Exemple choix de Flash pour Ligne de temps. Aujourd’hui le logiciel n’est donc plus disponible. Or, pas de solution à cela en dehors de la chance.

Nombreuses initiatives dès 2001 pour les standards d’annotation (Mosaic, Annotea...). WebAnnotation du W3C en 2014 après OpenAnnotation. WebAnnotation standardisé en 2017. Pour des modèles précédents comme le notre beosin de convertion pour adapter ce standard.

Le web browser comme plateforme univeselle ? Devenu de factor universal runtime. Mais inconsistance entre les navigateurs pas négligeable. Et certaines choses sont impossibles (lecture DVD), savoir où sont les données importantc ar parfois pb de droit.

Maintenance burden. Pb de coût. Qui maintient le logiciel. Le soin des choses, Jérôme Denis.

Préservation des données, enjeux de standards. Des standards pour les données, mais penser également la question des logiciels. Résultats de recherche pas seulement les sorties mais aussi les outils utilisés pour les produire. Donc besoin de contributeurs et de mainteneurs. Une communauté interdisciplinaire.

### Discussion

Question de la modélisation. Ligne de temps métaphore linéaire, alors que venait du monde de la modélisation des connaissances. Négociation nécessaire. Interopérabilité que doit envisager dès le départ.

### Media Ecology Project, Mark J. Williams

Un cercle vertueux. Possibile de développer approches interdisciplinaires qui permet de nourrir l’archive. Capacité à poser des questions de recherche qui n’avaient jamais été posées avant.

https://mediaecology.dartmouth.edu/wp/

Projet largement redevable au champ des DH. MEP premices largement redevable au projet Bamboo.

Prise de contact avec des archivistes qui ont voulu travailler ensemble. Plupart des logiciels de recherche développés pour les sciences. Besoin criant pour les Art s et humanités. Souvent attend que tout soit fait par les institutions. Or production demande travail et penser collectivement. Rompre logique de consommateur et se relever les manches.

Une subvention importante. 

- SAT Semantic Annotation Tool https://mediaecology.dartmouth.edu/wp/projects/technology/the-semantic-annotation-tool
- Onomy.org
- Scalar

Collaboratif, personnes qui ont des opinions différntes. Dissonances, collegialité, travail de traduction et d’expérimentation. 

Annotation feed, critical. Curation / preservatio. Pedagogy vs culture attention diffuse. Slow down, être attentif.

Online MEP Tutorails, SCMS 2022 Workshop. 

Bernard Stiegler un critique de la société néolibérale technologiste. Monté en puissance économie de l’attention présentiel. Ars industrialisas. Possibilité d’une vie meilleure.

Notion de pharmakon et contrôle de la technologie. Valeur des archives et attention. Nécessité de réenchanter notre relation à l’histoire.

Plusieurs projets d’analyse des médias financés par le NEH, collaboration avec les archives nationales. Legacies of USA moving images via internat’l Lenses.

AM&B Exhibitors catalogs

Tests récents avec Unity App (repérage silhouètes et pose des personnages). Mais plan américains, coupures de l’image, etc. pas bien pris en compte.

### Machine Intelligence for Motion Exegesis (MIME): Applying Pose Estimation and Related Technologies to Analyze Archival Performance Recordings.

Michael Rau and Peter Broadwell (Stanford)

Annotation des poses et viewing. Projet ML pour capturer la posture des acteurs et permettre l’annotation vidéo pour l’analyse de la performance (thématique et stylistique).

Application algo ML pour identifier toutes les poses et les rapporter aux chercheurs. Pas besoin de camera de capture de mouvements ou capteurs. Mais travail sur grande archives vidéos. Considérer pb cadrage, qualité, etc.

Approche distante parfois perturbante pour certains acteurs. Mais bénéfices d’une narrow-viewing. Vue sur le travail du performer. 

Human « in the loop » mais plutôt happy end. Pouvoir s’assoir avec ces données et développer une interprétation avec elle.

MIME Machine Intelligence for Motion Exegesis.

Travaillent actuellement sur un assistant pour identifier mouvements comparables.

- **Tired** Convolutional joint/armature estimation via Oepn PifPaf
- **Wired** Fully transfomerized 3D human mesh and armatique PHALP/4D

Analyse PinaBausch possible de voir motifs. Repérage intérêt de certains mouvements.

Questions auxquelles sommes confrontés.

Plusieurs questions posées par ces données. Les données sont très nombreuses et elles peuvent supporter de très nombreuses hypothèses. Ce qui implique que le chercheur puisse agir de manière active pour interpréter ces données. Cela implique d’avoir un humain dans la loop, très important d’un point de vue éthique.

Toutefois, techniques qui n’apporte rien fondamentalement que les humains pouvaient faire précédemment. Simplement possible de le faire de manière beaucoup plus rapide. Cependant pour pouvoir répliquer des réalisations un grand potentiel.

Des questions relatives au droit d’auteur au contexte qui sont très intéressantes. Raisons pour laquelles pas vraiment encore rendu public ces productions : qui peut analyser résultats, etc. Sans doutes des possibilités pour utiliser ce type de choses pour d’autres médias. Intéressant de savoir comment pourrait utiliser ce travail pour la production de nouvelles œuvres.

## The Temporal Dimensions of Distant Viewing

### Crossing Borders Archives. The Circulation of Stock Shots in Audiovisual Media

Matteo Treleani

Plateformes et leur importance pour la production de contenus. TV broadcaster. Programmes d’actualités composés d’images de stock. Utilisées à la place d’un fonds d’écran noir.

Pas de métadonnées sur les stock-shot. Documentation de l’importance du phénomène.

Parfois légendes très différentes, parfois contradictoires avec les images proposées.

### The Structures of Visual Exchanges

Nicola Carboni

Analyse de la presse et dissémination des images. Comment travailler à l’échelle. Difficile d’identifier des pattern. Enjeu de comprendre la dissémination.

Visual contagions. Essayer d’appliquer des algorithmes d’analyse d’image pour analyser la diffusion des images. Déterminer l’accès culturel aux contenus. Comprendre s’il existe une structure (Europe/EU). 

Constitution d’un corpus relativement large

- 19777 périodiques
- 1244 villes
- 51 pays

3,6 livraisons, 14,2 millions d’images. Extraction des illustration docExtractor et utilisation IIIF.

Actuellement utilise Vite network avec unsupervised approach. Fonctionne particulièrement bien pour des matériaux de différentes couleurs. Bonne capacité à trouver des similarités.

https://visualcontagions.unige.ch/explore

Possibilité de réorganiser les images. 

Comment extraire de la compréhension de ces images. Pour y parvenir doit explorer deux axes : le premier celui de la similarité, l’autre celui de l’information de production.

PAr exemple, Révolution surréaliste. Extraction d’une série de métadonnées basiques. Caractéristiques importantes, lieu de publication, titres, dates. Information géospaciales associées à l’image. 

Lorsque veut faire ça à l’échelle, nombreux enjeux. Les données pas toujours complètes ou inconsistantes. Catégorie de publications (avant-garde, humour, mode, etc.)

En chaînant des images similaires, on peut produire diverses visualisations des trajectoires visuelles. L’étude du phénomène révèle des pattern culturels ou économiques.

Comment y parvient-on. Extraction images IIIF, créée un graphe de connexion et produit analyse et clusterisation des images. Utilisation de Python ou autres outils pour travailler ce matériau.

Application analyse de réseau pour essayer de comprendre ce corpus. Ici visualiser interactions entre les villes de différents pays et leurs interrelation. Mais essayé de se focaliser sur des cas d’études comme par exemple l’avant-guarde. Comprendre comment dans le maché interne de l’avant-garde les images les plus impactantes pour la création du mouvement.

Analyse qui peut être menée à l’échelle nationale pour mieux comprendre comment l’information circule. Grâce à la visualisation permet de voir certains pattern apparaître. Paris par exemple très central, mais plus redistributeur que producteur. Rôle d’une ville peut donc varier dans le réseau.

Question de la communauté. Certaines communautés plus receptives, par exemple communauté architecturale qui rejoignent plublic plus général.

Utilisation images de voitures, 20e. Manque d’imagerie négatives. Outils qui permettent d’identifier faible présence d’images négatives alors que protestation contre les voitures.

SpaceTime Cube pour comprendre comment mouvement d’une image. Difficile de comprendre agrégat. 

Actuellement beaucoup d’images et méthodes que peut appliquer. Mais aussi intéressant de regarder ce qui peut nous manger. Ce qui est challenge, ce qui n’est pas là. Informations très importantes qui ne sont pas actuellement dans le projet. 

- Nombre de copies. Que signifie circuler, êrte représenter. Macrocosme large et être publié dans une revue ou une autre, plus ou moins important. Besoin d’avoir une meilleure compréhension des sources pour les qualifiées et améliorer approche distante et comprendre l’impact qu’une image peut avoir dans une communauté.
- Comprendre également quelles ressources disponibles pour les éditeurs à cette époque. Peu de sources disponibles à cet égard. De même prix qui est important pour comprendre le phénomène et manière dont évolue (ex. Publicité et réduction coût publicité).
- Ajouter un axe suplémentaire sur la réponse et ne pas se limiter à la similarité et à la production. Pour cela besoin de produire de nouvelles données.

#### Discussion

Arrêt automatisation car à un moment la machine ne parvenait pas à réaliser le travail. Aligner un très bon logiciel qui fonctionne très bien pour identifier exactement la même image. Mais pair par pair. Mais trop de temps.

### Using Multidimensional Vector Embeddings to Study Temporal Dimensions of Historical Newsreel Data

Mila Oiva

Un travail d’une équipe multidiplicinaire.

CUDAN Newsreel. Deux corpus Moscow et Tallinn.

Translation loss, partial view & emphasis on deduction. Image qui montre points de couleurs différentes, format différent et position différentes. Problème annotation. Vue partielle, emphase sur la déduction.

Des approches alternatives possibles

- utiliser computer vision Olesen et al 2016, Masson et al 2020
- distant viewiing framework Arnold et Tilton 2023 et 2019
- Représentation nuémrique et possibilité étudier perception humaine à travers graduation plutôt que catégorisation. Manovich 2020

Approche : proto-annotation avec machine learnirg puis étiquettage humain.

[Collection space navigator](https://collection-space-navigator.github.io), développé à Tallin

Clusterisation très claire du corpus

## Short Papers

### AVAnnotate: Creating Scholarly Editions and Exhibits with IIIF and AV Archives

Tanya Clement, University of Texas at Austin (USA)

Projet centré sur les utilisateurs collection AV. Collaboration SpokenWeb, etc. Library of Congress...

https://av-annotate.org Promouvoir utilisation de IIIF pour AV

Pas un outil pour créer des annotations mais un outil pour afficher des annotations.

### Bipartite Frame Networks in the Analysis of Film: a Case Study Utilizing Commercial Computer Vision APIS

Nabeel Siddiqui, Susquehanna University (USA)

Solutions comme YOLO fonctionnent bien.

Google Vision API, relativement coûteux. Reproductibilité limitée.

Reseaux bi-partis narratifs de films

Exemple 

- Hitchcock Face Surpise Network
- label detection

### Visualizing Rhythms Through Digital Annotations: Challenges and Issues in the Performing Arts.

Théo Heugebaert, Université Rennes 2 (France)

Thèse de doctorat.

*Ti esti Rhuthmos*. Rythme qui structure les qualité d’un mouvement. Nombreux éléments concernés.

Si le rythme change, suppose que bonne raison.

Paravents Arthur Nauzyciel. Variation d’interprétation par différents acteurs. Possibilité d’accompagner le processus de production.

Utlisation du logiciel MotionBank

### Intuitive Access to Oral History Video (The Pellaton Experience)

Bérénice Serra and Léna Frei, Institute Digital Communication Environments (Switzerland)

https://www.fhnw.ch/en/about-fhnw/schools/academy-of-art-and-design/institute-digital-communication-environments

https://sapa.swiss

Prototype pour permettre la visualisation d’un grand nombre de données.

https://sapa.swiss/fr/the-pellaton-experience/

Choix low maintenance, Open GLAM Hackathon 2021

### The Linked Editing Academic Framework (LEAF) in the Multimodal Annotation Ecosystem

Diane Jakacki, Bucknell University (USA), Susan Brown, University of Guelph (Canada), Michael Ilovan, University of Alberta (Canada) and Luciano Frizzera, Concordia University (Canada)

LEAF The Linked Editing Academic Framework (LEAF) in the multimodal annotation ecosystem. Outil utilisable pour des académiques plus ou moins versés dans l’encodage. Création de flux de travail itératifs.

https://leaf-writer.leaf-vre.org

Dévelopé par CWRC

Focalise sur des tâhces principales comme publication sources, etc.

Plusieurs instances. Chercheur pas toujours besoin end to end infrastructure. Déevloppé de Standalone instance. Avec GitHub possible de travailler avec des repos.

TEI/RDF editor. Un outil de publication LEAF-T et Table of Connect. Conçu pour journal.

[DToC revealing Tagged Entities](https://www.leaf-vre.org/docs/features/dtoc)

Melon, Innovation



## IIIF, from Images to Multimodal Corpora Annotations

### Overview of the IIIF Initiative for Interoperability of Digital Objects on the Web (Image, Audio/Video, 3D).

Régis Robineau, Biblissima +, Campus Condorcet (France)

IIIF Interop

un modèle pour présenter et annoter des contenus numériques (images et fichiers audiovisuels). Aussi une communauté qui développe des APIs ouvertes et implémentes des outils qui consomment ces APIs sur le web. Une communauté vivante et dynamique. 

100aine adopteurs et participants à travers le monde. Bibliothèques, archives, musées, agrégateurs, et utilisateurs.

Organisation en groupe utilisateurs. Consortium de 67 institution.

IIIF vision

- créer un framework global dans lequel les ressources visuelles ou temporelles peuvent être partagées sur le web...

Problème de silos où les données réparties entre des institutions séparées, pas possible de partager facilement en raison de barière technologique. Souhaite advenir un réseau de partage basés sur des APIs. Remote environnement... third party application annotation, outil de présentation, gestionnaire de contenu pour produire expositions.

- Zoom dans fichiers : Leiden Collection https://www.theleidencollection.com/viewer/david-and-uriah/
- Comparaison côte à côté dans même environemnt ex VanGogh
- Très efficace pour recomposition objets distribués pour créer des Mashup ex. Biblissima reconstitution virtuelle d’un manuscrit mutilé
- annotation de contenu pour pédagogie (cellule) ou raconnter des histoires (expo) ou encore crowdsourcer des documents

Deux APIs core Image qui fournit une manière standardisée de délivrer et manipuler une image (« get pixel ») et API de présentation pour...

Image API, pixel, http request, dérivées, tiles, deep zoom. 

- Mirador
- Universal viewer, avec son
- exemple en vidéo, idem ex Northwestern University

Pas d’API AV en IIIF, pas d’équivalent audio ou vidéo. 

IIIF Presentation apporte fonctionnalités d’annotation. Exemple dans Mirador. Autre exemple audiofile, ou vidéo (dans Mirador). Modèle pour présenter et annoter des objets numérisés ou numérique. Fournir une description standardisée de la structure, de la mise en page et des annotations.

IIIF Manifest contient toutes les métadonnées qui doivent guider l’expérience de vision. Principales unités de distribution dans l’univers IIIF.

IIIF Canvas 2D, conteneur virtuel. Comme Powerpoint un page blanche que comble avec contenus. 2D space qu’associe à des contenus. A droite image elle même associée au contenus avec annotation. Target et body. Canvas toujours target annotation et body n’importe quel type de ressource.

Une autre représentation possible. Canvas largeur et hauteur, aspect ratio de l’image identifique et image partage coordonnée. Mais peut avoir un second objet ciblant deuxième zone utilisant même système de coordonnées. Peut être image, texte océrisé.

Idem pour le contenu vidéo.

Initiative IIIF 3D, initiative dirigée par Technical specification group depuis 2022. Modélisation API comparable à celle proposée pour 2D modèle. Objectif

- enable interoperable 3D...
- Introduction d’un nouveau concept de scène coordonate system. Nouveau concept 
  - boudless 3D space...
  - ...

Permettre interopérabilité entre viewer : [Google Model Viewer](https://modelviewer.dev) ou [Sketchfab](https://sketchfab.com) Et intégration dans d’autres viewers pour expositions, etc.

### From Source Annotation to Scientific Publishing: the PENSE and PerVisum Projects.

Jean-Christophe Carius and Chloé Pochon, INHA (France)

Exemple images partagée à INHA, document qui contient images et textes mélangés. Collections INHA composites.

PENSE platform qui se focalise sur des méthodes numériques.

Digital archival boxs. IIIF autorise programmatic visualisation of thumbnails. Visualisations possibles. 

Projet Barye https://barye.inha.fr

Les décors Karbowsky, documents présentant la collection d’œuvres. Annotation structurale, identifiant des zones dans l’objet. Délinéation pour encoder des relations.

https://karbowsky.inha.fr

Plateforme, explorer possibilités du web pour publications.

Incorporer des sources annotées dans un article publié sur la plateforme de publication OpenEdition. Peu adaptable. Expérimentation embedding IIIF viewer similaire à lecteur exporté vidéo. Utilisation iFrame. Peu catholique dans environnement numérique. Mais introduit le paradigme d’une visualisation enrichie dans une plateforme web.

Multimodal annotation. Doucet et ses archives, album de dessins antiques, archive de voyages textuelle et spatiale, quatrième reconstruction topographique excavation.

Projet majeur récemment lancé PerVisum

DeVisu, a Scientific Journals Incubator https://devisu.inha.fr profite de la dynamique du projet Commons

Omeka, etc. Proposer un système innovant pour la présentation d’articles savants. Études de nouvelles formes de publication d’articles, en collaboration avec des auteurs. Nouvelle forme de publication et manifeste pour annotation visuelle.

Apparat critique, entête, etc. Combinés dans un manifeste JSON.

Travail pour chaîne éditoriale de Métopes. Réflexion du format. Web annotation model. Devrait avoir autres discussions spécialement avec Métopes pour identifier format attendu. JSON ou XML.

### IIIF, a Standard for Multimodal Corpora? The Building of SCENE

Clarisse Bardiot and Jacob Hart, Université Rennes 2 (France)

Historienne des arts de la scène, constamment confrontée à une multitude de documents, textes, photographies, vidéos, programmes, etc. Traces numérique d’un seul projet.

Exemple présenté à partir milliers de traces d’un spectacle de Jean-François Perret, Walden Memories. Installation Fresnoy, et spectacle à NY. Un processus de production complexe.

Depuis les 1990s arts de la scène ont développé approches génétiques. Observation participantes. Nécessite de créer un environnement numérique pour collecter les traces et l’analyse de toutes les étapes du processus créatif.

Méthodes comparatives, etc.

Close reading of documents et annotation

Approche intra-documentaire et interdocumentaire. Différente entre œuvre autographique et allographique.

Allographique rejouable, pour cela besoin d’une partition. Un système symbolique de transcription. Or, une annotation différent de cela. Suppose existance préalable d’un document et annotation qui vient préciser son interprétation et son contexte.

Continuum entre les deux. Deux catégories d’annotation. D’un côté intra-documentaire : possible d’expliquer, comment rendre implicite explicite. Et approche inter-documentaire, comment lier documents entre eux et traiter ces annotations.

Également un processus de redcocumentalisation. Cf. Manuel Zacklad, 2007.

## Keynote: Melvin Wevers, University of Amsterdam (Netherlands), A Multimodal Turn: Navigating AI Developments in Digital Humanities

A multimodal Turn

Navigating AI Developments in Digital Humanites. Parler des possibilités mais aussi des limitations.

Question des roadmaps pour aller au-delà. Peut espérer des avancées de la part des chercheurs IA mais aussi largement dépendant de ce que nous pourrons pousser.

L’année dernière publication article sur tournant multimodal. Argument que DH pendant longtemps travaillé sur les données textuelles car disponible informatiquement et traitable. Maintenant que réseaux neuronaux, ouvre de nouvelles avenues pour l’analyse visuelle. Peut faire clusterisation d’objet, détection d’objet mais aussi classification des images.

Très intéressant de pouvoir intégrer les images. Mais signification des textes et des images ne peuvent pas être comprises isolément, en réalité fonctionnent de manière coordonnée. Cela offre nombreuses choses auxquelles penser pour l’analyse.

Plusieurs travaux théorique autour de la multimodalité. Notammanet travaux de Hippala. Bateman et Hippala 2022. Une combinaison de formes expressives, textes, images, diagrammes, mais ne pas oublierles sons et les odeurs. Trois modes sémiotiques (Bateman & Hippala, 2022).

Un des outils qui rend multimodalité plus simple pour les gens, sans doute CLIP. Ce qui est particulièrement intéressant avec ce modèle c’est qu’il associe des données textuelles et des données visuelles. Prend une grande collection d’images issues du web. Mais deux type d’encodeur : encodeur de texte et d’images qui produisent des embedding et modèle essaye de résoudre les dimensions de ces deux vecteurs. Arrive avec un modèle qui prend en compte à la fois des informations textuelles et visuelles. Alors capable de comprendre que perroquet proche d’un oiseau. Pas besoin de training supplémentaire avec le modèle pour lui demander des choses pour lesquelles pas enrtaîné au préalable.

Ainsi peut produire des recherches texte vers images. Chercherche image to text. Mais aussi image to iamge.

Zeo-shot prediction. Utilisation de plusieurs milliers de vues de lanterne magique. UtilisatioN CLIP extraction images de chiens. Pour CLIP possible de retrouver facilement des représentations très diverses mais également pouvoir retrouver représentation plus abstraites.

Utilisation embeddings pour unsupervides clustering. Clustering plus efficace que RNN

Comprendre la temporalité. Gros biais avec gris. Lorsque colorisé, biais dans autre direction. Entraîné classificateur pour se débarasser du biais. Fonctionné, et prédiction à 5 ans. Par ailleurs classification qui permet de vraiment réduire le taux d’erreur dans la détection des objets et l’identification des personnes.

Vers une analyse contextualisée plus approfondie.

CLOP regare ensemble image. Focualisation textual and visual elements. Object détection encore challenge.

Deux développements récents. Deux modèles de fondation par Meta SAM & DinoV2 ainsi que Multimodal...

Modèles de fondation sont des grands modèles qui peuvent être utilisés comme des modèles de base.

- Segment Anything Model SAM, très commode notamment pour produire des annotations
- DinoV2 Depth Estimation & Sparse Matching, peut faire plusieurs sortes de chose. Self supervised model, capable apprendre pendant l’entraînement. Depth estimation, sparce matching proche de ce que font alignement dans la clusterisation. Mais possible alignement d’iamge. Ouvre de nombreuses possibilités pour la recherche en DH.

MultiModalLargeLanguageModel. Transition de Pure LLM (GPT3, Bert) to MMLLM

Vision encoder + LLM visual and language understanding at the same time. Similaire à ce que l’on fait avec CLIP. Zoom in on LLAVA

Petite expérimentation en anayse visuelle avec LLAVA

Image de publicité coca-cola à San Francisco. Demande ce que voit sur cette image. Répond de manière détaillée contenu image. Résulat qui paraît très surprenant. Quand demande quelle ville, réponse circonstanciée. Mais si lui dit que San Francisco, évoque bâtiment pas sur la photo !

ChatGPT4 plus d’informations. Mais ne fait que supposer. Intéressant d’un point de vue étude média critique.

Kosmos-2 un modèle créé par Microsoft. Un modèle basé sur les transformers avec information causale. Grounding objects and text in visual world. Des notions de causalité dans le modèle. 

Expérimentation sur collection coloniale. Intéressant car image accompagnées de légendes.

Ces modèles sont-ils en train de raisonner, ou bien juste de réciter. Ce que voudrait créer nouvelle connaissance. Mais souvent seule chose que l’on souhaite faire c’est extraire de l’information.

CLIP tel que conçu impose un étranglement. Or, ces modèles similaires dans leur conception que CLIP

Interprétation du visuel à travers le texte. Est-ce qu’on adresse vraiment le visuel. Est-ce qu’on exprime réellement la pensée visuelle : cf. Mitchell pictoral turn, Barthes notion *anchoring*, Gottfried Boehms iconic turn. Comment régler la question ? peut être rnedre les modèles moins sensibles au texte. Ajouter plus de features, visuels et métadonnées. Pour les rendre véfitablement multimodaux.

Rôle de l’observateur. Ce que sait de Berger, etc. on impose des croyances, des valeurs et des attentes sur les images. Il n’y a pas une réponse unique ou une signification unique à une image. Barthes, relaying. Using personas (Kruk et al.) pourrait améliorer empathie culturelle et historique.

Going forxard

- Nombreuses théories en média studies, art history, etc. Il est temps de les tester. 
- Problem décomposition : partir de la question de recherche et identifier problèmes plus petits et challenges
- pour ces ocmposants
  - identifier la tâche adaptée / modèle pour isoler les composants
  - penser à des manières d’évaluer les sorties de manière cirtique
  - aller au-delà de la description

Comment rester à jour au fur et à mesure des progrès. 150 publications par jour. Ne peut pas seulement lire les papiers dès que paraissent. Mais prenant un peu de recul plus clair.

- hugging Face pour modèles, codes, tutorials, et démos interactive (papiers sélectionnés)
- papers with code, website liste état art avec code
- regarder au-delà DH pour inspiration, beaucoup de recherche en critical data studies et manirèes créatives d’analyser culture matérielle dans champs alignés
- pas de solution un-seul outil, être créatif.

Peut faire les choses de manière très cool. Mentionne Thomas Smits, Nane van Noor, Alexandra Barancova, Nico de Vriend, Noord-hollands archives, Eugeen van Wees & Marjolin.

Littérature.

### Discussion

- Small data
- Données pour utiliser les modèles souvent biaisées.
- Quelle place pour compréhension plus humaniste, explicabilité et théorie plus humaniste de ce que peut interpréter. Peut être anthropologie des modèles, mais au moins clarification des biais.

Forcément amélioration facilitation en particulier détection. Important culture visuelle. 

moins convaincu d’un tournant pour HA (cf. article Leonardo Impett and Fabian Offert)

Quid de la plastique, stylistique

Interpretable machine learning

Pas un historien de l’art mais un aspect très formaliste en HA. Pouvoir accéder à la signification des images, sans doute un intérêt pour l’histoire de l’art. Pas seulement regarder les œuvres elles-mêmes aussi considérer son inscription dans le monde, etc. Ici sans doute beaucoup de changements. Hippala explique qu’un objet existe dans un plus grand espace discursif. Des modèles qui entrent dans le domaine de ce que les gens disent des choses. Sans doute que les historiens de l’art discutent de ces qustions.

RAC modèle possible de développer les modèles dans certains domaines. Sans doute pas une manière de 

Kosmos-2 sans doute possibilité d’encoder éléments et parties dans l’image. Sans doute possibilité extraire éléments de l’image.

Visual features

Computational research. Volonté de donner espace pour que computational work and humanist pourraient travailler ensemble avant de revenir à la grande communauté plus générale des humanités numériques. Espace plus petit pour mener ce travail.

Rmd voir DinoV2

## Annotations for contextualization and Narratives

### 3D Annotations as Multimodal Storytelling

Kompakkt un viewer 3D web et outil annotation pour explorer paratger objest 3D et multimédia, annotation d’obejts avec annotations multimodales, collaborer avec d’autres.

https://kompakkt.de 

Répertoire cherchante, métadonnées en CIDOC-CRM. Dimensions objets, etc. Chaque objet reçoit un identifiant pour le partage. IFrame viewer.

Annotations connectées à des points. Peut être liée à des aspects particuliers des objets 3D.

Storytelling avec annotations

https://kompakkt.de/entity/5d6f708c72b3dc766b27d750

Utilisation outils prospectifs. Exemple masque japonais. Annotation qui peuvent comprendre des commentaires mais aussi des contenus associés comme des vidéos qui fournissent une idée de la manière dont peut utiliser les annotations.

Possibilités de collaborations, création de groupes etc.

Kompakkt dévelopé en utilisant des technologies web modernes. Viewer séparé du serveur et repo.

Angular 17x, NodeJS 16x, BabylonJS, MongoDB & Reds. Optimisé pour l’accessibilité. Projet open source donc possible d’auto-héberger pour un usage externe.

Formats supportés : 3D Models et Pointclouds, .glb, .babylon, .glf, .obj, .stl. Formats singlefiles.

Images : .jpg, .png, .tga, .gif, .bmp (principalement brower support)

Audio : .mp3, .wav, .ogg, .m4a (principalement brower support)

Vidéo : .mp4, ... idem

Depuis sa conception en 2018 au Departement for Digital Humanities à l’université de cologne. À la fois un viewer et annotateur 3D, mais aussi un projet de recherche en cours.

Consortim de déevloppement en collaboration avec Leibniz Information Centrer for Science and Technology University Library, Hannover. Une intéragtion à Wilkiabse pour annotation objets avec concepts sémantiques. Semantic Kompakkt https://semantic-kompakkt.de

Particiaption in IIIF 3D Technical Specification Group. 

Intégration en cours ARTEST project Erasmus+ 2020-2024 (Cologne) travail sur intégration avec Wordpress. http://artestproject.com

Kompakkt in the CAVE (Université de Cologne), projet Virtual Campus 2023-2026. Pour faciliter chargement et comparaison des objets en application web.

Plusieurs questions de recherche en cours

- annotation au delà-information textuelle
- annotations comme partie du knowledge graphs, end-points of triples (CIDOC-CRM)
- **annotation lines and sufces on 3D objects**
- annotating points clouds
- measurements of distance, areas & volumes

Pour l’annotation des parties des modèles. Cherche à voir comment faire. Implique sans doute de pouvoir pointer des sous-ensemble du modèles. Voudrait peut être pouvoir définir les choses de manières plus lâches pour pouvoir annoter non pas des surfaces des objets mais des zones environnantes de l’objet en particulier dans les nuages de points. Car dans les objets 3D, souvent difficile de connecter des parties des objets.

### Coding the Encoder: Situating Subjective and Contextual Aspects in High-Level Image Annotations

Delfina Sol Martinez Pandiana, Università di Bologna (Italy)

Présentation liée à sa thèse de doctorat. Data labelling.

1769 présentation du mechanical Turk. Présenter invention, ouverture du cabinet exposition aspects mécaniques. Impressionne l’audiance. Fonctionnement exact mystérieux. Finalement fonctionnement révélé, un compartiment secret qui permettait abriter joueur. Une illusion intelligente.

Aujourd’hui beaucoup de développements en ML et IA sont également des illusions. Grande partie de choses qui interviennent en arrière-plan ne sont pas réellement montrés.

Amazon Mechanical Turk, une plateforme qui utilise des travailleurs pour traiter en masse les contenus. Data Hunger and digital Swetshops.  Une armée de travailleurs, souvent issus du global south annotent les données et rafinent les modèles. Un travail invisible.

Qu’est-ce que cet étiquettage. Souvent définis comme : Ground Truths. Définissent les vérités pour les problèmes que ces systèmes sont chargés de résoudre. Gold standards, utilisés pour entraîner sur d’autres contenus.

Relation entre les objets et des choses explicitées. Problèmes de sémantique sur l’intégration de ces éléments au modèles de données. En réalité des annotations qui sont attachées à des contextes d’annotation.

Exemples de savoir subjectif introduits dans ces systèmes. Critique car peut déterminer ce que le modèle apprend, et peut ensuite faire débat ou poser problème. Ex. Ugly, sexy, etc.

Ground truths and the ethics of classification. Particulièrement important lorsque l’on traite des individus. Implique diversité et complexité du monde. Le processus de designer et définir ces catégories embarque des représentations. Un moment de pouvoir important.

- question genre
- rôles, etc.

Decontextualise label particulièrement problématique pour le patrimoine historique. Analyse du type de tags de plus en plus utilisés. De plus en plus abstraits, donc censés encoder concepts de haut niveaux potentiellement problématique. Changement qui change les attentes à l’égards de ces modèles. Qu’attend-on de ces modèles aujourd’hui.

Ces enjeux liés aux logiques de production de ground-truth. 

Proposition d’ontologie situées pour produire des annotations.

Ontologies et knowledge graphs. Ontologie qui sert de framework pour fournir du contexte. Alors possible de faire de la curation des triplets. Possible de requêter cette information pour compréhension plus complexe.

Annotation un triangle. Rattacher annotation au contexte. Peut avoir beaucoup plus de propriétés. Explorer la situation de l’annotation, classe qui peut encapsuler état des affaires. Mais aussi rémunération skills, etc. Dataset auquel annotation entity appartient, etc. Si produit par la machine ou humain. Annotateur humain et communauté (éventuellement qui est, etc.)

Pour les images, création d’un module spécialisé sur le type de données que veut qualifier. Pixel data, ontology, etc. Possibilité de proposer plusieurs annotations concurrentes sur la même zone en comprennant d’où vient.

Expériemnetation sur le art-stract dataset. Cultural heritage dataset étiquetté avec des concepts abstraits. Création du knowledge graph. Information visual transformers, etc. Possible requêter le knowledge graph pour obtenir une compréhension de la manière dont les objets peuvent être compris.

Peut utiliser ces données pour entraînement. Possible embedding the knowledge graph lui même. Performance à peu près la même voir meilleure mais bénéfice explicité.

Annotation du mal dans les images. Discours haineux, etc. Complexité de ce travail. Exemple Malevolent multimodal memes. Annotater haine et le mal. 

### Discussion

Quid choix vocabulaire

Possibilité automatisation de cette démarche

### VR and AR Prototypes for Multi-sensory and Haptic Forms of Documentation and Archiving of Digital Art (LeFo Project)

Marie-Claude Poulin, University of Applied Arts Vienna (Austria)

Compagnie *Condition plurielle*

AR/VR prototype. Virtual Mata-Set. Trois productions mixetes développées par notre compagnie.

Diver questionne la question du corps comme polissé, etc. Image feedback déterminé par mouvement du spectateur.

Fullome installation. Nommer champ au micro, reconnaissance. 12 thématiques traitées.

Meta galerie, expérimenter différents états de présence. Interactions danseurs et personnages virtuels. Interaction en temps réel. 

Métadonnées qui peuvent être utilisées par les utilisateurs. Possible de sélectionner entrée par pointeur pour consultation des ressources. Notre but investiguer comment perception change quand les frontières entre réalité, documentation disparaissent dans un environnement virtuel.

Idée de considérer les gestes des utilisateurs, instabilité comme réactions à l’archives qui possède une dimention haptique et esthétique.

Accès virtuel, permet accès plus direct aux archives. Navigation path et processus de penser qui fait partie de l’expérience. Une nouvelle expérience numérique de l’archive. 

## Performing and Visual Arts Documentation and Analysis

### Distant Viewing with Libraries: Photography and the Library of Congress

Lauren Tilton, University of Richmond (USA)

- In Focus Digital Scholarship and Pedagoy, 2019
- The visual turn : using neurol network
- Digital Sound studies 2019

Appel à convergence de ces domaines d’étude.

Special eduction DHQ, Visual, etc. Mark Williams, Media ecology

TV studies, quelques programmes encore à la TV toujours traduits, etc. Si s’intéresse circulation, transmission, TV incroyable.

Film studies : close and computational analysis

Étendre l’analyse à la TV. Approches quantitatives.

Network era of US television

Questions de recherche : approches transversales, prendre en compte son et vision ensemble.

Données

Focalisation sur des programmes de sitcom (représentation femme), enjeux de droit auteur. Réelle question d’échelle pour travailler sur cela.

Annotation, détection des visages. Reconnaissance des espaces. Détection des objets. Analyse factorielle des correspondances. 

Analyse des interventions orales.

Durée moyenne des plans corrélé avec le nombre de personnes présentes dans le plan. Le temps média pour commencer à parler...

### Multimodal Video Annotations as Metadata for Performing Arts Documentation

Carla Fernandes, NOVA University Lisbon (Portugal)

### Curating Born-Digital Archives at the National Library of France: the Amos Gitai collection’s Case Study

Rime Touil, Bibliothèque nationale de France (France)

- BNF 41 M doc dépot léagl
- 10M de documents numérisés gallica
- collections nativement nuémrqieu, arts de la performance --> enjeux spécifiques de conservation

Assurer l’intégrite des données originiales par ex garantiqueque les données dont confié responsabilité au moment donation ne soient pas altériées = bit-lever preservation

fournir un accès direct et à long terme aux fichiers dans leur format original ou, dans certains cas pour des raison de conservation, néceiisté de la production d’une version aletenratiev, dans une forme aussi proche possible que l’original = stratégie de migration

ADDN workflow et plateforme SPAR

Frontin, a data analysis tool, accès à la structure classificatoire.

Donnation de la collection Amos Gitai, tournant pour nous.

Site Archifiltre https://archifiltre.fr

TriNum conài comme webservice. Nouveau système d’arrangement de fichier. Permet de visualiser le contenu et les caractéristiques des fichiers. Accepter, migrer, supprimer ou refuser des fichiers. Définir un niveau de description pour les métadonnées descriptives.

## Designing Tools and Workflows by and for Researchers

### Two Historians' Relationship with Sources in the Digital Age

Luca Federico Cerra and Sean Takats, Université du Luxembourg (Luxembourg)

Depuis 2020, équipe de 10 développeurs engagés dans le design et le développement d’une nouvelle plateforme pour l’analyse de données en sciences humaines. The Digital History Advanced Research Projects Accelerator (DHARPA) mais mauvais acronyme...

https://dharpa.org

https://github.com/DHARPA-Project

> We want to encourage historians and digital humanities scholars to lift the lid, to show how the application of their expertise works in tandem with technology to produce knowledge, how even digitally enabled research is not a product but a process, reliant on the critical engagement of the scholar.

Questions que pose tout le temps sur la littérature. Les annotations sont-elles privées ou publiques, sont elles destinées à être partagée, éphémère ou pour durer ? Quelque chose à réinventer ? Est-ce que des liens sémantiques aux choses ou à des questions de recherche (problème que veut résoudre) ou les deux. Liens avec le passé ou ce que veut faire. Quid de leur visualisation ?

Dans Zotero, annotation reliée à la source. Cœur de notre activité. Approche des annotations diffère. 

Data onboarding, etc. layers of annotation, ajout signal ou tracer les bruits. Travailler sur des workflows en DH pour transformer les choses en un meilleur design.

Kiara une plateforme backend de notre nouveau projet. Conçu comme annotation.

>*Kiara* is the data orchestration engine developed by the DHARPA project. It uses a modular approach to let users re-use tried and tested data orchestration pipelines, as well as create new ones from existing building blocks. It also helps you manage your research data, and augment it with automatically-, semi-automatically-, and manually- created metadata. Most of this is not yet implemented.

Sean Takats case study. Archives coloniales Aix-en-Provence. IPython, Jupyter. Idée d’extraire les données des IAD disponibles. Idée de voir comment pourrait manipuler ces ensembles de fichiers.

Plusieurs visualisation produites à partir de ces données. Utilisation des notebooks pas adaptée. Nothing but coding. Souvent, exportation pour Gephi pour mise en forme. Souvent perte de temps.

Exemple de ces réseaux. Lieux médicaux en France au XVIIIe. Conçu comme sorte de preuve. Mais comme vous le savez tous, Drucker explique que sorte interprétation. Alors remaniement pour communiquer à l’extérieur.

Recherche sur les guildes et les biens nationaux dans les département des Forêts. Nouveau contexte économique car loi de supression des Guildes qui transforme organisation. Guildes association urbaines républicaines autorégulées, discipline autoorganisée par les métiers.

Etude dans le Luxembourg (département des Forêts). Ici focus sur Arlon où archive. Tracer les liens entre les acheteurs, documenter les liens de confiance entre les acteurs.

Exemple d’un personnage Jean-Baptiste Gillé. Associé à 5 acheteurs.

Kira visualisation reserach workflow. Metadata augmentation. Personnalisation pour la recherche.

Mechanical Turk, ce que veut éviter depuis le début du projet. Explicitement dans l’idée de développer un logiciel qui évite ce truc. Veut précisément produire un environnement qui serait très lié au contexte.

Un logiciel pas conçu à partir d’une spécification générique mais directement à partir des besoins de recherche individuels que nous avons. Construire une équipe avec des chercheurs en début de carrière pour réunir des approches polyformes.

Où annote-t-on la recherche ? Que doit-on annoter ? Comment encourager l’annotation ? Mais toujours se souvenir que pas vraiment une question dès lors qu’est en mesure de proposer un environnement utile pour les chercheurs vont le faire.

Annotation automatique possible. Visualisation Refactorisation de son papier et manipulation CSV édition nom de colonnes pour faciliter mémorisation. Pourrait considérer qu’une activité que pas besoin de mémoriser. Mais considère que précisément quelque chose que besoin de mémoriser.

Développement de solutions plus sophistiquées. Nettoyage de fichiers, etc. Finalement offrait une bonne interface pour les chercheurs pour travailler. Inputs and output dans la source.

Python based, fournit un framework to écrire des modules. Formats exports, etc. en introduisant la traçabilité pour servir d’aide mémoire, etc. Potentiel de cela pourrait aussi être intéressant pour des applications de gestion de données.

Quid du design d’inteface. Passé beaucoup de temps à spécifier et respécifier. Question du public très important. Au départ du projet engagement pour produire quelque chose accessible pour le chercheur. Mais progressivement le projet s’est orienté vers des chercheurs qui ont de l’expérience en codage.

Actuellement un environnement Python qui nécessite d’être buildé. Ne voit pas trop comment faire différent. Sans doute pas pour l’utilisateur lambda.

### AI Toolkits for the Social Sciences and Humanities: A Closer Look at ModOAP, BaOIA, EyCon, and PictorIA.

Julien Schuh, Université Paris Nanterre (France)

Utilisation IA sur de très grands corpus. Mais avant d’entrer plus avant dans ce consortium voudrait amener un peu de contexte pour expliquer les prémices de ce consortium.

Questions émergeant des DH et digital application teools questions épistémologiques.

Émergeance outils IA actuellement dominées par de très grands acteurs commerciaux qui influence et interroge beaucoup le potentiel épistémologique de ces outils.

Un enjeux majeur d’autant qu’outils en grande partie conçus pour un contexte contemporain ou des enjeux commerciaux. Ce qui pose beaucoup d’enjeux pour explorer les données du passé. Manque d’historical framework, problème culture localisées.

Aussi question de savoir comment amène ce genre d’outils pour les chercheurs. Comment faire pour que les chercheurs puissent s’approprier ces outils sans nécessairement 

Depuis 2019 essaye de développer AI Toolboxs projet pour rejoindre les besoins de la communauté. Projet Labex Passés dans le Présent puis Huma-Num. Aujourd’hui consortium 

Redéfinir ces outils dans le contexte...

Emphase sur importance critique de ces outils pour les chercheurs alors que deviennent cruciaux pour interpréter et gérer des données culturelles.

Outils pour lesquels souhaitait voir se développer un dialogue entre des chercheurs issus de différentes discplines mais aussi différents métiers (bib archives, chercheur) qui travaillaient sur des contenus massives et besoin de tels outils. Non seulement besoin d’outils mais aussi créer une communauté pour s’approprier les outils et grandir avec eux.

Ne voulait pas créer des outils de nulle part mais pouvoir travailler sur un certain nombre d‘études de cas pour aller vers la création d’outils. Opérationnaliser (cf. Moretti). 

Projet Modoap. Photo-journalisme, etc. Classifier objets et images, etc. Une coopération avec Huma-Num pour engager un dialogue car voulait devenir partie prenante pour identifier des outils pouvant être industrialisés. 

Collection Elie Kagan. 

Comment obtenir informations. Comment recontextualiser l’archive. Comment ramener de la signification sur le contenu de cette archive et rétablir active rememberance. Possibilité de recréer à grande échelle le processus que pouvons avoir comme humain quand explore ces contenus.

Plusieurs tâches classique que voulait pouvoir faire. Par exemple extraction des illustrations des magazines pour pouvoir identifier leur provenance. Tâche relativement compliquée, plusieurs outils existants. Mais chaque fois qu’un genre différent de magazine ou mise en page différente, outils plus ou moins efficiants.

Comment annoter ces contenus pour obtenir meilleurs résultats. Plutôt qu’annoter, décidé d’utiliser les données déjà présentes à la bnf. La Bnf fournit en effet des fichiers ALTO qui indiquent directement la place. Mais problèmes avec API car utilisation inhabituel. Utilisation API pour entraîner le modèle et bons résultats.

Exemple autres outils employés pour identifer éléments significatifs. Par exemple Snoop pour repérer swastika. https://inalelab.hypotheses.org/642

Projet EYCON, VIsual AI and Early Conflict Photography https://eycon.hypotheses.org

### The Linked Infrastructure for Networked Cultural Scholarship (LINCS): Bridging the Research/Heritage Collection Gap.

Susan Brown and Kim Martin, University of Guelph (Canada)

LINCS ensemble d’outils, infrastructure.

CIDOC CRM, SHACL

Web Annotation model, plus facile à adopter, grand potentiel en conjonction objets culturels.

Stratégie de compbinaison CIDOC CRM et Web Annotation

Données extraites des fichiers TEI. Fournit contexte lisible par l’humain. Modèle qui permet de mieux traiter la provenance que le montre ici.

grand potentiel des annotations pour enrichir expérience des GLAM en ligne.

- contectaulisation
- LOD situer nuance
- potentiel de remédiation des données problématiques

Challenge de travailler à travers différents secteurs d’activités

- amener donnes et contexte ensemble in situ
- n’impacte pas large workflow institutionnel
- Dissémination savoirs de recherche

Challenges techniques

- usabillity
- interopérabilité
- scale

## Perspectives

Préservation, parfois reconstruction. Archives rôle de détruire. Peut-être inclure dès le début du projet une réflexion sur que souhaite conserver. Besoin de définir des projets qui ciblent des usages plus généraux d’emblée. Injonction à délivrer des résultes ou des solutions qui pourraient durer.

Clarisse, dit que ce qui la rend optimiste, c’est que dispose aujourd’hui de standards et de framework. Les gens font de plus en plus attention aux standards. IIIF, TEI, WebAnnotation, de nombreux efforts sur lesquels nous pouvons désormais capitaliser. Bien sûr rien de garanti. 

Si dispose d’outils basés sur des standards, peuvent être interopérable. Alors possible de créer des flux de données ou de concevoir un réseau d’outils ou de méthodologies.

Informaticiens, particulièrement sensible à la possibilité d’établir la confiance. Mais informaticiens, sans doute pas la solution des formats qu’ils considèrent comme réponse adaptée. Plus un enjeu d’évaluation que de standard. Plutôt mettre l’accent sur des métriques, mesures d’erreurs.

DH toujours publications relatives Semantic Web technologies. Informaticiens recutés venant chez HumaNum ne comprennent rien aux standards et formats (websem, XML), JSON oui mais pas de sémantique. CIDOC pour un chercheur moyen difficile à adopter. Parfois de très bons standards mais difficiles à approcher ou à s’approprier. Parfois aussi disparaissent.

Toujours une tension entre standardisation et localisation. Ce que je vois c’est qu’en matière de linked données, pas de bon standard pour documenter la nationalité. Les gens utilisent les pays, mais mauvaise utilisation car au final ne dit pas ce que dit. Vrai choix difficile dans LINCS utiliser CIDOC. Aurait pu faire des choix plus orientés vers les utilisateurs.

Sdts surper powerfull, disciplinary, mais formattent aussi les choses. Dans les projets différentes temporalités, parfois bricolage au début du projet. Mais lorsqu’un projet est terminé, sans doute besoin de tels standards.

D’autres types de choses que peuvent mettre en œuvre comme humanistes, en utilisant des standard peut nous aider à documenter nos modèles. Force à expliciter nos pratiques. Plusieurs standars, CIDOC-CRM, FRBR-oo, ArcheoCRM, RiCo, etc.

Dans le domaine de la protection patrimoniale, mais peut être doit apprendre du champ du ML mieux comprendre nos modèles de manière à ce qu’ils soient plus lisibles. Souvent challenge des utilisateurs de données que de mieux documenter. Exemple INA, construction knowledge graph fondé sur un CMS qui peut exposer ontologies et documents multimédias. Mais pas d’API pour cela. C’est model agnostic, peut exposer n’importe quel modèle que l’on veut, mais pas API, ni documentation.

SWAN Open API documenté mais fondamentalement détermine les points d’accès mais pas le contenu. En quelque sorte alors besoin d’une documentation de profil d’API.

Question écologique et réduction impact. Partage annotation.

Sharing embedding, Parfois pas besoin de IA pour traiter certains sujets, solutions anciennes peuvent être bonnes solutions. Parfois prendre marteau pour tuer une mouche. Sans doute pas une seule réponse. Réponse technologique que utilisations locales, coûts qui diminueraient. Une approche pourrait être seulement d’utiliser cela si absoluement nécessaire. Si questionne de manière raisonnée sans doute la meilleure solution. INA deux consommateurs de GPU : la recherche (gens qui font de l’entraînement) et travail sur les inférences (classification et enrichissement métadonnées). Ceux pour qui organisation pour réduire emprunte écologique du travail. Grouper les ressources rationnaliser.

Au niveau de Huma-Num, très clair que gens déposent données chez Huma-num mais ne savent pas toujours pourquoi. Souvent plutôt laborieux de nettoyer. Souvent aussi écriture de code informatique peu optimisée.

## Compte rendu

Colloque lancement projet ERC Clarisse Bardiot

- archivage spectacle vivant cf. https://memorekall.com DOCAM 2006 (Fondation Daniel Langlois), 2013 Rekall et MemoRekall
- analyse distante

Thématiques du colloque

Réunion acteurs de différents champs : culture visuelle, audiovisuel et arts du spectacle. Marginalement HA. Enjeux reliés aux évolutions récentes intervenues avec le protocole IIIF (flux vidéo, objets 3D) et croisement des travaux avec IA. Liens avec colloque IA La mesure des images. Perspective sur la multimodalité : audio/video, etc. mais aussi Tournant multimodal cf. conférence de Melvin Wevers U of Amsterdam.

Intervenants principalement étrangers

- Quid annotation
- Quid multimodalité

Workshops

- Lauren Tilton [Distant Viewing Toolkit](https://github.com/distant-viewing/dvt)
- Jacob Hart et Clarisse Bardiot [Scene](https://scene.tetras-libre.fr)

Ouverture Scott Delahunta (Coventry University) https://motionbank.org

- Analyse documents audiovisues
- Temporal dimension of distant viewing
- IIIF

Keynote Mevin Melvers et formalisme

- Storytelling and narratives
- 

