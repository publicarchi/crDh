Sem DH EHESS, 2014-02-05, Kinsource
============

Introduction
------------

[Kinsource]() une plateforme collaborative de partage de sources sur la parenté.
Repose sur plusieurs principes
- libre accès
- pérennisation
- partage des données dans des contextes différents
- contrôle de qualité scientique et documentaire
- mise à disposition d'outils d'analyse

Un séminaire méthodologique sur les Humanités numériques.
Trois types de séances :
- des séances de lectures
- des séances internationales
- des séances projets ou dispositif dans lesquelles invite les porteurs de projet à présenter leurs activités en mettant en avant l'articulation entre les logiques scientifiques et les logiques techniques et en particulier celles propres aux technologies numériques. C'est la raison pour laquelle invite généralement plusieurs personnes participant à une équipe projet car permet de disposer d'une polyphonie intéressante avec différents points de vue sur le projet. Ex. ediaspora et développement d'un outil par l'ingénieur qui a eu beaucoup de succès.

Pascal Cristofoli ingénieur EHESS, analyse de source
Olivier Kyburz, Université Paris-Ouest Nanterre, anthropologue. Spécialiste des peuls, depuis s'est spécialisés sur les outils informatiques pour documenter la parentalité.

Question de la relation de ce type d'outils avec la publication.
Réunion à laquelle avait participé, à la fin des années 90, Mickael Haussmann ??, et Doug Right ?? avait animé un atelier sur les réseaux de parenté. Une réunion tout à fait nouvelle dans le paysage intellectuel universitaire. Certains familiers de l'univers informatiques, mais peu.

De ce projet est né le projet TIMP qui concernait le traitement informatique des matériaux ethnographiques. S'y sont soudées quelques amitiés, TIPP traitement informatique des phénomènes de parenté. Ici que développement de l'embryon de Puck, le logiciel de traitement qu'utilisons encore. À partir de ce travail avons développé le projet de simulation de parenté. Enfin, comme aboutissement de cette cascade de projet est né le projet Kinsource.

Une poignée de chercheurs et d'ingénieurs ont participé à ce travail. En termes d'institutions, passe d'une institution à l'autre. INED, Nanterre, EPHE, compte-tenu de la lourdeur du portage.

Pascal C : TIMP c. 2005-2004. Fin 90s au sein du laboratoire d'ethnographie historique auquel appartient un axe de travail sur les réseaux sociaux. Dans les années 70, histoire de la démographie et des population = démographie historique. Dans les années 80, changement de paradigme du laboratoire vers la microhistoire et l'analyse des réseaux sociaux. Travaux de Maurice G??

À partir de cette expérience, ont également été amené à rencontrer Doug Right ?? secrétaire de l'International Social Network Analysis depuis des années. Dernière rencontre Kintipp rencontre sociologues et ethnologues sur des questions de parenté.

Doug Right ??
Un mathématicien élève de Harari ?? mathématicien spécialiste des réseaux. Déjà travaillé avec un anthropologue.
Doug Right son élève, une formation mathématicienne, mais intérêt pour les données sociologiques. A travaillé en Turquie. Collaboré avec Mickael Haussmann ??. Le pape de l'analyse de réseau en sociologie.

Présentation
------------

### Le projet

Un projet d'ANR corpus, édition 2012. Consiste en la mise à disposition de données pour la recherche.

