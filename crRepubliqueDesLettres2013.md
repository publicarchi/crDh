crRepubliqueDesLettres2013.md

(suite) voir notes ipad

http://emlo.bodleian.ox.ac.uk/

# Republic of letters, Edelstein

Nicole Coleman et Edelstein;

Au départ pas un projet numérique, mais rapidement aurait voulu pouvoir visualiser ces données établies par ? sur une carte. Alors travail en collaboration avec un étudiant de Stanford.

Question du cosmopolitisme et de l’internationalisme. Cartographie qui fait cependant apparaître la place centrale de Paris et de la correspondance nationale.

Un assemblage questionnable, peu de savoir historique à en tirer. Ceci dit quelque utilité historique de ce modèle qui pourrait par exemple servir de moteur de recherche. Une autre manière d'entrer dans un corpus. Offre également la possibilité de formuler un certain nombre d'hypothèses. Permet ainsi de visualiser facilement l'absence de l'Espagne ou même presque celle de l'Autriche. Il est cependant difficile de formuler des conclusions.

Comment utiliser ce genre de cartes pour susciter des questions de recherche. Il ne s’agit pas du tout de formuler des questions, mais plutôt de voir comment formuler ou faire émerger des questions de recherche.

En réalité cette carte ne présente pas vraiment la correspondance de Voltaire mais seulement celle pour lesquelles on dispose de la date et des localisations de l’expéditeur et du destinataire. Or c’est seulement ici 10% du corpus qui est présenté. Et ce corpus même ne représentant sans doute qu’une infime partie de l’ensemble de la correspondance de Voltaire. Westerman ?? supposant que sans doute plus de 50% perdue.

Dès lors comment produire des visualisations pour tenir compte de ces données partielles. Voici une autre approche développée aujourd’hui (plus en Flash). Un histogramme a été ajouté à la visualisation, c’est un graph par années qui montre le volume de lettres. Cet histogramme permet également de visualiser, par années, toutes les lettres qui ne sont pas sur la carte.

Nous avons ensuite essayé de voir comment présenter d’autres métadonnées sur la carte. Par exemple le genre du correspondant, sa nationalité, son occupation, etc. La nationalité ne signifiant pas nécessairement grand chose (ne serait-ce que pour les genevois) mais cela permettait au moins de situer tous ces gens dans l’espace. Deux graphes ont donc été ajoutés, l’un montrant la proportion de la correspondance d’après la nationalité. La même information étant proposée annuellement. Simplement une manière d’essayer d’utiliser la multi-dimensionnalité des données pour essayer de fournir plus d’information à l’utilisateur afin de lui fournir une idée du contexte.

Encore une fois, ici il ne s’agit pas d’envisager cela comme la production de résultats définitifs, mais plutôt comme une manière d’aborder la question du savoir sur cette période et de formuler des questionnements de recherche. Pour nous, ces visualisations et les DH en général ne sont pas une discipline où l’on doive employer des méthodes statistiques lourdes pour régler les choses de manière définitive, mais plutôt une approche mixe où va utiliser des informations quantitatives pour ensuite retourner classiquement à notre recherche.

Ainsi par exemple, peu de choses sur l’Angleterre, y est retourné ensuite et Voltaire dit clairement que se moque pas mal de l’Angleterre dont d’après lui le règne est passé. Finalement avec ce travail, on se rend compte que l’on se soucie un peu moins de situer les gens dans l’espace, plutôt question de l’identité. Dès lors pourquoi utiliser des cartes, ici a commencé à faire des visualisations de réseau avec Gephi. Or s’est aperçu que Gephi ne fonctionnait pas très bien pour nos données, car réellement conçu pour les sciences sociales. Outils conçus pour utiliser des algorithme, pour nous aucun sens compte-tenu du nombre et de la qualité de nos données. Dès lors, on a utilisé ces visualisations manuellement pour poser des questions qui nous intéressent. Par exemple savoir qui est en contact avec qui. Pas de rapport entre Franklin et Voltaire, néanmoins trois correspondants en communs si l’on sélectionne Voltaire ce qui peut permettre de reconstituer des réseaux.

Dernière visualisation adaptée de Maurice Stephaner (elastic search ?). Une manière d’explorer la multi-dimensionnalité des données. Au lieu de se demander qui sont les Allemands, etc. se demander qui sont les femmes nées en Allemagne qui sont en relation avec le gouvernement. La liste proposée devant permettre de se connecter à Wikipédia. Encore une fois, c’est plutôt un **moteur de découverte**. Toujours des grands motifs qui apparaissent, mais enjeu de poser des questions nouvelles. Une bourse disponible pour l’année à venir pour tout mettre ensemble dans une visualisation et le mettre à disposition en open source pour que chacun puisse examiner ses données avec les outils conçus dans le cadre de ce projet. Naturellement partage le rêve de cette époque qui consisterait à mettre ensemble toutes nos métadonnées pour enfin se faire une idée de la République des lettres.

# Republic of letters, Nicole Coleman (Stanford)

Première visualisation, la première réponse à la première visualisation. Second projet première manière de répondre à la question de ce qui était visible sur le plan et ce qui n’était pas visible sur le plan.

Notre approche consistait à modifier la visualisation pour correspondre à nos questionnements. Autre projet qui répond à la temporalité et la relation dans le cadre du projet sur le grand tour.

Autre projet ou cartographie.

Projet où visualisation du texte, transformation d’un texte qui prend la forme d’un listing de 6000 personnes comme une autre visualisation des relations exprimées dans ce texte.

Autre projet qui explore encore la correspondance ici révéler le processus qui nous fait produire un plan. Choisissons l’auteur, ou l’archive à utiliser. On peut ainsi disposer d’une vue transversale dans les collections, dans la temporalité, ou sur une carte et visualiser le résultat sur le plan. L’idée ici étant de supprimer la boîte noire en révélant le plus possible le processus en jeu dans la production de la visualisation.

