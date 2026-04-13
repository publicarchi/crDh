# Linguistique et Traduction et HN à l’ère de l’IA

CRIHN, 25 et 26 septembre 2025. UQAC Chicoutimi

## Mots d’introduction

Recherche, création et innovation. Explorer innovation qui transformeront choses de demain.

Vincent dans ce moment où IA transformer nos objets d’étude. Votre colloque précieux dans la région.

## Aurélie Néveol, Évaluation of MT and other tasks in the era of Large Language Models

évaluation qui doit couvrir la qualité mais aussi les impacts. Biais, etc.

Principes évaluation en NLP conçus pour permettre la reproductibilité. Paradigme d’évaluation qui s’appuie sur la définition d’une tâche.

Une tâhce, un corpus et un ensemble de métriques.

- Détailler description objet étude et inputs et output attendus
- Corpus avec annotation, pas de recouvrement entre entre les corpus d’entraînement et tests
- un ensemble de métrique : utilisation d’outils open source

Campagne WMT, organisation d’une tâche biomédicale. Consistait à traduire des textes de l’anglais vers autres langues. 13 langes par la suite couverte. 

Utilisation de la base MEDLINE et données additinnelles.

Métriques Legacy BLEU, chrF, CMET

Traduction, pb acronymes médicaux. Parfois pb de traductions ex. siège glottique. Contrôle de qualité au niveau de l’alignementd es prhases. En corrigeant alignement manuel, augmente record.

*BLEU* (bilingual evaluation understudy)

Essayé d’évaluer si natifs. Fréquents pour anglais. Moins le cas pour les résumés en anglais. Disparité dans la manière dont les résumés sont élaborés.

Avoir des corpus d’évaluation et d’entraînement très séparés. Voir qu’en terme de reproductibilité, Mais 10ans plus tard, difficile de garantir que les systèmes n’aient pas utilisé ces documents en corpus d’entraînement. D’autant plus que quand travaille avec des LLM, utilise souvcent des modèles fondationnels dont les données d’entraînement ne sont pas disponibles.

Acronymes fréquents bien traduit. Cependant consistance sur ensemble d’un texte est rare.

Haute prévalence des cas cliniques. Parfois non traductions incorrectes. Erreur sur plus ht ou plus bas. Cliniquement faux.

Enjeu de l’impact de la traduction automatique sur les praticiens. Gain de temps pour accès à l’information ? Accès à plus d’information ? Quel impact des informations eronnées ?

Performances et biais. Pointe émergée iceberg, questions environnementales, microworking, conflits d’intérêts.

5 sources de biais en TAL. 

Hovy D. Prabhumoye S. 2021. Five sources of bias in natural language processing.  https://doi.org/10.1111/lnc3.12432

- Conception et design de la recherche
- sélection
- annotation
- architecture des modèles de langues
- task model

Première question. Déterminer quel modèle de langue est adapté pour la tâche que souhaite réaliser.

Exemple de biais dans les sortes des systèmes. Variantes de traduction, profession quand passe d’une langue qui ne marque pas forcément le genre.

Biais liés à l’automation. Conflits d’intérêts liés à l’industrie. Autour de 2020, augmentation très importante de l’industrie. 4% à 14% en TAL. Mais sur les recherche dans les biais, 42% de présence de l’industrie... Ce qui pose la question des dynamiques de pouvoir (manière d’orienter les questions de recherche et de mener les travaux).

Impact environnemental des solutions d’IA.

SPEC Référentiel général pour l’IA frugale.

S’oriente vers des systèmes gourmands en calcul. Organismes comme AFNOR qui proposent des spécifications. 31 reocmmandations. 

- Le plus efficient possible
- bénéfice par rapport autres techniques
- soutenable impact planétaire

Mais mesure impact complexe. Prendre en compte fouille, entraînement ou raffinement. Prendre en compte les équipements et leur cycle de vie. Usage, fin de vie.

Bannour, Nesrine, Sahar Ghannay, Aurélie Névéol, et Anne-Laure Ligozat. 2021. « Evaluating the carbon footprint of NLP methods: a survey and analysis of existing tools ». In *Proceedings of the Second Workshop on Simple and Efficient Natural Language Processing*, édité par Nafise Sadat Moosavi, Iryna Gurevych, Angela Fan, et al. Association for Computational Linguistics. https://doi.org/10.18653/v1/2021.sustainlp-1.2.

MLCA https://github.com/blubrom/MLCA prend en compte analyse cycle de vie

Ecologits https://ecologits.ai/latest/ prise en compte de la phase d’entraînement

Mesure directe fait parfoi évaluation. Outils asynchrones, etc.

calculator.green-algorithms.org

semianalysis.com/2023/02/09/the-inference-cost-of-search-disruption

ChatGPT difficile de trouver info. Plus de 3 617 NVIDIA A100 pendant plus de 100 jours. Colossal.

Luccioni, Sasha, Yacine Jernite, et Emma Strubell. 2024. « Power Hungry Processing: Watts Driving the Cost of AI Deployment? » *Proceedings of the 2024 ACM Conference on Fairness, Accountability, and Transparency* (New York, NY, USA), FAccT ’24, juin 5, 85‑99. https://doi.org/10.1145/3630106.3658542.

718 T pour chatGPT. 2T par personne par an.

Consommation d’eau. Texte de 100 mots, ou 10 question : 0,5l eau.

COnsommation énergie Modèles de langues

Morand, Clément, Anne-Laure Ligozat, et Aurélie Névéol. 2024. « How Green Can AI Be? A Study of Trends in Machine Learning Environmental Impacts ». arXiv:2412.17376. Prépublication, arXiv, décembre 23. https://doi.org/10.48550/arXiv.2412.17376.

Distillation pas toujours moins impactante qu’un modèle global. Dépend beaucoup des techniques mises en œuvre. Besoin de vraiment mesurer les choses pour comprendre ce qui se passe.

Savoir si peut avoir confiance à ces modèles car tjrs besoins hypothèses pour couvrir informations dont ne dispose pas ou faire des approximations.

Différences relatives entre ces deux modèles comparables et si ne peut pas garantir mesure précises. Voit qu’impact élevé et en augmentation dans le domaine.

Plusieuurs solutions.

Ligozat, Luccioni 2021. A practical guide to quantifying carbon emissions for machine learning researchers and practitioners 

savoir si beosin ML/AI. Choix précis du modèle. Documenter les choses.

Lannelongue, Loïc, Jason Grealey, Alex Bateman, et Michael Inouye. 2021. « Ten Simple Rules to Make Your Computing More Environmentally Sustainable ». *PLOS Computational Biology* 17 (9): e1009324. https://doi.org/10.1371/journal.pcbi.1009324.

Calculer impact cabronne travail

inclure dans anaalyse coût bénéfice

données dans la durée qui peuvent être réutilisées.

ANR 23 IAS ...

Évaluation TAL et traduction auto devrait s’indiquer à la qualité des résultats avec des métriques mais aussi avec des impacts qu’il faut mesurer.

### Discussion

Texte avenir ar

## UQTR, Poirier

Science des données traductologique. Comme traducteur constaté le caractère variable des traductions. Intérêt pour pragmatique.

