---
date: 2015-12-03
tags: cr, conférence, virtuoso, édition critique, Laura Mendell, Seth van Hooland
---

# cr Virtuoso 3 décembre 2015

Présentations courtes pour commencer à engager le travail sur les éditions critiques.

## Modèles de données et édition numérique, Seth van Hooland

Documentaliste et historien.
Envisager comment les modèles de données ont un impact sur nos pratiques de recherches. En particulier les modèles documentaires pour des collègues en sciences humaines qui entretiennent souvent une relation problématique à l’informatique.

Content providers, service providers qui imposent des outils ou des standards.
Travail dans lequel cherche d’avancer vers une relation plus égale face à l’outil informatique.

Photographie de l’époque où courrier postal standardisé aux EU, envoi d’enfants : flick.com/photos/smithsonian/2584174182
cf. rapport que peut entretenir avec une nouvelle technologie comme RDF.

Accorder un peu de temps aux modèles de données de structuration.
Plusieurs modèles :
Le modèle le plus intuitif est probablement celui du tableau : colonne, entête et ligne. C’est l’approche probablement la plus intuitif pour produire une abstraction des éléments les plus caractéristiques d’un ensemble de boîte de chocolat. C’est le modèle le plus basique employé pour stocker des données dites tabulaires dans des formats de tableur ou CSV.

Mais très souvent ce modèle présente des limites. Quelles sont les limites d’un tel modèle : impose la répétition des descripteurs.
Il n’y a aucune abstraction, chaque nouvelle ligne doit donner lieu à un nouvel encodage. Il n’y a pas de prise sur la cohérence des données.

C’est la raison pour laquelle dans les années 70 on a migré vers les bases de données relationnelles qui présentent un plus fort niveau d’abstraction.
Dans ce modèle on va identifier des entités qui sont indépendantes les unes des autres mais qui sont liées entre elles. Ce modèle est actuellement dominant dans le monde informatique et le restera probablement longtemps.

Mais un tel modèle peut facilement toucher à ses limites. Ces bases de données gèrent très mal le changement. Le monde empirique évolue dans le temps, dès lors que modifie le modèle, doit modifier le schéma, etc.
Par ailleurs, dans le monde du web on a souvent besoin de partager ses données. Or pour cela pas possible de partager directement le fichier. Des fichiers binaires que ne peut pas partager directement comme du texte.
Même si le modèle opérationnellement puissant problématique pour le partage et pour la modification. Pour partager le fichier, une sémantique qui nécessite étude du modèle.

3e modèle de données arrivé c. 2000 XML
Un modèle conceptuel en arbre entièrement représenté par une sorte de science de hiérarchie. Comme un format entièrement fondé sur du texte, résolu le problème de l’interopérabilité technique. Avec XML arrive à dépasser l’interopérabilité technique, mais l’interopérabilité sémantique reste problématique car doit alors faire appel à un schéma. Et prendre le temps de s’assoir pour comprendre la vision produite par quelqu’un d’autre.

Raison pour laquelle nouveau modèle qui cherche à dépasser la limite de la barière sémantique en adoptant un modèle radicalement simplifié conssitant simplement en un ensemble de triplets. On décrit l’ensemble des informations à l’aide d’assertion et on opérationnalise cela à l’aide d’URL.

C’est un modèle extrêmement puissant pour le partage de l’information, mais dans le monde académique comme dans le monde informatique on prétend depuis 10ans que cela va révolutionner le monde. Si le modèle présente beaucoup de choses intéressantes, pb informaticiens se spécialisent dans les modèles, mais n’ont qu’une vision du monde et essayent de pousser les choses dans ce modèle. Or ne traitera pas tout en RDF car chaque modèle a ses avantages et ses désavantages. RDF un modèle du monde sans barrière, n’importe qui peut dire n’importe quoi. Puissant pour l’échange, mais problématique pour la qualité de l’information car peut être perturbant.

Il est donc important que chacun comprenne bien les inconvénients et les avantages de ces quatre modèles conceptuels qui continueront d’exister dans les années à venir.

Image Congo
projet elearning
Une armoire proche du bureau du recteur qui parle d’assurance qualité. Or l’armoire est vide. Cette image représente bien les travaux menés au niveau de la qualité de l’înformation numérique. Beaucoup d’ingénieurs développent des modèles théoriques sans que l’on arrive à rendre cela opérationnel réellement sur le terrain.

