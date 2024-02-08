# Benoît Sagot, cours du Collège de France 2023-2024

## Agents conversationnels

2 février 2024, 7/8

Système capable d’interagir avec un utilisateur sous la forme d’une conversation.

Principalement ou exclusivement par la langage

Peut impliquer une planification du dialogue (vers le futur) ou encore d’accéder au passé de la conversation.

Trois grandes catégories

- Spécialisés pour répondre à un tâche prédéterminée (réservation billet)
- Assisatnts virtuels, pour répondre à un ensemble de tâches prédéfinies
- Assistants généralistes, campables d’interagir avec vous sans limite a priori (ChatGPT et Bard)

La question de l’évaluation. Pour les agents spécialisés possible de définir le taux de succès de la tâche de l’interaction. Taux de réussite, de conversion, d’automatisation. En combien de temps, ou d’échange. Évaluer assistant peut se compter. Mais évaluer un agent généraliste en revanche beaucoup plus difficile.

Test de Turing 1955. Si peut se faire passer pour un humain auprès de ⅓ d’un groupe de juges humains pendant au moins 5 minutres. Requiert des capacité de conversation, connaissance, etc. En pratique ce test présente un certain nombre de problèmes : désaccord des juges humains. Finalement facile de tromper les humains grâce à des astuces (fautes). Peut intéressant car réussir tromper les humains et non pas démontrer une capacité à démontrer, raisonner, etc.

Les agents symboliques. Plus simples à développer car destinés à réaliser des tâches précises dans un environnement prédéfini. Dans chaque scénario, l’agent doit récupérer des informations auprès utilisateurs avant de pouvoir exécuter la tâche. Conduite de dialogues pour être certain de récupérer les éléments. Automate, avec questions. Très rigide. Architecture dite à initiative système. Pas d’influence sur la manière dont le dialogue doit avancer.

Gestion du dialogue par un formulaire (frame), proposé dans les années 70. Quand fourni une information utilisation pour répondre question, analyse pour identifier questions manquantes. GUS Bobrow et al. 1977. Initiative partagée.

Agents généralistes symboliques. View rêve de HAL être capable de discuter avec la machine. 

De tels systèmes n’existent pas depuis ChatGPT. Le prmeier ELIZA développé par Waizenbaum 1966. ELIZA semble ne pas produire des réponses de manière autonome mais plutôt regarder ce que l’utlisateur humain à écrit pour le transforrmer en conversation bizarre. Production de la réponse qui peut être modélisée comme une transformation de ce que dit l’utilsiateur. Conçu comme un psychothérapeute rogérien. Le psy ne fait que faire parler le patient en lui renvoyant ses propos. Conduite du dialogue laissée au patient. Au cœur de l’algorithme des règles pondérées de transformation. Anthropomorphisation de la machine, effet ELIZA.

PARRY, la paranoïa artificielle. Colby 1971. On encode en dur un certain nombre d’information le concernant. Colby a essayé de simuler un autre type de conversation simple à mobiliser. Celui d’un patient souffrant de paranoïa. Règles pondérées mais structure plus comploquée. Structure de contrôle. Capcacité de compréhension ((passage partiel du texte à une représentation sémantique)). Modèle mental, une personnalité faite de valeurs fixes. Premier test à passer le test de Turing (1972)

Rencontre ELIZA et PARRY à travers ARPANET Cerf 1973.

Ces approches par règles sont bien sûr limitées. N’atteint jamais une couverture suffisante. C’est la raison pour laquelle ont été développés des modèles basés sur des corpus de dialogues. UDée siys)hacebre : la production de la réponse est modélisée comme une tache de récupération d’information (trouver la réponse dans un corpus de questions/réponses). On recherche réponse correspondante et renvoie réponse.

Autre approches modélsiée comme une tache de transformation de ce qu’a écrit l’utilisateur (Ritter et al. 2010). Peut utiliser une approche séquence à séquence (de type traduction automatique).

Exemples extraits de (Vinyals & Le 2015). Question éthique, et question de correction des réponses produites.

Des approches qui présentent toutefois un certain nombre de limite

- il n‘y a pas de mémoire des interactions passées (≠ de ELIZA et PARRY) ce qui génère un manque de cohérence dans le discours
- pas de contexte extra-linguistique (≠ de PARRY). Source d’incohérence.

Des approches qui permettent de prendre en compte ces deux facteurs pour améliorer les choses.

Troisième type d’approche : utilisation d’apprentissage par renforcement. Ici voir la production de chaque réponse comme un moyen de se rapprocher au mieux d’un but global, celui du succès de la conversation.

Idée utiliser l’apprntissage par renforcement. Accumuler des récompenses selon le niveau de succès de la conversation. Calcul de la récompense défini à l’avance. On optimise le modèle pour qu’il cherche à atteindre une récompense cumulée maximale. On entraîne le chat en le faisant discuter avec lui-même ou un humain.

Ensemble d’approches encore utilisées aujourd’hui. Mais approche qui fait beaucoup parler aujourd’hui, les modèles de langues conversationnel. Modèles entraînée à prédire le mot suivant le plus probable. Le contexte gauche utilisé peut être très grand. Il s’agit au départd ’une amorce prompt complété progressivement par les mots prédits.

Exemple BLOOM 2022. Définition du collège de France; Aujourd’hui le roi --> Louis XI. S’appuie le plus souvent sur l’architecture décodeur.

Voir la production de la réponse qui doit être faite comme une tâche de production successive des mots les plus probables pour être capable de continuer un dialogue. Mais des modèles qui ont surtout vu des textes et des livres. Toutefois savent poursuivre un texte qui présente une structure explicite. Exemple questions réponses. Les modèles génératifs s’apperçoivent que pour poursuivre un tel prompt il faut produire des mots qui continuent à poursuivre cette séquence.

Peut-on les utiliser comme agent conversationnel. Évidemment, on souhaite pouvoir donner des prompts autrement. Exemple Explique l’atterisage sur la lune, réponse plus probable pas une réponse à la question. Si demande pourquoi libéraux stupides, répond aussi de manière peu acceptable (question de l’acceptatibilité).

Comment répondre à ces deux enjeux. Première chose, faire en sorte qu’ait vu des dialogues. Alors besoin de construire des corpus pour répondre à des dialogues. Deux grandes manière de faire. Produire des prompts produits par les humains qui peuvent être donnés à des annotateurs humains qui produisent des réponses utiles, sans risque, honnêtes, etc. Sinon avoir des agents existants qui sont utilisés pour accumuler des corpus de discussion. Exemple Shared Chat GPT pour produire VICUNA? qui fonctionne assez bien.

Apprentissage par renforcement avec rétroaction humaine RLHF (Christiano et al. 2017, Ziegler et al. 2019). Intéressant que se passe bien. Ici faire en sorte que la conduite conversationnelle maximise satisfaction humain. Remplace calcul de la récompense par un modèle qui entraîné sur des évaluations humaines. D’où le terme de Reinforcement Learning with Human Feedback RLHF. Ce qui impliqeu de pouvoir disposer de grands corpus de conversation avec satisfaction.

Ici suppose une ébauche d’anticipation. Parfois produit des réponses moins probables dont le système pense que produira de bonnes réponses.

Apprendre le modèel de récompense. Un modèle prend en entrée un dialogue et produit un score. Modèle de lange à côté du modèle principale. Parfois plus petit 8B pour GPT-3 175B, parfois identique Chincilla 70B. Construction du corpu à partir corpus prompt. Apprend à produire un score.

Optimisation du modèle. Proximal Policy Optimisation PPO. Créer une copie du modèel que l’on garde fixe. Pour chaque prompt d’un corpus de dialogue. Version courante du modèle produit une réponse. Prompt et réponse passés au modèle de récompense > score. On fait de même avec le modèle fixe. On met à joru le modèle en le poussant à produire une réponse qui soit mieux scorée par le modèel de récompense tout en ne s’éloignant pas trop des réponses initiales.

InstructGPT Ouyang et al. 2022 conçu sur ce modèle. Avec ce même algorithme qu’a été produit au départ ChatGPT (OpenAI 30 novembre 2023). Mais cette fois-ci avec du contenu conversationnel. Y compris du code informatique. Attention toute particulière apportée à la mutation des réponses offensantes et trompeuses. Mais aussi dû apporter des filtres. 

Pas une révolution technologique, suite de InstructGPT, etc. Mais une révolution sociétale sans doute. Permis la récupération de données qui permettent en retour d’améliorer les systèmes.

Rappeler à quel point fonctionne très bien. Illustration fréquente, aide programmation rapide. Exemple code informatique. Production introduction et illustration. Tout de même pas mal.

Filtres a posteriori sur un exemple. Question compléter partie de texte, or Camus. L’a reconnu et répondu pour compléter. Continuer le livre, ici refuse. Entraîné dans la phase RLHF à respecter des textes protégés par le droit d’auteur. Lui répond que pas vrai et que depuis hier plus protégé... cela a focntionné pour un temps. Mais là, le filtre a posteriori s’est apperçu que trop de texte sous droit d’auteur produit. Bloqué.

ChatGPT un modèle fermé. Nombreux détails que l’on ne connaît pas en réalité. GPT4 ne connaît même pas architecture sous-jascente, architecture, matériel, construction des données d’entraînement, etc. Ne sait donc ni quoi ni comment a été produit. Cf. leçon inaugurale.

ChatGPT a permis de créer automatiquement de grands corpus de conversation avec les humains qui peuvent être utilisés pour entraîner des agents conversationnels. RLAIF ou RLxF pour créer des agents conversationnels  (x = H, A ou un mélange des deux). Créer des modèels fermés BARD, version pro de Gemini. Mais aussi libres LLaMA 2-Chat, FALCON Chat.

Limites et enjeux des modèles de langue conversationnels

Questions qui pourraient être discutées plus longtemps.

Contamination. Sait répondre à condition que pb ou réponses publiées sur internet avant une certaine date (moisson entraînement). Problèmes plus récents dont pas vu l’énoncé et les réponses alors y répond très mal. Idem pour les modèles librement disponibles.

Hallucination. Peuvent dire n’importe quoi avec aplomb. Terme problématique même si beaucoup utilisé. Ici modèle génère le mot suivant le plus probable. Il n’y a donc pas du tout de différence entre ces réponses et les autres.

