# Du registre à la datavisualisation des trajectoires. Réflexions sur l’édition numérique des registres d’inscription à l’École des beaux-arts

https://agenda.inha.fr/events/du-registre-a-la-datavisualisation-des-trajectoires-reflexions-sur-ledition-numerique-des-registres-dinscription-a-lecole-des-beaux-arts

**Séminaire****« REGarts : archives et mémoires de l’École des beaux-arts de Paris »**, 12 mai 2023

France N Dernière séance de l’année universitaire de ce séminaire. Un séminaire qui est lié à un projet de recherche mené par trois institutions EcBA Alice Thomine, Déborah Lax CNRS et INHA France Nerlich. Travail débuté il y a deux ans pour réfléchir à la manière dont on pourrait rendre disponible la source très consultée des registres des élèves de l’Ec des Bx Art. 1809 à 1968 aux AN pour le 19e et aux BA pour le 20e. Conserve sur toute la durée une forme homogène avec des données sur les jeunes personnes qui se sont présentées à l’école pour participer au concours. Principalement des hommes au XIXe s, puis progressivement des femmes.

Sur toute la période des registres homogènes qui donnent des informations sur le nom, la date de naissance, l’adresse, le garant du jeune qui se présente ainsi que des observations sur le curriculum et les dates d’entrée à l’EBA. Il s’agit de colonnes dans les registres qui ne changent pas beaucoup mais qui sont renseignées de manière plus ou moins homogènes pendant toute cette durée et qui reflètent des données changeantes à travers le temps. Age, modalité d’inscription qui changent au cours du temps et qui font que la réalité derrière ces données est très changeante.

Les registres comprennent les élèves qui ont réussi les concours d’enrtée avec le bémol qu’il pouvait y avoir des entrées définitives ou provisoires. Par ailleurs des périodes où pas de concours d’entrée. Donc il s’agit d’une source homogène qui en réalité documente des réalités différentes.

Ces registres constituent par ailleurs une source très partielle pour rendre compte des élèves qui ont fréquenté l’EBA. D’autres sources comme des listes d’élèves et des dossiers d’élèves conservés aux AN et à l’EBA montrent que ces registres ne représentent pas la totalité des personnes qui ont étudié à l’EBA. C’est une dimension importante car il faudra rendre compte du caractère parcellaire de l’information contenus dans ces registres lors de la publication.

Ces questions importantes qui nous ont préoccupé au cours des dernières séances de séminaire (cf. enregsitrements en ligne). Cette dernière séance est destinée à partager le travail réalisé au cours de l’année par Paul Girard qui a réalisé pour nous la tranformation des données. Les registres ont été intégralement transcrits dans des fichiers excel avant d’être transformés en données structurées par un data curator qui sait donner un sens à ces données.