Autre projet où propose encore de manipuler les contenus. Permet de visualiser ensemble des nœuds par lieux et personnes. Ici nous n’avons pas utilisé de contrainte de temps autre que les bornes chronologiques du dictionnaire. La visualisation qui fait alors émerger des relations entre les personnes autres que la stricte contemporanéité au travers de l’appartenance à une même académie, etc.

Ensemble de ces travaux classifiés en fonction de leurs parties constitutives. Analyse de réseau, chronologie, cartographie. (galerie des projets visualisation en couleur silhouette des composants présentés sous la forme d’histogrammes l’un sous l’autre) et classification des fonctionnalités (chronologie comme filtre, etc.). À partir de cette distillation, nous avons commencé à travailler sur un outil qui combinerait l’ensemble de ces fonctionnalités. Cela constitue une nouvelle période dans notre développement au sens où il s’agit de rendre cet outil utilisable par chacun à partir de ses propres données pour produire ses propres visualisations.

Visualisation sur une carte. Permet de réaliser des sélection sur les éléments que veut voir figurer sur le plan, permet d’agir sur la dimension de la carte. De même fait évoluer les connexions. On propose également des filtres, par exemple un filtre qui présente les durées de vie. Une visualisation que l’on peut utiliser comme un filtre pour explorer les données. Permet de produire des rapports quantitatifs avec les villes de destinations, etc.

Pourquoi visualise-t-on ?

On visualise car c’est une manière simple de partager et d’échanger sur des données. Pourquoi adopte-t-on les techniques de visualisations déjà utilisées dans le domaine. Certes, parce qu’elles sont d’abord familières et compréhensibles.

-   chronologie

-   graphique de réseau

-   carte

Néanmoins, des choses qu’il est difficile à présenter sous formes visuelles ou chiffrée sous la forme internationale AAAA-MM-DD. Par exemple « late summer ». Nous force à produire une réduction de nos données. Nous avions donc besoin de formes plus complexes pour exprimer le temps, qui permettent notamment de prendre en compte l’incertitude. Comment produire des outils qui puissent prendre en compte cela sans introduire un nouveau filtre d’interprétation entre les chercheurs et le matériel original.

Nous avons ainsi conçus un ensemble de principe de design qui nous semblaient permettre de répondre à ce défi :

-   1 exposer la complexité

Au lieu d’adopter une simplification, exposons plutôt la complexité en fournissant tous les éléments aux experts. Ne pas utiliser l’ordinateur pour lancer des modèles pré-déterminés d’analyse. Plutôt utiliser la visualisation non pas comme résultat final du processus (output), mais comme un élément du processus de recherche lui même. L’envisager comme un nouveau processus d’exploration des données. Il s’agit aussi de pouvoir mettre fragments ensemble pour fournir plus de richesse de contexte.

-   2 Fournir un contexte

-   3\. Réveal Spatial-temporal-relational dynamics

Révéler la dynamique spatio-temporelle et relationnelle.

Souvent difficile à percevoir, trouver des moyens pour la montrer.

-   4 Let User Structure the Data

Permettre à l’utilisateur d’organiser les données.

Sans doute la partie la plus complexe du travail. Ce que l’utilisateur manipule généralement pas l’ensemble de l’information, une partie seulement. Laisser l’expert être partie prenante du processus. Cela a aussi à voir avec l’interprétation.

Exemple de notre processus de travail.

Ceci Joseph Chrisli ?? historiography 1765 ?? exemple newtonien pour montrer l’histoire. Le premier à établir une échelle de temps unifiée basée sur l’espérance de vie.

Un accès en ordonnée également. Une telle visualisation qui a été très inspirante pour nous notamment par sa manière de traiter l’incertitude au moyen d’ellipses de taille différente selon le niveau d’incertitude.

L’auteur met également en œuvre un groupement des personnalités très subjectifs. À la fois la production d’une forme très standardisée de présentation mais également très interprétative.

Exemple dictionnaire du grand tour où ont appliqué le concept de chronologie avec même chronologie mais dont la ville est Rome. Présente un panorama général des voyages à Rome. Une chronologie navigable et dimensionnable (timeline slider).

En plaçant le curseur sur un élément, on peut faire apparaître plusieurs éléments comme les dates des différentes visites et l’âge de la personne lors de sa visite.

On peut également chercher sur n’importe quel des termes présents dans l’entrée. Permet d’accéder à l’ensemble des entrées du dictionnaire à Rome au même moment. Une manière d’accéder au contenu textuel du volume la plus conceptuelle possible.

Autre inspiration A. Kirscher du réseau Jésuite

Présente maison mère à Rome et chaque branche qui présente les différents collèges comme s’ils fleurissaient.

Une cartographie typique de réseau, mais qui inclut les lieux mais aussi le temps. Avant d’arriver à ce modèle générique, utile pour réfléchir à la manière d’incorporer ces différents éléments.

Autre exemple d’un artiste

Travaillait sur des problèmes utilisant des graphs de réseau pour lesquels il a produit sont propre langage visuel. Une manière d’exposer la controverse entre CIA et Georges Bush. Intéressant de voir comment il incorpore ici le temps, et inclut un graphique dans l’autre sur une chronologie.

Sortes de mindmapping

Une grande partie des choses que l’on fait dans notre laboratoire proches de cela. Nous dessinons beaucoup pour voir ce que l’on peut tirer des données. Joue beaucoup dans notre processus de design.

Autre élément qui nous a beaucoup inspiré, visualisation d’un couple lors de son mariage avec ensemble des invités au mariage. Description des connexions entre ces personnes. Question centrale aux humanités, comment est-ce que nous annotons. Comment nous produisons et représentons l’information.