Une application concrète de ce modèle de linked data, basée sur le concept de distant reading. Pourrait imaginer que pour affronter un grand corpus et créer des liens entre les données, on pourrait adopter une approche fondé sur la reconnaissance d’entités nommées.
Ici catalogue de la bibliothèque de Notre Dame qui utilise cette technologie pour produire du distant reading.
dh.crc.nd.edu/sandbox/cyl/catalog/

Une technologie devenue très populaire ces dernières années mais en tant que chercheur en sciences humaines, rester critique et conscient.
Exemple Congo, or livre publié au moment où encore propriété privée du roi Léopold, ici l’application propose plusieurs manières de désambiguïser l’entité. Mais ici peut parler de plusieurs choses. Parle-t-on de la république démocratique du Congo de Mobuto, ou Congo Belge, ou encore propriété de Léopold.
Technologies faciles d’accès mais doit prendre avec un certain recul les résultats. D’autant que contexte linguistique et bais langagiers possibles.

freeyourmetadata.org
avec un collègue informaticien livre et tutoriel pour mettre en œuvre nettoyage de données et reconnaissance d’entités-nommées. Corpus d’outils qui peuvent être employés dans des contextes de séminaires pour mettre en place du distant-reading.
Recrute deux postes à Bruxelles.
Un poste après master pouvant déboucher sur une thèse.
Poste de 6 ans pour remplacer ancien collègue comme assistant. Suivi TP étudiants et thèses.

## Discussions

Articulation entre le matériau à constituer en corpus et les outils à développer.
Exposer l’intertextualité.

-   Cette intertextualité est-elle produite dans le projet et ensuite exposée
-   Comment réglez-vous la question du rapport entre les textes et les gravures.

Faire ressortir des choses par traitement algorithmique et points d’accès.
Cf. Viral text <http://viraltexts.org>

Quel conseil donnes-tu à l’ULB quand des collègues viennent te voir en disant qu’ils ont le produit parfait. Parviens-tu à résister aux informaticiens.

Lorsque commence à parler de projets d’édition ou transcription de sources, s’engage dans des projets sur plusieurs années. Pour l’accessibilité serait plus simple de travailler avec un simple éditeur texte. Mais comme peu de gens veulent passer du temps cela, parfois de nouveaux produits auront des interfaces plus agréables à utiliser. Faire la distinction entre un environnement de production et un environnement où l’on dispose de la parfaite maîtrise de la qualité des données. Ensuite déterminer comment on intègre la dimension collaborative par l’intermédiaire de liens. Actuellement wikipédia perd en qualité par rapport à Wikidata. Commen nombreux liens ne seront peut-être plus disponibles dans qqs années, faire en sorte que travail s’intègre dans un environnement stable de sorte que sources fiables, et couche de publication.

Application informatique rapidement dépassée. Beaucoup de projets où RDF pour encoder l’information. Problématique au niveau de la qualité de l’information. Avant tout savoir ce que l’on veut faire exactement. Souvent difficulté quand travaille avec les historiens et chercheurs.

Jean-Claude Guédon : un problème fondamental dans vos deux présentations d’une part la tension quant à la nécessité de maintenir une cohérence et une stabilité et de l’autre côté les possibilités d’encourager la collaboration et logique distribuée.

Comment fait intervenir utilisateurs postérieurs.
Quels sont les moyens d’étendre le travail.

= résumer en quelques mots le problème de base de l’informatique pour traiter la réalité informatiquement. Doit avoir recours à un modèle de base de la réalité et donc des standards, etc.

JCG Oui mais aussi avoir affaire à des acteurs parfois inatendus. Vieille question qui est celle de l’académie. Quels sont les pairs autorisés à intervenir. Une question sociale ici.
On a réglé la question des pairs d’une très mauvaise manière pour les éditions savantes. Mais même genre de système. Ce que vous présentez peut être envisagé comme les formes à venir des publications dans les prochaines années quand aura abandonné le livre monographique ou l’article papier.

## Anthologie palatine

Une énorme collection d’épigrammes, poèmes caractérisés par leur brieveté. Conçus pour être gravés sur la pierre.
Devient un genre littéraire en soi à l’époque hellénistique. Déplacement du genre épigraphique au genre épigrammatique.

Fin de la période constitution de collections de ces épigrammes. La première celle de Méléagre. Une collection raisonnée cad que organisé de manière spécifique avec un réseau proto-hypertextuel.

