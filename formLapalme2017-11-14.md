# Cr Lapalme 2017-11-14

## Graph of things

Alice Bamurange (Ruanda)

GoT intervient dans le contexte de l’internet des objets, implique une vision unifiée de tous ces objets interconnectés. Quantité de données énormes, suppose du big data.

Le graph des objets est un graph de connaissance, il peut être représenté par des données liées en RDF, il créée un flux de données unifiés, dont des données statiques.

Software stack

- Linked stream middleware
- parallel processing layer (distribue des charges de travail)
- back end data management system (gestion des données entrantes)

Exemple d’application rater un avion, manquer son bus, choix dîner au restaurant, pendant le dîner notification retard du vol suivant, cherche un concert.

Construire un graph pour implémenter un moteur de recherche qui trouvera des informations en temps réel.

Requêtes en SPARQL, possibilité de récupérer des données sur le moment et la région. Il est également possible de récupérer des données chronologiques.

Un graphe de connaissances en direct qui est basé sur des faits informés par les objets. Ce graphe utilise les avantages du web sémantique.

## Interopérabilité de l’internet des objets , a OSGI SIB

Smart-M3 Multi-plateforme, multi-vendor, multi-part. Développé par le projet SOFIA (Smart Object for Intelligent Application) fondé en 2008 par ARTEMIS. Plateforme abec une architecture publish-subscribe qui permet de fusionner approches du web sémantique et du web des objets.

Plusieurs knowledge processors qui communiquent avec le SIB où SPARQL endpoint.

IoT concept de pouvoir connecter n’importe quel appareil équipé d’un switch et d’une connexion objectif. Le web sémantique joue ici un rôle transversal car il permet de faire communiquer des appareils hétérogènes.

Problème de performance avec autres implémentations du SMART-M3, réglées avec PU (Persistent Update). Portage sur mobile.

OSGi SIB créé à l’université de Bologne en 2010, une architecture pour développer IoT. Modularité logicielle, fiabilité et portabilité et performance. Entités atomiques sous formes de Bundles, et définition d’appels de services.

Flexibilité et dynamité. Exécution de requêtes SPARQL.

---

# Méthodologie de construction d’ontologie

Étapes qui devraient d’une certaine manière être celles qui seront comprises dans votre rapport. Essayer de les suivre.

Cette méthodologique que retrouve dans le Semantic Web Primer, ou...

Il existe plusieurs manières de construire une ontologie.

AAA slogan, Anybody can say Anything about Any topic, d’où le besoin d’une certaine méthodologie.

Manuelle, ou réutilisation d’ontologies existantes, voir semi-automatique. Mais de manière générale construire de façon manuelle. Quelles sont alors les étapes à suivre ?

## Portée de l’ontologie

La première des choses consiste à déterminer la portée de l’ontologie. En toute logique l’ontologie n’est pas le but, elle sert à faire des choses, c’est un modèle ou une abstraction d’un certain domaine. Chacun, en fonction de ce qu’il veut faire va trouver une ontologie qui peut être raisonnable ou pas en fonction de la manière dont permettra de répondre aux questions.

Fonction de l’utilisation prévue, domaine, quels types de questions, mais aussi utilisateur et mainteneur. Cela vaut toujours la peine d’envisager les réutilisation ou importer.

- Préciser les questions auxquelles le modèle devra répondre.
- Prévoir l’intégration de nouvelles informations, du modèle dans le cadre plus général
- essayer d’imaginer comment se passera le processus d’inférence. Comme les ontologies de la classification d’instance, essayer de penser comment va procéder au classement des instances dans des classes.

## Énumérer les termes

Une fois la portée de l’ontologie déterminée, on va prendre les termes de notre domaine et en faire une liste.

énumération des termes du domaine

- noms: noms de classe
- verbes: noms des propriétés

Exemple des accords mets-vins

- noms: vins, établissement vinicole, rouge, blanc, poisson, viande rouge (des classes)
- relations entre ces choses : être situé à, avoir comme couleur, contenir comme sucre

Considérer les schémas de BD, vocabulaires ou thesaurus déjà présents dans l’entreprise.

## Définir la taxonomie

Placer les termes les uns par rapport aux autres

- top/down ou bottom/up (ou les deux)

S’assurer que c’est bien une hiérarchie

- si A est une sous-classe de B, alors toutes les instances de A sont des instances de B
- ex. *Pinot Noir* est une classe de *Vin Rouge*.

C’est définir et organiser les classes les unes par rapport aux autres.

## Définir les propriétés