Enfin une représentation géographique permettant de visualiser les changements géospaciaux dans le temps. Une des choses les plus difficiles à représenter les flux.

Pour ce faire on peut utiliser des GIS comme ARC GIS qui sont très précis, et scientifiques mais gèrent difficilement l’incertitude et l’inconsistance des données.

Carte des courants dans le Mississipi

Autre manière de prendre en compte le changement dans la cartographie. Plan par Christian Nold ??. Tradition de cartographie. Un artiste, donc pas encombré des problèmes qu’ont les chercheurs en matière de validité, et de précision. Travail de plusieurs années sur la cartographie de l’émotion. Ici pas un plan technique mais le genre de choses que l’on regarde pour explorer des pistes de travail ou trouver de l’inspiration pour des visualisations.

Enfin, Jeremy Wood artiste anglais qui fournit un exemple de dessin par les données. Ici des visualisations gouvernées par les données. Ici s’est pisté avec un GPS. Ici 4 saisons différentes. Montre que peut être expressif avec les données.

Un exemple dans le cadre de notre partenariat avec Irène, utilisant Gephi, avons établi les intersections entre Voltaire et d’Alembert. Gephi peu pertinent pour nous comme ne disposons pas de données quantitatives (metrics) importantes pour faire des analyses statistiques. Ici l’on a plutôt utilisé l’outil pour travailler les données. Plutôt une esquisse en utilisant l’outil pour déplacer les nœuds instinctivement d’après sa propre logique. Élite, salonière, genevois, etc. cependant ces catégories ne sont pas exclusives les unes des autres.

Doit pouvoir faire cela facilement, car une manière de penser avec les données. Sans ces connexions avec la visualisation, seulement une liste de noms peu intéressante. Ici possible de manipuler les relations pour les classer.

Autre manière où traite plusieurs neuds interactions avec les nœuds.

Cas où veut supprimer les doublons, autres où veut faire des rapprochement, autre où veut mettre les gens dans un groupe tel que Génévains et voir le résultat dès lors que les met dans un groupe. Pour nous central que les individus puissent ajouter des données dans la base. Qu’il soit également possible pour les personnes d’introduire leur propre schéma pour analyser les données.

# HuygensIng The ePistolarium, experiences in the development of a digital tool for the research of 17th century

Charles van den Heuvel, Nl

Comment combiner des données hétérogènes.

…

Peut-on reconnaître des schémas dans le temps

Comment rendre cette information disponible dans les humanités.

Comment rendre cette information annotables de manière collaborative

Pour produire les données, transcription de la correspondance.

OCR\_Files de 20 000 lettres disponibles avec métadonnées.

Pas d’uniformité dans la structure des éditions imprimées utilisées.

Le corpus pas uniforme du point de vue des langues et de l’orthographe

Pas d’uniformité dans les métadonnées

Comment traiter les figures et formules.

Gros travail de curation nécessaire.

Développer des outils pour reconnaître la langue et même le contenu mixte.

Bien sûr nécessaire poru l’outil de recherche.

Normalisation de l’orthographe

Retirer les articles défins ou indéfinis

Topic modeling, etc.

Topic modelling

Partie du texte basées sur les mots

Pour identifier les textes d’après mots comparables, documents comparables, ou fragment de texte comparables.

Premières expérimentations avec un outil de Stanford

Permis d’établir des graphes de correspondance qui paraissaient très prométeurs. Mais il est apparu que plus compliqué qu’il n’y paraissait.

Test sur deux ans de travail.

20 historiens des sciences, au sein d’un workshop pour leur demander ce qu’ils en pensaient. Savoir si quelque chose d’utilisable pour leur recherche. Réponse : Non !

L’outil qui ne nous présente pas des mots pertinents, etc.

Le problème quand travaille sur de nouveaux outils.

Continué à travaillé dans le domaine du topic modelling en combinaison avec les technologies du langage.

Augmenter les possibilités de recherche, etc.

## Résultat actuel ePistolarium

http://ckcc.huygens.knaw….

Pas encore toutes les reproductions des lettres.

Recherche plein texte comme avec Google.

Et recherche à facette.

Suggestion de termes en rapport.

Visualisation et co-citations possible.

Mais pas collaboratif et pas d’annotation possible pour le moment.

## Co-citation analysis

Générer automatiquement des co-citations pour chaque paragraphe dans le corpus des lettres.

Tester pertinence de cette fonctionnalité

Place centrale de Huygens dans le corpus, donc test sur cette correspondance.

Le cas de saturne

1611 première fois vue

1616 planet avec anneaux

1642 considère que sans

1642-1654 confusion, collecte d’information

1671-1672 Cassini…

400 réponses dans l’ePistolarium

Concentration des lettres sur une période chronologique données

Mentions de correspondance

Seuil de 10 pour la co-citation

… outil peu efficace.

Pour la période où Huygens concerné, ici plus pertinent 166 personnes incluses.

L’outil de co-citation permet de révéler généralement les acteurs les plus importants de la discussion sur saturne. Pour une interprétation correcte, interprétation historique experte nécessaire.

Les outils numériques fournissent d’énormes possibilité d’accélération de la recherche et opportunités pour répondre à des questions. Cependant les corpus généralement trop petits pour fournir des résultats surlesquels se baser de manière fiable.

Des corpus très importants de lettres sont donc nécessaire. Très nombreuses lettres de savants de la périodes pas même transcrites ou numérisées et dont ne connaît pas le contenu.

Ne pas avoir des attentes trop hautes. C’est un outil. Les questions doivent correspondre à l’outil et ses possibilités.

En termes de Maintenance et extension des projets financés, comment garantir maintient de ceux qui ne fournissent pas satisfaction.