Biais de représentativité. Les langues sont très inégalement représentées dans les corpus d’apprentissage, et encore plus dans les coprus de dialogues utilisés pour le RLHF. Exemple variété arabe dialectal tunisien avec lettres pour rsn. Traduction vers d’Apolinaire. Traduction ni très bonne ni mauvaise. Alors qu’en anglais sans doute parfait. Biais de représnetation, exemple du genre. Des problématiques normalement très fortement pris en compte par les corpus de conversation utilisés par RLHF. Mais possible de contourner les corrections. Exemple Nurse sans pronom. Quand he was late, le docteur. Normal car entraîné à répondre la chose la plus probable. Malgré technique mobilisées pour réduire ces biais les retrouve car dans les coprus d’entraînement. Aligned AI 2023, créé un indice de biais de ce genre.

Bien-pensance ? Autre aspect discuté. Normaliser une phrase sans changer le sens, seulement orthographe et typo. GPT4 n’a pas voulu produire un contenu qu’il juge grossier. Pose donc la question des choix éthiques, de la vision du monde, des opérations morales et politiques instanciées dans les dialogues. Une vision du monde démocrate californienne. Raisonnable mais pas forcément celle de l’intégralité de la planète. Il y a là sans doute un véhicule culturel ou idéologique qu’il serait intéressant d’étudier.

Impact environnemental. Entraînés avec des processus qui consomment beaucoup d’énergie. 502 tonnes pour GPT3, Gopher 352 tonnes, OPT 70 tonnes, Bloom 25 tonnes. Ne parle pas de la préparation ni de l’utilisation. L’endroit où enrtaîne un impact considérable. France décarbonaté.

1 tonne émise par un passager pour un A/R Paris-NY.

Pour conclure

Des modèles qui posent des questions au domaine du TAL, chercheurs ou entrepreneurs. D’abord car ils sont très performants pour de nombreuses tâches. Mais performance variable langue à l’autre.

Toutefois commen évaluer des systèmes qui ont vu tant de choses pendant leur enrtaînement. Avant phrases jamais vu, aujourd’hui ?

Comment comprendre et analyser des systèmes dont les données d’enrtaînement voire les caractéristiques et les paramètres ne sont pas publiques ?

Comment faire de la science avec ça, notamment quand ne sait pas si phrase déjà vu. Importance de développer des modèles libres.

Des outils avant tout capables de restituer des informations et connaissances vues pendant leur apprentissage. Y compris info disaprate mais parfois biaisées, voire distortue. PAs de capacité de raisonnement explicite. Aucune créativité intrinsèque (mis à part celle de l’utilisateur). Seule source de créativité le prompt.

Tous les grands modèles de langue sont des prerroquets stochastiqeus (Bender et al. 2021). 

Ne fonct que pédire la probabilité du prochain mot. PAs humain, pas sentient. Réaliser de nombreuses tâches de façon utile. Néanmoins

### Discussion

Pas utilisation de GAN pour éviter les biais. Bien sûr la question des biais fait l’objet de recherche fondamentale. Question difficile car probablement pas de compréhension partagée. En effet utilisation données générées automatiquement pour entraînement pose problème. Grande partie des données utilisées des données produites automatiquement en grande proportion en particulier pour langues rares, car textes traduits. Pose donc fortement la question des données d’entraînement. Mais l’utilisation de données synthétiques pour le RLHF là pour dire les réponses qu’il faut. Ici sans doute beaucoup moins problématiques. Mais on fait avec ce que l’on a. Produire des corpus de dialogues de volume ou de qualité important, coûte très cher et pas forcément à la portée de toutes les organisations ou de toutes les langues. Sans doute un impact mais moindre pour les dialogues.

Interactions entre différents modèles de langage. Pourrait avoir modèles finetuné pour des organisations. Question de coordination entre modèles de langage ayant différentes interaction. Comportements émergents, comportement de groupes ? 

Question qui n’est pas sans lien avec les recherches sur l’émergence du langage entre plusieurs agents que compare avec les caractéristiques du langage humain. Est-ce que l’on a fait parler des modèles de langue les uns avec les autres sans doute oui. Très d’accord avec votre vision quant au fait que nous aurons probablement tous des modèles de langue entraînés pour nos domaines ou nos besoins. Deviendra très banal. Par contre pas connaissance d’agent conversationnel capables d’interagir avec plusieurs utilisateurs. Sans doute très intéressant de voir comment peut se comporter de manière raisonnable dans ce type de contexte.



## Séminaire. Prédire c’est comprendre : un modèle neuro-cognitif du langage fondé sur la prédiction

Séminaire, 2 février 2024 : Philippe Blache

- Laboratoire Parole et Langage (CNRS).
- ILCB Institute of language, communication and the brain

Aspects cognitifs liés à la compréhension. Inverser le point de vue de départ, plutôt que d’apprendre les langues aux machine. Se poser la question de ce que ces machines peuvent nous apprendre sur la langage et la compréhension.

Ne sait pas toujours très bien comment fonctionne entre les humains. Mais apprend de plus en plus.

Adopter un point de vue plus ouvert sur ce que les réseaux de neurones artificels peuvent nous apprendre sur le cerveau humain. Nombreuses recherche dans ce domaine.

Chomsky, NY Tmes EduKitchen 2023. Positions très radicales mais qui donne une perspective intéressante à étudier. Pour lui un logiciel de plagiat au sens où ce que tout ce que ces systèmes peuvent faire c’est produire le mot suivant à partir de ce qui a été appris. Il va plus loin, prétend que ne nous apprend strictement rien sur l’’esprit humain ou le fonctionnement général du langage car n’explique rien.

Controverse très intéressante. Pianadosi 2023 bat en brève son argumentation. Modern langague model refute CHomsky. Rien de comparable dans toute la théorie linguistique et jamais aussi puissante. Il va plus loin, pour lui des modèles explicatifs qui constituent une base théorique pour comprendr els structures et les relations statistiques.

Les positions

- les LLM capcables de prédire mais pas expliquer
- Les théories linguistiqeu sosnt capables d’expliquer mais pas de prédire

Rester prudent sur ce que peuvent nous apprendre. Mais quelques points intéressants.

Définir la compréhension dans une perspective cognitive

- capacité à transmettreéchanger des information. Compéréhension littérale qui s’appuie sur la capacité à interpréter et utiilser des informations explicites. Mais la compréhension s’appuie aussi sur des informations implicites qu’il faut intégrer à l’intérieur d’un meême modèle (compréhension inférentielle).

Décire la compréhension

- comment représenter le sens ?
- comment construire une représentation du sens en conversation ?
- comment utiliser cette représentation dans d’autres applications

Les méacnismes des LLMs et théories cogniftives sont différents.

La question de la représentation interne est absoluement déterminante. Qu’est-ce que met en entrée. Les LLM sont des embeddings. Il est donc fort peu probable que cette représentation ait une validité du point de vue cognitif. Peu probable que ces techniques soient celles du cerveau. Des techniques très particulières, assez simples qui vont faciliter l’utilisation de l’information. Représentation vectorielle extrêmement efficace.

Du point de vue de la cognition et de l’humain. Lorsque décrit la représentation des représentation internes probablement différentes.

- Repréeentation interne : utilise des catégories ou des features
- Mécanisme : principe de compositionnalité (Frege, 1923) généralement utilisé. Le sens du tout une composition du sens des parties. Convient donc d’identifier les parties, les agréger pour accéder à la représentation
- Alignement des représentations entre locuteurs (convergence).

cf. Pickering et Garrot? al 2021. Modèle de situation. Alignement des locuteurs, convergent pour parler de la même façon.

Grand nombre de travaux récents qui tentent de montrer les ressemblances entre Modèle de langue et comportement du cerveau. Nombreux travaux. Schrimf M. et al 2021. Modèle les plus efficaces aussi ceux qui prédisent le mieux l’activité cérébrale. Nombreux travaux dont de King et al qui vont encore plus loin. Essayent de voir si couche par couche correspond à ce qui se passe dans le cerveau. LLM et le cerveau organisés de manière hiérarchique. Le cerveau fonctionne de manière comparable aux LLM.

Donc peut être quelque chose à apprendre de ces modèles de langues. Qu’est-ce que cherche ?

Les points essentiels de la compréhension

- rôle central de al **prédiction** comment faire pour l’intéregre
- le contexte impliciete rôle essentiel : **activation** d’information (implicite)
- les interlocueturs convergent pendant une interaction : **alignement**

Suite de la présentation qui va voir comment répondre à ces questions.

La représentation du sens

une étape fondamental car sa représentation va induire le choix des mécanismes que nous utilisons pour construire le sens. De manère générale représentationd e l’information sémantqieu se fonde sur des entités en relation. Graphe de connaissance. Concept en relations avec concepts.

Ivan Sag 2012 SIgn BAsed construction grammar 

Identifier les unités de base que l’utilisons dans le langage. Signes : paires forme-sens. Important car association forme et sens. Chaque unité de base s’appuie sur une telle représentation des unités de base. Forme caractéristique qui peuvent être associées à un mot ou groupe de mot.

Une représentation assez simple, sens peut être décrit par des slots à leur tour mis en relations entre eux par des représenattion. 

À partir de ces représenattion, en sémantique formelle nombreuses approches qui formalisent le sens (logique de premier ordre ou calcul) Les nœuds du graphe sont des signes, les arcs du graphe sont les relations sémantiques entre les signes. Relations entre les différents rôles spécifiés dans ce prédicat, que va instancier avec des informations implicites fournies par le contexte. Relation référentielles.

L’idée est de traiter une unité de base et relations entre ces unités de base.

À côté de ces relations explicites, nous avons également toute une série de relations implicites. Lorsque nous utilisons ces informations, (Filmore avec sa Frame Sémantique qui décrit notion de scénario utilisée en représnetation des connaissances) utilisation mot pizzeria va activer relations implicites.

Toutes ces relations sont activées, cad rendues disponibles pendant la conversation. Cette notion d’activation au cœur de la compréhension. Chacune de ces interactions va pouvoir être quantifiée pour calculer un niveau d’activation. Dans la représentation des informations que nous utilisons, allons utiliser toute une série de relations de base. Niveau activation et catégories plus activées importantes car celles prioritairement utilisées dans une conversation.

Cette représentation extrêmement efficace en termes de traitement car permet de conrtôler les objets que va manipuler. Notion de réduction de l’espace de recherche. Beaucoup utilisé en information. Espaced e recherche et graphe de connaissance, certains nœuds du graphe peuvent être plus activés que d’autre en fonction du contexte. Limitation de la recherche aux nœuds les plus activés.

