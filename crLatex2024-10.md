# Atelier LATEX, Robert Alessi

3 octobre 2024

Propose un tour d‘horizon de ce système qui est en soit très intéressant à étudier. Système qui remonte à longtemps car début de la conception 1977. Donald Knuth, professeur de mathématiques spécialisés dans les algorithmes informatiques à Stanford. Reçoit son deuxième volume de son opus magnum sur les algorithmes. Les épreuves sont catastrophiques. Positionnement des signes défecteux. Pb de lecture d’équations.

Grand avancement informatique. Hermann Zapft. Décide de prendre 6 mois pour travailler sur ce problème. Finalement 10 ans. Considère qu’alors le travail est relativement terminé. Dernière erreur corrigée justifiée, gens ont bien du mal à comprendre ce qu’il a corrigé.

50 ans d’existance et un système qui est d’une stabilité extraordinaire. Knuth a conçu TEX avec un certain nombre de principes.

Initiation à LATEX qu’avait conçu pour son laboratoire au cours de la période de confinement. Système pour mettre en page des textes difficiles ou travail de programmation sur la composition.

1988, invité par la Société de mathématiques américaine pour séance plénière. Lui remet alors un prix. Y présente non pas un logiciel mais deux qui vont ensemble. TEX et un autre programme piloté par TEX, qui s’appelle Métafont, un système de description vectoriel utilisant des courbes de bézier pour le dessin des polices de caractères. Les deux fonctionnenent de manière coordonnée, en somme : métafont dessine les caractères que TEX dispose sur la page. (Avec Jonathon Kew écrit article sur l’art de dessiner la lettre S.)

Knuth pose lors de cette conférence 3 principes fondamentaux qui restent actuels aujourd’hui.

- TEX conçu pour être utilisé par les auteurs eux-mêmes, les mieux à même de maîtriser les normes scientifiques de leur discipline
- le programme conçu dans le milieu universitaire devra toujours être libre et gratuit
- il devrait fonctionner de façon strictiement identique sur tous les systèmes informatiques

TEX pas un complilateur mais un interpréteur qui travaille ligne à ligne. Décomposées en lignes typographiques avec ruptures de pages, etc. Avec des astuces pour aller au-delà de nroff et troff.

Avec TEX un système que peut qualifier comme système d’instructions de bas niveau. Série de commandes pour différents éléments de mise en page. Circa 600 primitives et millier de commandes. Primitives que ne peut pas décomposer.

Une vision matricielle de la page sur laquelle va pouvoir positionner de l’encre ou pas. Exemple de la création d’une note de bas de page. Besoin d’un compteur, décision sur le positionnement des notes. Gestion place du texte. Par ailleurs possibilité de gérer les notes de bas de page dans des fichiers séparés (fichiers de style où définit tt sortes de macrocommandes). Dès le départ TEX est donc un système modulaire.

LATEX qui doit son nom à Leslie Lamport. Travaille sur réforme 1985. Invente systeme modulaire plus facile à utiliser. Isolement des styles. Alors TEX commence à quitter son domaine primitif de la documentation technique et mathématiques. Tout le monde s’en empare. Invention de MusicTEX, etc. Première chose à faire aujourd’hui, voir s’il existe des packages qui pourraient être exécutés.

1985 publication version 2,9. Passe la main au LATEX project. https://www.latex-project.org 1994, publication 2e édition 2epsilon. Seulement 2 janvier 2020, publication de LATEX 3. Donne une idée de la stabilité du système, de sa continuité.

Quelques remarques sur les différents moteurs de compilation. Avec TEX entre dans la composition. LATEX permet de bénéficier d’un système plus modulaire et de packets déjà réalisés. TEX bas-niveau, LATEX haut-niveau.

Ce que produisent TEX et LATEX, sortie d’un fichier `.dvi`. Ni du Postscript ni PDF, dvi pour « Device independant ». Encore proche de nroff. Peut avoir toute sorte de périphérique de sortie. Un système de description de page. Passe le fichier à la commande `dvips` pour le convertir en fichier PostScript que peut convertir en pdf. Puis `dvipdf`. Pdftex et pdflatex pour faire la transformation différente.