[Groupe Kintip](http://www.kintip.net) qui a d'abord développé le logiciel Puck
Première version décidée par Mickaël Fischer.

Collaboration de quatre laboratoires de recherche
- labo ethno et socio compa NAnterre
- labo d'anthro sociale coll. fr
- labo démo d'histoire sociale EHESS
- centre Roland Mounier

Donc deux laboratoires d'histoire et deux laboratoires d'anthropologie sociale présents dans le projet. Le regard disciplinaire permet de croiser les questionnements, généraliser les choses et conséquences sur le développement.

Prestataires Clevinsy pour développements. Designers.
HumaNum.

Page web du groupe Kintip depuis 2005, page du logiciel Puck.

De 2009 à 2012 une ANR sciences complexes, sur la simulation de parenté, SIMPA. Avec l'INED etc.


### Le logiciel Puck

Un outil pour l'utilisation et l'analyse des données de parentées. Un outil créé en 2007, dans sa première version par plusieurs contributeurs. 
Program for the Use and Computation of Kinship data.

Un logiciel libre et open source.
Se base sur des informations relationnelles, une liste d'individus dans laquelle va coder des informations de relations sur lesquelles pourra faire des requêtes. Comme dans les logiciels de généalogie, va traiter les relations et les alliances, en étant plus ouvert à d'autres question. Par exemple pour prendre en charge l'analyse de corpus.

Le logiciel permet de gérer les individus, leurs filiations, mariages, etc. Un module de saisie aujourd'hui disponible dans le logiciel. Problème de ces logiciels d'abord conçus pour leurs capacités techniques d'analyse plutôt que d'usage. Un des avantages du logiciel est de permettre à la saisie d'individus et de famille simultanéement.

Un individu correspond à une ligne.
Peut disposer d'informations sur les couples, les mariages. Modèle qui a changé sur ce point, les anthropologues pas nécessairement besoin d'informations sur la date de l'union, alors qu'une question plus fréquente pour les historiens.

Au départ partis sur une modélisation dans des graphs où possible de donner des attributs aux personnes mais pas aux relations. Pour pouvoir qualifier ces unions, est passé à une modélisation différente, composée de graphes double où deux individus pointent vers un objet union. Chacune des relations pouvant être typée. Un objet plus complexe, posant plus de difficultés pour les algorythmes de parcours, car doit permettre le traitement de vastes réseaux de personnes. (jusqu'à 30 ou 40 000 individus)

Modèle qui s'est également enrichi pour prendre en compte d'autres types de relations sociales autres que les relations comme l'union. Par exemple des relations de parainage, de parenté spirituelle, de témoins, de transactions (type notariales), etc. Le fait d'avoir introduit la relation comme un objet, donc qualifiable qui permet aujourd'hui de mettre en place ce traitement. Possibilité d'introduire des éléments de type prosopographique. Un outil qui permet non seulement de gérer ces données, de les analyser, mais également de les archiver.

#### Étudier les réseaux de parenté avec Puck

Logiciel qui permet de faire des recherche de cycles dans un graph. Il est possible de chercher dans le groupe familial, mais aussi dans les groupes alliés.

Il est donc possible de réduire la recherche de cycle à des relations de co-sanguinité. Ou l'élargir à des afins, avec des niveaux de profondeurs plus ou moins importants.
Cf. schémas intéressants

Logiciel qui dans le cadre de l'horizon que lui a fixé, explore tous les cycles présents, et les identifie en donnant un chemin.

Un des aspect du projet consiste également à traiter les terminologies de parenté asosciés dans les diverses sociétés.

Pour un historien, peut expérimenter toute la relation de parenté, vis à vis de la relation de parainage.

Plusieurs notations possibles, une notation qui identifie le sexe des personnes impliquées dans le cycle. De plus en plus utilisée. Une notation std pour les anthropologue par lettres, sinon sous forme graphique.

Dans la notation graphique : triangle les individus hommes, rond individus femmes.
Relations verticales parenté (hiérarchie haut/bas). Arcs la propriété de la relation.

#### Étudier la population et ses relations

Se servir de la parenté comme structure de fonds. Idée d'exploiter des corpus. De cette idée qu'est née l'idée d'archivage.


### Archiver et publier des données scientifiques

Nombreux corpus.
Dans l'ANR Kinsources, idée de rendre publics ces corpus sous forme numérique et de les rendre accessibles pour les traitements et l'exploitation.

Alors besoin de données ouvertes, et d'outils libres pour les traiter.
Outils du Max Plank pour travailler sur les données généalogiques que voudrait pouvoir rendre interopérable dans le cadre du projet. [de 430 passés à 330 000 euros].

Publication de "données ouvertes", assurer leur pérennité, promouvoir leur réutilisation, etc.

Archiver les données scientifiques.
Des données numériques, il s'agit de corpus codés, pas de docuemnts.
Des données de la recherche (Anthropologie, histoire, Ethnologie, démographie).
Des données généralogiques au sens large.

Mémoire généalogique variée selon les cultures. Des corpus biaisés à certains égards. Intérêt limité mais titre documentaire, aspects pédagogiques de l'archivage.


#### Une fonction patrimoniale
Nombreux corpus réalisés sur fonds publics. Nombreux corpus en perdition. Départ des auteurs, absence de conservation, problèmes des outils et des formats. Pas de problématique générale de sauvegarde des données de la recherche.

Nombreux corpus codés perdus. Par exemple, les 18 générations de... par Segalen : données perdues par ex.
INED une politique stricte d'archivage des données.
Versement pas systématique aux archives, dépend souvent de la bonne volonté des chercheurs.

De fait, dégradation des corpus historiques, partie liée à des changement de perspectives méthodologiques lors du désamour à l'égard des approches quantitatives.

Diffusion auprès de la communauté scientifque en apparaissant comme une solution viable et simple pour des projets de recherche afin de pérenniser les corpus.
Devenir un acteur identifié par la communauté pour la diffusion des données de la recherche.

#### Une fonction scientifique

Reproductibilité des analyses, approfondissement
Comparaison des coprus.
OUverture vers d'autres analyses, autres champs de recherche, ouverture à d'autres problématiques comme analyse spaciale des terminologies de parenté, etc.)
Point de départ pour des recherches.
Interroger la parenté à partir d'autres données.
Jouer sur la cumulativité.

#### Création de dispositifs techniques au service de la publication

Pour sauvegarder les corpus, etc.
Dispositif pérenne, sécurisé, permettant le dépot indivisuel.
Lieu pour publier des corpus, validation collective, référence unique pour un corpus.
Versionning, licences, gestion de l'anonymat, barrières mobiles.

Volonté de ne pas trop dissocier la sauvegarde de la publication. Difficile car volonté de se réserver les données. Se réserver la publication.

Un travail en surcroît pour publier ses données. Or ce travail n'est pas valorisé en lui-même. Un travail ingrat.
Donner à la publication de corpus le statut de publication à part entière.
Comment ?
- édition de sources ou description d'enquête
- validation scientifique
- identification du corpus et de ses "auteurs"
- statut de "publication électronique" d'un corpus ?
- valorisation de la publication vis-à-vis des institutions
- problème des enquêtes collectives

Si voulait comparer avec l'édition critique. Question de la reconnaissance des collations. Précieux, compliqué à publier. Pourrait donner lieu à valorisation, mais pas publié avant la publication.


### Susciter adhésion : une plateforme collaborative reposant sur les contributeurs

Un des enjeux notables du projet. Si personne n'est opposé a priori, en pratique plus compliqué.

Plusieurs stratégies mises en œuvre pour augmenter les dépôts.
Incitation au dépôt individuel.
Atteindre une masse critique par l'exeemple (qualité des corpus archivé, célébrité, diversité, utilité et apporte des outils associés).
Susciter de nouvelles contributions (recencement, sauvegarde, initiatives de codages)

Jouer sur l'effet boule de neige. L'idée étant de pouvoir récupérer le maximum de corpus déjà codés de manière automatique.

Stratégies de corpus pour chaque labos. Clusters régionnaux thématiques.
Distinguer les collections.


### La plateforme kinsources.net

Depuis fin novembre, une première version.
Plateforme développée dans le cadre de l'ANR par l'intermédiaire d'un prestatiare infromatique. C. Momon (Devinsy) et A. Martial pour le design.

Dégagement de temps de développement d'un des partenaires pour visualisation.

Formulaire de dépôt.
Première analyse au moyen d'une batterie de tests pour vérifier la cohérence interne du corpus.
Validation (bien formé)

Un comité scientifique pour la plateforme.
Composé d'experts internationaux : valider la publication des coprus de données en vérifiant notamment si les corpus soumis pour publication sont cohérents, s'ils satisfont aux critères de la recherche scientifique (documentation suffisante) et s'ils respectent les lois en vigueur concernant la protection de la vie privée.

...
Michael Fischer
Klaus Hamberger
Michael Houseman
Olivier Kyburg
Dwight Read
Douglas R. White

Ne se prononce pas sur le bien fondé de l'existence.
De ce point de vue comprend que ne peut avoir la même valeur qu'une publication dans une revue avec un comité de lecture.

Peut envisager la mise en place d'une validation plus forte. Plus cette validation est forte, plus s'approche d'une publication et l'incitation à publier serait forte pour les chercheurs.


### Développement

Par une société spécialisée en logiciel libre, Devinsy
Associations outils techniques métiers.
GNU/Linux, Eclipse, LibreOffice, Gimp.
CeCILL

V.1
52 000 lignes de codes, 279 classes Java

Fonctionnalités
- soumission de corpus
- téléversement
- procédures de validation des soumission
- export des données
- gestion utilisateurs
- collection de corpus
- recherche multi-critères
- navigation dans les corpus
- fil d'actu
- aide
- design et aspect général/multilinguisme

Contraintes techniques à intégrer
- interop (Puck et KinOath, + OAI-PMH)
- validité
- sécurité (car parfois données sensibles)
- ouverture du code

Métadonnées des corpus
Auteur, codeur,  contact, description, bibl, citation, note sur la collection, localisation, groupe ethnique ou culturel, coordonnées géo, histoire, condition d'utilisation et licence, autres répertoires.

Formats
- Une table : id, nom, sexe, info qualifiant l'individu de manière unique
- seconde table : n° famille, marié/pas marié, père, mère, nb enfants.
- relations : baptèmes, parain, maraine, etc.

Peut saisir sous forme de fichier texte, ou fichier excel à plusieurs feuilles.
De même autre format.
Lit GEDCOM format généalogique mis au point par les Mormons.

À terme un des enjeux de conservation consistera à coder les données dans un format XML où l'on stockerait à la fois la structure des données et les données elles-mêmes.

Développeur souhaitait utiliser le locigiel Terra Cota, beaucoup utilisé dans les projets de big data. Un projet libre et ouvert, mais racheté depuis juin.

Fiche de présentation des corpus
Statistiques sur le corpus, identifiants, etc.
Accès rapides aux corpus par pertinence.

Une des fonctionnalités principales de la plateforme pas d'explorer un corpus, mais de pouvoir exploiter les similarités. Un des critères de réussite du projet, que soit suffisamment attractif pour que la plateforme soit nourrie.

Dans les logiciels de généalogie grand public, des fonctionnalités de fusion d'arbre. Pour le moment rien n'est développé dans ce sens au sein du projet.

#### Questions en suspens

Publication d'un corpus = publication ?
Question des auteurs / codeurs / contributeurs
Question des droits
Partager "ses" données ?
Différence dépôt / publication
Données scientifiques ?
Comment motiver les dépôts ?


Discussion
-------

À Marseille un projet de Laurent Doucet pour archiver des données de terrain notamment sur l'Océanie.
Des projets de documentalistes sur les données des anthropologues et des ethnologues. Le cas aux archives de la MAE. Idem au LAS Laboratoire d'Anthropologie Sociale.

Question sur l'archivage pérenne.
Projet labellisé par Adonis pour hébergement sans garantie de pérennité. Depuis reprise du dossier.
Pas travail péalable sur un format. Héritage du projet lié à la constitutions historiques d'un stock de données. Le travail de formalisation s'est fait au niveau de la représentation des relations. Dès lors la question du format est d'abord apparue secondaire.
Relations suffisamment simples pour ne pas poser de difficultés particulières pour le format.
Mais il y aurait certainnement intérêt à pouvoir disposer d'un format qui permette l'analyse avec Gephi ou systèmes d'analyses de réseaux.




Rmq perso
-------

Surprenant qu'ils n'aient pas d'abord travaillé sur un format pour construire une application autour de ce format.
Il semble que l'application web repose sur un stockage de clefs-valeurs (intérêt en termes de performances). Dès lors que le format de pérennisation doit être XML, il faudra produire spécifiquement un export.