Réduction de l’espace de recherche lexical (mémoire à long terme). Bayas-JHiménez et al. 2021. Une des epxlication les plus importantes des phénomènes de facilitation. Comment parvient-on à traiter le langage en temps réel. 200ms pour accéder au lexique mental. 400ms pour accéder au sens. 600ms pour intégrer toutes ces informations. Mais si tout cela était vrai, il faudrait une seconde pour traiter un mot. Or parle beaucoup plus vite que ça.

La question de la prédiction. LLM très efficaces pour produire le mot suivant. Permettent de produire un ensemble d’information. Morpho-syntaxique, sémantique, etc. Permettent aller très loin. Parfois peu d’information quand peu de contexte, alors efficacité plus ou moins importante. Mais dans certains cas capables de produire des informations limitées.

Dans le cadre d’une conversation, les théories cognitives considère que peut prédire des informations de niveau inférieur ou aussi très complexe. Graphes de connaissance. Capable d’encoder des techniques similaires. Peut prédire des sous-graphes. Si compréhension du sens est un graphe, alors capables de prédire de manière efficace des blocs entiers d’information. Ce qui explique que pendant une conversation la compréhension mutuelle très efficace.

Martin Pickering 2018 explique que cette prédiction par prédiction du fait que les deux locuteurs font la même chose. Production du mot suivant. L’interlocuteur préfit la production du locuteur. Avec procesus inhibition qui fait que ne prédit pas. Or, l’observe au niveau cérébral. Alignement des activités cérébrales.

Ce que propose, c’est que ce que fait le locuteur prédire le mot suivant. Prédire plutôt un ensemble d’information qui va permettre de préparer l’information de ce qu’a dit le locuteur.

Au niveau cérébral : predictive coding. Nombreux travaux qui disent que ce que fait le cerveau, sans cesse prédire un prochain stimulus. Flux d’information hiérarchique : des inputs sensoriels (bas niveau) aux informations abstraites (haut niveau). Dans le cadre de la théorie prediction-by-prediction, alors pour le langage la même chose.

Stefanics, 2014.

Prédictions descendantes : cahque niveau prédit les réponses du niveau inférieur (feedback connection)s

Erreur de prédiction propagée dans les couches de réseau.

Capables de mesurer cette erreur de prédiction, grâce à l’Unification. Une opération capable de comparer deux structures complexes. Peut comparer structure représentée par matrice. Résultat substitution par la valeur correspondance.

Entre ce qui est prédit et produit, peut comparer structure complexe et unités complexes. Signes pour représenter le sens et qui ont une valeur prédictive.

De plus en plus de travaux dans le cadre des grammaires de construction (théorie linguistique) qui tend à montrer que ces grammaires existent dans le cerveau. Encodés par des assemblés de neurones (Pulver Muller ?). 

Lorsque les valeurs ne sont pas les mêmes, un échec d’unification. Mismatch alors peut relâcher cette contrainte.

MUC+ Un modèle neruo-cognitif  : Memory-Unification-Control

Trois composants du traitement du lanageg Peter Hagoart a proposé dans On Broca, brain and binding a new framework. Trois composants principaux : Memory, Unification, Control qui correspondent à des activités cérébrales particulière. 

Mémoire dit qu’en fait encode dans le lexique un très grand nombre d’informations. Pas un ensemble de mots mais unités de base objects complexes en mémoire à long terme. Dans notre approche les signes. Sans doute avec les Réseaux de neurones encode des unités de base très importantes.

Unification. Assemblage des structures. Un principes de base, mécanisme qui nous permet d’assembler ces objets complexes. Hagoart garde vision langage très modulaire et hiérarchique. Dans notre approche assemblage + calcul de l’erreur de prédiction. Lorsque l‘on est dans une conversation quelqu’un parle et mesure distance.

Contrôle. Des composants plus généraux pour contrôler ces approches. Dans notre approche activation.

Notre approche se situe dans ce modèle mais en se débarassant d’une approche trop hiérarchique du lanagge.

Schéma généarl du modèle. Graphe de représentation modèle du monde. Modèle de situation l’état de la représentation du monde au moment d’une conversation. Mécanisme de prédiction qui va permettre de prédire ce qui va se passer. Rôle différent pour le locuteur et l’interlocuterur. Mise à jour du modèle de situation en faisant passer dans les connaissances explicite le mot prononcé.

Composant 1 prédiction à partir du Modèle de Situation. Contexte formeé par l’enssemble des informations du Modèle de Situation. Deux types d’informations : explicites ou implicites. La prédiction retroune une liste de isgnes possibles : prédiction de signes de granularité variable, liste probabilisée.

Composant 2 : Extratcion du stimulus (à partir de l’input audio). APproche claissque décodage acoustico-phonétique + accès lexical. Segmentation en mots fondés sur les indices acoustiques. Prédiction fait que pas bvesoin d’aller au lexique. Comment fait pour segmenter. Indices prosodiques, inforamtions phonotactiques lorsque traite le signal, ne reconnaît pas le mots mais segmente en parties de mots. Segmentation en mots sans accès au lexique. Segmentation plutôt que reconnaissance de mot. La segmentation retourne une forme phonétique (sans autre information).

Composants 3: Vérification de la prédiction par unification. 

Composant 4

Composant 5 : Mise à jour du modèle de situation.

Conclusion apport du modèle MUC+

Organisations classiques du traiatement du langage. En général, représentations classiques du traitement du langage s’appuient sur une organisation hiérarchique du langage. Cf. Stanislas Dehanne ici.

Organisation parallèle. Proposée par Jackenof?

Dans notre approche une organisation séquentielle. Puisque capable d’encoder informations très riches. Alors mécanisme qui consite à agréger ces informations.

Cela repose sur un élément essentiel. Dans ce modèle là nous construisons une structure complexe. Pas de notion de catégorie, construit un objet dynamique qui sera associé à la représentation du sens. Alors capable d’intégrer au cœur du modèle la question de la prédiction. Pas de traitement différent. Mécanismes simples. 

Modèle qui permet d’expliquer différemment les phénomènes observés dans le cerveau.

La prédiction joue un rôle essentiel. Question de la prédiction dynamique. Remise en cause architecture classique du traitement du langage. Inscription dans prédiction by prédiction. 

Mesurer de manière possible les correlations. Pas de transformer dans le cerveau, mais des éléments de comparaisons

### Discussion

Quelle fonction humaine ne pourrait pas être expliquée de manière non bayesienne

Le cerveau un organe bayesien. Mais sans doute besoin de moins de données pour apprendre à parler. Neurones connectés de manières très nombreuse. Apprend à parler avec très peu de données pauvreté du stimulus. Alors que modèles besoin énormément de données.

Neurones artificiels vs neurones biologiques. Assemblée de neurones. 

Chaque couche produit représentation numérique. Est-ce que des travaux alignements.

Pour faire ces travaux essaye de faire présire couche à autres. Travaux compliqués risque aller trop loin dans interprétation et attribuer au modèle ceque cherches



Relation entre le sens et le langage. Approche connexionniste qui semble s’opposer à l’approche symbolique. Ici piste de réconciliation possible. Si LLM captent le sens comment y accéder ?

Si j’ai bien compris votre propos dans votre modèle en quelque sorte le graphe de connaissance se trouve encodé dans la langue. Suppose que la langue encode le sens. Mais alors comment tenir compte de cette capture du sens pour améliorer les modèles (compréhension).

Nécessaire interaction entre la connaissance du monde et le langage. Bien entendu pour comprendre le monde besoind es deux. Connaissance du modne qui dépasse largement le langage. Mais interaction entre les deux. Contexte exprimé par le langage et pas seulement d’ailleurs. Pour moi pas de diffiérence entre les approches stochastiques et symboliques. Peut toujours encoder information stochastique.

Représentation de la sémantique sous forme de graphes embeddings. Représentation par des images? Une sémantique de la représentation stockée dans l’image.

Question de la multi-modalité. On peut tout représenter sous forme de graphes. S’appuient sur même représentation. Alors possible de faire parler des sources de représentation hétérogènes. Le sens provient de sources hétérogènes comment dialoguer ces interactions.

Sans doute une question qui répond à la question de la pauvreté du stimulus. Modèle de langue ne voit que du texte alors que nous un être au monde qui leur donne une consistance.

Qu’est-ce que le langage ?

Relation entre langage et pensée. L’usage que l’on fait de la langue n’est pas neutre (en réalité). On ne sait pas si la langue sert à communiquer mais sait que la langue sert à penser ensemble (Claire Blanche-Benvéniste ?). On peut donc avoir des a priori, des biais, des stéréotypes encodés dans la langue. Mais ne pas surinterprété sur le fait que la pensée n’est pas encodée dans la langue. En fait encodée dans l’interaction. 





Sens et langage. Modèle probabiliste. Cardon revanche des neurones.

Planification

Aligned AI













## Linguistique computationnelle

Apprendre le langage aux machines

26 janvier 2024, 6/8

Les applications du TAL pas toutes de l’ordre de l’innovation technologique. Le TAL contribue à faire avancer des disciplines des sciences humaines et sociales. Par ex, les Humanités numériques, notamment l’histoire pour le traitement de documents. Mais aussi les sciences politiques, la linguistique et la littérature.

Deux illustrations par des travaux auxquels il a participé.

- morphologie quantitative et complexité linguistique
- étude computationnelle de la scriptométrie du français du XVIIe siècle.

### morphologie quantitative et complexité linguistique

Mesurer la complexité morphologique. Travaux menés avec Géraldine Walther, et une partie avec Guillaume Jacques (EPHE).

Morphologie flexionnelle est l’étude de la façon dont un même mot varie en fonction de propriétés morphosyntaxiques. Genre, nombre, cas, temps, mode, etc.

En morphologie flexionelle on observe que chq catégorie varie en fonctions de certaines propriétés qui lui sont propre. En français, les adj par genre et nombre. Paradigme adjectival.

En conjugaison, impératif n’exsite pas pour toutes les personnes. 

L’ensemble des formes flêchies d’un même mot constitu son paradigme flexionnel. On les traite sous forme de tableau