Un genre essentiellement inter-textuelle. Un art de la variation où les auteurs réutilisent des topoï et font référence les uns aux autres.

Constitution d’une base de données. Se concentrent sur les premiers textes. Manuscrit qui contient une grande quantité de scholies soit comme commentaires ou informations concernant les auteurs, sous-titres, etc. Un ensemble d’informations que l’on voudrait intégrer dans la base de données qui contiendra donc les textes mais aussi tous les marqueurs de la réception des textes tels que les connait aujourd’hui.

Face à un tel matériel, ne pouvait que faire du numérique. D’un point de vue ontologique, tout est comme si cela était du numérique. Des fragments en liens les uns avec les autres, une idée 4 s. avant JC.
L’autre élément purement numérique, l’absence de notion d’auteurs ou d’originalités. Des attributions mais qui deviennent des mises en scène. Un esprit anthologique qui est exactement ce que nous vivons à l’ère du numérique. Les commentaires marginaux, etc.

Besoin heuristique car le fait de baliser nous permettra de voir des choses qui sont absentes dans le document. Enfin, le besoin de mettre en valeur ce patrimoine qui est très présent dans l’imaginaire culturel.

Objectifs :

-   transcrire les scholies
-   faire des traductions
-   d’aligner les traductions si possible mot-à-mot pour enrichir les bases de données qui sont insuffisamment riches en français.

L’intertextualité existe grâce aux formes d’éditorialisation. Rendre compte de l’imaginaire anthologique.
Des topoïs qui circulent dans l’imaginaire collectif et que voudrait réinscrire dans la culture collective.

Cf. amoureux devant la fenêtre : cf. Barbier de Séville, tradition littéraire mais aussi populaire.
Stratification d’imaginaire qui s’est faite en deux millénaires que voudrait mettre en avant. Il ne peut donc pas s’agir de quelque chose qui s’adresse seulement à des héllenistes.

On va donc produire une base de données ouverte. Pour la traduction, on essaye de contacter des lycées pour produire des essais de traduction. Idée de laisser le plus ouvert possible la base de données.
La question sera donc de savoir comment gérer les niveaux d’autorité. Mais dès lors que l’on identifie les contributeurs et leurs contributions possible de produire plusieurs représentations.
Une API ouverte : tout le monde doit y avoir accès.

Base relationnelle
Production de XML.

<https://3.14159.ninja/naos>

## Interactive with Print