Standardisation des métadonnées est urgente pour pouvoir opérer ces contenus.

Et enfin une coopération internationale est nécessaire. Nous devons rejoindre nos forces sur le sujet de la république des lettres pour travailler à une autre échelle.

Voulons élaborer pour la suite un colaboratoire. Nous avons un très bon outil d’édition mais pas combiné encore à cet outil. Il est également nécessaire de lier les lettres à d’autres documents, connecter ces lettres.

Lien avec les premiers périodiques car souvent lettres imprimées, pas sans conséquences sur leur contenu et possibilité d’analyser différences de ce point de vue.

Catalogue de métadonnées de correspondance aux NL.

# Discussion

## Catherine J.

Vous avez commencé votre intervention en disant qu’il n’y avait pas de « big picture » en disposez vous aujourd’hui. Est-ce que permettent de voir ces outils nous permettent de nous faire une idée plus précise.

## R.

Vous mentirez en disant que l’on l’a. travaillant sur Voltaire, avoir les 19 000 lettres en tête déjà difficile. Commence à avoir une bonne vue générale cependant.

Quant à savoir si c’est même désirable où si ce sont les agences de financement qui nous encouragent pour aller dans cette direction, je pense qu’il y aura toujours des outils génériques, mais il me semble que tout le monde peut s’accorder sur le fait que nous avons besoin de disposer de métadonnées globales. Pour ce qui est de mener des recherches plus spécialisées, sans doute utile de disposer d’outils plus spécialisés.

## R. nl

Permet des recherche que ne peut faire à la main. Un vrai avantage, mais reste des outils, pas une réponse. La réponse celle des chercheurs. Lorsque finance les projets souvent supposé que les big datas vont résoudre des questions. Pas si simple.

## Irène Passeron

Question des points aveugles.

Données numérisées celles de Voltaire, Descartes, etc. et moins souvent les éditeurs, etc. Or effectivement voit apparaître nombreux personnages chez qui se réunissaient, etc. ni été saisie ni conservée, ou pas encore traitée. Doit en tenir compte en tant qu’historiens pour aborder cette république des lettres.

R. sw

Tout est fait pour aboutir dans une base de données cf. Mallaramée. Mais rien n’indique que doive en rester aux correspondances.

## Jean Gabriel G\[alarcia\]

J’ai vu cet été un travail de Kaplan sur les confessions, en regardant les personnages qui apparaissent pour créer des relations entre les personnages. Des graphes qui ressemblent à vos graphes même si d’autres sources.

Agréablement surpris d’autant que peu coûteux comme travail car se contentait de réduire les index.

Autre question, vos évoquez des correspondance imprimées.

## R

Repose sur l’utilisation d’édition imprimée à visée scientifique. S’est restreint aux éditions modernes.

## ?

Trouvé très intéressant manière dont avez pointé la question de l’incertitude. Pour toutes les données pas toujours possible de calculer l’incertitude, et très souvent ne savons pas à quelle date telle lettre a été écrite, ou bien encore qui est le destinataire, ou si d’autres lettres entrent dans cette correspondance.

Vous avez présenté des logiciels. Me semble utile, peut-on les utiliser.

Gephi permet d’avancer un peu. Mais pas suffisant.

## Nicole Coleman

Pour ce qui est de l’incertitude, je formulais l’hypothèse qu’il y a des efforts à conduire pour s’occuper de l’incertitude. Par ailleurs également nécessaire de mesurer l’incertitude, mais n’avons pas voulu mesurer l’incertitude.

Au lieu de penser notre projet en nous disant comment visualiser l’incertitude, plutôt révéler la complexité.

## R sw

Questions traditionnelles que peut se poser sur ces réseaux si nous étions sociologues, etc. cependant pas conservé toute la correspondance et difficile de tirer des conclusion.

En revanche avec un clustering pourrait peut-être faire sortir des choses significatives. Dans notre cas, ne peut rien conclure des absences, mais par contre peut trouver des présences qui ont une certaine valeur.

## R.

Rapidement rendra les matériaux produits ouverts et open.

Fera circuler une feuille pour tester.

## R Bodesian

Relève qu’ont également commencé à noter les lettres mentionnées dans la correspondance pour commencer à produire des entrées.

## R. nl

Dans la datation nous utilisons la date réelle recalculée

Écriture du nom de Huygens peut être écrit de plus de 30 manières différentes. Doit donc pouvoir aussi incorporer le savoir de ce type.

# Christine Blondel, Présentation de l’édition numérique de la correspondance d'Ampère

Offrir accès en ligne à l’ensemble des publications d’Ampère. Ouvrages imprimés et fonds d’archives, fonds intégralement disponible en ligne. Autre partie du projet consacrée à l’histoire de l’électricité pour construire un parcours historique pédagogique. Phase active 2005-2010. Depuis peu de développements faute de financement.

Nouveau projet financé ANR Corpus 2011. Rebâtir le site en tenant compte des nouvelles problématiques et des événements intervenus dans l’édition numérique ces dernières années.

## Pourquoi une édition numérique ?

Souvent le volume rédhibitoire pour éditeur privé.

Avantage de permettre de tenir compte des découvertes ultérieures.

Édition imprimée qui présente néanmoins certains avantages, lectorat bien identifié et habitude de consultation de l’appareil critique. Question de l’audience des sites internet qui constitue un vrai problème car a constaté que nous tirait vers un public plus large.

Dernier point, en termes d’évaluation pour les chercheurs, des dates de révision, des enjeux de citation ou d’évaluation.

Souvent primauté du texte par rapport à l’analyse avec les éditions numériques car confrontés à des corpus importants. Un processus éditorial continu, on peut toujours revenir en arrière, en même temps jamais fini. Les liens avec les autres ressources disponibles. La possibilité d’extraire des sous-correspondance, indexation, visualisation de réseaux, etc.

