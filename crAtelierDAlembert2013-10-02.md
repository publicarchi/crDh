CR Atelier D'Alembert et les Digital Humanities, 2013-10-02
=============

[Atelier « D'Alembert à l’heure du numérique » : Projets en cours, collaborations et perspectives](http://www.transfers.ens.fr/index.php/activites/recherches/programmes/284-atelier-dalembert-et-les-digital-humanities)
Observatoire de Paris, Salle du Conseil - Mercredi 2 octobre 2013, 10h15-17h


Introduction par Irène Passeron, responsable de l’édition des Œuvres complètes de D’Alembert
-------------


Oxford (Bode library)
-------------

Projet fondé en 2009
Achèvement prévu en 2014

S'affronter au matériau particulier que constitue la correspondance
Par leur nature, internationale, savantes, ressources dont mesure mal les ressources
Souvent mal repérées et sioui rarement avec un niveau de granularité adapté pour les repérer de manière adéquate

Première étape du travail qui a donc constitué à produire un catalogue. 

Early Modern letters Online
Catalogue en ligne. Preuve de concept de la première phase du projet. Production de métadonnées basiques sur la majorité de la correspondance que voulait traiter.
4000 lettres concernées

The digital assets management system (DAMS)
Technique le domaine de notre partenaire, pour ma part seulement éditeur.
Scalability, sustainability
Établissement de données d'autorité biologiques, géographiques

### Emlocollect

Publication des documents libres à télécharger
Basées sur open office
Utilisation d'un CMS, Emlocollect, créé spécialement pour le projet pour l'édition des lettres dans le backend. C'est ce système qui propulse les pages dans le front office.

Facilité d'édition avec open office avec menus déroulants, etc. Alors information prête à être uploadée dans l'application.

Communauté d'éditeur distribuée. Métadonnées peuvent être amendées sur une base individuelle et éventuellement intégrée dans l'ensemble du catalogue. Réelle joie à utiliser le système. Code source librement disponible depuis github.

### Quantités

60 893 lettres
66xxx versions
9039 images
13282 personnes
568 organisations
3845 lieux
138 dépôts
21239 ressources en rapport

Voudrait aujourd'hui permettre enrichissement avec autres ressources
Par ailleurs volonté de développer les visualisations. Deux post-doctorants sur le sujet.

Pense qu'en 2014 disposeront d'une collection relativement significative de cette galerie de superstars scientifiques
Scholarly crowdsourcing des métadonnées
Deux post docs dont le Focus portera sur les DH

### Évolutions futures

Révision du modèle de données
Celui-ci crée en 2009
Aujourd'hui traiter des relations, le penser comme sensible aux dynamiques temporelles, beaucoup plus granulaire et adapté pour prendre en compte la république des lettres.
Date de naissance, mariage, etc.
Données biographiques et prosopographiques
Évolution du modèle pour prendre en compte correspondance

Par ailleurs travaille sur la visualisation pour offrir de nouvelles manières de naviguer dans le catalogue. Sera implémenté avec des outils open source comme Gephi, etc. 

Ajouter nombreux graphs qui viendront compléter les nombreux histogrammes déjà proposes pour présenter des distributions temporelles

Prochain travail sur la géo localisation
Les lettres un travail intellectuel géographiquement situé. Traiter des évolutions dans le temps de ce réseau

Générer automatiquement ce réseau sur la base de la fréquence des relations.

### Conclusion

Espère que disponibilité des outils n'ajoutera pas seulement nouvelle valeur mais engagera partage de nouveaux ensembles de métadonnées

### RMQ Perso

N'a cité aucun modèle documentaire
Pose beaucoup de questions sur l’interopérabilité


« Présentation d’une interface ORIGAMI pour l’édition de la correspondance de D’Alembert », Marie-Laure Massot et Irène Passeron
------------------

Comment articuler données développées comme celles-ci avec autres collections développées spécialement dans le cadre de corpus

Groupe d'alembert un groupe pluridisciplinaire  travaillant collaborativement sur la correspondance de d'Alembert
Plusieurs séries dans les œuvres complètes, cf site du projet.

Pour la série 2 décide d'éditer partie critique d'une autre manière
Développement d'outils pour édition correspondance et des lettres


### Origami (alexandre)

Ses différentes interfaces et application à différents corpus

Début du travail en 2007
Sur corpus des éloges d'Alembert dont plupart des manuscrits conserves à l'Institut.

Problèmes rencontres pour l'édition de ces éloges académiques
Souvent dispose de plusieurs versions manuscrites
Qui dit œuvre complet dit édition ensemble de ces versions.
Si reste dans l.imprime alors choisir texte de base auquel rapporter les versions

Mais études des versions révèlent des choses sur la constitution du projet philosophique, stratégie, etc. Cf. Olivier ??

Développer projet éditorial qui permette de mettre à l'épreuve cette hypothèse et si possible de visualiser à l'écran ces variantes

Exemple éloge de Bossuet
Deux versions manuscrites avec corrections manuscrites de d'Alembert qui donne lieu à version du copiste elle même corrigé sans doute d.autres manuscrits avant l'imprimé.

Version matérielle
Notion d'état zéro sans biffures, etc. Elle qui permet visualiser les ajouts déplacements et biffures
Rendre compte partiellement de la stratification des corrections avec limites concernant la possibilité de stratifier chronologiquement ces corrections. À donc restreint l'analyse au paragraphe ou au folio

Sélection ms état zéro
Toute transcription étant par nature imparfaite, devenu standard de mettre en regard le manuscrit avec sa transcription. 

Visualisation du processus de genèse du texte.
Visualisation d'une biffure simple, ou remplacement. Passé par un état intermédiaire niveau 1,5

Des calques de couleurs permettant de mettre en regard le texte de la version 1 avec l'état 2 et de mettre en évidence un processus d'écriture en marqueterie.

Un module programmé en java permettant de transformer automatiquement n'importe quel fichiers de transcription en base de données afin de visualiser les différents états. Interface exploitant certain nombre d'images relatives aux manuscrits.

Utilisation d'un format d'encodage maison, mais pas standard en vigueur : XML-TEI
Ceci dit conservé pour le moment ce système car très logique et proche des processus d'édition et permet de fair travailler n'importe quel chercheur sur le projet

Prévoit moulinette pour transformation en XML-TEI. En attendant de disposer d'une interface graphique d'édition collaborative pour cela.

Par ailleurs travaillent sur l'édition des archives de Claude Simon avec l'école des chartes

Vincent Baridon, Alexandre Guilbaud , ...
Irène passeron

### interface

Corpus important 2200 lettres
Plus de 429 correspondants pour lesquels au moins une lettre
Une grande variété de sources donc un corpus difficile

déjà un inventaire qui était un outil intéressant
Mise en place de nombreux outils pour exploiter la base de données de l'inventaire.
Également mise en place d'un moteur de recherche.

À voulu faire des éditions séparées soit pour valoriser un fonds patrimonial ou un travail de recherche. Trouver des solutions à des problèmes éditoriaux : sources contradictoires, rendre lisible des notes d'édition trop longues, ou la genèse des textes.
Bref voulait mettre en place une édition numérique qui exploite le potentiel et renouvelle l'édition en la valorisant

L'interface origami est une interface d'édition collaborative de lettre en cours de développement. 

Plus de 130 institutions qui conservent des ms
Réfléchissent donc à des manières de lettre en valeur les institutions et présenter les courriers par bouquet sur la page d'accueil
Arborescence pour montrer que deux versions disponibles de la lettre, choix de la version.
Accède à une transcription du manuscrit. Bandeau gauche fournit information tirées de la base de données de l'inventaire incipit, daté etc.
À droite formulaire qui renvoie au site et sa base pour accéder à d.autres lettres

Pour le moment possibilité de voir transcriptions en regard de la lettre. Présentation de la lettre comme un chapeau. Description matérielle de la lettre. Un outil pour citer la lettre dans l'outil.
Enfin possibilité de visualiser les corrections au moyen d'un code couleur.

Possibilité de voir les cachets, possibilité pas disponible avec une édition papier.

### Origami dans le cadre

Voudrait rendre les lettres intelligibles pour le lecteur
Qu'ils puissent disposer d'un fil directeur. Ici à faire à une multitude de fonds d'archives. Intérêt de pouvoir présenter l'ensemble, mais ici concentré sur le fonds de l'académie. Fonds important car l'académie importante dans la carrière de d'Alembert mais important pour le chercheur de s'interroger sur la présence dans les fonds et significations

Affaire Toloma
Importante car met en jeu à la fois son identité et...
S'interroger sur ce que donnons a lire au lecteur.
« Affaire » qui met en jeu de ara des entités, personnages mais aussi nombreux personnages sur lesquels information biographie faible.

Comment rendre ensemble compréhensible
Pour cela double approche, à la fois chronologique et matérielle de façon que chercheur toujours accès au document mais aussi aux sources utilisées par les chercheurs.

Politique éditoriale qui a pour objet par le moyen d'un onglet de permettre au lecteur de revenir aux principes de cette édition car bien conscience que des principes subjectifs et cette caractéristique que veut rendre explicite au lecteur.
Principes de transcription, etc.

Spécificité de l'édition numérique, accès direct à la note, etc. Pour le reste une édition classique.
Une affaire, une querelle polémique comme il y en a au 18e siècle, controverse. Toloma un jésuite, et comprend tout de suite l'enjeu pour d'Alembert. Rendre compte à la fois de l'historiographie mais aussi de manière plus objective l'affaire.

30 nov 1764 bib collège trinité à Lyon. Discours rentrée contre l.article collège paru en 1753 rédige par d'Alembert
Une affaire à partir de laquelle peut visualiser l'apparition d'un réseau.
Choix d'une chronologie présentée en regard des textes verticalement. Débuté par la parution de l'article collège de l'encyclopédie auquel donné accès directement par sa transcription avec l'image de la page de l'encyclopédie et diverses informations. Peut suivre transcription en regard. Commencé à voir partie  de d'Alembert après le G de... Pas une évidence.

Revient à chronologie permettant de suivre de mois en mois l'affaire.
Chronologie flexible à dimension variable en fonctions des documents entres.
Passé à la sortie du 4ème volume de l'encyclopédie en 1764 qui réactive certainement vindicte jésuite à l'égard de l'Encyclopédie et l'intervention à Lyon du père Toloma. Intervient dans le cadre opposition académie locale.

Ne dispose malheureusement pas du discours. Seulement le placard de publicité. Pourquoi ce document conservé, en fait dans les papiers de Malesherbes.
Onglet histoire pour bien distinguer ce qui est de l'ordre de l'interprétation, de l'historiographie, de ce qui est de l'ordre du document, du matériel.

2 décembre 1764 (les nouvelles vont vite dans la république des lettres) Bourgelat des décembre écrit lettre à Malesherbe. Onglet historique car permet de savoir que conservé dans fonds Malesherbes et diverses informations publiques.
Deux derniers paragraphes concernant la querelle des académies lyonnaise.
Qualifie les choses d'« incartade« « vomit pendant deux heures un très mauvais latin » etc. Confierez-vous vos enfants à quelqu'un ni père ni patrimoine. S'attaquer à l'académie dont d'Alembert venait d'être nommé membre deux jours au paravant.

Discours à l'académie française de d'Alembert
Janvier 1755 ou manifestement ne se passe pas grand chose dans les registres de l'académie de Lyon. Cependant trouve lettre de Boiffon ? faisant oart art de ses inquiétudes pour la reconnaissance Académie.  Et que d'Alembert se serait plaint du discours.

Zoom sur la lettre facsimile
Matérialisation du changement de folio en couleur dans le texte (niveau de gris)

Au lois de février voit au travers ces documents que c'est l'effervescence et comment se manifeste dans la société. Lettre de Boiffon, puis d'émissions de 5 membres. Une séance houleuse de la société royale de Lyon, ou intéressant de comparer le journal et le « verbal » du secrétaire qui fait apparaître des choses pas transcrites au registre.

Accès à la liste des documents
Possibilité de revenir à la chronologie
Au mois de mars, directeur de la société royale de Lyon, Soufflot, monté à Paris, se contente de dire qu'au courant de rien. Secrétaire de plus en plus inquiet

D'Alembert écrit une nouvelle lettre à Bourgelat (conservée en copie à l'Académie) or manifestement très énervé à ce moment là si en juge par l'écriture. Non édita le car 4 niveaux de correction.
Ici édita le avec Origami.