[Interactive with Print](http://interactingwithprint.org)

Historiens, travail pour repenser la monographie savante.
Ce qu’avait conduit avec ce groupe de recherche qui abordait l’histoire de l’imprimé.
Comment se retrouver historiens, études littéraires, histoire de l’art.

Interacting, terme issus du monde numérique, mais comment l’historiciser. Interaction entre médias au 18e :

-   objet et imprimé
-   personne et imprimé
-   comment structure relations entre personnes et modes de pensée.

Organisation de multiples expositions avec étudiants commissaires. Bâti notre propre communauté. Argent du CRSH, que faire : revue savante ? livre ?
Un des membres Andrew Piper qui faisait des DH.
Comment penser interaction entre l’imprimé et le web.
Andrew Piper avait l’idée d’un multigraph. Repenser notre manière de communiquer en tant qu’universitaires ou de penseurs. cf. [Re:Enlightenment Project](http://www.reenlightenment.org) idée de reconstituer République des lettres et manière de communiquer.

Voulu trouver des relations entre l’imprimé et une plate-forme Web 2.0. Voulait créer quelque chose entre une monographie et le volume édité. Nombreux auteurs, une idée qui créée quelque chose de nouvea, 22 chercheurs invités. Une communauté de chercheurs sans hierarchie.

Processus
<http://interactingwithprint.org/project/multigraph>
Trois étapes dans le processus : semenses, greffes, presses.
Chaque auteur devait créer une semense sur un concept clef de notre discipline (paratexte, théâtre, etc.) sans être spécifique mais pour repenser notre discipline. Ne pas concevoir ce court texte comme quelque chose d’abouti ou de fermer, mais plutôt comme un élément qui donne lieu à des débats.
Plusieurs semaines plus tard, enfermés dans un hôtel pour chaque semense et en faire des greffes à plusieurs. Une expérience incroyable pour retravailler le texte d’un auteur par les autres. Ensuite passait à un autre groupe. Textes qui devenaient des textes collectifs proprement dits.

Une forte sociabilité est née à cette occasion.
Après ce multigraphe, le processus de pressing. Aurait pu conserver les choses sur le web. Mais on a considéré qu’en sciences humaines, le web restait le moyen de communication clef. Processus de transformation en livre en cours. Accepté par presses de Chicago.
Comment présenter la réalité des 22 auteurs sur la couverture.

Parallèle entre la production de connaissance à l’époque moderne. Connaît bien l’importance de la sociabilité dans la République des lettres. Le fait de se réunir physiquement à plusieurs occasions qui a permis au projet de réellement aboutir. Très impressionné par le fait qu’autant de personnes aient accepté de travailler de manière aussi forte pour quelque chose qui ne serait pas réellement valorisé.

Comment comptabilise notre contribution, comment traverse les limites disciplinaires, comment partage le travail.
Objectif de produire une sorte de synthèse, processus qui a permis de construire ce genre de choses. Le fait d’avoir bâti une communauté très important, partage de vocabulaire. Évaluateurs eux-mêmes surpris. Un effet de l’interaction avec l’imprimé. Car c’est l’imprimé qui a fait l’auteur.

Discussion
Frein le plus évident et le plus fort pour ce type d’activité. Tout le monde reconnaît que ce type de travail celui qui a le plus d’impact sur l’activité des chercheurs par rapport à la publication d’article ou de chapitre dans une monographie. Pour autant, un travail qui n’est pas formellement reconnu par l’institution. Pourtant un travail de ce type, prend autant de temps que la rédaction d’un simple article. Important de dire que ce type d’initiative qui fait le plus avancer la recherche. Il est temps de dire que plus possible.

Comment écriviez-vous à plusieurs ? Un secrétaire ? Déjà une expérience d’écriture collaborative. Semenses écrites seules. Mais rôle important de l’éditeur à chaque étape du processus. L’auteur ne faisait jamais parti du groupe qui discutait, et ce n’était plus son texte. Idée de former successivement des groupes pour retravailler les textes, et toujours quelqu’un responsable de prendre en notes les points clefs, et un éditeur qui avait le rôle de mettre en ordre tout l’ensemble.
Enfin une relecture linéaire pour l’uniformité. Introduction qui décrit l’ensemble.

Serait intéressant de pouvoir retranscrire numériquement l’évolution de ces textes dans un site. Un peu à la manière de l’historique des articles de wikipédia. Donnerait une dimension dynamique à ce travail.
Un modèle ici dans le logiciel libre, ou avec Git. À nouveau verrait ici que dans le numérique, à l’inverse de l’imprimé, l’auteur régresse.

Ce qui était important pour le groupe, c’était de voir quel était l’impact du numérique sur la recherche.
Avez-vous pensé à une étape suivante de soumission aux commentaires et de réintégration des commentaires.
Deux versions papiers proposées. Aurait été intéressée par la soumission aux commentaires, mais pas tout le monde pour l’essentiel pour des questions de maintenance.

Romantic circles où essai de sections pédagogiques, réutilisation de ressources dans un contexte pédagogique. Jean-Michel Salaün qui donne beaucoup de textes à commenter aux étudiants. Un travail de collecte.
<http://dhdebates.gc.cuny.edu>

Ce qu’avez réussi à faire, une sorte de métastabilisation de quelque chose mais qui demande immédiatement après une refonte et un réemploi. Finalement notre vie intellectuelle dont on parle et qui se matérialise par une conversation. Numérique qui rendrait plus accessible ces questions.
Ceux qui auraient besoin d’un plan d’affaire pourraient garder la main sur le plus haut niveau de validation. Il y a donc moyen de conjuguer le côté pécuniaire et le côté libre.

Les groupes de chercheurs qui développent chacun pour leur besoin particulier une plate-forme. Or besoins qui se recoupent, et déjà un cimetière du web avec des projets financés.
Les chercheurs devenus par la force des choses des éditeurs, alors que dans le monde imprimé des presses universitaires. Ou seulement quand veut imprimer un libre.
Manque de publishers pour offrir solution matériel. Aime beaucoup de ce point de vue le projet Zooniverse. Ex. extraction de données métérologiques.
Même mis à disposition une plate forme

Édition devenue logicielle
Exemple de SynopsX

Plate-forme le web
Les éditeurs universitaires peuvent aller dans cette direction là. On leur donne la possibilité, déjà expérience avec Parcours numérique. Peuvent considérer qu’important d’aller dans cette direction.
Si ne le font pas vont mourrir. Et par ailleurs d’autres instances éditoriales qui vont émerger. Cf. Wikipédia une instance éditoriale d’exceptionnelle qualité, GitHub un système éditorial. La question de savoir si les anciennes maisons d’édition veulent remplir la tâche nécessaire aujourd’hui.
N’étant pas accompagnés par des maisons d’édition, cherche à produire des logiciels open access. Or très difficile pour les éditeurs de financer ce genre de produit en laissant utilisation par les autres.
Une responsabilité des éditeurs, un modèle économique qui résiste derrière. Il faut arrêter de financer le papier, et les locaux pour conserver les cartons de papier.

Un aspect très intéressante avec Multi-graph, extension à laquelle dépasse modèle classique édition. Cf. Wikipedia. Me souviens premier article dans MLA, alors assistant et pas suffisament argent. Profession magazine faisait un editing incroyable. Chaque année MLA avait une partie où verre de vin. Alors rencontré éditrice, et remerciait. Répondait que beaucoup d’auteurs se plaignait. Un auteur de science-fiction. L’éditeur du MIT expliquait que quand avait nouveaux auteurs aide pour réécrire le livre. Un réel effort collaboratif.

Sauf que ne veut pas considérer cela, particulièrement en France où notion romantique de l’auteur. Si pense au rôle des journaux aujourd’hui, le problème est que l’édition numérique est plus près de ce que l’édition des revues était au 18e siècle. On s’est cristalisés sur une sorte de circulation du savoir statique et stabilisé alors que la naissance de la revue consistait plutôt à faire circuler le savoir et à l’ouvrir.
Culture hellenistique numérique en sens.

JCG pour revenir sur cette question du destin des presses universitaires, on a oublié un partenaire important ici qui est la bibliothèque. Or la reconfiguration de ce modèle devrait probablement se faire à la convergence entre les bibliothèques et l’éditeur pour créer les logiciels et de l’autre la bibliothèque. Notion de fonds.

Au lieu d’organiser des antagonismes entre sections, probablement d’autres moyens de collaborer contre les hiérarchies, d’autres modèles plutôt que la fusion, etc.

## Laura Mendell

Francis Gendra secrétaire faculté :

Très heureux d’être ici à l’occasion de cette journée consacrée aux changements dans le domaine de l’édition. Des questions qui nous intéressent, nous médiévistes, depuis le début des années 90 avec la nouvelle philologie avant même l’irruption de l’internet. Changements que ces nouvelles technologies introduisent dans l’échange des savoirs. En tant que médiéviste, bien évidemment particulièrement sensible au rôle du médium dans ces évolutions.

Des questions essentielles à penser car aussi des changements qui doivent avoir lieu dans le cadre universitaire.
Penser le statut de la monographie. Ne pas le subir.

Laura Mendell directrice initiative for Digital Humanities, media and culture
Apporte perspective de première main sur cette question.


After the Scholarly Monograph
Présentation de son dernier livre.

Numerous articles. What literarly history is ?
Directrice
Deep code documents for data-mining and OCR.

Manifesto on the consequences and effect of digital medium.

New forms of scholarship are reshaping the format and forms of scholarly communication.
À quoi doit ressembler à terme la monographie scientifique à l’ère du websemantique etc.
Doit d’abord ressembler à un environnement digital.

Transformer argument long en un objet dynamique qui soit réellement dialogique. Pourrait l’appeler un multi-graph, une expression qui contraste avec celle de monographie. Ici idée un peu différente que celle du projet présenté tout à l’heure.

Proclamer la vérité d’une personne. Pensée monographique conventionnelle.
Datamining et visualisation. Pensée positiviste de la littérature plus valorisée par les institutions qui coupent financement pour les humanités.
Savoir si mes arguments sont vrais ou faux, le moins interessants en ce qui les conserne. Une sorte de visualisation qui rend accessible un ensemble d’information.
Offrir l’occasion pour définir de nouvelles formes nouveaux contre-arguments qui sont complémentaires pour produire la vérité.
Complémentarité.
Nous avons l’opportunité de créer des choses différentes.
Savoir si numérique peut introduire nouvelle forme d’objectivité ou non, mais aussi possible que permette de supporter nouvelles subjectivités.

Stanford univ press, etc.
Annoncements qui disent que ne vont plus seulement produire ebook mais nouveaux environnements numériques comme Scalar press.
Permet publication de clics dans la monographie. cf. We are all...
Media commons press une autre expérimentation majeure dans le domaine des monogrpahies. Utilisé par MLA.
Ex. Planned Obsolescence, première monographie publiée dans cette plate-forme. Permet aux lecteurs de s’engager dans des discussions autour du texte. Permet à la monographie de devenir un espace de travail.
Maintenant disponible en copie physique ce qui suggère un problème dans ces expérimentations.

Conçu de sorte que les comités peuvent réviser l’ensemble des contributions et ses commentaires. Mais est-ce réaliste ou ont-ils réellement le temps de le faire.
Quelle reconnaissance professionnelle.

Mode du commentaire coûte tant de temps. Vaut-il de l’imprimé.

Jason Midle, Complex TV publié avec Scalar
Par les numéros de page réalise qu’une instance Scalar d’un livre physique.
Pas plus que d’ajouter du contenu numérique à un contenu imprimé.

De même Comment Press
NYU Press
Amazon ebook.

### Présenter des initiatives qui cherchent à remédier à ces problèmes.

CWRC Writer
Un travail pour rendre possible des commentaires et des annotations qui soient ensuite partageables.
Conçu sur la base de Shared canvas.
Open Annotation initiative qui a produit des normes pour la description.

Existence de données disponibles dans le LOD réutilisables.
Datahub
Nouvelle initiative au Canada LINCS ouvre beaucoup de promesses. Se propose d’agréger des agrégats académiques disponibles qui peuvent être mobilisés dans différents contexte.

### Monograph as VRE

Voyant tool
Jeffrey Rockwell et Sinclair, outil qui permet à des personnes qui n’ont aucune connaissance technique de visualiser et explorer leurs contenus textuels.

Hermeneuti.ca
exploration de la campagne de Barack Obama
Une fenêtre ouverte livre sur les données.
Un lecteur peut se demander dans quelle mesure la répétition d’un terme est plus significative que tel autre.

Un environnement de recherche plutôt qu’une page statique.
Malheureusement lecteur qui ne peut rien ajouter à ce qu’il lit. Ne peut pas se loguer en un endroit quelconque.
Serait intéressant de pouvoir enregistrer son interprétation des données dans l’œutils.

Par exemple
Just a comparison
Permet comparaison d’un texte et collation de la manière dont diffère.

ACR catalogue ?

Image comparison
Comment monographie empêche échange scientifique.
Dans son essai fameux Rhetoric of temporality, dans Blindness and Insight de Paul de Man, explique que texte ne permet pas de produire des symboles mais seulement des allégories.
Son argument crucial dans l’histoire du développement de l’ironie romantique.
Pour lui l’écrivain romantique déconstructionniste lui aussi.
Or il modifia sérieusement la citation
Probablement d’autres auteurs ont relevé cette mauvaise citation, mais aurait aimé une infrastructure qui permette de disposer d’une note.
Possibilité de visualiser autres versions de la citation. Idéal de fenêtre lives qui pourraient être présentées comme aspects de la monographie.

Pensée monographique
What stylistic and thematic elements, exactly ?
http://dhmc.tamu.edu
Données aujourd’hui disponibles.
Visualisation qui représente œuvres hommes ou femmes. Même si visualisation dynamique n’aiderait pas à travailler l’objet. Car quelles sont les données utilisées dans cette visualisation ou dans la constitution du corpus.
Une décontextualisation des termes utilisés pour dénoter les genres.
Nancy Amstrong social constructed feminim
David Hoover analyse confrontant stéréotypes de genre.
Jan Rybici email to Mandell 2015

échange sur la question que pourrait facilement reproduire avec un multi-graph dynamique.

Susan Brown
interaction as further thought
Où pourrait travailler en changer paramètres.
Autre possibilité manipuler les ensembles de données elles-mêmes. Quelques journaux envisagent déjà la publication d’ensemble de données accompagnées de commentaires méthodologiques et de code pour les manipuler.

Methods Commons

Jeffrey Rockwell
https://www.computecanada.ca/research/humanities/
https://www.computecanada.ca/research-portal/
http://hermeneuti.ca
HTRC portal

Sticky Annotations::Shared Workspace
Data Analytics Window::Saved and Changeable Parameters

Suppose que soient valorisés et qu’en tienne compte dans l’évaluation.

Journal of DH
Crowd sourcing peer reviewing
Digital humanities now.


"Nothing can please many and please long but just representations of general nature"

Pour transformer monographie en multigraph doit avoir envie de changer, mais valeurs pourrait être considérable.

Corp writer and Susan Brown, use of TEI

## Discussion

Question de la pérennité.
Usage standards comme TEI et Open Annotation
Dès lors question obsolescence peut être réglée même si plus tricky.

Plus question établir vériter mais construire des narations.
Créer plusieurs niveaux significatifs qui pourraient être mis ensemble.
Idéalement ensemble données quantitatives qui donnent l’oportunité d’opérationnaliser les choses. Possibilité de paramétriser les choses. Mais besoin de le faire dans un lieu et de pouvoir travailler dans le même ensemble de données. Besoin d’une infrastructure.

Cette question de la diversité, au niveau épistémologique ou ontologique.
S’agit-il simplement d’une possibilité épistémologique ou bien d’une question ontologique. Andrew Piper à McGill a eut cet argument exactement.
- épistémologique seulement à voir avec la réception.
- ontologique pour ??

Encore quelque chose qui peut être discuté collectivement.
Ce genre de conversation que voudrait avoir qu’appelle-t-on un problème esthétique par exemple ?
Finalement ce genre de choses que fait déjà par exemple critical inquiry où possibilité d’échanges très approfondis.
Christopher Newfill argument possible avec commentaires.
Serait très intéressant que ces choses puissent être disponible ensemble.

Question du dissensus.
Si généralise la question quand publie une monographie alors plante réellement un dissensus par rapport à ce qui a été dit précédemment. Comment feriez vous pour faire émerger ce dissensus.
L’environnement numérique est à cet égard probablement plus favorable que celui de l’imprimé. Johana Drucker a designé un espace appelé interpret où possibilités de plusieurs interprétation dans le même environnement.

Nous sommes dans le cadre d’un modèle d’édition où la temporalité pas celle de la discussion.
Brown Université étude collaborative de Dickens. Avec des critiques littéraires, mais aussi des urbanistes, etc. Possibilité d’envoyer des signaux aux autres personnes.
Sorte de chose que aimerait imaginé, or fait dans les 90s.
MLA media commons ce qu’essayent de faire.

Possibilité de disposer de profils, et infrastructure où publie ensemble code.

Comment penser le lien entre les millions de monographies qui sont dans nos bibliothèques et les nouvelles formes de multigraphes dont vous parlez.
Comment va-t-on faire la connexion entre elles ?
Car les nouvelles monographies sont pourtant fondées sur les anciennes.

Sans doute important de numériser tout ce qui a déjà été imprimé. Google books a déjà tout numérisé. Hati trust, grand challenge de sortir le texte des pages. OCR pour le faire.
Premier multigraphe qu’aimerait écrire si personnes volontaire. Livre sur ...

Quelles formes d’attention émergent.
Digital environnements.
Formes hypertextuelles où pourrait faire se rencontrer des arguments distincts et le lecteur pourrait décider à ces endroits où suit et alors bénéfice.

Question sur le fait
Swiss plots on the level on the interface, best possible balance between the traditionnal narrative, and going on the long go.

JSTOR recherche nouvelles interfaces pour arguments longs
Si revient à la forme de l’argument long, alors de nouveau redevient prisonniers de la forme imprimée.
Ne serait-ce que longueur de l’ouvrage liée à des conditions physiques.
cf. Foucault, tester existence d’episteme.
DH aurait beaucoup intérêt à prêter attention plus soutenue à la question de l’échelle, granu


What could be the infrastructure for such a research environnement.
How far do you think that the Semantic Web can support such environnement ?
Semantic web is a real proposition in the field. It seems that the formalisms brings by ontologies allows different representations of the same things and connect them. It could also allow to express dissensus.
But still researchers not that much engaged with semantic web.
LOD much more
Before question of ontologies, real investisment in autority files, and naming of resources.

En un sens pourrait considérer le web sémantique comme un gigantesque multigraph.
Sans doute penser le multigraph comme agonistique par rapport à l’argument long de la monographie. Un environnement de réseau curated.

Utilisé par les juristes Westler X database
déjà possible référer articles, etc.
Complexité de cette base de données ferait exactement ce que voudrait faire pour les monographies.
Wesla system

@mandelic