## La correspondance scientifique du 18^e^ siècle

Marie Térail ?? dit que les savants du 18^e^ siècle ne laissent paraître aucune émotion. C’est extrêmement faux pour Ampère qui laisse beaucoup paraître de sa vie affective et de ses émotions.

L’audience, c’est-à-dire les usages, de ce que l’on met en ligne sont inattendus.

Qu’il s’agisse d’histoire des réseaux, de la vie bourgeoise en province, de l’enseignement. Des tas d’utilisation que l’on ne peut pas prévoir. Raison pour laquelle insiste beaucoup sur le fait que le texte est primaire.

Seulement à partir de la correspondance d’Ampère que peut voir que l’électricité une phase dans sa vie et que son véritable intérêt la philosophie.

## Le site web

Le site web est présenté en deux parties.

Ensemble des publications, problème des niveaux de lecture qui est difficile. Ici diaporama, devra y réfléchir. Certaines publications plus ardues. Fonds des manuscrits, documents Ampère.

Premier projet qui consistait à permettre un usage **jointif** de différents types de documents : correspondance, publication et manuscrits. Et d’utiliser au maximum les autres ressources disponibles sur internet. Le nouveau projet consiste à transcrire les pdf en mode texte en XML-TEI, l’idée de renforcer le côté jointif du projet.

La correspondance qui se compose d’environ une 100 aine de lettre concerne tous les domaines de la sciences, philosophie et religion. Correspondance que l’on peut isolée sur la vie de jeunesse totalement inédite. Sorte d’enseignement mutuel avec son correspondant où dispose de la correspondance active et passive ce qui est relativement rare. Enfin correspondance avec amis et famille qui donne idée vie d’un scientifique en province puis inspecteur général et tournées importants pour l’histoire de l’enseignement.

Édition fin 19^e^ où les courriers très altérés, mais succès fou !

Édition de référence 1936 faite par un scientifique à laquelle avons ajouté plus de 3000 lettres inédites.

Manuscrits classés par chemises. Dossiers et sous-dossiers. Problème des figures et des formules mathématiques, caractères non latins, qui posent souvent des problèmes lorsque passe au numérique.

Choix éditoriaux : offrir pour la consultation à la fois la correspondance et consultation du facsimile. Avons ajouté à la lettre d’autres sources.

Moteur de recherche

Index des noms propres

Index des sujets

Ébauche d’étude de réseau

Tout cela ayant été fait à la main, le problème étant aujourd’hui de savoir ce que l’on peut en faire.

Un inventaire de sa bibliothèque

Les ouvrages mentionnés dans la correspondance qu’a essayé d’identifier en précisant la référence autant que possible. Chaque fois que l’ouvrage en ligne donner le lien de consultation au lecteur.

Texte, facsimile édition imprimée, facsimile edition manuscrite. Prochaine édition voudrait facsimile en regard de l’édition. Autres sources de la lettre. Parfois six sources possibles pour la lettre. Permet de renvoyer à des éditions de référence.

Possibilité de proposer une transcription au moyen d’un éditeur en ligne, accès par login. Dans le futur l’idée serait de pouvoir ouvrir au-delà de l’équipe la transcription avec tous les problèmes de validation que cela pose.

Processus éditorial en XML, open access, référencé par un entrepôt OAI-PMH.

Le projet d’ANR qui vient de commencé a permis le recrutement de deux personnes, Philippe Pons (du master 2 ENC) et Aude (du master Tours). L’objectif de ce projet, comme l’objectif initial, toujours de relier les documents et de connecter les différents types de relations entre le brouillon, manuscrit imprimé, etc. et annotation même si reste encore prospectif. L’idée est de permettre de permettre au chercheur d’annoter en ligne les documents comme il le ferait sur son propre ordinateur, cela en dehors de l’édition critique. Sachant même que cette question d’édition critique susceptible d’évoluer. Est-il vraiment encore utile de transcrire de façon diplomatique alors que fournit le facsimile compte-tenu des difficultés de recherche dans le texte que cela implique.

Question de la gestion à la fois des annotations éventuellement collaborative et d’une édition critique qui serait produite sous une responsabilité éditoriale.

## Les défis

Souvent avec les sites, le sentiment que des projets sans fin. C’est faux dans la mesure où les financements sont à court terme, dans la mesure où ces objets ont besoin d’être nourris soignés dans le temps pour être conservés.

Je pense que pour ce qui est de la conservation des données, des procédures qui se mettent en place, peut-être pas pour la partie éditoriale.

En France, par rapport au paysage anglo-saxon, des petites équipes qui travaillent de manière dispersée sans pouvoir s’appuyer sur de grands centres de digital humanities comme aux États-Unis.

Évolutions rapides du domaine informatique. Choix technologiques que le chercheur doit assumer sans nécessairement avoir la compétence informatique nécessaire pour le faire.

Pas de modèles stabilisés pour des éditions numériques. Pas de consensus, en train de construire ce consensus, pour cela que ce genre de réunions très importantes car permet de se rencontrer et de partager sur des questions très concrètes et pratiques.

Collaboration entre les métiers. Avec les informaticiens mais aussi avec le domaine de l’ingénierie documentaire, car très souvent les problèmes qui se posent des problèmes classiques dans le domaine de l’ingénierie documentaire. Aurait tout intérêt à travailler et échanger plus avec eux. Cependant ne pas perdre de vue que des pratiques différentes.

Archives

Recherche

Et ingénieur

(en rosace). Pour conclure, voulait insister sur l’aspect de travail collectif de ces projets qui est aussi l’un des aspects nouveaux de tous ces projets.

