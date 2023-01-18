## Présentation

(Elena Pierazzo est professeur à Tours, au Centre d’études supérieur de la Renaissance, où elle est responsable de la Mention Humanités Numériques, du Master Intelligence des données de la culture et des Patrimoines et du Master Médiation Numérique de la culture et des Patrimoines. Après un doctorat à l’Ecole Normale Supérieure de Pise en philologie italienne en 2001, elle a travaillé à l’Université de Pise jusqu’en 2006 ; a été Research Fellow à l’Harvard Center for Italian Renaissance Studies « Villa I Tatti » de Florence (2002-2003) ; puis elle a travaillé au King’s College London (de 2006 à 2014) avant d’être élue professeur à l’Université Grenoble Alpes. De 2012 à 2015, elle a en outre été présidente de la TEI et en 2019 a co-présidé la conférence DH à Utrecht.)

## Rmq



Merci beaucoup Elena pour cette très intéressante présentation qui offre non seulement un état de l’art sur les enjeux de l’édition génétique numérique mais dont la portée générale ne se limitait pas aux aspects techniques. **D’emblée je dois reconnaître que je ne suis pas un littéraire et surtout pas spécialiste de critique génétique textuelle.** Je suis certain que d’autres sont certainement beaucoup plus compétents que moi parmi le publics et qu’il n’hésiteront pas à t’intérroger. **Sans oublier que ton argument reste que l’on manque de théorisation et qu‘il ne s’agit pas difficulté technologique, mes questions porteront plutôt sur des aspects méthodologiques et relatifs à l’utilisation de langages de balisage ainsi qu’à la production des interfaces.**

**Le domaine des éditions génétiques numériques est sans doute l’un de ceux où l’application de la Text Encoding Inititiative présente je crois, encore aujourd’hui, le plus de défis.** En regardant ta présentation, je me suis souvenu de la première fois où je t’avais entendu – il me semble que c’était à Lyon, tu étais alors encore au King’s college – et tu y avais présenté des recherches sur l’articulation entre le traitement de la dimension topologique de la page et le traitement du texte avec la TEI en lien avec le travail du SIG sur la représentation des manuscrits et la génétique textuelle. Ce sujet occupe donc tes recherches de longue date, comme en témoigne plusieurs publications, mais aussi dans une certaine mesure ton ouvrage sur la théorie de l’édition numérique qui me semble-t-il découle directement de cette riche confrontation à un matériau textuel qui résiste à la modélisation. **Tout l’intérêt du propos, c’est qu’il ramène au cœur de la discussion, la matérialité du travail de la littérature, mais aussi du travail savant lorsqu’il s’agit de produire une édition critique.**

### Question des limites de la TEI. Qu’est-ce qu’un texte réellement ? OCHO

Dans ta communication, tu montres que si le rendu ultra-diplomatique parvient à rendre de manière aussi mimétique que possible la disposition de l’écriture, il lui manque une dimension fondamentale pour pouvoir rendre de manière satisfaisante notamment les brouillons : la dimension processuelle, dynamique d’écriture. Et qu’ainsi, transposer le texte sur la page se révèle bien souvent décevant.

Une des choses qui m’avait frappé dans le travail conduit avec le SIG sur la génétique, c’était qu’il introduisait dans la TEI une approche topologique ou "géographique" fondée sur structures surface, zone et line qui diffèrait complètement du modèle linéaire du texte retenu en premier lieu par la TEI. 

Sans nécessairement vouloir réouvrir débat sur la représentation du texte comme un modèle d’objets hiérarchiquements contenus OHCO, il convient tout de même de constater que l’on a là deux points de vue en partie irréconciliables sur le texte. Deux visions qui si elles sont toutes les deux inclues dans la TEI nous oblige en partie à choisir. On peut bien sûr relier ces deux visions sur le texte par des mécanismes de balisage externe, et déterminer l’ordre d’affichage ou de restituttion du texte indépendamment de celui de l’encodage pour échapper au paradigme de la page, mais **dans ce cas, reste-t-on réellement dans le modèle hiérarchique, ou bien n’entre-t-on pas précisément dans une autre dimension du texte qui l’envisage comme un graphe ?** Depuis quelques années la TEI a cherché à se détacher du modèle XML, quelles avenues vois-tu dans ce domaine ?