Alors 7bit ASCII. Dès le début TEX système 8 bit. Mais manipule sans problème ce qui sert à la description des caractères dans la table ASCII. Universel absolu.

Années 80/90 arrivée de la micro-informatique. Dans les années 80, création des pages de codes nationales. Système de superposition pour les accents. Référence à un système international. Selon le système d’encodage de fontes utilisées, aura soit 

Package de translation (inputInk fait la translation pour interpréter le fichier, ensuite FontType qui permet de préciser T1) pour laTEX, le bon vieux TEX va compiler deux boites. Aujourd’hui des polices de caractères qui encodent de manière plus précise les glyphes. Alors si veut utiliser ce système charge un autre package permettant l’utilisation de fontes spécifiques : systéme T1.

Standard Unicode même vocation que ASCII, universalité. Agrandit table pour encoder non seulement toutes les langues du monde mais aussi tous les signes du monde. 2000-2001 spécifications Unicode. JOnathan Kew qui sort un nouveau moteur de compilation nativement Unicode : XeTEX (se dit xi tech) nativement Unicode. Mais important de bien régler son éditeur de texte.

Toujours la même logique, un compilateur de bas-niveau et haut-nivaeu. XeTEX et XeLATEX.

Fin des années 90, discussion dans l’équipe et ressent la nécessité de coupler TEX (un interpréteur de commande à un autre langage interprété). Un débat sur le choix des langages et essais. Finalement 2007 adopte définitivement Lua. Apparaît alors un nouveau moteur de compilation : luaTEx et LuaLatex. Ici comme XTex unicode mais capable de travailler avec deux langages de programmation.

Permet d’intervenir sur des tâches que TEX ne peut pas faire facilement et qui pourraient plus simplement être réalisées avec un langage interprétable comme Lua. Mais aussi intervenir sur des points noirs comme blocs et retours que TEX ne nous montre pas pour intervenir sur des éléments subtils comme des insersions en début de ligne, fin de ligne, etc. que TEX ne montrerait qu’à la fin.

Peut aussi imaginer interompre la compilation et pouvoir traiter chaîne de caractère par Lua et renvoyer le résultat à Lua. Intercepte des flux de textes dans la pure logique Unix. Petits programmes conçus pour une petite tâche bien déterminée. Ainsi que eKotis fonctionne.

**ConTeXt** une entreprise de publication pragma-design qui invente systéme qui peut être installé, fonctionne avec des modules. Syntaxe différente. Un système packagé comme une grosse unité avec laquelle peut faire beaucoup de choses sans avoir à packager tel ou tel package. Hans Hagen a sorti première version d’une future version de LuaMetaTEX qu’utilisèrent Context pour compiler le document. Système plus rafiné des call-back.

https://wiki.contextgarden.net/LMTX

https://github.com/contextgarden/not-so-short-introduction-to-context/blob/main/fr/introCTX_fra_s.pdf

Permet de prendre en charge la disposition de textes en vis-à-vis de manière native. Grand intéret pour faire des choses comme ekdotis. Peut aussi faire des choses très intéressantes car peut compiler pour avoir une sortie Pdf un fichier XMLTEI. Un nouvel univers de compilation.

Page fondamentale pour entrer TEX Users Group https://tug.org point d’entrée fondamentale.

Dans les logiciels TexLive, MacTex, etc. Conseille d’installer full.

Chaque année une version stabilisée qui sort. Vers mars. Développement courants, mais idée de publier version stabilisée chaque année. 

