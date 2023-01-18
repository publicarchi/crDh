## Martin Grandjean, 2022

Enseignant en histoire à Lausanne.

Approche d’extraction de données et analyse de réseau. Demain un cours sur la visualisation en général. Analyse de réseau. 

Moment introductif, essai de Gephi.

Analyse de réseau permet d’analyser des relations entre des choses en contexte. Aller dans le fond de la relation entre deux entités ou acteurs en regardant le contenu d’une correspondance par exemple. Dans une analyse historique chacune de ces lettres est le témoin d‘une relation entre deux individus. Mais il pourrait tout aussi bien s’agir de twitt. Disons qu’il s’agit des personnes comme on s’intéresse au social.

Quand on observe cet ensemble de relations, on peut peut-être identifier un pont entre deux individus. Relation particulière. Mais dans ce réseau, peut aussi dire que des voisins ont des relations entre eux. Intéressant de savoir que les personnes qui ont des échanges ont aussi des échanges, les uns avec les autres.

Voir ce que la connaissance de l’ensemble du réseau nous permet de fournir du contexte à cet élément. Aura une influence surtout si cette relation apparaît dans des contextes différents.

Ici 4 représentation de graphes qui comprennent le même nombre de points, le même nombre de relations. Mais voit que les lettres en deux acteurs présentent un rôle très différent dans un ensemble. Le fait qu’apparaissent au centre d’un groupe, rapport très différent que si le seul pont ou dans le cas où un groupe séparé, ou encore des relations très homogènes. Le rôle structurel est sans doute moindre.

Faire de l’analyse de réseau, c’est essayer de comprendre la relations de points entre eux dans un groupe de relations en essayant de qualifier cette relation.

Ici la visualisation aide beaucoup à faire la représentation de cette relation dans son contexte, mais on comprend aussi qu’à un moment cette visualisation ne deviendra plus possible. Au niveau d’un village, d’une ville, d’une région ou un pays en entier. Rapidement devient plus lisible, et besoin d’autres choses pour travailler. 

Big spaghetti monster, ou hair ball. Il s’agit d’une représentation graphique qui n’est plus vraiment lisible. Elle est lisible globalement comme une sorte de carte qui présente des relations ou des clusters, mais il n’est plus possible de travailler au niveau de deux relations.

Ici 10 ans de financement de la recherche scientifique. 305 000 relations. 35 000 chercheurs.

Il est possible d’avoir une lecture diagrammatique ou encore une lecture topographique, ou encore comme une heat map ou une carte de chaleur et de densité où on lie des relations qui ont beaucoup d’importance. Exemple ici clusters des sciences de l’ingénieur, physique nucléaire. Sciences humaines très différent.

Un graphe qui est illisbile et pour lequel on a besoin de trouver d’autres moyens pour l’analyser. Ce que l’on va plutôt utiliser ici, ce sont les métriques. Des mesures issues de la théorie des graphes, qui portent sur l’analyse des résultats des réseaux structurés. Réseau représentation du fait social, graphe représentation pure au niveau mathématique. Analyse les nœuds et les arrêtes, les points.

Quels sont les outils ici à notre disposition ? D’abord bien sûr l’analyse visuelle, ensuite l’analyse des métriques globales, cad la mesure du réseau : à quel point est-il grand, divisé en groupe différents, dense, ou tendance à s’organiser entre groupes plus denses, etc. Ces métriques globales sont utiles pour pouvoir comparer des graphes différents. Densité = total de relations divisées par le nombre de nœuds du réseau.

En général en sc hum et sociales, nos réseaux sont très peu denses.

Ensuite il existe des métriques locales, comme les mesures de centralité qui mesurent la centralité de certains nœuds par rapport à d’autres à partir de mesure canoniques. Qualifient la position d’un point par rapport à d’autres points du réseau. Est-il proche globalement des autres points, sur le chemins d’autres points, dans des cliques, etc.

Exemple : degree centrality, betweenness centrality, closeness centrality, egenvector centrality.

Mesures qui se sont imposées comme étant des mesures graphiques pour les interpréation du graphe. Selon manière dont calcul centralité se rend compte que position qui sera variable.

Distance dans un graphe qui se calcule en nombre d’étape en prenant le plus court chemin. Selon cette mesure, la personne la plus centrale celle qui a la moyenne des chemins la plus petite. Closeness centrality.