R.



### Ma deuxième question porte sur le traitement algorithmique de l’édition

L’utilisation de logiciels de collation automatique est particulièrement intéressante dans le contexte de ce genre d’édition, mais tu pointes plusieurs inconvénients relatifs à leur utilisation. D’une part, une dissociation du contexte de la page, et dans d’autres approches la nécessaire création d’avatars de textes sans que l’on puisse leur donner une justification scientifique.

En même temps, en insistant sur la production d’interfaces, tu laisse entrevoir un modèle d’édition numérique dynamique, ou l’on pourrait déléguer à la machine le soin de produire différents états de l’édition parmi lesquels le lecteur pourrait choisir. 

L’édition devient alors dynamique, reconfigurable par les lecteurs pour l’étude et l’analyse du texte.

Quelle place pour l’auctorialité dans ce genre d’édition. Dans quelle mesure d’après toi la production d’une telle édition consiste en une sorte d’éditorialisation ?

### Le modèle source/output et la textualité comme processus

matérialité physique de l’écriture et de la littérature, et plus généralement travail intellectuel et sa transposition numérique.

L’**Edition génétique envisage la textualité comme un processus**. --> Il s’agit selon toi de savoir comment évaluer les ms de manière qualitative et faire comprendre des processus de composition. Et tu expliques que le nouveau médium numérique pourrait offrir de nouvelles possibilités et des solutions à ces questions théoriques qui caractérisent la critique génétique.

- représentation des brouillons (facile car transcription reste obligatoire, une activité herméneutique force chercheurs et chercheuse s’intéroger sémiologie)
- représentation du processus de création de l’écrivain (ordre, phases élaboration)
- représentation de l’évolution de l’ouvrage (diachroniquement évolution ouvrage ou plusieurs)

Durabilité technologique, logique et sémantique fondamentale. vs Traduction dynamique de la page par l’interface. Mais dans ce cas quid de la stabilité privilégiée par la TEI dans la restitution du texte ?

> **Modèle de données source/output** qui sépare fonctionnellement la source des modèle de publication. Garantit survie des sources mais la durabilité technologique ne peut pas suffir. Il faut également une durabilité logique et sémantique.

Le **Modèle source/output en séparant le contenu et la forme précisément, ne pose-t-il pas ici problème ?** Il renvoit à l’interface le soin de traiter la page et l’édition mais n’est pas pris en charge par un modèle structuré ou une norme. Dès lors que l’édition devient fortement logicielle, ne faut-il pas inventer ou imaginer des standards qui prennent en charge la présentation à la fois du point de vue logique et sémantique pour faire face à un réel risque d’obscolescence technique ?

Comment s’assurer aussi de la durabilité de ces interfaces face au caractère très évolutif de HTML5. Peut-on seulement confier cette partie à HTML5 et JavaScript ?

--> Format plus un pb. Modèle de donnée qu’un pas important. Recherche interface qu’à ses débuts.

Est-ce souhaitable ? 

> numérique ne doit pas être seulement transposition d’un modèle analogique dans le monde numérique mais doit explorer possibilités nouvelles

Normalisation qui pourrait brider les dynamiques d’innovation, possibilités nouvelles. 

Dimension logicielle de l’édition.

Une des promesses édition numérique, l’affranchissement des éditeurs. Mais si caractère logiciel plus complexe, est-ce encore possible ?

### Les enjeux de la transcription automatique

Transcription automatique, reconnaissance des mains. Changement manière concevoir travail éditorial. Gérer ces changements en tranvaillant sur la théorisation et modélisation sémantique des brouillons.

De même transcription automatique semble présenter de nombreuses perspectives nouvelles sur l’extraction de traits pour présenter l’édition.

---

Discussion