[CTAN](https://www.ctan.org) The Comprehensive TEX Archive Network offre la liste de toutes les extensions disponibles sous LaTEX

## TEX ou l’écriture comme programmation du texte

Comment programmer une édition critique avec TEX

L’idée générale de cette présentation, c’est que quand travaille avec TEX on a deux choses, le texte que l’on souhaite imprimer et d’autre part des commandes de structuration du texte. C’est ainsi que TEX est souvent présenté comme langage de balisage. Cette vision des choses est à mon avais fausse.

Insiste sur le fait que l’on a affaire à un langage de programmation. Ce qu’on pense commande de structuration, en réalité une commande de programmation : il s’agit d’une fonction qui détermine une transformation à appliquer au texte.

Pas un langage de balisage. TEX et la page, on peut facilement faire traiter ce qui a été saisi sous la forme d’un tapuscrit. Volonté de mettre un titre et un sous-titre et des variantes. 

- utilisation police punk de Knuth pour sortir extrait de Proust, 
- police variable de type machine à écrire
- Packagée dans une macro dénommée Randsom !

Possible de composer le texte avec des actions qui sont le résultats de calculs ou de fonctions opérées sur le texte. Macro commande qui vont opérer un traitement différent. Pour le mécanisme de composition, ce que fait TEX. 

Traitement ligne à ligne. Les paragraphes de texte sont assemblés en lignes typographique. Le paragraphe entier est pris comme unité de calcul. Une unité de texte entre deux lignes blanches du mode s, mode n, etc. Tokenize en séquences de contrôle. Traité de manière continue comme une très grande ligne de texte (l’estomac de TEX).

Comme TEX prend le paragraphe comme unité de calcul, le dernier mot du paragraphe va avoir une incidence sur l’ensemble du §. Éviter les lignes courtes, ou encore éviter les lézardes dans un paragraphe qui constitue un défaut typographique. TEX fait ces calculs. River 

\thepage retourne la valeur du compteur, \thefootnote, etc.

Mais comme le num de § calculé avant, si rupture de page alors pas le bon num. Mais comme un système à deux passes, astuce écrire dans un fichier auxiliaire un ensemble de données qui seront récupérées ensuite par le système auxiliaire pour reprise lors de la composition suivante avec la bonne valeur.

Quand compile on a donc trois sortie : fichier.dvi, fichier.log journal, fichier.aux qui est le fichier auxiliaire où écrit toutes les données temporaires que besoin de récupérer. Raison pour laquelle quand compile avec ekdotis premiere fois, ne voit pas son apparat car besoin de collecter nbses informations. Ekdotis un système à trois passes.

Décision prise lors de la conception de TEX prendre le paragraphe comme unité fondamentale.

Assemblées en ligne typographiques

Le paragraphe entier est pris comme unité de calcul \badness et \tolerance

Ligne idéal, une ligne dans laquelle TEX va avoir une maîtrise totale sur l’espacement entre les mots et les lettres de chaque mot. Tout va être calculé, et si TEX a la place de travailler sur une ligne, va sortir une ligne considérée parfaite : badness 0. Une tolérance que peut déterminer.

Une fois que c’est fait, les lignes sont assemblées en page. Pour les pages mécanisme différent. TEX peut couper les pages à plusieurs endroits à la fin d’une ligne.

- *glue* doit être précédé par non-discordable item. Fixé par la cohérence.
- *kern* à la différence de glue est un espace fixe. Une distance que ne peut pas bouger. 
- Ou encore *penalty* qui devient une valeur numérique (entre 0 et 10 000). Selon la valeur que lui donne se dit qu’un endroit où plus ou moins raisonnable d’ajouter une coupure de page. Plus haut plus coupure de page intervient vite. Si zéro impossible. Package comme ekdotis fondamental pour éviter l’oscilating problem !
  Peut entrer directement `\penalty=10000`. En LATEX des commandes plus user-friendly que de directement entrer ces commandes `\pagebreak` équivalent de 10000, mais peut varier `\pagebreak[1]` 1, deux, trois quatre. Plus user-friendly mais moins de valeurs.
- Le processus d’optimisation dans les points de coupure est local et non pas global. 
  Prise du § comme une unité de calcul. Ne va jamais prendre en compte les pages. Aucune idée de la page qui va suivre. Tourne les pages à la manière d’un humain qui tourne les pages d’un livre.
  On aurait pu imaginer inclure toutes les pages, mais en 1977 pas suffisamment de mémoire à accès rapide. Mais jamais jugé nécessaire de revenir sur ce principe. Mais aurait de toute façon posé des problèmes pour ceux voulant un très grand nombre de pages.

Langage de programmation

Définition de \beginsection en plain TEX

```te
\outer\def\beginsection#1\par{\vskipOpt plus.3\vsize\penalty-250 
	\vskipOpt plus-.3\vsize\bigskip\vskip\parskip
	\message{#1}\leftline{\bf#1}\nobreak\smallskip\noindent}
```

Par la commande def, décide de programmer une commande de nouvelle section. Cette commande va prendre comme input un paramètre (un flux de texte, symbolisé par #1). Si avait vouly faire traiter deux flux #2, etc. Ensuite beginsection suivi de l’input que va envoyer. Ici délimité par \par la commande qui compose un nouveau paragraphe

Commande ensuite définie dans une paire d’accolade où commande ouvrante et fermante. Tout ce qui s’opère ensuite dans la paire d’accolade. À chaque fois que #1 ce que j’aurais saisi comme titre de section.

vskip sauter espace verticale, donne dimension. vsize dimension totale de la page. Puis si à cet endroit fin de la page bonne idée de couper = valeur de penalty. Fait descendre la tête de lecture de TEX et décide coupe.

Important car une pure logique algorithmique. Algorithme entendu comme la façon de formaliser un problème qui doit être traité par l’ordinateur. Doit donc être décomposé en étapes, test et décisions pour déterminer des actions. Il y a donc un algorithme de composition.

Supprimer l’idée qu’il s’agit d’un outil de structuration. 

Ensuite revient où était puisque la décision prise. Pas d’effet si au début de la page.

Ensuite bigskip une commande pour sauter un peu d’espace. Ensuire introduit un espace vertical. Reprend parskip, l’espacement fixé entre les deux paragraphes. Ici en train d’arranger typographiquement l’agencement de la page. 

Ensuite introduit message #1 pour renvoyer au terminal le titre de la section. Enfin, commence une ligne alignée à gauche, et passe bf, une commande dans un groupe s’arretera d’avoir son action quand fermé. Passe le titre en gras.

Puis no break pour formellement interdire la coupure de page. Smallskip no ident pour commencer paragraphe non indenté sans retrait d’alinéa.

étape suivante

```tex
\beginsection Titre de la section

Début de la section. Retenons bien que \TeX\ n’est pas un 
langage de {\it markup}.
```

Espace après beginsection pour que la tête soit en s skipping blank. Raison pour laquel espace ignoré. Compose la page et la sortie. Après parskip espace qui ne peut pas être imprimé car mode skipping blank. De même penalty, etc.

Composer un titre pas dans le markup, soumet un texte à un traitement algorithmique avec une série de tests et d’action sur des directions que peut prendre.

Dialogue entre TEX et lua. Possibilité de faire fonctionner avec deux langages. Input et output. Introduction de code LUA, fonction démo qui se termine ligne 8. Prend en argument str, une chaîne de caractères.

Introduction d’un traitement fonctionnel grace à Lua.

Leo said: Ah. You read Aristophanes without an apparatus criticus cf. Keeline, Tom. 2017. « The Apparatus Criticus in the Digital Age ». *The Classical Journal* 112 (3): 342‑63. https://doi.org/10.5184/classicalj.112.3.0342.

Partage du vocabulaire et ontologie. Surtout utilisation schéma digital Library dll.

Encodage différent de la sortie papier. Aparat critique conçu comme un § conçu par le savant qui fait l’édition. Tt le layus mais aussi des datas. Ce que ekdotis va faire, rédiger les choses comme le souhaite mais n’imprimerait dans XML que les données.

Quand à Naples, très impressionné par la communication de Mastandrea ?? Un site qui permet de visiter texte avec apparat critique. Musisqueteoque

Deux types XML apparait critique finement rédigé. Celui 

---

Intéressé de voir que cette programmation de niche puisse susciter de l’intérêt. Un peu un acte soliutaire, on essaye d’inventer des fonctions ou des comportements. Comme pour soi un peu seul juge de l’ergonomie. Ne sait jamais si va susciter de l’intérêt. À Paris peu d’intérêt. En même temps qu’à Montréal, peu d’intérêt pour cela. 