Arrivée des LLM en traduction massive. Évaluation de la traduction, analyse des écarts.

Méthode traditionnelle, méthode directe. Objective mesurer et comparer quantité information brute ou lettre du texte source et autre par mots lexicaux. Manière cavalière de définir l’information.

Trois modules scripts, Python

Bitextes alignés en format cv avec [LF Aligner](https://sourceforge.net/projects/aligner/). Segmentation par phrases [Sentence Boundary .Disambiguation - ruel-based](https://github.com/nipunsadvilkar/pySBD) (retour analyses par règles). Coefficicent de similitude angulaire entre segment source et cible. Traitement multilingue et monolingue (Spacy).

Algorithme à base de règle offre résultats plus intéressants qu’approche statistique. Car utilisation point dans les noms de personnes. Nombre de pages suivi par points. Obstacles pour la segmentation. Règle apporte réponses plus intéressantes.

Spacy analyse morphosyntaxique (Module NLP spaCy). Décompte des mots lexicaux (N, V, Adj, Adv, Nombre, noms propres). Règles ad hoc, auxiliiares, etc. TRaitement des locutions.

Algorithme. Précision de l’information traduite PIT

Repérage des écarts e PIT, repérage des mauvais alignements. Non détection des anomalies antagonistes. Bruit relativement élevé dans la détection de traductions non littérales ou hors normes (en longueur) https://depot-e.uqtr.ca/id/eprint/11009/1/POIRIER_E_25_ED.pdf

Produits dérivés

- validation de la qualité des alignements
- détection des textes traduits automatiquement par la segmentation isomorphe des textes.

S’est aussi aperçu qu’un indice important, assymmétrie dans la segmentation par phrase. Traduction automatique tendance suivre modèle phrastique. Humains ajout, etc.

Voudrait mettre en ligne l’algo sous la forme d’un service. Deux versions : *textum comparationis* (monolingue) et lexico-précision (analyse bi-lingues, pour toutes les langues modélisées)

Réplication analyse sur les lois du Québec pour utiliser les LLM.

Pour calcul similitudes angulaires utilisation Calembert v2.

Dans le premier analyse n-gram.

Utilisation LLM urtilisation agent conversationnel pro clé-api.

Intéressant de pouvoir créer des modèles.

Opportunité « culturelle » pour les humains. Exemple, pour vs aux. Anomalies liées normalisation LLM. Proposer des LLM qui introduisent bon goût dans la traduction.

Jean Delisle, manuel de traduction raisonnée. Des textes déjà travaillés par l’auteur avec corrigé.

Similitude angulaire cosinus chez les étudiants plus proche que le corrigé lui-même. Interroge sur la pertinence de cet indicateur pour évaluer la qualité de la traduction. Mais peut être choix modèle.

Entropie : meusre de l’incertitude ou de la diversité des choix linguitsiqeus dans une séquence. Une entropie élevée indique une plus gd variable ou imprévisibilité

Perplexité : mesure de la « surprise » d’un modèle de langage face à une séquence donnée. Plus la perplexité est basse, plus le modèle juge la traduction ...

Améliorer algo en TALN

avec GML - LLM analyse syntagmatique (granularité plus fine)

avec vectoration

avec...

Améliorations conceptuelles possibles.

Interdisciplinaire TALN. Démarche empririque reproductible des méthodes.

## Les limites de la TA et de la TAO dans la traduction des termes de fantaisie : étude sémio-lexicale du Seigneur des Anneaux

Maryam Akramifard

Récits mythiques et fantastiques occupent une place importante dans la littérature mondaile, mais traduction pose défis particuliers, remplis créativité et néologismes.

Souvent public jeune. Pose pb, comt traduire ce qui n’existe pas dans le réel. Concilier fidélité à l’univers et réception culturelle. Limites pour TA et TAO.

Perspective sémiotique. Propositions pistes évolution.

Amazon, liste 50 livres plus vendus. ⅓ de la fantaisie. Souvent très traduits ou adaptés.

Tolkien, monde parallèle, mais mémoire mythique. Univers enracité dans les mythologies nordiques. Traduit en plusieurs langues. 

Altérité, ex. Hobbit. Altérité même dans langue origine.

Triangle sémiotique

Carré sémiotique de Greimas en traductologie. Permet de dépasser approche purement lingyistique en introduisant une analyse structurelle et axiologique. Utile pour comprendre comment la traduction, neutralise ou réorganise les valeurs culturels.

traduction automatique ou assistée par ordinateur.

Analyser la résistance sémiotique à la traduction.

Analyse de Rivendell d’après carré sémiotique de Greimas. Ambivalence sémiotique.

Autre terme non traduit par le traducteur. Mordor.

Pour chq narratologie, ontologie, morphologie

Exemple traduction automatique selon Deepl ou Google.

Chmps de développement de la TA neuronnale

- intégration de connaissances exeters : base culturelles et mytho pour contextualiser néologismes
- enrichissements morpho-sémantqiues
- hybridation TA/TAO
- Adaptation contextuelle
-  évaluation sémiotique. Aller au-delà de la métrique BLEU pour mesurer adéquation culturelle et sémiotique de la traduction.

Logiciels qui permettent parfois intégration de vocabulaires spécialisés.

Approches plus hybrides avec ChatGPT. Pb validation et controle.

## Les grandes promesses de l’IA à l’épreuve de la traduction : entre biais algorithmiques et balbutiements réglementaires

évaluation

Postédition permettent aux étudiants atteindre qualité globale comparable. Voir meilleure qualité avec DeepL. Mais une forte homogénéisation des notes autour de la moyenne. Traduisait un effet nivelant. Plus étudiant est faible, plus augmente sa qualité. À l’inverse étudiants doués en traduction humaine chez qui on observe une baisse de la performance en traduction.

- maîtrise des règles usages
- tendance traduction littérale
- effacement information
- rupture codé textuelle
- irrégularité termino
- moins diversité lexicale

Lorsque sa thèse arrivée outils génératifs. Résultats tjrs des limites celles observées en traduction neuronale : calques, glissements de sens, voire contresens. Mais également nouveaux pb hallucication.

Forte influence anglais avec calque syntaxique. « qu’ils intrinsèquement imposent ». Ponctuelle erreur grammaire. Appauvrissement lexical. Glissements de sens.

Exemple hallucinations --> réponse évaluateur

Hallucination, liste de synonymes en contexte, très utile (DeepL traducteur) mais parfois propositions très pbtique. Quels gains qualitatifs. Mais aussi des contresens.

Cas où, ajout : exemple conducteur, pas vu 30kmh. Et IA ajoute : Il a donc été arrêté !

Enjeux qualitatifs, mais aussi juridiques

Protection des données perosnnelles RGPD en Europe et données confidentielles (ex. DeepSeek interdit en admi fédérale, mais continue de privilégier des outils propriétaires am)

Question de la responsabilité en cas de préjudice : fournisseur IA ou traducteur ?

Repsect des droits d’auteur (ex. procès Anthropic)

Arrivée de réglementations en matière d’IA (AI ACT en Europe)

Mai 2024 entrée en vigueur. Cadre pleinement en application en août 2026. Définit des règles communes, exigeances et obligations pour IA.

Approche fondée sur les risques, jugés acceptables, modérés, etc.

Usage en milieu universitaire repris. Risques associés à la trajectoire des étduiants. Ex. Annotation des examens. Plusieurs cas de figure distingués pour l’évaluation. Détection de cas fraudulex aussi risqué.

Les système IA utilisés dans le domaine foramtion pour évaluer acquis orienter le processus d’apprentissage et surveiller les comportements malhonnêtes et les fraudes sont soumis à la loi IA et traités comme systèmes d’utilisations à « haut risque ». 

Encore un gros flou. Donc risque application disctincte.

ChatBot risque limités. En raison des enjeux de transparence. Quand communique avec Chat doit le savoir. 

Droit auteur. idem

Enjeux cognitifs pour Mathieur Corteel 2025.

> L’IA, telle qu’imaginée par les géansts du numérique, repose sur le vol de notre activité cognitive et une dévaluation étendue des activités humaines non protégées par le droit d’auteur.

Utilisation croissante IA qui boulervse rapport au savoir. Plusieurs risques

- uniformisation lange et pensée Alombert, 2024. Bien construits, mais monotones, pas humour. Force répétition disparition termes rares, risque appauvrissement lexical et culturel.
- Risque de confusion cognitive (Alombert 2024). Illusion de véracité, termes probables difficile de distinguer les deux.
- Délégation cogniftive (cognitive offloading) perte de capacités mentales (Abbas et al 2024, Batsani et al, Kosmynyna et al. 2025).

Mathieu Corteel Ni dieux ni IA. 

Bolter, différence fondamentale entre fonctionnement moteur de recherche ou chatbot. Moteurs nous emmènent à des endroits où information existentes normalement créées par les humains, là où chatbot va créer sa propre réponse. Pour elle utiliser comme source mauvaise idée.

Pourtrant nbx outils pour recherche biblio. Perplexity Academic, Felo, Elicit, Sci Space. Aline Bouchard souligne que aligne référence sans synthèse. Par ailleurs cherry picking. Risque de citations de pure forme ou biais de citation au détriment d’une lecture critique ou pluralité disciplinaire. 

Pb de faisabilité de la vérification humaine. Complexe de tout vérifier. Cf. Aaron Tay « La menace IA pour la revue de littérature... citation article inappropriés mais réels (système de type RAG) »

de l’illusion de la conpréhension et de la perte d’expertise. Donneraient illusion de penser. Produirait plus que l’on comprend. Résumer et bêtement synthétiser, pas analyser et agir.

Contrecourrant slow science.

Question aujourd’hui plus savoir ce que peut faire mais où allons-nous et ce que voulons faire avec ces technologies. Éclaircir flous juridiques. Consciences enjeux cognitifs, notamment en contexte apprentissage. Essayer de privilégier outils qui favorisent acquisition de connaissance et esprit critique plutôt que des outils qui les entrave.

### Discussion

Guerre des Gaules, Jules César explique que refus écrire car déteriore leur mémoire. Stratégies de mémorisation.

Bien sûr déjà discussion avec calculette. Mais ici technologie n’est pas fiable.

Important de faire des tâches sans les outils. Faire comprendre que vient quand on a déjà acquis des compétences.

Important de mettre en avant le cheminement. Quand on évalue les étudiants, l’enjeu pas avoir le résultat de la traduction du texte mais le cheminement. Exercice, ce qui permet la compréhension des mécanismes et la présentation des résultats. Ne faut-il pas revenir à des systèmes de traduction statitistique, phrase à phrase. Exemple en traduction de textes critiques avec post-traitement. Traduction modèle génératif meilleur score mais traducteurs préfèrent éditer traduction statistique car moins le risque d’avoir des contenus qui n’étaient pas dans le texte.

Ajout IA générative dans les systèmes de traduction. Pas convainquant, mais en met partout. Repérage des erreurs en effet moins simple alors que dans traduction neuronale.

Une discipline récente. Fortement affectée par la traduction automatique neuronale sans doute avant les autres. En réalité enjeux IA à peu près les mêmes. Se redéfinit comme disciplines mais surtout les programmes de formation. Nous oblige à nous adapter car subit fort les effets du discours marketting. Gros décalage entre ce qui est dit et les performances réelles du système. Question du nom des spécialistes que veut former. Experts linguistes, etc.

Savoir si apprentissage type prompting.

## Simon, projet Balsac

Une des premières infrastructures numériques du Canada. Projet créé par Gérard Bouchard dans les années 70. S’intéressait d’abord aux extraits d’actes de naissance paroissiaux. Débuté sur une paroisse, puis Chicoutimi, Saguenay puis Lac Saint-Jean avant de faire tt le Québéc. 7à

Méga-généalogie du peuple Québecois. Hélène Vézinat après Bouchard. Puis lui. Une infrastructure numérique car un jumelage de données nomnatives issues d’actes d’état-civil. Transcrit d’abord manuellement puis par OCR.

Couverture pas uniforme. Saguenay couverture complète jusqu’en 1970. Peuplement tardive. Charlevoix complète. Reste complète pour les mariages mais pas naissance et décès.

Mais couverture qui s’écroule à partir des années 1970. À la recherche de nouvelle voie pour poursuivre collecte. Ne peut plus avoir recours aux mariages car les gens ne se marient plus, ou très peu. Aujourd’hui moins de 20% des unions scellées par les mariages. Il faut donc une autre source.

A donc exploré l’utilisation des nécrologies. Pratique longue, souvent publique. Adapation aux réseaux sociaux et à l’internet. Section des résidences funéraires. Des données publiques mais il s’agit de données nomminatives, or ce type de données est hautement confidentielles.

Garde information mais change la structure de l’information. Ce qui va permettre d’organiser la diffusion. Nécrologies au Québec qui sont non structurées. Pas de convention. Il y a donc un problème au niveau de la classification. Pas de répertoire des chronologies classifiées.

Partenariat avec Fédération généalogique. Et nécrologies. Pense avoir bientôt intégré ensemble des décès. Rare de pouvoir dire que travaille sur tout le monde. Chutte 70s mais relai données journéaux. Comparaison possible avec institut des statistiques. Bien sûr des variantes. Mais peut penser avoir projet global.

4 ans. Prmeière étape données validées. Pas de méthodes pour le réaliser. Quand parlé de ces questions plusieurs à discuter comment résoudre le pb. Pas de moyen de résoudre sans disposer d’un set de données validées. Première étape pour déterminer pertinence de notre modèle.

Emploi étudiants possibles. Finalement activité plus ludique, le nécrothon ! Charge imposée à tout le monde pendant 10h. Événement fun fin festive. 

Obtenu un set de données validées. Une interface poru annotation des nécrologies. Dévelopée par Pierre-Carl. Interface partageable pour d’autres projets.

Création d’une base de donneés par Thomas. Contrôle de qualité. Secondaire 4. Tout le monde n’anotant pas de la même manière. Révision pour valider concocrdance.

Plusieurs LLM testés. Accès à plusieurs cartes graphiques pour tester différents modèles. Majorité des modèles qui roulent avec une performance similaires, mais performances différentes. Raison pour laquelle choisi Owen3 car meilleures métriques.

Rapidement pb de token, car nécro avec commentaires. Condoléances.

Tourné sur Rorqual. Permis faire plusieurs fois. Au début plusieurs jours. Permis de développer une approche en deux étapes.

Identification des points d’ancrage. Étape n° 1. Métriques. Super performance.

Capable d’aller chercheur autres informations. Provenance. Montréal moins représenté. Peut être cultures utilisant moins.

Test inférence sur la maladie. Mais représentation sans doute similaire à la vérité.

Balzac arrêt couverture à partir de 1960. Possibilités de rattachement : individus avec parents mariés avant 1960, ou avant 1930. 

1,2M de nécrologie. 860K utilisable

228 éco prête pour intégration. En moyenne 15 individus. 3,5M individus jumelables. Donc poss doubler taille bdd que construit depuis 50 ans. Essaye tester intégration. Commencé à faire reconstitution



Anonymisation --> définitive ? Quid pour alignement ?

Comment se fait le pairage.

Comment gère confidentialité

Finetuner modèle spécialisé.

14h20

## Garcia 14h25

- Analyse de données à partir de la statistique Bayésienne
- Incertitude autour des estimations des modèles
- Exemple illustration : la variation des sentiments dans un roman : incertitude et distribution a priori

Analyse de données à partir de la statistique Bayésienne

Essor des outils IA pour le texte. Parle souvent de boites noires

- grands modèles de langage 
- Ex ana de sent
- extraction fio

Mais... comment évaluer la fiabilité ?

- résultats opaques
- fausse précision 73,2% de sentiments positifs
- Biais cachés dans les données d’entrainement

Possibilité inclure des biais inclus dans la littérature pour calculer la performance dans ces modèles. Estimer la performance avec analyse statistique plus complète.

Comment analyser les textes de manière transparente et rigoureuse face à l’incertitude ?

Analys de données traditionnelle.

- estimations ponctuelles
- tests de significativité
- résultats binaires (significatif ou non) le plus souvent. 

Pb de binarité des résultats. Possibilté de changer la valeur p selon les objectifs p hacking.

Ici possibilitéutiliser approche bayésienne. Quelques avantages

- Quantification de l’incertitude de manière plus complète
- intégration de connaissances préablaes (connaissance déjà établies dans la littérature, modèle qui ne commence pas à zéro. Plusieurs possibilités de faire entrer. Aspect connecté à la notion de biais. Poss faire entrer de manière adaptée et transparente selon les objectifs)
- énoncés probabilistes directs : scénario possible selon la tâche

Exemple d’un roman de Bovary. Démontrer les avantages de l’analyse bayésienne pour les HN. Possibilité de créer résultat

Théorème de Bayes

p(hypot| données) = P(données | hypo) x P(hypo) / p(données)

Bayésienne prend la probabiilité de l’hypothèse et les données. Permet ajouter information sur la fréaquence d’un phénomnène. En termes pratiques : ce qu’œn coris et proportionnel à ce que l’on observe multiplié par ce que l’on savait avant.

Philosophie Bayésienne. L’incertitude qui est intrinsèque à la connaissance. On met à jour nos croyances de manière rationnelle à mesure qu’on reçoit de nouvelles données. La logique bayésienne de façon visuelle.

Sur tout peut avoir plusieurs étapes pour simuler les résultats. Important pour formuler représentation de la science.

Une façon de visualiser le processus. Si certain à propos d’un effet. Exemple 35 mots positifs 55 mots néga que l’on observe dans la surface. Imaginer que connaissance de base nous donne information dans la littérature selon laquelle proba 55% (hypothèse neutre). Plus ou moins 50%

Prior, data, and posterior. Supposition initiale, observe les données en bleu. Distribution effective en noir. Ce que l’on réalise le plus souvent dans la vie.

Ex. Littérature donne information que pour un auteur observe 70% de mots positfs. Différence relativement grande entre les données obs et littérature. Si dit que certain, dans conclusion, observations plus proches. Problématique en psychologie mais intéressant.

Va analyser comment modèles nous permet de jouer comme cela. En phonologie utilise souvent les régressions. Deux paramètres, échantilllonage des valeurs probables étant donné les valeurs ded données.

On ne peut pas calculer la loi a posteriori elle-même (impossible en pratqiue) mais on peut l’approximer en tirant des échantillons de cette loi.

Exe illustratif d’une distribution à posteriori conjointe... si proche du sommet...

En pratique différence immense ou zéro.

Fréuqnetiste paramètres fixes. Paramètres incertains dans Stat bayésienne. Deux philosophies. Données fixes bayésiennes. Aléatoires en fréquentistes. Intervale de confiance en féquentiste. Intervale de crédiblité en bayésien, plus facile à interpréter.

Interprétation difficile en st.

Analyse des sentiments chez Bovary.

Trois partie du roman, vérifier les sentimens.

Origine des sentiments. Différence imense à partir du chapitre 6.

Comparaisons multiples.

On a des options mais auj explore modèle binomial. Une extension d’une régression logistique. on modèle une proporition qui compare deux modèels bayésiens.

spécification des modèles : deux hypothèses dans les effets aléatoires.

Structure chapitre, ou chapitre organisés dans des parties.

Les deux modèles supposent l’a priori B) ~N(0,1) distribution autour de zéro.