### Conclusion Marie-Laure

Perspectives d'évolution pour l'outil
Insérer possibilités de sélections par lettres liées par thèmes, parcours, personnes
Insérer une chronologie de d'Alembert
Voudrait faire des liens avec des notices biographiques fiables établies par ailleurs dans le projet.

À terme une base unique de données qui devrait être exploitable avec des liens entre origami et ancre.

Aimerait aussi pouvoir faire des liens avec projet républiques des lettres
Voudrait également visualiser dans Pairs

Enfin, possibilité de personnaliser l.inetrface. Permettre d.annoter car édition le fait de nombreux éditeurs. Possibilités collaboratives deja disponibles dans ancre.

Aimerait plus généralement à partir des outils du groupe d'Alembert renouveler les méthodes d'édition et de travail.

Disponible sur site. Qqus mois nécessaires encore de dev.
Migration vers les serveurs IN2P3


Projet édition numérique critique et coll de l'Encyclo
-------------

Des membres de l'équipe édition d'Alembert
Mais dépasse largement

Faire quelque chose qui n'existe pas c'est à dire une édition critique.
Souligner qu.il existe déjà des éditions électroniques de l'encyclopédie. Donc commencer par un État de l'art

### État de l'art

Édition Redondant
Édition Morisset ATFM Chicago
Alembert.fr plus récente
Et ouverture interface Wikisource consacrée à l'édition d'Alembert