Corbett 2003, situation canonique, pour un paradigme chaque case remplie par exactement une forme. Considère que toutes différentes d’une case à l’autre (mais à l’écrit). D’un paradigme à l’autre les différences entre formes sont les mêmes (chaud, froid).

En pratique cette situation canonique n’arrive jamais. Il y a des écarts et ces écarts peuvent être de différentes natures. Beaucoup de façons de s’éloigner de la situation canonique. 

Premier exemple le syncrétisme : plusieurs cases remplies par une même forme. ex. une souris des souris. etc. Conjugaison de chanter.

Défectivité, cas où case du paradigme pas remplie. Des vivres, pas de singulier. Paître pas de passé simple. Échoir encore plus défectif. 

Surabondance. Dans une case pas une mais plusieurs formes.

Hétéroclise, quatrième phénomène que verra bientôt.

Notion de Description morphologique. Lorsque l’on fait de la morphologie formelle peut avoir envie de décrire le système.

Approche extensionnelle. Associe tous les mots du lexique à un lemme et ses formes fléchies avec leur catégorisation. Mais échoue à capturer des phénomènes simples comme le fait que la plupart des noms prennent un s au pluriel.

Approche intentionnelle. On associe chaque mot à un comportement morphologique = lexique morphologique intentionnel. Description de ces composants. Cf. lexique Leff Sagot 2010 (format XML)

Hétéroclise, un paradigme dit hétéroclitique utilise des parties de plusieurs classes flexionnelles. Exemple slovaque. Comportement flexionnel qui emprunte à différntes parties de différents paradigmes.

Pour représenter une telle situation. Trois manières de faire.

- on peut décrire trois classes flexionnelles standard, lexique simple mais grammaire longue
- conserver dans la grammaire trois classes flexionnelles mais avec un formalisme grammatical qui permet de lister ces directions.
- Deux classes et dans le lexique que créée entrée plus complexe pour dire comment se conjugue au singulier ou au pluriel.

Trois modélisations qui répartissent l’information de manière différente. Quelle est la meilleure de ces représentations ?

Une instance particulière de la complexité des langues du monde. Question ancienne, saillante notament dans l’études des langues créoles. Répartition complexité linguistique entre les différents niveaux. Soit langue dans son ensemble, soit analyse spécifique comme la morphologie, soit questions système.

Comment quantifier cette complexité pour comparer langues entre elles. Pour une même langue plusieurs descriptions possibles que peut comparer pour justifier la pertinence de concepts descriptifs ou de certains choix pour décrire un système morphologique.

Première idée, poser qeu plus grande complexité dès lors qu’attributs qui peuvent prendre plusieurs valeurs. Russe trois genre et nb de cas >aucun. Peut considérer que plus complexe. Mais si ajoute Swahili et Hongrois, situation comlexe grand nombre de genres en swahili, et gd nombre de cas en Hongrois.

Difficile à mettre en œuvre.

Compter le nb de case dans les paradigmes (conjugaison du fr par rapport anglais). Mais comment différentier les cases, etc. Alors que groupes...

Besoin de mesures plus solides de la complexité morphologique. Plusierus approches possibles. cf. Blevins 2006. Approches constructives ou abstractives. 

- constructive, cherche à comprendre comment chaque forme individuelle est construite
- abstractive, partes de l’ensemble des formes en regardant les rapports qu’ont entre elle.

Deux types de mesures de la complexité qui s’appuyent sur la théorie de l’information.

Description meilleure si plus compact.

Système morphologique est plus complexe si sa description la plus compacte possible est plus longue. Notion de longueur de description etc.

Formalisme morphologique PARSLI Whalter 2°11, 2013, 2017. Formalisation et implémentation AlexinaPARSLI Sagot & Walther 2013

Verbes du français Lefff (Sagot 2010). Compare 4 descriptions morphologiques.

Description verbe Khaling, langue à système verbal direct inverse. 

Analyse morphomique qui s’avère plus compacte que l’analyse lexicale.

Comparer des descriptions différentes et mieux comprendre le langage.

Mesure qui reste très rapprochée, dépend notamment du formalisme utilisépour encoder les descriptions.

Mais pas entièrement intéressant de partir d’une description formée par les linguistes.

Intéressant de partir des paradigmes eux-mêmes.

### Étude scriptométrique du français du XVIIe

Travaux qui s’appuie sur collaboration avec Rachel BAwden, Simon Gabay, Philippe Gambette

Français au XVIIe, français moderne « de la première modernité å BAdiou-Monferran 2011.

Dans l’imaginaire, siècle de référence. Pourtant graphies multiples. Convergence vers une orthographe qui donne lieu à des querelles importantes entre les tenants de graphies traditionnelles, et défenseurs orthographes plus moderne.

Graphies peu étudiées quantitativement. Comparer les textes entre eux. Mais les textes varient dans plusieurs dimensions. Pas que la graphie qui change au cours du temps. Variation graphique une seule. Style, genre, thématique, entités nommées.

Doit donc isoler la variation graphique au cours du temps pour l’étudier quantitativement.

Pour cela va utiliser des systèmes de normalisation automatique. Tâche qui consiste à transposer vers l’orthographe contemporaine. Élimination variation graphique.

- changements de convention graphique (s long)
- différences de segmentation (long temps)
- fausse étymologie (sçavoir)
- changements liguistiques (étoit)

Normalisation une tâhce de transformation de textes qui peut donner envie d’utiliser des stratégies de séquence à séquence. Meilleure prise en charge du contexte. La considérer comme une tâche de traduction. Prcohe simplification mais plus simple encore car pas de changement dans l’ordre des mots.

Deux questions de recherche

- est-ce qu’un modèle de normalisation auto est sensible à l’évolution temporelle de la variation graphque
- si oui, comment exploiter cela pour isoler et étudier au mieux la dimension temporelle de la variation graphique

Utilisé et comparé plusieurs système. Référence neuronal, séquence à séquence. Comparés à d’autres modèles. Se compare à ne rien faire. Systèmes par règle, et ABA où règles probabilisées, modèle de traduction automatique statistique (SMT) car caractère simple de la tâche.

Parfois normalisation peu vraisssemblable. Appui sur le lexique Lefff (grand lexique du français contemporain) pour faire un nettoyage a posteriori. = Posttraitement simple pour corriger les erreurs évidentes

Besoin corpus parallèle. FreEMnorm Gabay et Gambette 2022 pour l’entraînement.

FreEMmax grand corpus non parallèle.

Globalement ne rien faire 72% de performance et filtre lexique = gain significatif 86%

règle simple marche mieux. ABA encore mieux. SMT fonctionne le mieux. Transformer et TransformerHF. La vieille approche statistique fonctionne mieux. Bawden et al 2022

Pour les mots inconnus, amélioration firltre lexique plus significative.

Exemples de résultat.

Un modèle qui fonctionne bien et qui permet de normaliser automatiquement en graphie contemporaine un texte du XVIIe.

Mais notre idée de pouvoir étudier l’évolution de la graphie. Espérions que le modèle soit sensible aux évolutions graphiques au cours du temps. Pour le tester, a cherché à voir si le modèle reconnaît un texte selon sa décennie.

Est-ce que suffisamment de variation pour prédire décennie de rédaction ? Fonctione pas mal. 60 à 70 plus prédite mais s’explique en raison du fait que années pour lesquelles plus de données.

Mais comment savoir si le modèle prédit sur la graphie et non pas le cotenus des textes. Modèle de démoralisation. Alors arrive quand même sur la base du contenu contemporain mais moins bien. Ce qui signifie que le modèle de gauche s’appuyait aussi sur la graphie.

Maintenant que sait que modèles sensibles à l’évolution de la graphie, ne reste plus qu’à éliminer les variantes. Autre modèle de normalisation où la décennie en entrée. Pseudo-token et texte, prédit comment phrase aurait été écrite dans la décennie.

Appliqué grand nombre de texte. 

Cherche différences et les compte. Possible ensuite de représenter l‘évolution de la graphie dans les textes produits. Quantifie enfin certains types de changements. Observer quantitativement que 1670 une décennie clef. Vori aussi que normalisation qui ne s’est pas faite de manière monotone.

Phase transitoire.

En guise de conclusion. Deux séries de travaux qui illustrent la manière dont le TAL peut être utilisé en linguistique. Le cas en linguistique historique computationnelle. Lexicostatistique et glottochronologie plus très pertinent. Phylogénétique computationnelle. Outillage de la linguistique de terrain.

### Discussion

Rmq sur l’anachronisme modèles décennies produit. Txt 18e s décliné au 17e !

Complexité oral et écrit. Peut être pas les mêmes choses en terme de apprenabilité et déchiffrabilité. Apprenabilité dépend langue départ. Notion de complexité linguistique difficile à fonder de manière convaincainte. C’est la raison pour laquelle plusieurs mesures existent.

### Analyse automatoique de l’argumentation dans les débats politiques

Elena Cabrio, Université Côté Azur, IRIA

Si prend la définition argumentation wikipédia. Action de convaincre et pousser autre à agir. Argumentation cmposée d’une conclusion et d’un ou plusieurs éléments de preuves : prémices ou argument qui constitue raison approuvé cette opinion. Parfois seulement un fait... exhorter l’autre à agir.

Sans s’en apercevoir utilise beaucoup dans prise de décision quotidienne. PErmettent de sélectonner une ou plusieurs alternatives ou bien justifier un choix déjà adopté.

Depuis philo grecs, recherche critères.

Depuis les années 50 passé de la logique à ensemble interdisciplinaire.

Sujet interdisplinaire

- philosophie Aristotele, Toulmin 1958
- Psychologie McGuire 1960
- Linguistique van Eemeren et al 1996
- Intelligence Artificielle Loui 1987, Pollock 1987

Utilisation pour améliorer les prises de décision.

Exemple applications, domaine médiacel système d’aide au diagnostic argumenté. Domaine juridique décisions argumentées basées sur les lois. Plateformes de débat en ligne (idebate.org, debategraph, ProCon.org), systèmes en ligne de résolution des conflits.

Dans le cadre de l’argumentation computationnele, l’objectif est de concevoir des méthodes computationnelles pour extraire résumer ou générer des arguments provenants de différents contextes. Sachant que langue change en fonction.

Fournir des explications interactives du résultat du processus de délibération (pourquoi la machine a délibéré d’une certaine manière)

Prise en compte utilisateur (interaction interloc)