Premier modèle 3 parties, rassemblées pour des raisons esthétique. Deuxième modèle chq partie une structure particulière. Et similarité au sein des parties.

Deux modèles qui ont la même structure aléatoire. Deux modèles et présiction. Erreurs std là. Pointillées concentrées c. 50% moyenne globale. Chapitre concentrés par rapport à une partie. Sinon estimation individuelle pour chaque partie.

Différence hypo dans le modèle. Intervale de crédibilité à 95%

Peut condiséer les deux modèles et évaluer celui pour 

LOO ELPD diff. Modèle hiérarchique meilleur. Les parties du livre un rôle plus important.

La précision prédictive du modèle est suppérieure. Améliore la précision du modèle en supporant que chq chapitre a ses propres caractéristiques.

Possiblité vérifier en générant des données pou rdéterminer la précision. Courbes plutôt autour de 

Possibilité vérification prédictive du modèle.

Finalement arrive différence essentielle quand parle modèle fréquentiste. Intervale de confiance qui ne sont pas des distribution de probabilité. Alors qu’ici peut dire que plus probable. Plus d’information sur la densité de la distribution des effets. Repère aussi différences entre certains chapitres.

Ici partie comme fait aléatoire.

Plus d’information dans les essais. Plus de flexibilité. Un autre avantage possibilité de simuler la variance. Distribution a priori, possibilité d’estimer la variante.