Exploitation des données que nous produisons et où se situe acte herméneutique. Possibilité lecture distante. Mais quelle place du lecteur et du nous ocmme être humain jusqu’où nos litteraties peuvent-elles aller. Car comprendre ensemble présupposés nous mènent trop loin. Où se place l’acte herméneutique, quelle est la place du lecteur. À quel point le lecteur produit-il l’éditorialisation ?

Acte épistémologique de créer une visualisation n’empêche pas d’avoir d’autres actes herméneutique. Ce que met dans le balisage, mais aussi ce qui se passe quand fait une publication d’un texte avec sa mise en page. Je suis une philologue, ne présente pas forcément toutes les interprétations du texte, mais seulement avec les outils que peut utiliser ou pas. Présenter des actes, et des visualisations, mais aussi permettre le type d’utilisation que tu veux faire toi. Sans doute pas si différent des lectures que faisait avant.

D’accord sur le fait que des algorithmes que ne contrôle pas du tout, ou bien que l’on ne comprend pas. Peter qui expliquait comment faire des réseaux de neurones. Où va-t-on s’arrêter ? une conversation que devrait avoir. Quelles sont les compétences de l’éditeur savant sur le texte numérique, compétences que veut produire. Plusieurs questions sur lesquelles devrait avoir des réponses partagées. Intelligence de données Tours, inclue API, ontologies, web de données, Deep learning car pense qu’obligatoire. Mais pas solution ajouter trois années de formation pour apprendre à faire tout cela. Toutes les sociétés ont défini un programme primaire pour comprendre société. Où est la place de l’informatique pour comprendre la société informatique. Besoin pas seuleemnt pour interpréter le texte mais interpréter notre vie.



édition génétique...

En génétique ne parle pas de texte à la différence de la philologie comme ne parle pas de variante mais de versions mais d’états du texte. Car des échelles différentes.

Axes syntagmatique et paradigmatique. Façon dont réécrit le texte, autre façon dont texte se reconstitue, l’un est liée à l’autre.

trait qui peut avoir valeur particulière. Ms hypertexte latent avec différentes strates, et tous ces objets sont en relation. La difficulté de pouvoir séparer, isoler toutes ces relations pour pouvoir constituer une génèse. Difficulté de l’édition de croire que va pouvoir produire une genèse avec toutes ses versions et ses états. Alors que genèse d’un motif. Je crois que n’arrive pas à dépasser cet état là.

Édition multi-échelle, mais pour moi le manuscrit, c’est un hypertexte. Va devoir trouver dans toutes les couches du ms un motif qui se répète ailleurs. Donc doit pouvoir restituer une échelle de lecture. Car édition génétique produit une autre lecture sur le processus scriptural.







MS de Proust, parcours chemin, diagrammes. trajets, séquences d’écriture.