Oubliait de préciser que cette nouvelle édition sera totalement en mode texte, traitée en XML-TEI pour permettre le partage et l’échange de fichier et possibilités de mettre en place des recherches de co-occurrences telles que celles vues tout-à-l’heure. Très intéressant de voir aussi comment les projets présentés précédemment des **outils heuristiques** d’exploration et non pas de displaying.

# Présentation de la base de données du réseau eulérien et d’outils de visualisation par Siegfried Bodenmann

Siegfried Bodenmann, éditeur d’Euler

David Lodge, dans Small world, quel type de conférencier présentait. Ceux qui écrivent au dernier moment, ceux qui ne préparent rien, et un crétin qui rédige avant départ, essaye de l’achever la veille et entame devant l’auditoire un discours dont ne connaît pas la fin. Le crétin c’est moi aujourd’hui !

Par ailleurs changé de titre : « Anatomie d’une correspondance savante »

Partir à l’a chasse d’une bête assez singulière. Un vrai sac de nœud, un être complexe surtout sur le plan relationnel. Partons à la quête du réseau ! et surtout d’un réseau d’un genre particulier, celui épistolaire de Euler.

Au stade embryonnaire un réseau est composé de nœuds et de liens.

Mais à quel moment peut-on finalement parler de la naissance d’un réseau. Est-ce qu’un simple échange intervenant entre deux nœuds constitue un réseau. Sans doute non. Est-ce qu’un réseau à trois point constitue un réseau ? L’historien parlera d’ego-réseau. Un réseau plus complexe à trois bandes fera apparaître quelque chose de plus complexe encore. Enfin avec plus de points encore possible de s’interroger sur le passage d’un réseau à l’autre, la centralité de certains nœuds, etc.

Quelques propriétés importantes qui permettent de catégoriser un réseau, ses nœuds, ses liens.

Ici s’intéresse à des ego-réseaux.

Des liens qui peuvent être dirigés ou non dirigés. Ici intéressant de faire la distinction correspondance passive, active.

Des réseaux multipolaires. Des réseaux très homogènes avec des personnes tous membres d’une même sociabilité (académie), etc. Ici plus hétérogène.

Des réseaux fortement contraints par des conditions autour d’eux, d’autres plus libres. Certains plus fragiles (peu d’interconnexion), d’autres plus ou moins étendu.

Enfin la dimension du temps. Stabilité, instabilité, durabilité ou réseaux qui vont dépérir ou disparaître. Des réseaux qui peuvent exister sur une courte durée, ou une longue durée (d’une vie, d’une académie).

Une des pathologie de cet animal de laboratoire : l’égocentrisme.

Beaucoup des réseaux publiés jusqu’à présents centrés sur une seule personne et peu permettent de situer diverses personnes dans un réseau plus large.

Peu de réseaux font attention au temps.

Virus de la quantification. Beaucoup de données quantitatives mais peu de données collaboratives notamment sur la nature de la relation qui est mise en place (dans le cadre d’une controverse, etc.)

Travaille avec plusieurs outils.

Stocke information dans Excel, importe données dans Gephi, utilise Google map pour représenter l’information, traitement final avec Photoshop.

Euler extrait de son réseau en haut de la représentation pour éviter d’écraser les autres correspondant et permettre de mieux voir ce qu’il se passe.

Ici a donné à chaque point une intensité assez faible. Les points sont placés de manière géographique. Plus le nombre de personne est important plus ils sont gros. Plus intensité de la relation importante plus épaisseur du trait importante.

Plus de 300 correspondants. 3163 lettres, auxquelles peut attacher au moins 2000 de perdues, en outre aucune lettres de familles dont peut penser qu’ont été brûlées. Au moins 5000 à 6000 lettres dont ne voit que moins de la moitié.

Temps qui couvre toute la période de la fin de ses études jusqu’à sa mort. Quasiment un siècle d’histoire des sciences.

Du point de vue géographique, bornes de Édimbourg, jusqu’à la Sibérie (voyage), Moscou, Italie avec Naples et Turin.

Plusieurs centres apparaissent très clairement

Bâle, Paris, Saint-Pétersbourg

Au Royaume Uni chapelain du bibliothécaire du prince de Galles avec qui correspond le plus. Son principal contact britannique qui joue pour lui un véritable rôle de passeurs.

Des centres plus petits autour de Genève et de Bâle. Cf. travaux de René Siris ?? sur l’histoire de la science dans cette petite ville.

Fait également apparaître de grands absents : Espagne, l’Autriche, peu de choses en Italie. On ne parle ni même de la Grèce et de l’Irlande. Montre que le réseau de Euler est relativement contraint, il est très protestant. Mais si Voltaire ces mêmes pays sont peu représentés, d’autres facteurs à prendre en compte qui montre que par rapport à la renaissance le réseau est plus septentrional.

Un réseau relativement centralisé, multidirectionnel

Un réseau décidément hétérogène ne serait-ce que par l’intensité des correspondances, la langue employée dans les lettres. L’impression qu’énormément d’imprimeurs. Aussi un réseau assez ouvert et instable qui évolue beaucoup dans le temps comme nous allons le voir.

Un réseau en cache toujours un autre. Dans cette visualisation se confond plusieurs réseaux ceux de l’académie, du collège, etc. Ici réseau germanique, montre que l’Allemand est très utilisé déjà dans la correspondance. Quelque chose que n’a pu voir qu’à partir du moment où l’on a tout mis dans une base de données. Jusqu’à présent sentiment qu’une correspondance essentiellement écrite en français, mais parce qu’avait d’abord traité la correspondance avec les grands personnages. Or nombreux petits personnages avec qui correspond en langue allemande. L’anglais est en revanche très peu présent alors qu’Euler en savait assez pour donner une traduction des *Principles…* tandis que le français est très présent en Angleterre.