Degrès plus complet.

Analyse bayésienne. Mais comment les comparer.

Partie comme variable prédictive. 

Résultats similaires mais pas identiques : intervalles de crédibilité ≠ intervalles de confiance.

La différence ... effet de régularisation aussi.

Prmière chose, taille des intervale. Fréquentiste plus large. Car correction et ajustement typique. Technique Tuckey. Change pas la position relative mais taille. Corrections pour éviter erreurs type 1. Pas besoin de corriger intervales dans bayésien.

Modèle hiérarchique déjà conçu pour réduire les erreur de type 1. (mais continue à corriger, ne sait pas pq). Les a priori exercent un effet de régularisation natruelle. Cela stabilise les estimatiosn et peut en améliorer la précision.

Intervales plus ou moins les mêmes que modèle sans correction. Mais vérifier que pour les modèles en jaune et orange. Plusi proche 0. Régularisatio nnaturel. écart type dans la distribution a priori

Modèle conservateur.

Interavales de confiance de vrais interavales alros que crédibilité de vrais distribution donc plus intuitif. 

Manière rigoureuse et transparente. Dans un contexte boite noire. Méthod qui permet de conciciler précisions et reconduire résultats 

https://gdgarcia.ca

https://gdgarcia.ca/files/uqac_llm_2025_garcia.pdf