Souvent fait en même temps que la définition des classes.

Une fois que les propriétés sont définies on va associer les propriétés à la plus haute classe à laquelle elle s’applique.

Ensuite définit les domaines et les portées. Cherchera à être le plus précis, parfois pas trop car n’aide pas à détecter les inconsistances. C’est ici qu’il y a l’art et la manière et toute la réflexion.

Il y a souvent des tensions entre généralité des domaines et portées et spécificité pour détecter les inconsistances.

## Définir les facettes

On va définir les facettes sur les popriétés

Cardinalités

Domaine, portée, type

Valeurs requises

Caractéristiques relationnelles

- symétrie, transitivité, inverse, fonctionnelle

Une fois que l’on a cela, on peut généralement vérifier la consistance de l’ontologie. Si par exemple a défini des classes pour lesquelles ne pourrait pas avoir d’instance (alors suspect car voudrait dire que définitions contradictoires).

## Définir les instances

Le but d’une ontologie est d’organiser des instances.

Le nombre d’instances est beaucoup plus grand que le nombre de classes.

Souvent créées automatiquement à partir d’une base de données ou bien extraites d’un corpus.

Vérification d’anomalies.

## Modélisation pour la réutilisation

Lorsque l’on fait une ontologie, il faut aussi tenir compte du fait qu’elle va servir de documentation pour les humains. Comme un programme pas seulement écrit pour un compilateur.

Il convient donc de trouver des noms évocateurs pour les classes (noms) souvent des verbes pour les propriétés.

Ajouter des rdfs:label et rdfs:comment, rdfs:seeAlso pour les propriétés.

Conventions habituelles (ex. celle W3C)

- ressources en CamelCase
- nom d’une classe au singulier et débute par une majuscule
- nom d’une propriété qui débute par une minuscule

## Garder la trace des classes et des individus

Quand on fait des classes, parmi les choix que l’on fait, tenir compte du fait que les instances des uns sont les classes des autres

- espèces d’animaux vs les animaux
- lignes d’affaires vs les entreprises

Une classe devrait pouvoir avoir des instances

Les valeurs précises des propriétés devraient s’appliquer aux instances.

## Tester la modélisation

Une fois que toutes ces opérations ont été réalisées, il convient de tester la modélisation. Peut-on répondre aux questions identifiées au début ?

Comment se comporte l’ontologie en présence de sources multiples ?

Quelles inférences peut-on en tirer ?

## Réutilisation d’ontologies

Codification par des experts

- Cancer Ontology du National Cancer Institute
- AAT
- Thesaurus of Geographic Names

Vocabulaires intégrés

- Unified Medical Language System (750 000 concepts, 10M de liens)

Upper level ontologies (gros bon sens...)

- Cyc 
- Standard Upperlevel Ontology

Tout cela pouvait faire partie des réutilisations d’ontologie. On peut également utiliser des hiérarchies de sujets comme Open directory project, des ressources linguistiques WordNet.

Mais aussi quelques librairies d’ontologies

- DAML (DARPA Agent Markup Language) ancêtre de OWL
- Protégé
- Swoogle

Peut-être sources à aller voir pour s’en inspirer.

## Problème d’acquisition de connaissances

La création manuelle d’ontologie est longue, coûteuse, très spécialisée et parfois fastidieuse.

Méthodes d’apprentissages pour 

- acquisition et extraction des connaissances
- maintenance et révision des connaissances

mais difficile car peut de données d’apprentissages.

Tâches envisageables par apprentissage :

- extraction d’ontologies (mais nécessite une révision manuelle car une ontologie finalement une réflexion sur un domaine, risque d’avoir des classes qui ne disent rien)
- plus intéressant en revanche pour faire de l’extraction de données et de métadonnées
- fusion et mise en correspondance (prendre deux ontologies et essayer de les aligner, parfois difficile)
- maintenance d’ontologie par analyse des instances
- observation des usagers

Techniques d’apprentissage

- clustering
- mise à jour incrémentale d’ontologie
- support pour l’ingénieur des connaissances
- amélioration d’ontologie pour la langue naturelle
- apprentissage d’ontologie (mais comme une vision du monde que l’on donne, celle de la machine peut-être pas celle qui nous aide le mieux à comprendre un domaine, cependant peut nous aider à faire des tests)

## Conclusion

La création d’ontologie reste un art, pas encore de recette miracle.

Exemples de création

- ontology development 101: A Guide to Creating Your First Ontology
- Développement d’une ontologie 101

un vieux classique qui date des années 80, reprend grosso modo les étapes ici définies.