- SIG Manuscrit. Ce *Special Interest Group* a élaboré dans les années 2007-2011 une proposition pour le codage des  manuscrits modernes et des éditions génétiques. Cette proposition a été  réélaborée ensuite par la TEI qui l’a incorporée en décembre 2011. Voir  <[www.tei-c.org/SIG/Manuscripts/](http://www.tei-c.org/SIG/Manuscripts/genetic.html>.
- cf. Pour une réflexion sur cette question, voir Elena Pierazzo et Kathryn  Sutherland, « The Author’s Hand: from Page to screen », dans *Collaborative Research in the Digital Humanities*, dir. Marilyn Deegan et Willard McCarty, Aldershot, Ashgate, 2012, p. 192 *sq*. ; Françoise Leriche, « Quelle édition pour quel public ? », *Recherches & Travaux*, no 72, 2008, [>.

- Julie André and Elena Pierazzo, “Le codage en TEI des brouillons de Proust : vers l’édition numérique”, *Genesis* [Online], 36 | 2013, Online since 09 July 2015, connection on 28 January 2021. URL: http://journals.openedition.org/genesis/1159; DOI: https://doi.org/10.4000/genesis.1159



@todo Fait d’ailleurs penser à la distinction parfois identifiée entre HTML5 et SGML. Modèle de données qui distingue HTML5 des langages structuré.



http://shelleygodwinarchive.org/

3 tâches : représentation brouillon, processus de création écrivain, représentation de l’évolution de l’ouvrage. Premier seulement pris en charge de manière courante. Argument que manque de théorisation et non pas difficulté technologique.

--> quelle std ?

2014 envisageait intégration actes éditoriaux.

Patrick Sahle



**Modèle de données source/output** qui sépare fonctionnellement la source des modèle de publication. Garantit survie des sources. Durabilité techno ne peut pas suffire. Durabilité logique et sémantique.

Format plus un pb. Modèle de donnée qu’un pas important. Recherche interface qu’à ses débuts.

> numérique ne doit pas être seulement transposition d’un modèle analogique dans le monde numérique mais doit explorer possibilités nouvelles

Une des promesses édition numérique. Affranchissement des éditeurs. Mais si caractère logiciel plus complexe, est-ce encore possible ?

Journées Mutec de 2010 (où rencontré Aurélien) ?

Transcription automatique, reconnaissance des mains. Changement manière concevoir travail éditorial. Gérer ces changements en tranvaillant sur la téhorisation et modélisation sémantique des brouillons.

Edward Vanhoutte 2007

> This and other digital editions based on the separation of source and output, while still aiming at presenting traditional editorial formats, are clearly already something else, in search of a theoretical definition. I have called them ‘paradigmatic editions’ (Pierazzo, 2014b), as the choices offered to the reader are collocated in the paradigmatic axis, the axis of variation, but another name could be ‘generous editions’, in the sense that they offer more to their readers than a simple one-dimensional text.



2011 traitement page à page introduit dans TEI. Prototype Brouillon manuscrit de Proust. Explorer nouvelles voies pour traiter à la fois de la page et fournir édition. En évitant le paradigme de la page (Sahle 2008). Tentative de faire s’interpénétrer le facsimile et l’édition.

édition digital et imprimé

Ergodic is a term first used in this context by Aarseth, 1997, deriving from the Greek ἔργον – work, and ὁδός – path, namely something ergodic implies a difficult laborious pathway.

## Pour une philologie (numérique) des brouillons

Importance des manuscrits d’auteurs, et l’importance de leur étude en littérature.

Portée littéraire, idée de la textualitat, plus fluide, plus dynamique de la création littéraire.

Livret opéra Tosca

- Couches de corrections
- Faux départ
- reformulations
- versions

= laboratoire de l’auteur, matérialité physique de l’écriture et de la littérature.

Paradoxe, difficulté montrer importance fondamentale de ces recherche et présentation amicale et facile à consommer pour le public.

Édition Flaubert Erodia

Pb pour offrir édition accessibles. Coût diacritiques, etc.

--> page éditée presque plus difficile à lire

Manzoni, 1000 p. folio. Signes diacritiques dépasse 6 pages. Personne n’a la force morale et pysique de déblayer cet apparat, imperfection certainement du à la complexité.

Édition livret de Tosca Ravini en 2 T. Facsimile et transcription diplomatique du texte qui utilise des couleurs indiquer les contributeurs au texte. Édition manque de clareté et relations entre les différents contributeurs...

Numérique invoqué plusieurs fois comme la solution pour rendre compte variations textuelles parmi des versions différentes et gérer les versions des brouillons.

- **certaines initiatives plus accessibles**. Hypercard, obsolescence.
- représentation hyperdiplo brouillons (Bovary) rivalisant

**--> Comment évaluer les ms de manière qualitative et faire comprendre des processus de composition.**

**Questions théoriques qui caractérisent la critique génétique pour lequel le nouveau médium pourrait offrir nouvelles possibilités et des solutions.**

Trois axes de recherche

- représentation des brouillons (facile car transcription reste obligatoire, une activité herméneutique force chercheurs et chercheuse s’intéroger sémiologie)
- représentation du processus de création de l‘écrivain (ordre, phases élaboration)
- représentation de l’évolution de l’ouvrage (diachroniquement évolution ouvrage ou plusieurs)

Risque d’obscolescence. Penser dans la longue durée.

Même si perte de certaines ressources, réalisation précosse. Modèle édition numérique XML et HTML pour l’affichage publique

Modèle source-output

Durabilité technologique, logique et sémantique fondamentale.

XML pas de sémantique en soi.

TEI modèle de balisage capable répondre aux trois axes précédents. Modèle qui a démontré à travers plusieurs éditions que fonctionne.

- Shelley Goodwin archive http://shelleygodwinarchive.org
- et du ?

Tous les pb pas résolus. Si modèle solide dans la poursuite recherche dans l’axe de ses trois axes. Affichage qui pose plusieurs problèmes selon ces trois axes.

**Manque de théorisation et de modélisation et non faiblesse technique.**

Représentation des brouillons. 

- Bovary, difficile suivre interventions
- Samuel Becket (CollateX) représentation du texte mais une phrase à la fois, perd connexion avec matérialité des brouillons dans comparaison phrase 
- Exemple manuscrit de Beckett, un des exemples les plus vertueux avec possiblité de suivre évolution du texte dans les deux langues. https://www.beckettarchive.org
- prototype : Alessandro Manzoni, Dal Fermo e Lucia agli Sposi Promessi. Alessia Marini, Elena Pierrazzo, raffaele Vignlianti

Retravaille sur colonne de gauche, réécriture. Remaniement importants, ajout de paperole. Deux premiers chapitres où les deux ouvrages cohabitent.

https://promessisposi.weebly.com/fermo-e-lucia.html

http://www.alessandromanzoni.org/opere/1

Traduction dynamisme de la page --> apparition zones de texte dans l’ordre, et stratification textuelle sous forme apparat critique dynamique.

apparat à peine plus lisible

Essai avec Version machine (TEICAT), sépare différentes couches d’écritures en versions parallèles

EVT2 montre comme versions, chacunes avec leur propre apparat.

Partiellement réussi car oblige création artificielle de sources (couche de base, finale et milieu) sans que puisse donner justification scientifique pour constitution de ces avatars de texte.

Pour représentation diachronique

édition de Maironis. Paulius Subačius https://dariuskucinskas.lt/research-projects/

http://www.pb.flf.vu.lt

Modèle de données qu’un premier et important pas. Modèle de développements d’interfaces complexes que le début. Numérique pas seulement transposition d’un modèle analogique dans l’espace numérique mais doit pouvoir explorer possibilités nouvelles, modèle renouvellé par rapport à l’imprimé.

Travailler d’avantage sur le plan de la modélisation sémantique des brouillons pour ne pas être pris au dépourvu.



à lire

https://journals.openedition.org/variants/

http://www.pb.flf.vu.lt/principai/?lang=en

high-profile digital editions, for instance *Jane Austen’s Fiction Manuscripts*, the edition of the *Manuscrits de Madame Bovary*, the *Walt Whitman Archive*, the *William Blake Archive*



2007 Gabler felt the need to advocate for new attention to documentary editions, which, in his opinion, were still underestimated in the editorial scene, and he claimed that the digital environment is the most suitable for this type of edition.6 

Privilégié ce type d’édition sur l’édition de témoins multiples. 

> Perhaps these types of editions could be called *paradigmatic editions*, as they embed many alternative options for the same string of text in a nonlinear way, as opposed to editions that can only display the text in one format (such as printed editions, among others), which could instead be called *syntagmatic editions*. Text encoding has in fact enabled editors to have their cake and eat it: features that were once normalized without mercy to produce reading, critical (or syntagmatic) editions can now be retained and simply switched on and off at leisure to please different audiences, thereby opening the way to new scholarship and readership.

Fonctionnalités qui ont attiré l’attention de collègues pour qui ces preuves documentaires ont un rôle central. Nouvelle philologie et critique génétique.

The battle for critical editing versus documentary editing27 has been fought on many fronts: disciplinary, theoretical, methodological, and economic.

Pb Joseph Bédier Lachmannien

Documentary editions are Tools not theories : A Venetian proverb says that “an umbrella can be useful for more than one rainfall”; here we can perhaps say that (digital) documentary editions can be useful for more than one theory.

Dveloppement édition documentaires et **Capacité de représentation d’un ordinateur**.

--> propose elle éditorialisation, justification choix, formulation et enregistrement hypothèses.

quid stabilité de ce qui est proposé ? quid de l’auctorialité de l’édition dans la mesure où serait dynamique ?

---

Rappeler que première fois que ait eu la chance de l’écouter, à Lyon.

Dire que pas un littéraire et propos portée générale, mais question méthodologique.

Critique génétique, textuelle et philologique. Matérialité du travail de la littérature, mais aussi du travail savant lorsqu’il s’agit de produire une édition critique.

- question limites TEI
- matérialité physique de l’écriture et de la littérature, et plus généralement travail intellectuel et sa transposition numérique.

Si page éditée presque plus difficile à lire, quel apport.

Question de la diachronicité du processus.

Modélisation des actes éditoriaux quelles propositions. Modèle page versus modèle texte.

Limites techniques du modèle hiérarchique ?

Question du balisage externe

Modèle source-output et pb de la représentation des balisages externes.

Représentation des brouillons, limites de HTML et traduction HTML. Pb de la représentation numérique des éditions en HTML. Question de la prise en charge de la forme. Débat sur introduction éléments pour mise en page TEI point de vue spatial vs tetxuel.

Autres modèles possibles que linéaire pour rendre compte phénomènes complexes. Vieille discussion sur la modélisation du texte et le caractère approprié du modèle OHCO.

Cf. modèles alternatifs The Codex.

Pb du balisage externe.

Laissé de côté les aspects computationnels. Au-delà HCR Toutefois : Peut-on confier à un algorithme la prise en charge du traitement. Quelle place pour ces rendus ? quelle valeur herméneutique ? Cf. différents algorithmes Medite, etc.

Acte éditorial ? Vaut-il acter ? cf. pb stemma dans l’approche Lachmannienne. Est-ce que la délégation au traitement algo pas une possibilité envisageable dès lors que l’édition numérique peut être redéployée sous différentes formes par l’utilisateur ?

Possibilité enregistrer dans l’interface des lectures. Alors orientation vers une édition logicielle et rejoint un peu ici vos propositions pour l’investissement sur les interfaces.

Mais nouvelle question qui se pose alors. Si l’interface est partie constitutive de l’acte éditorial, se pose la question de sa pérennisation et de sa conservation. HTML suffit-il comme modèle pour prendre en charge l’édition ? Conception est-elle suffisamment stable (nouvelles règles de dév) pour garantir conservation de l’édition ? N’a-t-on pas beosin ici de nouveaux modèles normatifs pour définir l’affichage. Mais contradiction avec exploration et expérimentation à laquelle tu invites depuis longtemps.





Elena ­Pierazzo’s *Digital Scholarly Editing*: *Theories, Models and Methods*

> ­Pierazzo has much more to report than intelligence from the  battlefield. She places numerous accounts of the practice within a  broader framework of editorial theories and their historical and social  contexts. As such, she continues and expands on notable studies like  those of Jerome McGann (1991), Peter Shillingsburg (1996; 2006) and  Eggert himself (2009). Her work demonstrates once again how scholarly  editing intertwines with various cultural practices, and thus how it  affects the current and future conditions of humanities research.

Stand-off markup might offer a solution to overlapping XML hierarchies, but it is *not* free of interpretation (Chapter 5);

> She proposes to distinguish two parallel strands of digital editing: one that concentrates on the production of digital editions, and  another, more experimental or “daring” digital editing. As a proper  research activity, the latter would on principle allow for innovative  experimentation (and failure!): editions as “laboratories of textual  scholarship” (204).

**Microhistory of “The Voices of Spring”: genetic reconstruction of modernization of Lithuanian Texts**