## Ces machines qui parlent sans savoir : optimisme et limites des LLM 15h02

Bonne connaissance de la manière dont on entraîne les modèles de fondation.

Stimuler la discussion

Bref retour comment arrivé aux LLM et arrivé aux modèles de fondation. Modèles qu’est-ce que cela fait.

Intelligence ambiante. Habitations intelligentes, réseaux de capteurs. 70 habitants intelligents avec des personnes agées. Essayer de garder ces personnes le plus en sécurité. 2e axe par opportunité. 

Beaucoup sollicité pour faire des applications. Un chercheur appliqué.

Beaucoup travaillé, reconnaissance minéraux. Segmentation lames minces. Synergie, UQAC et Hydro, etc.

Pourquoi les modèles de fondations ont-ils changé l’IA ?

L’IA un long historique, mais une courte histoire. Depuis les années 1950, IA traversé plusieurs phases d’enthousiasme et illusion. Premiers modèles de représenattion de données ELIZA puis A* et Alpha-Beta plusieurs travaux ont changé el monde dans l’ombre. Ou de façon plus éclatante DeepBlue 1997, Stanley...

Orientation symbolique et échec industrie des systèmes expetrs dans les années 80. Progressivement les projets ont gagné avec les données. Avènement informatique. Plutôt que de tenter de reproduire, pourquoi ne pas regarder les données pour résoudre les pb ou trouver la solution. Sans vraiment se préocuper de cmt marche.

Apprentissage supervisé (trouver meilleur algo pour résoudre nos tâhces, faire meilleure régression, capacité algo à résoudre tâche spé), non supervisé (majorité des données sans étiquettes, comprendre résultats, voir ce que l’on voir. Demande beaucoup expertise) ou par renforcement.

ML tjr splace importante...

Beaucoup de travail avec renforcement. Lorsque machine évolue et fonctionne dans un environnement et essai et erreur. Beaucup pensé que avenir de l’IA car sans doute manière naturelle dont les humains ont fait apprentissage. Peu nformation sur manifère dont machine apprend par les données. Mais l’information de rétroaction très très limitée. Comment tirer autant de connaissance et structurer rétroaction. Aujourd’hui plutôt utilisée pour paufiner les modèles existants.

Réfléchi et petit être autoorganisation qui est la clef de l’apprentissage. Alorithme flockingbird, etc. algo relativement simples qui dépendent de pt règles et comportement ou résultat intelligent émerge plutôt de l’interactions. Capacité simuler groupe de déplacmeent animaux, etc.

La tâche n’était finalement pas la clé. **En réalité les données, trouver une façon de les représenter en exploitant toute la richesse de l’information.** Commencé avec les auto-encodeurs, 1987. Entrée et sortie, et calcul de la sortie. Modèle censé pouvoir synthétiser information importante dans la données. Finalement développé bcp auto-encodeurs. Plusieurs modèles dévelopés de ce point de vue word2vec qui introduit fondamentalement modèle auto-apprentissage.

Idée de construire des réseaux de neurones qui vont condenser tt info en synthétisant les données.

Hinton, « le cerveau possède 10^14 synapses mais vit que 10^9 seconds. Donc, nous avons plus de paramètres que de données ». En qqsorte apprend de manière non supervisée sans objectif.

Cela motive l’idée que nous devons faire beaucoup...

Le bon LLM. Révolutionné le monde de l’IA. Au point que magique certains convaincus que sera remplacer dans certaines années. 

- démocratisation et accessibilité au savoir humain (en fait par rapport YouTube alléatoire tjrs mieux !)
- productivité augmentée sur de nombreuses tâches
- aide à éduqeur et prendre en main un sujet
- améliore la qualité des rapports présentations et comptes-rendus
- Créativité et expression augmentée (brainstorming interactif)

Puissants assistants. Exemple donner exemple calcul noyau polynomial. Exemple simple trois caractéristiques, etc. De qualité mais valider les calculs. Car souvent.

Aurait pu le faire tt seul.

Balance stimulation intell, et faciliter travail.

Utilise beaucoup. Éducation aux limites.

Meta analyse de Wang & Fan The effect of ChatGPT. Mais étude contraire MIT Kosmyna et al 2025, Your brain on ChatGPT.

Humain vs Machine. 

https://mmmu-benchmark.github.io/#leaderboard

L’écart ne se creuse pas entre modèles privés et open source. Meilleurs modèles qui battent les meilleurs experts humains.

Beaucoup de tâches fondamentales. Monde manipulable, peut être manipulé. Langage discret par rapport au monde réel.

Pb mécanismes d’oublis. Image enfant qui attrape une balle, problème qui reste complexe en robotique.

Je suis plus intelligent qu’un LLM. Souvent compare machines aux humains mais pas à armes égales.

Lyam a entraîné 15 000 000 000 000 tokens soirt 120 000 go et envrion 11 250 000 000 000 de mots

si lit 250 mots par min...

et énergie et quoi mange.

probabilité que jetton en dehors ensemble correct. Divergeance exponentielle. Plus réponses longues plus peu de chances de données réponse inadéquate.

Diviser pour régner. Fonctionne mais reste pb exponentiel.

n puzzle pb classique IA

Faith and Fate : limits of transformers on compositionally. arXiv.org/abs/2305.18654

IA pas capable, sauf si programmation agentique qui appele résolution de pb.

Plus réponses longues plus ...

Raisonnement autre pb classique, celui des blocs. Résultats LLM sont mauvais. Humains le résolvent facilement. 

Et en math? sont-ils meilleurs ? Souvent répondent car vu le pb. Proof or bluff ? evaluating llms on 2025 usa math Olympiad. Compétition évaluée sur le raisonnement et non pas la réponse.

Quelles sont les menaces.

Jugement important sur le droit d’auteur. Avoir appris à partir œuvres pas diff et écolier. Bartz v. Anhropic. 

AI models, privatisation de l’IA. Historiquement une discipline ouverte. Donné le code et partagé les données. Changement ex. OpenAI au début ouvert.

Labo en dehors de la course alors que technologies .

Menace de créativité. Beaucoup descriptions faites par les humains. Niveaux de créativité des modèles génératiques par rapport aux humains. Mais écart type rapproché.

contamination données

Métaphore biologique. Neurones, etc.

## Exploring literary works with LLMs.

Christophe Coupé

Un travail exploratoire, pas d’affirmations fortes. Pas intention prétendre expertise en littérature. Une focalisation sur les méthodes.