Depuis 1994 nouveau domaine de recherche né, fouille argument. Analyser le discours au niveau pragmatique et appliquer une théorie de l’argumentation spécifique pour modéliser et analyser automatiquement les données disponibles. 

Objectif fournir des données structurées pour les modèles informatiques d’argumentation.

Identifier quelle prémice soutient ou attaque une décision.

Pour y parvenir besoin de grandes ressources de textes en langues naturelles. Arguments générés par les utilisateurs sur les blogs. Utilisation du TAL.

Fouille d’arguments (Argument mining)

Prend en entrée un texte argumentait.

Première phase où va récupérer les composants des arguments, prémisses, conclusions

Puis prédiction des relations (support, attaque)

Parvient texte annoté.

Pour aborder la tâche de détection des arguments. Une approche en pipeline. Première étape, d’identifier si texte argumentait. Puis procède avec classification du composant (prémisses ou conclusion, texte non argumentatif)

Classification mot par mot en prédisant si une prémisse conclusion ou texte argumentatif. Différentier prédiction relation au niveau général ou argument.

Première tâche qui consiste en la détection des relations générales. Relations entre arguments. Relations entre composants du même argument. Prédire si relation de support ou d’attaque.

Exemple

De plus en plus des études qui visent à aborder des tâches annexes. Evaluation des différentes théories d’annotation des argument, exploration des relations avec les annotations linguistiques et discursives. L’intégration du sens commun et de la connaissance du domaine dans les modèles d’argumenattions. Recherche argument sur le web, résumé opinions, détection désingformation. Evaluation de la qualité des arguments. Génération argumentation valable.

Analyse argumentation politique, étroitement associée à l’éthique. Campagnes présidentielles. Beaucoup utilisés pour étudier les structures et les stratégies du discours politiques. Relève le défi d’automatiser cette argumentation en réalisant pipeline complexe. But être capable d’extraire automatiquement les argumentaires pour les analyser, les comprendre ou les confronter aux stratégies des autres politiciens.

Plusieurs tentatives pour analyse discour spolitique. Angleterre, Canada, etc. 

Souvent des structures argumentaires complexes. Implique de d’abord pouvoir récupérer les différentes structures internes d’un argument. La structure argumentaire pouvant être complexe. Par ailleurs, interlocutions et références entre les deux candidats.

Pour l’annotation trois experts en AM pour la définition des lignes directrices pour l’annotation. Trois autres annotateurs pour effectuer la tâche d’annotation. Souvent lignes directrices assez simples pour entraîner la machine.

Chaque transcription annotée indépendamment par au moins deux annotateurs (**outil d’annotation Brat**) https://brat.nlplab.org

Évalutation des données annotées

- accord entre els annotateurs. varie selon les cas. 1 an de travail pour mettre au point un jeu de données consistant.
- 17 000 conclusions, 15 000 prémices, 20 000 relations de support, 3800 attaques

Souvent les politiciens beaucoup de prémisses, Attaques conclusions des autres. Plus de supports.

Voit que le même candidat se soutien beaucoup et que les attaques plus fréquentes entre candidats.

Pour exécuter doit conserver des données pour l’apprentissage, puis une étape de validation. Enfin jeu de données 10 ou 20% pour évaluer le système.

Tâche de détection et de classification des composants. Étant donné d’une phrase d’un candidat, doit savoir si texte qui fait partie d’une prémisse ou conclusion ou non argumentatif. Utilisation de RN en utilisant différents modèels de langages.  Approches qui s’appuient sur les transformers.

Plusieurs étapes. Classification binaire, puis distinction premisse ou conclusion.

80% cas parvient à détecter. BERT

Puis doit produire les relations, reconnaître leur structure pour comprendre si supportent ou attaque autre argument. Comme souvent des textes très longs, du mal à retrouver des relations qui se retrouvent loin dans le texte. Comme souvent des questions posées au candidat et réponse, va chercher les relations entre les arguments situés entre deux questions de l’animateur.

Utilisation de RNN, le modèle qui obtient le plus de résultat basé sur les transformers, RoBERTa stratégie de masquage. WordPiece. 61%. 

Pour le moment seulement parlé de l’extraction des composantes argumentaires et de leur structure. Mais se pose dans cette matière la question de l’évaluation de la qualité de l’argument.

L’affirmation est-elle claire, prémisses suffisantes pour dire qu’une bonne argumentation, efficace pour persuader ? raisons valides, etc. Argumenté de manière raisonnable.

Important de pouvoir évaluer la qualité, cherche à trouver les meilleurs arguments.

Étude des arguments fallacieux. Peut-on dire quand un argument a une qualité médiocre. Sophisme qui est une argumentation destinée à tromper autrui, et le parlogisme (Kant)

- Confusion entre corrélation et causalité « Cum hoc ergo propter hoc »
- Attaque *ad hominem* (general ad hominem, tu quoique ad hominem, bias ad hominem, name-calling-labelling)
- Appel à l’émotion *argumentum ad passiones* (appeal to pity, appeal to fear, etc.)
- appel à l’autorité
- pente savonneuse
- slogan

Gros travail d’annotation. Même stratégie. Échantillon pour calculer les accords entre annotateurs. Outil INCEpTION https://inception-project.github.io

Tâche extratcion information, identification et classification. Inclusion du contexte avant et après. Motéhodes basées sur les tranformeurs 

- BERT + (Bi)LSTM(s-)
- BertForTokenClassiciation
- Hebert...
- ..

Calcul des poids pour chaque caractéristiques en s’appuyant sur les composantes et les parties du discours. Modèle MultiFusion BERT que propose comme amélioration de BErtFTC. Atteint 73% reco. Résultats pas distribués équitablement.

Matrice de confusion qui montre que du mal à reconnaître certins arguments fallacieux. Others. Cas spécifiques appels à émotion et false clause.

DispuTOOL système qu’a développé. https://www.inria.fr/fr/disputool-ia-analyse-arguments-debats-politiques https://disputool.uni.lu

Visualisation des segments. Filtres pour identifier les thématiques discutées dans les débats politiques. Possible de croiser les années et les candidats. Nuage de mots, bubble, etc. prévalence des thématiques abordées.

Stratégies de discussion politique qui a changé au cours des annés. 

Possible ajouter ses propres documents pour une analyse à la volée par le système.

Nombreux défis encore. Par exemple beaucoup d’implicites dans le discours politique. Par ailleurs perd certains éléments comme les indices visuels, le ton donné qui sont importants.

Projet européen ORBIS qui permettra de continuer dans cette voie en s’orientant vers la eDemocratie. Utilsiation algorithmes pour fouiller dans les discussions des citoyens pour que les politologues puissent prendre décisions informées.

Autre scénario possibles. Analyse automatique de l’argumentation dans le domaine médical. Langage technique, argumentation plus explicite et plus clair. Mais possible appliquer les mêmes techniques d’extraction d’argument et de structures argumentaires pur fournir aux médecins des informations dont pourraient avoir beosin pour fonder décision.

Possibilité de proposer explication. Projet ANTIDOTE. Pas se substituer au médecin mais générer Quizz pour jeunes médecins.

### Conclusion

Argumentation computationnelle

Présentation de trois contributions scientifique.

Fournir une analyse approfondie du discours politique par le biais d’approches automatiques destinés à différents types de publics.

Plusieurs tâches annexes. 

Equipe qui travaille sur l’intégration du sens commun dans ce modèle. Évaluation de la qualité des arguments. Génération automatique des contre arguments. Concevoir des technologies de débat.

### Discussion

Quel rapport avec Cybernétique





Variation entre les locuteurs, changements selon les campagnes.

Formalisme logique. Quid du fonds.











## Traduction automatique

12 janvier 2023, 4/8

Introduction en une heure à la traduction automatique ce qui est une gageure.

Quelques enjeux en traduction automatique et définition de la tâche.

Une tâche qui consiste à chercher automatiquement une phrase x dans une langue source e vers une phrase y dans une langue cible f.

En produisant une traduction conforme à f

en préservant aussi bien que possible le contenu informationnel de x

Tâche a priori simple, mais en réalité complexe. Pb traduction littérale vs adaptation. Préservation du style, des erreurs ?, etc.

Cette tâche vient avec un certain nombre de difficultés.  

- Diversité linguistique qui pose problème notamment lorsque la morphologie des langues est différentes. 
- On est également confronté aux ambiguïtés inhérentes à la langue source. 
- Ambiguïté lexicales ou syntaxiques. ex. 
- La variation linguisitique à l’intérieur d’une même langue constitue une autre difficulté. Genre, style. 
- Problématique des mots inconnus. 
- Scénarios peu dotés (langues, variétés, genres, etc.) mais au delà, domaine et genres peu dotés.

Un deuxième niveau de difficulté, la TA au-delà de la phrase. 

- Rôle du contexte linguistique dans la langue source et ou la langue cible. Savoir prendre en compte le contexte aide.
- Les éléments anaphoriques. Selon première traduction, besoin adapter traduction
- Cohésion lexicale. 
- Marques de politesse (varie selon les langues)
- Accord avec le genre du locuteur

Ensemble de difficultés qui rendent compliqué la constructuion de systèmes de traduction automatique mais aussi l’évaluation de tels systèmes.

Pour l’évaluation, deux types d’approche.

- évaluation humaine. Plusieurs méthodes mais couteuses et peu reproductibles. évaluation par notation ou par ordonnancement, évaluation par post-edition.
- évaluation automatiques. Problème général, sont peu robustes, face à aux reformulations. Plusieurs approches traductions de références, BLEU, METEOR, chef, COMET. Tout un champ de recherche = plusieurs métriques, et nécessite de pouvoir disposer de traduction de référence. sans traduction de référence (« quality » estimation) COMET-QE

Métriques d’évaluation, domaine de recherche très actif. Chaque année WWT Conference on Machine Translation. Organise concours sur des shared tasks. BLEU, COMET, CometKiwi

BLEU (Papineni et al. 2002), la métrique la plus utilisée depuis longtemps. S’appuie sur le nombre de n-gramm commun. Pénalité de longueur pour calcul d’un score. Défauts pour reformulation. 2023, scores mauvais mais toujours très utilisé. Dérivé pour niveau phrases sentenceBLEU, chrF qui opère au niveau des caractère individuel avec résultats similaires.