Financement de la Fondation ... qui a permis de recruter Lucie Lachemal pour y travailler. [Thèse 2017, Beaux-arts et critique dans la presse parisienne sous la Restauration (1814-1848)
 Membres du jury : Marie-Claude Chaudonneret (CNRS), Thierry Laugée (Université Paris IV-Sorbonne), Christine Peltre (Université de Strasbourg), Bertrand Tillier (Université Paris I Panthéon-Sorbonne), Pierre Wat (Directeur de thèse/Université Paris I Panthéon-Sorbonne]

Comment passe d’une base de données à un outil qui pemret non seulement des interrogations mais aussi d’en faire plus ensuite. Atelier expérimental autour des données organisé il y a 15 jours pour voir ce que pourrait visualiser en termes d’espaces de réseau, et pour travailler sur l’ergonomie de l’interface que l’on imagine.

## Paul Girard

### La chaîne de traitement des données

Six registres conservés aux AN et à l’EBA

Transcription et normalisation, données principales regarts.csv

Validation de document datapackage.json + Versionning
normalisation de description des variables présentent dans un tableau mis en place par OKF, très utile car permet la validation et d’outiller la gestion du jeu de données de manière très utile.
Utilisation du GitLab de l’INHA pour gérer les versions des jeux de données. Permet de garder la trace de l’historique sur qui a modifié le jeu de données, quand et comment.

script python mode_data

= élèves garants, lieux de naissance

Alignement avec Open Refine et API de réconciliation

Adresses, alignements Alpage et Paris Vasserot

LinkedArt
Format de formalisation mis en place par le Getty qui permet de qualifier les informations.

Données relationnelles
L’objectif de l’ensemble de la chaîne est de pouvoir sortir des données relationnelles. Cad quelque chose qui supporte la quantification. Une table avec les élèves, une table avec les inscriptions, des choses qui avec un schéma de données facilite les interrogations.

Noter qu’un important de travail mené manuellement.

Pour la réconciliation utilisation de différentes variables de réconciliations. Fait pour les élèves. Un algirithme de réconciliation amélioré

Corrections de problèmes de l’API existante

- gestion des duplications des propriétées
  La source fournit jusqu’à 7 prénoms, l’algorithme n’utilait que la dernière valeur pour des raisons techniques
- méthode alternative de scoring des listes de valeurs (prénoms, professions)
  La quantification de la proximité, pb sur les lisets de valeurs, quand 7 prénom vs 1 comment calcule-t-on la proximité, puisqu’il y a 7 paires possibles. Or, faisait la moyenne de l’ensemble des valeurs si bien que la multiplicité des prénoms baissait le score !
- méthode alternative de scoring des dates
  L’algorithme de base varie de 0 à 100. Si exact = 100 si un autre jour 0. Aucune nuance ! Or, on sait que des dates proches à considérer. Pas évident de mettre de la nuance dans la comparaison de dates car cela implique donner un absolu...
- méthode alternative de scoring des données manquantes
  Pour les données manquantes, l’absence de données ne signifie pas que l’information n’existe pas. Or, l’algorithme d’appariement considérait que les valeurs vides étaient comparables. Ce que l’on a choisi, c’est de ne pas mettre de score pour une valeur manquante. Correction des pondérations pour avoir des scores corrects.

De la logique flou lorsque manipule des algorithmes très stricts. Important de faire de l’heuristique pour retrouver dans la nuance dans cette machine d’appariement. 

12 000 résultats pour lequels on a fait le choix d’utiliser la machine pour proposer des candidats avec des scores mais en faisant en sorte qu’un humain valide ces apariements. 

La proportion d’appariement réussi de l’ordre de 25% mais avec des proportions différentes sur les différents volumes, les registres anciens ayant un taux de reconnaissance plus important que les récents.

Idem sur les lieux.

Alignement qui permet la réutilisation mais qui permet également d’augmenter notre jeu de données avec celui des autres. Comme dans Wikidata on dispose par exemple des ISNI des individus, on peut le rapporter, etc. Date de décès, ou le fait que seulement une vue parcellaire sur la carrière des artistes.

Les garants sont les personnes qui ont présenté les élèves au concours. Souvent seulement un nom. Un travail qui reste donc à faire. Intéressant pour savoir aussi qui a été élève avant. Indispensable pour pouvoir faire de l’analyse de réseau par la suite.

Les adresses, aussi un travail en cours. Le jeu de données donne parfois les adresses de domiciliation des élèves, le plus souvent à Paris. L’idée est de géolocaliser ces adresses à partir du plan de Paris (l’Atlas Vasserot comporte la nomenclature des voies).

## Datathon, mercredi 19 avril

Réseau version dynamique du travail.

Des composantes connexes qui regropes les élèves d’un même professeur à l’EBA. Codification du genre avec des couleurs. Un registre d’hommes et des registres de femmes. Exemple Narbonne. Ensemble des élèves qui n’ont pas eu d’autres garants dans leur scolarité, et n’ont pas eu eux-mêmes des garants. = une bulle de relation.

Pour une partie importante du corpus, on a quand même de la relation qui se créer avec différents acteurs. Jean-Paul Laurens, Jean-Léon Gérôme, Cabanel, Cormon, Léon Bonnat, etc. Question du genre et du temps que peut faire varier avec des couleurs. Ce qui permet notamment de repérer différentes choses.

Utilisation de Gephi Light pour prototyper ce qui pourrait être fait dans le cadre d’un site par la suite. Peut utiliser deux types de dates, comme année de naissace ce qui permet de filtrer l’année. Ici plutôt que colorer, va filtrer. Une composante importante du temps dans la fabrication de ces relations. Possible ensuite de faire évoluer la chronologie pour voir à quoi ressemble le réseau sur cette partie du réseau (en filtrant et en conservant les positions, ou bien en faisant retourner l’algorithme qui positionne les nœuds).

Des traductions, une autre manière de voir ce qui est dans le registre physique. Spectaculaire mais attention. Cependant aussi un outil mathématique qui permet de faire des calculs de communauté.

Possibilité de géolocalisation par lieux de naissance.



##  Ergonomie

Importance de la précision du vocabulaire pour pouvoir nommer ce que l’on va utiliser et préener.

Possibilité d’inscrire les noms dans des bornes chronologiques pour la recherche et les inscrire dans les évolutions réglementaires de l’école.

Rendre tout de suite visible et compréhensible. On est face à un document d’archive en partie parcellaire. Toute source est subjective ou limitée. On est en réalité face à un univers beaucoup plus complexe. DH peuvent donner l’impression que tout est stable alor qu’il y a beaucoup d’incertudes en arrière-plan. Une dimension importante dont il s’agit de rendre compte par le biais du design de manière visuelle.

## Exemples

Mise à disposition dans cet état très intéressant, même si simple présente une importante quantité de travail.

Exemple, édition numérique des registres matricules de l’Académie des beaux-arts de Munich. Projet réalisé à l’occaison des 200 ans de l’Acad BA de Munich. Un projet lancé en 2008, renouvellé en 2015. À l’époque, les outils évoqués par Paul, n’existaient pas.

Sources proches, 5 volumes de registres qui couvrent des périodes longues et assez proches. 14 000 données.

« Matrikeldatenbank - Akademie der Bildenden Künste München ». s. d. Consulté le 12 mai 2023. https://matrikel.adbk.de. 

Mêmes problématiques, informations problématiques.

Utilisation FileMaker Pro, puis gestion dans un CMS Zlot ? Puis alignement des données du GND, et le AKL. Les données sur le genre ont également été ajoutées de même que les dates de mort. Religions pas bien normalisées, commission réunie pour choisir des termes génériques.

Présentation de l’édition qui débute par une liste de professeur de la période avec des informations fournies sur les enseignants. Avant d’arriver aux registres proprement dits. Ceux-ci ont introduits par une remarque sur l’édition et des avertissements préliminaires qui sont assez courts mais qui permettent de comprendre comment les informations sur les données ont été traitées.

Possibilité ouverte de commenter les registres par les utilisateurs. Ouvrent la porte à ceux qui souhaiteraient apporter des ajouts complémentaires. 

Pour chauqe entrée, indique les cours suivis, l’année d’inscription (avec le nb par année), le lieu de naissance.

Transcription du registres, et information bibliographique produite par l’équipe.

Une géolocalisation, volonté de travailler histoire de migrations mais pour autant l’outil pas facile à exploiter ou faire sens.

Dictionnaire des élèves architectes

2004 à 2015, projet intitié par Alice Thomine, travail qui s’appuyait sur un travail initié dès 2001 par Marie-Laure Crosnier Lecompte. 18 000 noms.

Des éléments structurés liés à la scolarité à l’école. Différentes sources utilisées. Dossiers d’élèves numérisés disponibles en IIIF. Une partie qui relève de la gestion des notices. Chaque notice en lien avec d’autres.

Une faiblesse, les garants ont été traités de la même façon que les professeurs avec lesquels les élèves ont suivi des cours (dans une notice événement, Atelier de). Ce qui n’est parfois pas approprié. Il n’y a pas eu de différentiation des garants des professeurs de l’EBA qui sont les plus grands garants.

À partir de cette bdd, Antoine Courtin avait produit une interface expérimentale. Skylab.inha.fr/dicoarchi2/index2.html un alignement avait été réalisé et 18 000 noms reversés dans Wikidata. Une visualisation de réseau. Cartographies dyanmiques et temporelles pour les lieux de naissance.

Projet datant dans le temps. Une correction effectuée car un registre matricule pour lequel erreur. Bis.

« Portail de recherche dans les archives de la Biennale de Paris 1959 - 1985 ». s. d. INHA : Portail de recherche dans les archives. Consulté le 12 mai 2023. https://bdp.inha.fr/.

> Ce portail de recherche permet d’accéder à l’ensemble des 6388 dossiers de participation d’artistes à la Biennale de Paris (1959-1985) conservés aux Archives de la critique d’art à Rennes (collection INHA) et à la Bibliothèque Kandinsky (MNAM-CCI – Centre Pompidou) à Paris. Il permet de croiser les données issues des deux fonds d’archives, de réaliser des recherches ciblées sur les 5043 artistes répertoriés, de trier les données et de produire des visualisations et des statistiques à partir d’une série de filtres. 
>
> Ce portail est réalisé dans le cadre du programme de recherche « [1959-1985, au prisme de la Biennale de Paris](https://www.inha.fr/fr/recherche/le-departement-des-etudes-et-de-la-recherche/domaines-de-recherche/histoire-de-l-art-du-xviiie-au-xxie-siecle/au-prisme-de-la-biennale-de-paris.html) » conduit de 2017 à 2021 à l’Institut national d’histoire de l’art (INHA), sous la direction d’Elitza Dulguerova, en partenariat avec les Archives de la critique d’art, la Bibliothèque Kandinsky et l’Institut national de l’audiovisuel. Un double objectif animait ces travaux de recherche d’envergure internationale : 1° réfléchir aux apports de cette manifestation à l’histoire de l’art contemporain et de ses institutions, par l’organisation de séminaires, d’une exposition et de publications scientifiques et 2° faciliter la consultation des documents d’archives qui en conservent la mémoire. (Pour plus de détails, voir la section [Ressources](https://bdp.inha.fr/ressources/#Critique)).

Lancement l’année prochaine. We Do Data, SS spécialisée dans le Datajournalisme qui nous a aidé à concevoir le design graphique lié à ces données.

Vues listes avec filtres interrogeables.

Le service numérique de la recherche de l’INHA accompagne le projet depuis le début, depuis la transcription des registres, mais aussi tout au long de la préparation des données.

Pour le moment pas encore travaillé sur la liasion entre les deux bases. D’abord, un projet commun, c’est l’EBA qui va publié, il n’est pas encore prévu de publier sur Agorah.

Pour le moment Wikidata a été utilisé comme point commun. Sera facile de créer un référentiel des artistes car utilisation de Wikidata comme dénominateur commun.

LinkedArt pas mal spécialité.

https://linked.art/model/actor/

Description des activités mais notions pas évidentes à qualifiées. Carried_out pour décrire les activités, le fait d’avoir été à l’EBA, fat d’avoir passé le concours

Contrairement à l’architecture, pas de fin. Pour les études, pas de diplôme. 

**Le début du registre fait presque objet de dossier d’élève.**

Pour les envois de Rome, avait numérisé tous les règlements car séjour qui a évolué dans le temps. Fluctuation dans la durée des études avec la guerre par exemple. Élèves qui ont sans doute menti sur leur âge pour rester à l’école plus longtemps.

Séminaire qui reprend en octobre (le 13 octobre) aux BA de Paris. Séance consacrée aux artistes chinois à l’EBA. Puis 24 novembre et 15 décembre.