Présenter un ensemble de méthodes pour travaillr sur des œuvres littératures

- approch quanti
- un lllm assessment of agency
- Agency in the light of other story dimensions
- discussion et perspectives

Comment les images sont-elles construites ? Comment un écrivian construit-il une histoire convainquante ?

Si s’intéresse structure narrative, comment l’histoire évolue-t-elle au cours de l’histoire. Jeu sur les temporalités, etc. Si étudie un grand nombre d’histoire repère-t-on des tendances, ou des universels (cf. linguistiques). Universels car répondraient à nos attentes cognitives.

The Hero’s Journey, ak the Monomyth, Joseph Campbell 1949, The Hero with a Thousand Faces. Une approche comparative pour souligner la structure des mythes.

> A hero ventures forth form the world of common day into a region of supernatural wonder: fabulous forces are there encountred...

Grand nombre de mythes progression au cours de différentes étapes. Toutes pas nécesssaires. Mais Campbell 17 étapes. S’applique à l’Odyssey d’Homère mais aussi à la guerre des étoiles ou Harry Potter.

Mais aussi de nombreuses histoires qui rejettent ou subvertissent ce modèle là.

Intéressant car une question d’échelle. Les histoires écrites sont organisées en parties, chapitres, scènes. Comment une histoire est-elle organisée à ces différentes échelles.

Si pense à la consomation d’électricité voit des variations au cours des 24h que dure la journée. Mais aussi des variations au cours de la semaine, des saisons, etc.

Les histoires... Nouvel état, fin de l’histoire. Structure que pourrait retrouver au niveau de chaque scène. Qqch intéressant à étudier.

Le domaine de la littérature celui d’approches détaillées en profondeur, qualitative. Le close reading avec tous les bénéfices et réussite que peut avoir au-delà des principes simples introduit précédemment.

Ceci étendu un certain nomb de chercheur essayé de déevlopper des concepts quantitatifs pour étudier œuvres littéraires.

Lutoslawski, Wincenty. 1898. « Principes de stylométrie appliqués à la chronologie des œuvres de Platon ». *Revue des Études Grecques* 11 (41): 61‑81. https://doi.org/10.3406/reg.1898.5847.

Peut s’intéresser à la forme du texte. Mais aussi au contenu. Approches quantitatives qui peuvent être automatisables. 1000 à 10 000 possible. Alors possible chercher des schémas d’organisation sur 10 000 œuvres et voir ce qui ressort.

Exemple réseau social des personnages dans un ensemble de texte. 

Coll Ardanuy, Mariona, et Caroline Sporleder. 2014. « Structure-based Clustering of Novels ». In *Proceedings of the 3rd Workshop on Computational Linguistics for Literature (CLFL)*, édité par Anna Feldman, Anna Kazantseva, et Stan Szpakowicz. Association for Computational Linguistics. https://doi.org/10.3115/v1/W14-0905.

Difficulté de résolution de co-occurence. Pour une machine faire correspondre il ou elle au personnage introduit peu avant souvent difffile. Admettons que sache faire cela. Fabrication possible réseau de connexion entre protagoniste. Et réseau de cooccurrence.

De même arcs émotionnels. Manière dont réseau se déploie quand on lit une histoire.

Regarder valence émotionnelle, émotion positive ou négative.

Exemple score émotions Potter.

Reagan 2016. The emotional arcs of stories are dominated by six basic shapes.

Exemple étude utilisant edonomètre.

Possible aller au-delà des émotions. Ni Wenjing 2023. Exploring storytelling with NLP... Thesis. 

Plusieurs techniques pour identifier les émotions. Par exemple LIWC  qui permet d’analyser texte selon tt sorte émotion (outil payant). Approches plus ou moins avantageauses. Dictionnaires très limités, quid des négation. Aproche par règle ne répond pas à toute la complexité des textes littéraires.

Les approches basées sur les réseaux neuronaux finetuné marche mieux sans être la panacée.

Grands modèles de langage. Perroquet statistiques mais si perroquets très malins. Alors possible toucher ce que peut faire avec le distant reading avec la précision du close reading.

Processus pour LLM agency.

Ce qui est intéressant, plus nécessairement besoin de finetuning.

Brown, Tom B., Benjamin Mann, Nick Ryder, et al. 2020. « Language models are few-shot learners ». *Proceedings of the 34th International Conference on Neural Information Processing Systems* (Red Hook, NY, USA), NIPS ’20, décembre 6, 1877‑901. https://dl.acm.org/doi/abs/10.5555/3495724.3495883.

Dès lors que donne exemples précis. Modèle capable réaliser la tâche de manière très efficace. Alors possible aborder diverses dimensions.

Train de pensée. permet de juger de la qualité de ce que propose. Possibilité centrer sur un personnage.

Ne pas parler immédiation émotion. Mais savoir si le personnage principal fait preuve d’agentivité. Essayer apporter solution à un pb. être courageux et résoudre le pb. Ou au contraire ne pas résoudre le pb.

Hermann Hesse, Siddhartha, 1922.

GPT4.1-mini et autre. Modèles moins évolué, du mal à traiter les phrases avec qualité dont on a besoin. N’utilise pas interface mais API. Ici va écrire un prompt. Va lui donner un rôle, celui d’un critique littéraire. Dire que emphase sur le personnage principal. Expliquer ce qu’entend comme agentivité en fournissant des exemples. Indique ce qui est fort ou bas. Explique qu’important de faire de la co-référence et pq important pour analyse agentivité.

Phrase par phrase analyse du contexte avec contexte des phrases précédentes. Dans un chapitre.

Une approche aspect-based

- ce qui est demandé des extraits de phrases qui véhiculent information sur l’agentivité d’un protagoniste.
-  en dessous du niveau d’une phrase.
- « ... »
- sortie structurée pour pouvoir rapidement fabriquer des tableaux

Fait tourner. 

Pourquoi lissé, etc.

Retours efficaces. Ch7 très contrasté. Perdu dans cette voie.

Travail mené sur plusieurs romans. Peu comparer car le même prompte utilisé pour différentes histoires.

Alors possible de répliquer sur plusieurs œuvres littéraires et catégories œuvres selon différents critères.

#### Agency in ...

assessing other dimensions of stories.

À quelles difficultés confronté...

Possibilité de regarder si des corrélations

- plus heuruex quand autres personnages, plus actifs ou seuls
- est-ce que être plus actifs améliore agency, est-ce que réaction plus grands challenges
- lags consistants entre deux séries temporelles.

Des outils mathématiques pour représenter fréquence et corrélation

Transformé par ondelette : wavelet transform

Possibilité de faire des spectres de cohérence

Prompt qui réclame expression très claire. De la place pour un expertise en littérature. Le contexte que vous allez donner doit être informé par une expertise en littérature. Que donner pour que fasse sens dans le domaine littéraire.

Du langage naturel, se modifie se travaille et s’améliore. Placer de l’expertise dans e domaine.

Comparer avec annotateur humain ? Scores raionnables.

Du close-reading ? Exemple Rivendell. LLM ne pourra pas faire pareil. Mais est-ce que en expliquant suffisamment capable de faire mm chose en travaillant sur carré sémantique de Greimas. Essayer !