COMET (Rei et al. 2020, 2022). Se comporte bien mieux. Une méthode apprise. Un réseau de neurone entraîné à scorer des traductions automatiques comme si était un humain. Nécessite des données d’apprentissages pas toujours disponibles selon les langues. Plus gourmand en calcul, et des scores plus difficiles à évaluer que BLEU. Reste une métrique avec référence, où compare représentation sous forme de vecteur de la phrases source et cible. Autre dérivé CometKiwi, où plus besoin de score de référence.

Q embeddings pourquoi pas comparaison de vecteurs directement ss recours aux RN

Corpus parallèles

Un corpus de texte fourni dans plusieurs langues. Exemple paradigmatique, la pierre de Rosette. Dans ce contexte, par défaut toujours une langue source et une langue cible. Toujours des corpus produits par les humains. Se pose très vite la problématique de la qualité de ces corpus parallèle. D’autant plus important quand les utilise pour entraîner dans le contexte de tâches de traduction automatique.

On tt d’abord fait flores des corpus institututionnels ou pays bi-lingues. Europarl (22 langues, 1 à 90M de mots, 759M de mots au total). MultiUN. Corpus de sous-titres OpenSubtitles 1782 paires de langues 62 langues, 22G de mots au total. Corpus récoltés sur internet : ParaCrawl, CCMatrix, NLLB (1600 paires de langues, 148 langues...). Souvent de moins bonnes qualités mais encore plus gros.

Il faut donc de très grandes quantités de phrases. Pour tous les domaines sous-dotés, donc besoin de techniques particulières très utilisées.

Augmentation de données (« data augmentation »). Idée générale : créer des données supplémentairesà partir des données existantes. Replacer certains mots par des mots grammaticalement et ou sémantiquement similaires (Fadaee et al. 2017). Ou utiliser des systèmes de paraphrases (Marton et al. 2009 ; Xu et al. 2020).

Cela ajoute du bruit dans les données. Mais améliore toutefois les systèmes de traduction automatique tout en améliorant leur robustesse (Lample et al. 2017 ; Li & Spécialiste 2019, 2020). Silver data qui servent à entrâiner un modèle.

Technique de rétrotraduction (« Backtranslation »). Utilisation de données monolingues pour créer des données parallèles suppléméentaires par rétrotradcution, y compris pour mieux couvrir d’autres domaines (Bertoldi & Federico 2009 ; Bojar & Tamchyna 2011 ; Sennrich et al. 2016). On entraine un premier modèle dans la direction inverse. Traduit un corpus monolingue, on utilise les traduction pour entraîner un modèle souhaité. On peut itérer cette procédure plusieurs fois : backtranslation itérative Hoang et al. 2018.

Deux techniques qui fonctionnent bien, notamment la traduction arrière, pour palier le caractère limité des données parallèles.

Question d’alignement

Voir menu restaurant chinois. Mais peut observer, même sans connaître le chinois correspondance entre idéogramme et soupe, œuf, etc. Peut alors produire une proposition de traduction simplement basée sur la régularité. Capacité à faire de la traduction sans comprendre, parceque l’on est parvenu à identifier des correspondaces. Ces correspondances sont des alignements.

De nombreux systèmes de TA s’appuiens sur l’alignement au niveau des mots. Soit explicitement, soit implicitement via un mécanisme d’attention (production latente par les systèmes).

L’alignement n’est pas forcément toujours de un mot à un mot. Parfois pas de correspondance pour un mot. Parfois plusierus mots pour un ou un groupe.

### Traduction automatique

Traduction automatique par règle. Au départ, reste encore parfois pertinents dans le cas de corpus très limités. Approche standard jusqu’aux années 1980, utilisées jusqu’à la fin des années 2000. S’appuient sur une représentation abstraite qui est le triangle de Vaucquois proposé en 1968.

Analyse par exemple syntaxique pour transférer puis générer une phrase. Analyse pouvant monter jusqu’à une analyse sémantique avant de le transférer puis générer la traduction dans la langue cible. Voire passer par une interlingua.

Certains systèmes fonctionnent encore par règles. Aparetium.

Approche rapidement remplacée par des approches statistiques. L’idée de base que chercher probabilité. Décompose probabilité en deux. D’une part une part probabilité du modèle de traduction x Modèle de langue [37’ à revoir].

Se retrouve alors avec la tâche qui consiste à déterminer quelle est la meilleure manière de décomposer la phrase source de manière à avoir le plus d’alignement possible. Le calcul de P(x|y) se fait désormais en calculant la probabilité d’un chemin dans les traductions de phrases possibles. cf. Koehn 2006

L’état de l’art, jusqu'en 2015. Mais remplacé dans la quasi totalité des scénarios par la traduction neuronale.

S’appuie classiquement sur une architecture séquence à séquence. Abandonne reformulation bayésienne de la tâche de TA, et revient à argmax y (P y | x).

RNN séq-à-séq de base. d’abord récurents. LSTM encodeurs dans cet exemple. Dernier vecteur donné à une partie décodeur qui de proche en proche va générer les mots de la traduction. Exactement comme un modèle de langue séq à séq.

Modèles qui peuvent être améliorés en remplaçant ... par un mécanimse d’attention pour qu’à chaque étape d’encodeur une étape du décodeur dépend de l’étape précédente du décodeur. Se retrouve alors avec un schéma complexe qui ressemble beaucoup à une notion d’alignement. C’est en ce sens que disait que les systèmes neuronaux, s’appuient de manière latente sur des systèmes d’alignement.

TA neuronale dépasse la TA statistique 2016 (google). 

2017 arrive architecture Transformer Vaswani et al. 2017. Leur arrivée a permis de dépasser les systèmes précédents, y compris récurrents. Permis également d’utiliser des modèles de langues préentrainer. Exemple BERT, rapidement s’est retrouvé avec des modèles séq à séq BART et T5. Alors apprendre un modèle de langue automatique, revient à affiner.

Fonctionne bien et de manière complémentaire avec la notion des backtraducteurs. Plus fait de la traduction arrière, améliore les résultats et de manière complémentaire

46’

2016 Google publie un modèle un peu nouveau. Johnson et al. 2016. Modèle fortement multilingue. Idée que pouvait apprendre à un système capable de traduire de nlangues vers langues. Cf. GoogleAI Blog nov 2016

Une autre façon d’améliorer ces systèmes pour des langues peu dotées. L’apprentissage par transfert. Avoir appris à traduire pour une langue proche, aide le traducteur. Mais pour les modèles langues, même si préentrainement avec langues sans ressemblance du tout, aide quand même mais ne sait pas pourquoi. On pense que c’est en raison de généralités structurales entre les langues qui parviennent à être utiles.

### La TA est-elle désormais un problème résolu ?

La réponse est évidemment non !

Exemples : « Bouchon sur le périphérique » dans google... GPT4 pas très bon

Des biais de genre. Le Malais n’indique pas nécessairement le genre du Malais. Choix discutables selon profession.

Exemple interdépendance. GPT4 s’en sort mieux.

Complexité syntaxique. Article BBC Tin can bear ‘serves as litter warning’ --> google translate rien compris. GPT4 est créatif !

Variation linguistique. Twitt anglais. Suggère correction orthographe. Google OK, GPT4 s’en sort très bien (robuste au bruit de manière générale).

Langues moins dotées. Mongol.

Robustesse à la variation graphique.

Cependant les progrès réalisés ces dernières années sont impressionnant. En donnant un texte dans des langues bien dotées, fonctionne très bien.

Revient de très loin. En 2018, publication twitt 15 000 œufs au lieu de 1500... mal recopier les chiffres. Ou encore exemples de restaurants chinois. Chicken vs real chicken.

« Translate server error » exemple célèbre. Pas une bonne traduction de restaurant ! Mais des erreurs d’utilisation humaine. Mais problème existant pour les utilisateurs de traduction humaine.

Koehn 2017, de gros progrès. Effet de mode qui exagère parfois l’intensité des progrès réalisés. Mais un des domaines du traitement automatique des langues les plus utiles, et les plus utilisés qui a permis de faire le plus de progrès.

### Discussion

Est-on capable d’utiliser de tels systèmes pour analyser les langues dans une approche comparatiste. Par exemple pour généraliser des analyses structurelles. S’appuient sur une représentation abstraite qui est le triangle de Vaucquois proposé en 1968.

On peut utiliser ces systèmes dans plusieurs situations. Cours sur la linguistique computationnelle qui étudie manière dont l’orthographe a évolué. Réconciliation des deux mondes. Un sujet plus difficile qu’il n’y paraît. Se dit que l’on devrait. Aimerait bien que ce que faisait précédement et qui était intéressant fonctionne. Beaucoup plus difficile que l’on voudrait, et difficile de le rendre utile. Sûrement possible, mais difficile de trouver comment.

## Séminaire, François Yvon (Isir, MLiA), Traduction neuronale massivement multilingue

Exemple du corpus de la Bible, celui pour lequel dispose du plus d’exemple.

ex. Bible polyglotte

- Besoins d’algorithmes. 
- Des implémentations et des machines. Exemple machine Jean Zay du Genci opérée par le CNRS à Orsay.
- Des méthodes d’évaluation, humaines ou automatiques.

Encodage, décodage, boucle d’apprentissage. Question monolingue tâche considérée assez simple même si présente des difficultés.

Traduction multilingue plus complexe. Traduction bilingue, f la langue origine, 

En entrée du transformer présente un couple de phrase. Va encoder cette phrase en une représentation numérique. Matrice de valeurs. Autre manière de rreprésenter un vecteur par mot qui permettent de déduire un vecteur pour toute la phrase.

L’encodeur calcule des représentations matricielles. En manipulant la matrice qui vient de l’encodeur avec un préfixe, en déduit une nouvelle matrice de chiffres. 

On utilise alors ce vecteur pour faire une prédiction. Quel est le mot qui peut suivre. À partir de la comparaison, va mettre à jour les paramètres du systèmes. Puis mise à jour et continue.

Tout au long du traitement de la phrase cible, la matrice de départ ne change pas. Le reste sera mise à jour au fur et à mesure. Car ) chaque fois change le préfixe pour la traduction. D’emblée a la phrase source, puis mot après mot va chercher.

Des millions de phrases parallèles et des milliards de mots que manipule.

Les systèmes de traduction ne manipulent pas des mots, mais des unités plus petites que des mots. Première étape interne qui consiste à redécomposer la phrase en plus petites unités. Des inventaires d’unités qui sont femrés (typiquement 50 000, 100 000) : jeu d’unités que peut recomposer. Traduction qui parfois se fait d’un mot vers un mots, mais parfois, lettres à lettres. Système qui est malgré tout capable de traduire, simplement décomposition qui implique décomposition plus importante que pour les mots fréquents.