Pensait donc voir émerger l’Allemand comme nouvelle langue vernaculaire, où l’on commence à être fier de sa langue alors qu’émergent des philosophes. En fait, tout le contraire. Euler parle d’abord allemand et latin, mais plus vieilli plus il oubli l’allemand au profit d’une écriture en français.

Visualisation du réseau dans sa totalité de 1727 à 1783

En réalité ce réseau n’a jamais existé. Pour le visualiser dans sa réalité, il est nécessaire de l’examiner dans le temps. Pour cela une vidéo dans le temps qui permet d’avoir une visualisation biographique et contextualisée. Permet alors de faire une biographie de ce réseau et de son comportement dans le temps.

Pour commencer Euler à Saint-Pétersbourg, garde contacts avec Bâle. Étonne car sur place et beaucoup de contacts avec personnes à Saint-Pétersbourg, mais plusieurs correspondants qui ne seront plus sur place lors de son séjour. Parfois toujours correspondance mais parce que contacts officiels, sinon réseau physique qui n’implique pas nécessairement de trace, car correspondance surtout avec les personnes auxquelles n’a pas physiquement accès.

Plusieurs contacts à l’étranger. Avant 30 ans reste limités. Puis s’intensifie et tout à coup apparaît Paris. Une époque où commence à penser à lui comme membre de l’Académie. Plusieurs réseaux vont s’intensifier. Un changement de secrétaire. Mais perte de l’usage d’un œil en 1738 ce qui implique une baisse de l’intensité de ce correspondance.

Euler déménage, appelé à refonder l’académie des sciences à Berlin. Déplacement du réseau avec des gens que ne voient plus car à Saint-Pétersbourg, disparition personnes que voit directement à Berlin. Et comme si déplacement géographique permet étendue du réseau vers la Suisse.

Si regarde ce qui s’est passé jusqu’à présent du point de vue générationnel voit qu’au départ beaucoup correspondu avec personnes plus âgées, plus tard dans le temps des personnes plus jeunes.

Lors séjour Berlinois correspondance essentiellement administrative. Lors polémique ???, plus de temps de correspondre. Une guerre mais pas de réel impact. Lors période beaucoup plus de gens jeunes qui vont correspondre avec lui. Ont constate qu’alors Euler est pleinement établi, il devient un acteur auquel va demander des choses.

Lorsque se brouille et retourne à Saint-Pétersbourg, véritable évanouissement de son réseau de correspondant. Les vieux sont morts et période où il booste sont travail littéraire.

Matérialité des échanges. Coût de la lettre. Problème de réciprocité. Fidélité. Que ne peut montrer dans les échanges.

Stratégie de la correspondance. Ex. de la période des *Introducio* fait apparaître moments où élabore, discute, construction de l’œuvre. Voit ici apparaître le discours dans les correspondance. Si ici avait un facteur de temps, verrait comment une idée peut circuler dans le réseau.

Revenir à Foucault, Bruno Latour et Calon. Ici travaille beaucoup avec les personnes. Mais aussi question du contenu. Dans les concepts de la sociologie des sciences. Idée que plus une idée est stable, peu importe l’idée si le réseau est fort alors cette idée va percer. Voudrait montrer que le contenu épistémologique impose aussi le réseau. Partir des faits contenus dans les lettres pour essayer de comprendre pourquoi, comment ces faits ont un impact sur la structure du réseau.

Remet un peu en question l’intérêt de cette visualisation.

Pour moi intérêt à deux moments de ma recherche. Au tout début pour identifier des choses non intuitives, ou encore pour suivre un chemin. Booste la recherche, aller plus vite, suivre les chemins que propose la carte.

Deuxième étape où utilise ces visualisations à la toute fin pour montrer quelque chose. Si le texte me permet de montrer quelque chose et que j’aime beaucoup raconter les histoires, l’image permet également de montrer quelque chose que le texte ne peut pas montrer avec autant de facilité. Malgré tous les problèmes que posent les bases de données dans notre recherche, il y a deux moments où elles peuvent être vraiment intéressantes : au tout début et à la fin.

# Discussion

## Sur les manques et la prise en compte de l’incertitude

Degré d’incertitude qu’essaye plutôt de montrer à partir du texte.

Dans la majorité les lettres que possède celles qui ont été adressées à Euler, relativement normal car correspondance passive qu’a pu léguée. Toutes les lettres de la correspondance active surtout trouvées par hasard.

Ce que pourrait faire, prendre que les lettres reçues, constituerait peut-être un meilleur élément indicatif sur l’usage de la langue. Mais il faut toujours relativiser. Car au centre de mon travail, pas les réseaux. Ici les réseaux un instrument de mon travail. Rien ne remplace une étude de cas qui pourra être contextualisée dans un réseau. Va alors permettre de repositionner les lettres dont parle dans un réseau plus important.

## Dan

En t’écoutant même si loin d’avoir reconstitué encore la République des lettres, tout de même intéressant de voir se répéter le même motif. Peut alors devenir une indication plus grande.

Mais aussi un cas particulier ici. Dans toutes les correspondance qu’a étudié au contraire une gérontocratie des lettres. Vaudrait donc la peine de chercher. S’agit-il de la correspondance perdue car jugée personnelle. Ou bien véritablement en lien avec le boom des publications.

## R.

Plusieurs facteurs. Boom des publications. Près de 800 articles dans les revues de l’époque. Longtemps été considéré comme le mathématicien le plus prolifique de tous les temps. Il faudrait parler des stratégies d’édition. Mais en fait un boom de publication qui s’explique par l’ensemble des publications restant à publier après son départ de Berlin que publie alors même que publie de son côté à Saint-Pétersbourg.