### Discussion

Coûts

Quand utilise API paye pour les tokens requête et tokens de la réponse. Disent que n’utilisent pas les tokens envoyés. Pas sûr.

Voie maltée

Stats101 Garcia

## Jean-Philippe Magué

Langues varient, variation très corelée à la structure sociale. À travers la variabilité, on est en train de convoyer et performer notre identité à travers nos choix linguistiques. Quand on est en situation de locution, peut inférer des traits linguistiques. Possible de répondre à ce genre de question même si pas évident.

Travaillé sur corpus de tweets, essayer de comprendre comment à travers ce corpus variation pouvait nous informer sur la structure et inversement. Diffusion des changements dans la langue. Conditionné par la situation sociale. 

Voir comment BERT peut répondre à ces questions. Aujourd’hui ChatGPT. Est-ce que un grand modèle de langue est capable de répondre à une question comme celle-ci, et est-ce que c’est pertinent.

650M de tweets, 3M d’utilisateurs.

5M de tweets, géoloc, revenus, âge, genre.

42 tweets, 21 autrices, auteurs. 180 participants. Recrutement en boule de neige. Forte sureprésentation trentenaires. Pas représentatif. Noter que vision très binaire du genre.

Quand pose la question 63% des cas. Tweet des hommes versus femme, pour les femmes pas de chgmt. Alors que les hommes se trompent plus quand reconnaître une femme, moins quand un homme.

Distinction très présente dans les LLM et donc va nous intéresser.

Est-ce que ces gds modèles de langues sont capables de venir inférer les genre d’utilisateur de tweeter. 

Extrait 1000 tweets du corpus. Proposés à GPT4. Proposé de faire la tâche en distinguant trois conditions. Dans une dit que personne de genre masculin assistant en tant que tel. Dit de ne pas renoncer parce que c’est trop dur. Pas grave si se trompe. Identifie le genre... en indiquant quels éléments pour pencher un ou autre.

Masculin, féminin ou inconnu. Essayer de voir comment questions de positionnement social vont venir transformer positionnement socio-linguistique. 

Taux de bonnes réponses étonnamment proche de ce que les humains sont capables de faire. 63%

Savoir si change selon condition, en adoptant posture sociale. Réponse est oui !

3000 justification dans lesquels le modèle explique ses positions.

Envoyé à Voyage AI embedding model. Il s’agit d’un modèle qui prend un texte et lui associe une représentation vectorielle telle que la proximité de cet espace vienne capturer une proximité entre les textes produits. = nuage de points de 1024 dimensions. Regarder comment ce nuage est structuré. Possible de le voir en 2D, en le projetant, comme si regardait son ombre dans plusieurs dimensions.

Support de discussion car pas intention de l’analyser en 2D. Résultat de l’analyse en composantes principales (projection optimale). Objectif pas de venir réduire la dimensionnalité du problème. Plutôt un moyen de parler ensemble.

Savoir comment il est structuré. Deux parties apparaissant dont on se rend compte que correspondent aux justification sur l’identification du genre. Mais une autre représentation où voit les points colorés en fonction du genre. En réalité, plus mélangé avec les inconnus.

Si seulement justifications. Essayer de voir si cette opposition va pouvoir venir structurer un aspect de la forme. Procède en deux temps. Regarde d’abord les justifications pour dire qu’une femme, puis autre.

Prédictions autrice uniquement.

Peut-on distinguer d’une manière ou d’une autre les justifications femmes/homme. Ici utilisation d’une méthode : Linear Discriminant Analysis. Étant donné deux classes, chercher la direction, l’axe qui va venir distinguer ces deux classes.

En effet, trouve une manière de regarder qui distribue de part et d’autre d’un axe se distribuent les justifications des prédiction selon que produit par un chatGPT masculin et féminin. À gauche, justification féminines, et à droite les justifications masculines qui s’opposent géométriquement le plus.

Regarde les extrêmes pour repérer les stéréotypes. Fourni à chatGPT les 4 justifications. Demande dégager les justifications.

GPT féminin sur les autrices Mobilisation de stéréotypes d’expressivité amotionnelled e sensibilité d’attention à autruit et aux relations souvent associés au féminin.

GPT Masculin sur les autrices : émotions exprimées sans filtre, à l’usage marqué d’émojis, à l’esthétique et à la sphère intime/relationnelle.

Sur les Hommes même chose. Retrouve analyse connue. Discours des hommes moins tourné vers lui même. Moins d’émotions, énoncés plus factuels.

Quid quand dans une condition inconnue. Si idem, ne marche pas très bien. Grandes bandes denses. 

#### Conclusions

Les LLMs ont des compétences socio-linguistiques. On leur propose une tâche et le taux de bonnes réponses étonnamment très proche de celui d’humain. Quand demande d’expliquer pourquoi, montre qu’a su internaliser ce point de vue et reconnaître sur leur discours des stéréotypes existants. Ne le voit pas de la même façon selon qu’il est homme ou femme.

Aimerait ancrer conclusion dans un débat existant. Deux points de vue sur un modèle de langues. Perroquets stochastiques, versus une position qui considère que appris des choses, construit une représentation. Et que mobilisation de concepts de connaissance et agencement. Qui se traduit, certes par une distribution de probabilité sur certains tokens, mais qui découle de ce qui a été appris.

Il y a des représentations qui sont là. On n’est pas juste dans la production de signifiants de manière automatique et probabiliste. Derrière des signifiants que va pouvoir manipuler. Regard rétrospectif sur les raisons qui ont justifié les résultats. Une méthode pas inintéressante pour creuser ces représentations.

Modèle qui a mobiliser dans son traitement des représentations, adopté des points de vue. Et qu’existent et est capable de les manipuler.

Les LLMs mobilisent des représentations pour générer du texte. En fait Les LLMs mobilisent des représentations pour énoncer des discours. Texte énoncé et donc besoin des conditions sociales pour comprendre comment ce discours est produit. Ne peut pas être situé. Point neutre qui socialement ne dirait rien.

Les LLMs sont socialement situés. Le sont même deux fois. Position sociale qui joue à deux moments. Lorsqu’en position de récepteur et réception d’un tweet. Notre position sociale qui va déterminer manière dont reçoit. Théorie du lecteur. En situation d’énonciation, on est également situé puisque conditionné par ça. 

Quand fait des SHS, position sociale énonciation qui va avoir un rôle particulier.

Henri-Irénée Marrou. De la connaissance historoque, 1957

> L’honnèteté scientifique me paraît exiger que l’historien par un effort de prise de conscience, définisse l’orientation de sa pensée, explicite ses postulats...

Discours éminemment subjectif. Mode administration de la preuve pour tendre vers forme objectivisme en sciences sociales, multiplinat les discours éminament subjectifs. En croisant les points de vue qu’arrive à qqchose. Expliciter d’où parle pas juste une politesse, nécessité épistémologique.

Plus largement question des biais. Expliciter et contrôler les points de vue, les sous-jacents, les implicites, les syst§èmes valeurs, les représentations culturelles et sociales. Nécessité épistémologique.

