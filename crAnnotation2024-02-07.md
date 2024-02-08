# Reimagining Annotation for Multimodal Cultural Heritage

7-9 Feb 2024 Rennes (France)

https://reimagining-amch.sciencesconf.org

## Workshop: SCENE

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

## Distant Viewing Toolkit

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

## Inauguration

Colloque qui fera probablement date. Mémoire du geste créatif

Annotation et enjeux. Première talk ouverture.

## Scott Delahunta (Coventry University)

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

## Advene, 20 years of vido annotation

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

Discussion