Centralité d’intermédialité, nombre de fois qu’un nœud est sur le chemin d’un autre. Ici prend tout les couples et donne un point à toutes les étapes entre les points. Quelqu’un qui permet la connexion. Mesure très proche de la théorie des liens faibles. Aussi le point que si on l’enlève va couper le plus de relation dans le réseau. Fort en termes de connexion, et en même temps le plus vulnérable pour le réseau. verrou du chateau-fort. Si la tour est prise tombe.

Eigenvector centrality, comme le page-rank. Centralité de vecteur-propre. Notion que connaît avec les moteurs de recherche comme Google. Score d’autorité, où donne 1 pour commencer, et chaque point donne une partie de son autorité à tous les sites vers qui fait un lien.

cf. article Grandjean et Jacomy, short paper 2019. Communauté qui s’est petit à petit fixée sur certaines métriques pour telles ou telles interprétation.

Grandjean, Martin, et Mathieu Jacomy. 2019. « Translating Networks: Assessing Correspondence Between Network Visualisation and Analytics ». https://halshs.archives-ouvertes.fr/halshs-02179024.

Distinction de Tucky ? entre la dimension exploratoire et l’axe démonstratif. Le fait de travailler sur des données ou de l’inforamtion récoltée.

Illustration, démonstration, interface, recherche

Data visaulsiation / information visualisation.

Important quand travaille avec ces techniques de savoir où va commencer à se situer.

Des usages très variables. Parfois seulement illustratif. Parfois des sociogrammes, où pas besoin de le visualiser pour le comprendre mais peut permettre au lecteur de comprendre cet objet. D’autres réseaux pas directement communicables au public mais qui sert à faire notre travail.

https://jhnr.uni.lu/index.php/jhnr

Peut avoir des interfaces de réseaux pour consulter des archives.

Histograph : pour consulter des archives.

Imaginary Map of the Literay Livv.

Interface de lecture de pièces de théâtre

Peut aussi faire de l’illustration pour synthétiser de l’information. Réseau qui ne sera pas analysé avec les métriques de la théorie des graphes mais une représentation tout aussi valable.

Parfois commence avec l’idée de faire une visualisation de recherche mais va utiliser comme illustration quelque chose. Parfois complètement l’inverse. Car faisant cette démarche, découvre une relation ou une organisation que n’avait pas notée.

En histoire pour la visualisation surtout liée à des sources. Divise le spectre des images en 4 catégories. Qui sont les suivantes : metaphorical networks, reconstitued networks, extracted networks, metadata networks

Métaphorique mais nous intéresse peu.

Usage historique pour reconstituer un réseau à partir de plusieurs sources. Ne travaille pas sur source sérielle mais ensemble de documents en faisant des liens.

exemple 1993, Padget et Ansel, sur les relations entre grandes familles florentines. Mais finalement graphe qui ne peut pas vraiment être analysé mathématiquement. Car ne sait pas si ne manque pas des informations. Mais une synthèse de ce que sait sur les relations d’après les archives disponibles. Un acte de critique des sources. Visualisation qui sert à être le panorama de ce que l’on sait sur ces familles.

Troisième niveau d’analyse qui consiste à extraire des informations d’un ensemble de document. Exemple notarial acts. Les historiens aiment bien faire des listes.

Enfin travailler non plus sur le contenu des documents proprement dit mais leur circulation. Expéditeur et destinataire, etc.

- Mapping the republic of letters, Stanford
- Circulating of knwoledge
- Culture of knowledge

Sorte d’uniformisation dans ce genre d’approches. Cartes avec des réseaux. Pas toujours pertinent. Selon la manière dont va voir le graphe, va voir des choses différentes. Regard structurel, versus géographique.

Un gros enjeu de la représentation d’analyse historique est celui de la temporalité. On cherche toujours à montrer quand est-ce que la relation commence, comment elle finit. Plein d’outils pour faire des sliders pour voir comment les relations évoluent. Mais pose le pb de la carte mentale. Si fait évoluer dans le temps, aucune chance que garde la carte mentale de qui est où. Quels moyesn pour explorer diachronicité sans briser représentation graphique. Plus a une interface qui permet de jouer avec un slider, plus risque de perdre public qui n’a pas la littératie du graphe.

The Historical Network Research Community https://historicalnetworkresearch.org/

Gephi pas représentatif de l’école française. Plutôt un outil qui plaîra côté anglo-saxon.

Gephi, gephi.org un outil qui a le mérite d’inciter à une créativité visuelle. WYSIWYG. Mais intérêt car démarche d’înteraction avec le graphe lui-même qui est très fructueuse pour certains usages. Impression d’être en face d’un objet que vous allez pouvoir modeler de plein de manières différentes.