Technologie jamais été neutre, tenir compte façon dont voit et perçoit les phénomènes à travers les technologies une vraie question. Cette question vient d‘entrer dans une dimension tout à fait différente dès lors que peut déléguer ce genre de tâches à des outils.

Si demande qui est ChatGPT, peut aussi se demander Qui suis-je ? et si ne devient pas surnuméraire. Dans cette tâche là, tweets qu’a à peine lu. À peine lu aussi les justifications du modèles. Les a traité de manière automatique. Lecture plus que distante. Délégation maximum envers les modèles. Un contact avec les données le plus faible que puisse imaginer. C’est tout juste même si j’ai programmé les analyses. De plus en plus code assisté, voir complètement produit. Exemple animations. Pris un peu de temps, mais qqs heures seulement. Gain de productivité incroyable. 

À quoi sers-je ? quelle est ma valeur ajoutée dans ce processus ? impression de la voir fondre comme neige au soleil. Si on délègue d’un côté, et s’efface de l’autre. Où en est-on dans l’établissement de la preuve et de faits.

#### Discussion

Quid de la température. Quel impact si dit à la machine

Pas deux requêtes différentes mais la même requête. Au moment où produit réponse, dans le même jugement. Lorsque produit le dernier token, s’appuie sur le tout dernier token. Causalement directement efficace de la ...

Multinationales qui essayent de créer des modèles les plus personnalisés possibles. Nous déchiffrer à partir de nos énoncés linguistiques fait partie du modèle économique. Adaptation qui arrive sans aucun doute à tous les niveaux. Arrivent à nous déchiffrer par nos écris. Risque de rapidement nous trouver submerger par ce type d’agents qui seront partout autour de nous, implémenter dans des robots, nos ordinateurs ou les téléphones et être partout. Nous place dans une certaine vulnérabilité de savoir que peut lire en nous comme dans un livre ouvert.

Beaucoup apprécié utilisation analyse régression linéaire. Pourquoi ne pas avoir utilisé d’algorithme de réduction de dimensionnalités comme disnee ?? ou umap. Et pq pas ??? dans hyperplan.

Aime bien l’idée, ce qu’a voulu faire ici, de travailler avec des méthodes purement linéaire pour essayer de décrire la forme de cet objet. Aime bien avoir en tête l’idée qu’un objet en 1024 dimensions, et accepte que ne voit pas tt. Umpap ou disnee défaut de casser l’objet, déformer l’objet, bien sûr de manière intéressante mais au prix perte information. Alors que regarder l’objet en restant sur les 2D dimensions en le regardant différente manière.

Premier test de turing, partie entre homme et femme. Quid des tweets, n’ont-ils pas déjà été écrits par des machines ? Corpus trop vieux pour avoir pu être polué par ce genre de choses. 2014 et 2020 collecte. Avant IA générative. Mais contenus automatiques, liens de partage, etc. Ceci étant, identité qu’on performe peut varier au cours du temps. Pas de vraie vérité.

Question sur la grammaire, etc. savoir si détecté pour la justification du genre. En fait, très bonne mais grande variabilité par rapport à la langue std. Sans doute pris en compte de manière implicite. Même si pas demandé explicitement de les utiliser. Ex. émogis.

## Transcription automatique des langues peu dotées à l’ère de l’IA

Éric le Ferrand, Buffalo

Langues peu dotées, langues dont les données insuffisantes pour créer des technologies langagières à l’échelle internationale. Idée d’avoir un ensemble de données qui aura une entrée et une sortie.

Comment déterminer qu’une langue est peu dotée, quelle limite ? Sur un spectre entre langue très dotée et peu. Groupe de langues internationales comme anglais, français, mandarin, espagnol. Deuxième cluster langues nationales mais avec beauciup de locuteurs : finnois, letton, turc. Puis plus pt, et premières nations.

Limite que place habituellement au-delà du groupe de langue très dotée (20aine), reste peu dotées mais très hétérogène, situation économiques et sociales très différentes.

Quid des ressources. Accès inégal.

évaluation de la prononciation. Utilisation distance de Levenstein pour déterminer valeur de la transcription.

## Dictionnaire Algonquin

Louis André, jésuiste 1631-1715.

Terminé en 1690. 800 pages. Sans doute plagié ouvrage précédent mais manifestement corrigé.

travail de compilation avec Olivier Dallaire et Jennifer Pothier.

Utilisation de Transcribus.

Révêle des traits culturels des algonquins du Nord. Casse calumet, rompre la paix. Phrase qui revient souvent.

4 tomes de reconstructions de dictionnaire mais n’inclue pas ce travail malheureusement. Impact sur la linguistique des langues historiques. Mais ouvrage posthume paru en 2022.

Sans doute importance du manuscrit pour l’étude des µours et coutumes (ethnohistoire du N-E américain). Texte qui contient des mentions techniques et des pratiques culturelles qui ont probablement disparu. Espère que peut servir aux historiens mais aussi aux locuteurs pour identifier certains pratiques.

## Vers le développement d’une méthodologie de l’exploitation du web comme corpus linguistique

Travaille beaucoup avec des corpus en linguistiques. Oraux, écrits.

Limite des corpus en syntaxe (îlot d’adjoint). besoin enquête psycholinguistique.

Limite des corpus en phonologique (opacité). Exemple nasalisation des voyelles devant consonne nasale. Effacement des consonnes nasales en coda complexe. 

Le web en tant que corpus pour les linguistes. Tellement énorme que peut se demander si ne peut pas offrir des manières alternatives pour obtenir des informations habituellement acquises par l’intermédiaire d’enquêtes psycholinguistique. Est-ce qu’une qualité émerge de la quantité. Trouve de tt sur le web.

En anglais ablaut. Parfois utilisation morphologie irrégulière de manière productive. 

Infication de fucking en français montréalais. Datamining de tweet qui permet d’en trouver. 1200 tweets contenant fucking. Imaginer le temps qu’aurait pris de bâtir un corpus pour observer ces cas.

Exemple de recherche : différences régionales. 

défectivité verbale. Conjugaison défaillante. Trois cas : pragmatique : il neige mais pas de je neige, tu neiges, etc. Pragmatique car différent d’un livre pour enfant. Formes deviennent prévisibles. 

VErbes sans formes finies. Douer, doué. Existe seulement infinitif et participe. Encore une fois pas de difficulté à s’imaginer les formes.

Les trous paradigmatiques. Cas où les locuteurs ne savent quelles sont les formes. Faire frire (causatif). Frire, nous ??? Dans certains cas formes qui existent ou pas. Comportement typique, locuteur qui nous dit je ne le dirait pas comme ça.

Ex en anglais strided ? normalement stridden. Verbe strive très semblable. Mais pas rapporté pb.

Trou à la conjugaison sur le web. Utilisation Google avec guillemets, combiné.

Si le ratio une indication de la défectivité. Confirme ce qui est rapporté dans la littérature. Des explications mais ici, montrer comment peu le quantifier en utilisant le web.

Besoin expertise linguistique pour analyser le web.

Choisir le bon corpus. Poser les bonnes questions, être conscient des biais les admettre.





évaluateurs

- Jean-Philippe Garric
- Diego Zurich
- Mengin