Pas possible, en format papier compte tenu de l'ouvrage et des niveaux de relations qui se déploient à son sujet.
Redon sans doute l'édition la plus complète.
Très utile de développer des outils en ligne.

Plusieurs critères de qualité :
— Qualité de la transcription
— Accès à la matérialité de l'ouvrage
— Rendre compte des liens internes
— Respect ortho, des désignants (chaîne de mots donnant une indication du propos auquel l'article se rapprote)
— Avec quelle finesse les éléments caractéristiques de l'édition son décrits

ARTFL proprès considérables dans la transcription mais reste des problèmes. Beaucoup de lacunes pour l'édition des formules mathématiques et des tableaux.
En revanche Wikisource, une interface collaborative abouti à une très bonne transcription et licence libre.

Respect intégrité ouvrage : seuls Wikisource et ARTFL
Respect des liens, beaucoup de lacunes, possibilités de navigations restreintes et problématiques pour rendre compte de la manière dont les éditeurs ont conçu la consultation à l'époque.

Pour moteurs de recherche, ARTFL qui s.appuie sur philologie 4 un moteur très puissant. Et Wikisource bof.

Façon dont les éléments sont spécifies
Sur ARTFL, nombreux noms
Les désignants
Les noms du ou des auteurs de chaque article
Début du code qui fait apparaître des métadonnées mais qui s'appliquent à l'ensemble de l'article, c'est à dire que les éléments de l'article ne sont pas spécifiés.

Renvois établis à partir du plein texte directement. Le lecteur s'y perd donc.

Ici que voulu penser quelque chose qui nous permette d'articuler une édition avec la recherche.

### « Présentation du projet ENCCRE : édition numérique collaborative et critique de l’Encyclopédie de Diderot et D’Alembert (1751-1772) », Vincent Barrellon (LIRIS), Olivier Ferret 

Édition critique collaborative et de recherche de l'encyclopédie

Créer les conditions d'une édition numérique qui s'appuient fortement sur les recherches effectuées par l'encyclopédie et exploite au mieux les possibilités offertes aujourd'hui

Une œuvre immense et hétérogène qui a suscité de très nombreuses recherches. Nombreux laboratoires, et revue

La politique éditoriale
Une édition complète et en libre accès
Licence libre
Édition critique très articulée avec la recherche
Veut une édition qui implique une distinction très claire entre ce qui relève de l'édition critique et de l'œuvre
Essayer de présenter une édition critique pas seulement pour les chercheurs mais pour le grand public sans trahir les recherches récentes.

Édition qui va s'appuyer sur une interface d’édition collaborative. Développement prévu pour trois ans.

Équipe de chercheurs charges édition, transcription, enrichissements. Fait par interface collaborative d’édition avec contrainte être bien pensée de manière à ce que n'importe quel chercheur puisse y travailler.
Produire des données textuelles et des données critique
Le tout accessible par une interface de lecture et de recherche dans l'encyclopédie.

Volonté de permettre la création de comptes utilisateurs pour porter des annotations sur l'édition pour leur travail de recherchée t'oublier leurs apports sur l'interface.

#### Réflexion qui a d'abord reposé sur la structuration des données.

Identification de la structure préalable de l'encyclopédie
Quels éléments à décrire et comment organises entre eux

Deux structures identifiées une structure macroscopique et structure microscopique relative au canon de l'ouvrage, notice, planches.

Identifie adresse, un désignant, une indication lexicale, une mention de Chambers, un ensemble de renvoi et pour finir une signature. Le texte n'est pas spécifié (texte par défaut)

Ensemble des éléments reconnus dans l'article ont un lien avec l'adresse
Renvois vers deux éléments

Des cas plus complexes
Notamment pour la question des renvois
Ex jet d'eau cosigné par deux personnes.
Renvoi en italique «consulter ces articles à leur lettre»
Comment traiter de tels renvois , va définir deux nouvelles catégories : une indication de renvoi non explicite qui permettra de lier ces catégories à des renvois explicites.
Possibilité ainsi de restituer le mode de circulation original de l'ouvrage

#### structure pour l'édition critique

Établir la structure pour établir le lien entre cette édition critique et les données encyclopédiques.

Exemple double signature dans l'article. Comment rendre explicite cette information au lecteur. Comment rechercher de l'ensemble des contributions de d'Alembert, ou dans l'ensemble de l'encyclopédie. Nombreuses choses à valoriser, pour se faire ne peut se contenter de spécifier les choses de manière externe.

Pour cela choisir d'établir un lien entre entité externe et interne. Identifie signature collaborateur, lien avec passage concerné, puis avec le collaborateur proprement dit

Une classe le résultat d'une attribution critique de cet article au rédacteur correspondant.
Va donc non seulement tisser des liens entre ces catégories mais aussi annoter ces liens. Par exemple en indiquant qu'elles sont les recherches qui nous permettent de faire ce liens.

Permet de respecter la structure de l'ouvrage. Permet également d' annoter ces liens et de les traiter.

Exemple d'Argenville passage qui suit signature de Diderot
Typiquement passage attribué à Diderot, or on a montré qu'attribuable à D'Alembert.
C'est ici que tout cela prend son sens.

Existence du lien renseigné par note renseignant l'attribution.
Schéma qui permet de régler tous les cas des articles non signés.  Suffira d' annoter le lien pour expliquer, annoter, l'attribution du passage.

Généralisation de ce mode de travail à l'ensemble des métadonnées critiques de l'encyclopédie.
Les à ensuite regroupées dans des classes abstraites
Afin de regrouper ces catégories dans des listes de catégories critiques et d'établir des liens, avec idée que puisse appliquer une telle analyse à la fois en amont aux sources et en aval aux conséquences.

59 catégories encyclopédiques établies

Idée annoter le texte à plusieurs échelles
Édition classique, notes critiques et historiques, mais nouvelle façon d' annoter puisque notes sur les liens permet annotation impossible sur le papier, c'est à dire notes sur les liens.
Aimerait également pouvoir développer de tels outils d'annotation sur les planches.
Besoin de pouvoir lier des éléments précis avec des données critiques sur les planches encore peu étudiées.

### Équipe
Noyau des membres de l'édition
Des lors que travail collaboratif, équipe pluridisciplinaire de chercheurs internationale
Équipe informaticien pierre Édouard portier, thèse Vincent Baridon consiste adapter DINAH plate forme édition philologique pour en faire une interface collaborative d'édition. Travail édition critique pouvant être lancé dans 3 ans.

Projet soutenu par l'Académie des sciences qui vise à valoriser l'exemplaire.

### RMQ Perso

Il est nullement question du websémantique ?
Surprennamment, le modèle TEI n'est pas cité


Discussion
-------------

Daniel : Tenez vous compte des lettres de savants qui ont pu être envoyées ?

R : oui bien sûr, lors de la production de ces metadonnées la possibilité d.indiquer qu'il s'agit d'une autre manifestation d'une lettre telle qu'une copie, publiée, etc.

?? Me semblait que travaillaient sur la transcription
R pas le Focus principal, mais selon les perspectives des chercheurs aussi le cas.
Mais ne voudrait pas réinventer la roue, donc probablement travailler avec des collaborateurs.

Sur le projet encre, que pensez-vous faire dans le cas des passages empruntes. Comment intégrer les sources primaires ?
R schéma montré fonctionne de la même manière pour les mentions, qu'elles soient mentionnées ou nom. Trois éléments qui permette avec les même mécanismes de séparer à la fois les hypothèses des avis portes sur l'édition. Dispositif qui permettant de bien distinguer apparat critique du contenu de la source qui permet de produire une cartographie. Important de bien pouvoir spécifier ces données là de sorte à pouvoir les analyser

Endelman? 
Quelles bornes chronologiques
R en fait ignore les dates. En fait étendu beaucoup les bornes. Initialement seulement jusqu'en 1720 à partir du catalogue mais rien ne justifiant réellement cette date.

Abondance de donnée, comment offrir un chemin de lecture dans ce contenu ?

R pour cela qu'encore besoin de temps. Un des enjeux principaux et aussi l'enjeu pour les outils collaboratifs. Quand veut réunir certain nb information, les organiser pour les rendre lisible et rendre la présentation ergonomique, pas seulement des spécialistes.
Aujourd'hui test pour réaliser des parcours de lecture qui soient ergonomiques

Oui pas seulement car dans imprimé une introduction qui offre un chemin au chercheur.

Ta question une question importante au cœur de notre travail comment gère le fait d'avoir d'immenses bases de données et les rendre accessibles au lecteur.
Deux sortes d' intelligibilité' comment rendre compte que nos bases de données sont fiables, mais aussi comment donner des chemins d'accès au document.
Un lecteur peut donner à lire son propre parcours, et le donner à lire.

En enjeu très important pour lequel pas seuls à être confronté au pb.

Catherine (qui travaille sur montesquieu)
Question de donner du sens, interprétation versus objectivité
De fait interprétation c'est donner du sens.
Cherche moyen de mettre en valeur corpus Montesquieu. Tout petit donc important de le mettre en lien pour le lettre en valeur.

Problème d'origami, l'absence de TEI et son enfermement.

R pour Claude Simon schéma pour convertir. Idée de développer en TEI directement.

Question sur le statut des textes dans la correspondance.
Quel est le statut du scripteur, en quoi il est responsable de l'édition. Quel intérêt de publier l'imprimé lorsque dispose de l'autographe. À moins qu'un brouillon.

R en fait une édition par d'Alembert donc intéressant. Mais de manière générale éditions du 19ème expurgées donc intéressantes du point de vue de l'historiographie. De même publications polémiques de l'époque importantes.

Quelqu'un de Europe

développe plate-forme d'édition critique
Édition Wittgenstein
Connaissant travail de DINAH surpris que pas plus de liens et d'engagement
Logiciels d'annotation sémantiques en cours de développement

Je pense qu'au moment de votre passage à XML verrez que d'autres solutions.
Voir à philo source ce qu'est déjà capable de faire. Des choses déjà en place, des problèmes de convergences après.

R oui mais tout cela existe aussi dans DINAH. Publication multi-structurées de documents un vrai champ de développement informatique. Mais par ailleurs travaille aussi dans un environnement avec Lyon.
Veut s'adapter de manière collaborative à la modification de vocabulaire. Volonté de pouvoir développer un outil informatique générique. Une thèse en informatique sur le sujet.

Oui mais pb avec Wittgenstein, difficultés pour sortir les manuscrits. Obtenir des facsimilé de la Bnf très important mais passé par une convergence. Or accord Bnf et Europeana. 

Christine Boulet ? Projet Lambert ?

Si j'ai bien compris les sources de la recherche, c'est à dire les documents primaires sont en ligne. Un des avantages fabuleux de l’édition numérique que de pouvoir donner accès à des documents.
Alors renvoyez vous par des systèmes de liens de manière automatique à d'autres ressources comme Bnf, etc.

R évidemment pas intérêt à travailler dans son coin. Déjà doit convertir en XML-TEI, équipe de mapping sur ça. Mais petit budget, travaille doucement. Ici 


Le projet Mapping the Republic of Letters : état des lieux, des outils proposés et des collaborations
----------------

Présentation du projet collaboratif et international Mapping the Republic of Letters développé à Stanford Humanities Center par Dan Edelstein, co-responsable du projet MRofL.Une présentation des outils de visualisation déjà proposés au public et de ceux en cours de développement : Nicole Coleman, Academic Technology Specialist, Stanford Humanities Center : Knot (Août 2012), Ink (janvier 2012), Fineo (juillet 2011), Inquiry (septembre 2010), Corrispondenza (janvier 2010), RofL Viz (2009). Voir le site http://republicofletters.stanford.edu/
Perspectives et discussions 


Table ronde et discussion : « Les acteurs d’un projet en humanité numérique, fonctions et compétences »
----------------