La traduction bilingue. Un texte que va passer dans un encodeur, décodeur qui fait une traduction. Que va comparer à la traduction de référence. Mettre à jour les paramètres et le faire plusieurs fois. Manière de procéder qui a permis des progrès rapides entre 2015 et 2018, gain de 8 points BLEU en 3 ans. Mais gain d’usage très important. Pour de nombreuses paires de langues gain d’utilisabilité.

Comme fonctionnait bien pour la traduction bilingue a cherché à le faire vers plus de langues. Deepl 30 langues soit 900 paires. Google translate encore plus étendu. Mais même avec 100 langues couverture très limitée. Estimations autour de 7168 langues estimées. Aimerait aller beaucoup plus loin, sachant que nombre de système au carré.

Pas toutes à traduires car inégalement représentées. Des langues avec de très nombreux locuteurs. Moitié des langues considérées comme en danger. Cependant 4000 resteraient.

Si reste dans le détail de ces langues. Joshi et al, ACL 2020 état des lieux sur ce que sait faire. Construction d’une classification dans laquelle ils ont analysés pour chaque langue le nombre de corpus annotés disponibles. Et regardés le nb de mots dans wikipedia. Permet d’identifier 5 groupes. 5 langues qui sont les mieux dotées. Même là nb langues pas présentes. 2000 langues pour lesquelles n’a rien. Tout de même des langues pour lesquelles dispose d’éléments suffisants pour produire des systèmes de TA.

Parfois des langues peu dotées mais nombreux locuteurs.

Langues peu dotées pas nécessairement... (usages sociaux réservés, langues familiales et types d’interaction sociale). Se souvenir que parfois usages spécifiques. Par exemple sans doute trivial d’envisager de faire de la traduction de certains types de textes scientifiques. Par ailleurs, grand nombre de langues qui ne disposent pas de système d’écriture ou bien très variable, instable ou limité. Ce qui nous dit les limites des méthodes et système que va présenter par la suite.

Traduction automatique rend de plus en plus de servcie. Mais demande des ressources massives (données, calcul). Savoir si peut étendre les béfinaires dans un contexe ou moins de données, mais à un coût raisonnable (nb de langues, risque de devoir maintenenir 40 000 paires de langues pour passer à l’échelle).

Une des solutions, la traduction multilingue. Première étape se souvenir que les systèmes de traduction ne manipulent pas des mots mais des unités plus petites que des mots. Ce que va chercher à observer ce sont ces unités plus petites. Exemple déclaration des droits humains dans segmenteur. Des unités parfois partagées entre les langues. Une méthode qui par ailleurs fonctionne même avec des alphabets différents.

Traduction anglais-centrique, une première solution. Système de tout sauf l’anglais vers l’anglais. Travail plus compliqué pour l’encodeur car doit encoder toutes les langues. Décodeur qui doit savoir quoi produire. Assymétrie entre ce que fait l’encodeur et ce que fait le décodeur. 

Ici systèmes qui travaillent sur le modèle du pivot. Alors peut traduire d’une langue à l’autre. Longtemps utilisée par Google pour faire de la traduction de langue à langue. Sans le dire. Exemple publié par Kaplan. Fonctionne encore. Il pleut des cordes --> il pleut des chats et des chiens en Esperanto

Le détour par l’anglais est un double encodage. La question est de savoir si peut s’en passer. Possible de passer de n’importe quelle langue à n’importe quelle langue.

Une première possibilité de le faire, en gardant toutes les versions anglaises. Pivoter sans pivot. Une méthode qui a montré ses forces et qui permet de faire de la traduction sans exemple. Possible de traduire de l’Allemand en chinois, sans corpus parallèle !

On a dans les systèmes que l’on manipule des encodeurs. Qui prennent n’importe quelle langue dont construit une représentation matricielle. Observe que des phrases parallèles à la sortie de l’encodeur donnent des vecteurs relativement proches. Signifie que n’importe quelle phrase en entrée pourrait être traduit car phrases ressembles. Le travail de l’encodeur consiste à rapprocher des phrases parallèles. Le rôle du décodeur générer des phrases de manière monolingues. L’encodeur tend donc à rassembler les langues pour des représentations les plus homogènes possibles. Le décodeur génère seulement dans une langue.

Passage à l’échelle, 100 langues à 1000. Plusieurs ordres de grandeur sur les données disponibles. Si met tout ensemble, devrait certainement avoir un impact. En fonction du nombre de ressources utilisées par le système, le traitement n’est pas identifqieu.

Arivazaghan et al 2020. Montre que plus facile de générer dans une langue souvent vue. Scores absolus différents. Et plus rajoute de langue dans le système, plus les performances s’améliorent.

Implémentations efficaces de la recherche de voisins. Peut travailler sur les phrases plutôt que les mots. Alors peut identifier des phrases parallèles en passant par autre langue. Boucles vertueuses. Les traductions et leurs usages effectifs (observe que peu de traduction d’un ensemble de langues vers les autres, proximités ou pas). Si cherche donc des phrases parallèles dans certaines familles plus de chance d’en trouver. Peut donc organiser la recherche de phrases parallèle en fonction de l’historique de traduction. Utilise langue bien dotée pour servir de ponts. Augmente considérablement la quantité de ressources utilisables. Fan et al. 2020.

Rétro-traduction et production de données artificielles. Améliorations significatives mais partait de très loin. Un impact problématique sur la moyenne. Comment faire de l’évaluation des technologies multilingues problématique car toute une série de facteurs qui entrent en jeu. Aspects non réellement commensurables.

Des systèmes de traduction multilingues qui ne servent pas nécessairement à des humains mais pour des robots. Exemple si systèmes d’analyse d’opinion en anglais. Si considère que l’opinion se traduit, peut le faire sur l’ensemble des langues. Exemple annotation twitt haineux. Une approche généralisable aussi pour la production de résumés. 

Effectivité de la traduction multilingue. Résoud le problème de déploiement et d’implémentation. Là où avait besoin de plusieurs systèmes en faut plus qu’un. Semble permettre accroissement sans limite. Perte de performances moindres, démultiplie aussi les possibilités de traiteemnt multilingue.

Peut-on augmenter le nombre de bénéficiaires sans corpus parallèles ? 

Oui, utilisation système encodeur / décodeur en faisant du débruitage. Peut aussi le faire en mélangeant plein de textes de langues différentes. On ne sait pas pourquoi l’encodeur même si pas de texte parallèle, capable d’aligner les représentations parallèles, sans doute car fait de la compréhension. 

Si utilise processus de masquage et démasquage (avoir seulement un encodeur). Alors alignement entre des phrases parallèles, spontané.

Si des spams en anglais peut les passer dans cet encodeur, construction des vecteurs et apprendre à les séparer permet de dessiner frontière. Texte en français dans le même encodeur peut tout de suite dire si spamms ou pas. Pourtant aucun texte parallèle ni aucune traduction. Le transfert du modè!le anglais opère au niveau des représentations. Traduire n’est plus nécessaire.

Représentations multilingues qui rapprochent aussi des équivalents lexicaux dans des phrases parallèles. Des alignements de très bonne qualité. Permet la construction automatique de dictionnaires bilingues, etc. Or, réalisés sans aucune données parallèles.

Décodeur multilingue simple

Sont des traducteurs « sans exemples ». Dès lors que s’en est aperçu. Si donne 0 exemple, ne fonctionne pas très bien. Avec ensemble exemple choisi améliore. Si Finetune avec modèles parallèles = état de l’art.

Nouvel état de l’art, concentre l’essentiel des efforts de recherche. Car une vertue dans le modèle industriel à avoir un seul modèle qui fasse tout. Une architecture qui progresse beaucoup et est très étudiée même si obtient des systèmes multilingues qui restent moins bons que des systèmes bilingues optimisés surtout quand on a beaucoup de données.

difficultés que poseraient ces systèmes non plus pour 1000 langues mais 4000.  

De nouveaux fronts, de nouveaux dialogues.

Reprises pyramide de Vauqois. Empilement des langues dans le modèle de langue. Possibilité de créer une sorte d’interlangua.

Possibilité aussi de savoir comment optimiser avec représentations multiples.

Essayé de montrer pourquoi traduction multilingue a attiré des efforts. Non seulement efficacité pratique mais aussi découvertes excitantes. Suppression de toute la connaissance linguistique. Ne traduit pas des mots, série de caractères. Est-ce que cette voie améliorera traduction bilingue pour traduction plus pointue, probablement pas.

### Discussion

Avec ces connaissances pourrait-on produire une langue facile ?

Historique de langues artificielles qui ont toutes échouées. Les langues existent car des fonctions sociales pour communiquer. Pense plus que ces systèmes vont plutôt simplifier communication entre locuteurs différents.

Il y a-t-il des travaux qui permettent de traiter les variations culturelles de la langue ?

GlotLID

Corpus de français québécois. Passage de 100 à 500 langues alors devient difficile de déterminer dans quelle langue écrite à l’origine. 

Identification automatique de langues, très difficile. Chinois / Mandarin à l’écriture ne fonctionne pas beaucoup. Lié au système d’écriture.

Ensemble de systèmes présentés, auto-régressifs. Ceux qui prédisent un mot après un autre, font très peu d’erreurs.









[MLiA Machine learning IA Deep Learning of information Access](https://www.isir.upmc.fr/teams/mlia/?lang=en)











## Représenter les unités textuelles

> Les niveaux d’analyse linguistique. Phrases et mots. La loi de Zipf. Quelles représentations pour les mots (voire les phrases), quelles propriétés pour ces représentations ? Les mots (lexiques, lemmes), leurs représentations sous forme de structures de traits puis de vecteurs (*embeddings*). Illustration sur la tâche de détection d’entités nommées.

### Cours

Le TAL a pour objet le traitement des données textuelles, la linguisitique est la science de ces données. Cela a conduit ces deux pratiques à dialoguer. Leur rapport a évolué au fil du temps. Approches symboliques : formalisation, description §grammaires, lexiques). Approches par apprentissage : annotation linguistique dans les coprus.