La correspondance périclite rapidement avant même que perde la vue. En revanche sans doute un transport. Fils aîné de Euler qui va devenir secrétaire académie et aussi son secrétaire particulier. Mais n’arrive pas à mettre la main sur la correspondance. Ces deux individus qui vont reprendre la correspondance du père. Le fils qui reprend la correspondance à la fin de la vie de Euler. Ne signifie donc pas véritablement qu’arrête véritablement de répondre. En même temps à Saint-Petersbourg a une vie très sociale. Devenue l’animal de Catherine et … le grand mathématicien que voit dans le cabinet de curiosité. Dès lors moins de temps de correspondre.

## Alexandre

Question sur le classement des archives numérisées.

## R

Fonds qui a souffert classement. Pour la numérisation clichés réalisés dans l’ordre physique du fonds. Organisées par N°.

Mais par l’analyse interne des documents, évident que tel ou tel document telle page suivi par telle page plus loin. Question de savoir comment permettre continuité de lecture dans un document qui est en fait coupé et espacé.

Pour le moment sécurité vu le nombre de faire en sorte que chaque document soit une image. 53000 documents. Déjà 1500 pages transcrites. Pas encore en TEI mais permettent d’avoir accès au document. Pour le moment s’est contenté d’indication « \[le lecteur trouvera la suite p. xxx\] ».

Vrai problème à traiter. Tout comme peut avoir besoin de faire des rapports entre les documents.

Un réseau documentaire qu’il s’agit de traiter.

Préserver l’intégralité du fonds. La source, puis l’interprétation. Concrètement pas de solution miracle.

Prévoir des usages, tout en tenant compte du fait que certains usages sont encore imprévisibles.

## Question

Quelle métadonnées.

Quel organisme pourrait organiser cette discussion générale.

Comment construire une plate-forme fédérative des correspondances.

## Siegfried

En tant que chercheur, ce que je désir. Mais en tant que chercheur ayant des enfants, ne vaut mieux pas tout mettre à dispositif. Mais à un moment aura une masse critique avec des données qui permettront de faire des choses plus générales. Au début on est seul, et pour avoir de l’argent mieux vaut rester seul.

## Dan

Des intermédiaires. Différents cas, étudiants qui produisent métadonnées dans le cadre d’un travail de thèse. Avec emlo possible d’uploader les métadonnées sans les publier au moment où est prêt à les partager.

Mais expérience particulière, mieux vaut ne pas avoir été trop utilisé ou trop donné.

## Alexandre

Dépend sans doute des correspondances et des pays.

Le fait de produire des métadonnées, ou produire la recherche. Partie recherche pas séparée de cette partie là.

Question peut être différents selon les pays, et les moyens.

Question de la numérisation et de la recherche peut être des temps différents.

## Dan

Se pose aujourd’hui une question qui devra être résolue d’une manière ou d’une autre dans quelques années. Pas comme si le gros lot à décrocher en faisant le moissonnage des métadonnées.

## Irène

Comment mettre en commun. Pour ce faire doit définir des stds communs. Garder du temps pour la description des correspondances et données biographiques.

## Catherine

Me rappelle tous les colloques qui ont eu lieu dans les années 70, adoption système commun. Après recul, paraît dérisoire.

Si chacun traite correspondance de Euler, Diderot, c’est qu’ils ont écrit autre chose. Notamment que s’inscrivent dans un autre ensemble qui sont leurs œuvres. Si normalise, tout le reste. Vaudrait mieux avoir une cohérence entre la correspondance de Diderot et les 25 volume de son œuvre qu’avec celle d’Euler.

## Irène

Peut-on, ou est-il utile d’avoir des standards

Par exemple pour les références bibliographiques, clair qu’aimerait pouvoir avec des références à des ouvrages cités. Mais avoir raison gardée. Quelle édition citer. Prendre notice autorité de la BNF pas forcément la bonne solution.

Comment à la fois organiser les choses.

## ?

Technologies comme le XML permettent de s’affranchir d’une grande partie de ces problèmes.

Ensuite possible de passer d’un format à l’autre.

Si commence à faire un réseau

Distinguer modèle documentaire et format.

Profil d’application de XML-TEI

Définitions de bonnes pratiques

Dans un travail a défini les 15 éléments DC pour description de correspondance.

Pas été pris ANR.

Pas de Guideline pour l’édition de la correspondance, standardisée.

## Ingénieur documentaliste

Partage de l’information quelque chose qui se pratique maintenant largement. Sans doute quelque chose à ajouter sur le partage de la correspondance. Chacun a produit ses données dans son coin. Mais pour moi les standards existent. Déjà DC et OAI qui constituent des modèles minimum.

Avec VIAF travail international pour la création d’identifiants uniques pour des personnes à partir des notices d’autorité.

Sans doute un enjeu général pour produire des identifiants.

## Nombreux outils

Mais problème de visibilité. Parfois recherche qui vous oblige à modifier les données. Qui sera l’autorité pour modifier cette valeur ?

## Exemples de standardisation

Description des manuscrits

http://www.tei-c.org/release/doc/tei-p5-doc/fr/html/MS.html

Profil d’application pour les manuscrits

http://enrich.manuscriptorium.com/index.php?q=tei-p5

http://projects.oucs.ox.ac.uk/ENRICH/

Demarch, 2010

http://www.bnf.fr/fr/professionnels/normes\_catalogage/a.ead\_demarch.html

TEI SIG on Libraries, Kevin Hawkins, Michelle Dalmaud et Syd Bauman (éditeurs), Best Practices for TEI in Libraries, version 3.0, octobre 2011.

http://www.tei-c.org/SIG/Libraries/teiinlibraries/main-driver.html

Weboai

http://sourceforge.net/p/weboai/wiki/solution/

Whitman

http://www.whitmanarchive.org/mediawiki/index.php/Correspondence\_Encoding\_Guidelines

RDF

À la base avoir un UI