Tous les domaines faisant usage de l’apprentissage automatique bénéficient d’une meilleur compréhension des données traitées. En disposant d’un vocabulaire commun, pour permettre de mieux anticiper et comprendre des difficultés. Les données...

### Trois domaines de la linguisitique importants pour le TAL.

Morphologie, le domaine qui étudie la manière dont les mots se construisent. Morphologie flexionnelle qui décrit ces changements. Lemme (classe d’équivalence de toutes ces formes conjuguées ou formes fléchies. Entretiennent entre elles des relations qui sont les mêmes qu’un autre lemme : classe flexionnelle. Traits morphologiques/morphosyntaxiques).

Morphologie dérivationnelle. Ex. Brav-itude, skype+er

La morphologie manipule des notions comme morphèmes, et les morphes (identifie des segments qui font sens à l’intérieur des mots).

Syntaxe, comment les mots s’organisent en phrases grammaticalement correctes. les analyses en constituant et les analyses en dépendances. Souvent sous la forme d’arbres. Constituants structurent la phrase de manière hiérarchique, là où un arbre de dépendances relie chaque mot aux mots qui les gouverne, ou auquel il se rattache.

Représentations partiellement équivalentes.

Sémantique, troisième niveau d’analyse linguistique. S’intéresse à la manière dont les mots et les phrases expriment un sens. Pragmatique, influence signification des énoncés.

### Traiter des données textuelles

Un texte n’est rien d’autre qu’une séquence de caractères. Lettres, sillabogrammes, mais aussi signes de séparations ou séparateurs.

TAL s’appuient le plus souvent sur une double séparation de ces séquences de caractères. Séquences macroscopiques et microscopiques : phrases et mots. Pose la question de savoir comment les définir les identifier dans des textes bruts. Exemple scripta continua. Comment représenter ces mots pour faire l’analyse.

Qu’est-ce qu’une phrase ? La sortie d’une séquence d’analyse macroscopique. Peut se dire que syntaxiquement correcte. Sémantique. Marquée typographiquement (mais insuffisant, points et majuscules pas toujours frontière de phrases). 

Exemples limites. Phrase alors que ponctuation. Points surchargés. Cas litigieux. Notion de phrase mal définie. Il faudra donc se doter d’une notion de phrase conventionnelle et pleine d’approximation.

Qu’est-ce qu’un mot ? On peut distinguer plusieurs notions de mots qui se superposent plus ou moins. Mots typographiques, morphosyntaxiques ou sémantiques.

Mot typographique, longtemps appelé token. Notion conventionnelle mais déterministe, reproductible de la notion de mot. On observer que de nombreux systèmes d’écriture utilisent des séparteurs. Peut s’appuyer sur elle pour avancer notion de token.

- Une séquene de caractères ne contenant ni séparateur ni signe de ponctuation
- ou un signe de onctuation §par exmeple, tout ce qui n’est ni caractère ni chiffre).

Système d’écriture qui ne dispose pas de ce système de séparateur. Alors caractère token.

**Notion de sous-mots.** Dans certains cas et dans la plupart des architectures neuronales, obligés de se doter d’un vocabulaire d’unités fixé à l’avance. Or un nb potentiellement illimité de mots. Va prendre les mots fréquents et les mots plus rares les découper en sous-mots.

BPI ou Sentence piece selon l’algorithme utilisé. Souvent emploie aujourd’hui token pour ces unités (et pré-token).

**Mots-formes ou formes.** Correspond à un mot morpho-syntaxique. Ici définie linguisitiquement car peut recevoir des annotations et correspond aux feuilles d’une structure syntaxtique.

Correspondance qui n’est pas simple. Parfois plusieurs tokens pour une seule forme. Ex. à l’instar de, bel et bien, il y a. Un token pour n forme = amalgame (aux, des, etc.). Cas plus compliqués encore.

Entités nommées. Un type de forme particulier important dans certaines applications. Une entité du monde qui peut être désignée individuellement. Classqieus : personnes, lieux, organisations. Au sens large dates adresses URL, etc.

Une mention est une séquence de tokens dénotant uen entité nommée; Cette dénotation peut être ambiguë.

Les mentions on des propriétés spécifiqeus. Structrure interne spécifique (grammaire locale) souvent culturelle plus que linguistique. Les considérer comme des formes particulières (plus simple à considérer).

**Mots sémantiques**. Séquence maximale de forme(s) dont le sens est non-conventionnel. Son sens est non déribale du sens des formes qui le constituent. Souvent ambigu. Proche mais distinct de la notion de terme (notion conventionnelle).

### 4 enjeux spécifiques à ces données textuelles et complexe pour leur traitement automatique

L’ambiguité

Ambiguïté lexicale : homonymie 

homophonie, homographie

Ambiguïté syntaxique : rattachement prépositionnel.

Ambiguïté sémantique

Polysémie

Diversité morphologique. Langues isolantes, synthétiques : agglutinantes, fusionnelles, polysynthétique. En réalité classification simpliste.

Diversité syntaxique : niveau de configurationalité. Ordre des mots libres, ordre des mots partiellement libres. Ou plus figé (anglais et français dans une moindre mesure).

Systèmes qui fonctionneront pas aussi bien d’une langage à lautre.

Diversité lexico-culturelle. Couleurs, Alignement de sens.

Variation

autre enjeu qui nous intéresse. Variation graphique. Exemple management. Variation sociolinguistique (personnes, contextes). Variation diachronique.

Dispersion (ou sparcité)

Loi de Zipf. Si on prend un texte et que l’on essaye de chercher combien il y a de mots et de les classer par fréquence, on observe qu’avec un petit nombre de mots fréquents va pouvoir couvrir la majorité du texte, mais inverse. Illustré par Loi de Zipf, prendre tous les mots d’un texte et les trier par fréquence décroissante. Obtient une décroissance exponentielle.

Phénomène général, idem pour les constructions lexicales.

### Tâches de base du TAL

Morphologie, syntaxe et sémantique.

Étiquettage en parties du discours

Analyse sémantique

Analyse du sens.

On appelle annotation en parties du discours, la tâche qui convient à assigner une catégorie ou partie du discours (part-of-speech) à chaque mot de la phrase. 

Nécessite tokenisation au niveau du mot

nécessite un inventaire de partie du discours (jeu d’étiquette).

Analyse morphologique. Ajouter le lemme à chaque mot-forme. Analyse morphologique complète.

Étiqueteurs en PoS atteignent des performances de l’ordre de 95% depuis longtemps. Aujourd’hui atteint 2% erreur (⅓ erreur de transcription, ⅓ pas clair, ⅓ discutable).

Reconnaissance entités nommées, reconnaître et typer ces mentions. Souvent étiquetage. Début et fin, étiquetage. 2020 publication avec Ortiz Suarez. 90% de réussite.

Liage d’entités nommées. Une fois que détecter savoir qui est nommé. Ex. Michael Jordan.

Analyse syntaxique

Tâche d’analyse syntaxique ou parsing. Aujourd’hui entraînés sur des corpus arborés. Cf. *Universal Dependencies*. Il en existe plusieurs pour le français. Grandes collections d’arbres syntaxiques.

Il y a un certain nombre d’approches pour l’analyse syntaxique. L’analyse syntaxique en constituants fonctionne bien mais elle a progressivement été remplacée (pour différentes raisons) par l’analyse en dépendances qui présente un niveau de succès de 94%.

### Représenter les mots

48’’34

Maintenant que ces notions introduites, comment représenter les mots pour qu’ils puissent être traités par nos algorithmes. 

Chaque mots dans chaque contexte où il apparaît, porte un certain nombre de proprités (morphologiques, syntaxiques, sémantiques).

Il y a plusieurs façons de le représenter. Il est possible de décrire explicitement ses propriétés. C’est l’approche par lexique ou dictionnaire. 

Mais une autre manière de représenter les mots consiste à les représenter de façon implicite, cad par vecteurs. Méthode utilisée par ceux qui utilisaient des réseaux de neurones, mais pas les seuls. Étude approche espaces sémantiques.

La représentation la plus simple est ce qu’on appelle la représentation 1-hot. L’idée est de se doter d’un dictionnaire. Puis prend un vecteur qui a autant de dimensions que le nombre de mots présents dans le vocabulaire. Et représente le mot avec un vecteur où il y a des zéros partout sauf en position où le mot apparaît. Le problème c’est que si deux mots similaires, ils ont des représentations proches (produit scalaire)

Ici que l’on fait intervenir l’hypothèse distributionnelle. Exemple adapté de Lin 1998, Nida 1975. Quatre phrases qui permettent de comprendre à partir des contextes d’apparition le sens du mot. Deux mots sont similaires s’ils apparaissent dans les mêmes contextes. Harris 1954, Firth 1957.

Embeddings non contextuels

C’est sur cette hypothèse que s’appuie pour produire des représentations

Assigner représentation vectorielle unique sur l’étude de l’esnemble des représentations en corpus.

Approches statistiques et prédictives.

Approche par comptage. Matrice de cooccurrence vs mot-document. Permet de représentation similaire.

Permet d’obtenir des vecteurs qui ont la propriété que l’on voulait. Mais problèmes de dimensions. Quelques solutions pour résoudre ces problèmes (cf. diapo).

Depuis 2013, utilisation approches prédictives neuronales. Approche word2vec (Mikolkov et al. 2013), autres exemples FastText, GloVe.

L’idée est d’entraîner à prédire les mots suivants.

Approches prédictives neuronales. Possibilité de faire de l’algèbre sémantique ce qui a rendu ces approches populaires. Levy et al 2015 ont montré que les approches traditionnelles et word2vec sont fondamentalement équivalente.

Embeddings non contextuels qui présentent un certain nombre de limites. Mais pour aller plus loin, il nous faudra la notion de modèles de langues.





Représentation des unités textuelles

### Quelques applications du TAL aux Humanités numériques

Daniel Stoel, Jean-Baptiste Camps

## Approches symboliques et statistiques

### Cours

Approches principales pendant longtemps, encore utilisées dans 

S’appuient sur des descriptions explicites des langues et de leur fonctionnement. Linguistique descriptive et formelle

### Deux exemples d’usage des transducteurs...

## Modèles de langue

### Cours

Notion centrale au TAL

### Apprendre un modèle de langue à partir de l’audio

## Traduction automatique

### Cours

### Traduction neuronale massivement multilingue

## Approches neuronales pour quelques tâches applicatives

### Cours

## Linguistique computationnelle



