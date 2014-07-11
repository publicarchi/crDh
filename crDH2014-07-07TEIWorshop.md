DH2014, W Hacking with the TEI, 7 july 2014
======

Gr1
----

Travail sur XSLT trois personnes pour convertir la TEI vers JSON, autre groupe pour l'interface utilisateur, trois autres pour la visualisation.

Voulu donné à l'utilisateur la possibilité de spécifier n'importe quelle source de données avec laquelle voulait connecter ses données. L'utilisateur fourni des URL, ensuite entre le document XML, puis spécifie chemin XPath. L'idée étant que dans le navigateur les documents soient transformés par le processeur XSLT et produise du JSON dans le browser. Mais dans cette solution légère, il n'est pas possible de traiter plus d'un document à la fois. En dehors du navigateur, il est possible de traiter plus de documents, mais le workflow devient plus compliqué.

Sortie à partir d'expressions prédéfinies. Pas de méthode de paramétrisation pour le moment, mais sans doute quelque chose que pourra faire par la suite au cours d'un hackathon. La transformation produit du JSON à partir d'une expression XPath. Chaque entrée représente un fichier. Id de l'édition numérique qui permet de retourner à l'édition originale.

Rentrer dans JSON pris du temps, besoin de paramètres dans le script XSLT (or sans doute présent dans XSLT3.0). S'est donc replié vers TEI to JSON avec Perl. Mais encore une possibilité, paramétriser la XSLT par l'intermédiaire d'un template. Sinon, l'utilisateur pouvant fournir un XPath dans l'interface.
Peut-être aurait-il été possible de contraindre l'utilisateur, comme pas vraiment besoin d'une expression XPath complète, peut être possible de proposer des choix préparés. L'idée était que l'utilisateur puisse spécifier par l'intermédiaire d'une interface.

Enfin, le groupe travaillant sur la visualisation a récupérer le fichier JSON et essayé de produire une visualisation avec. Travail qu'ont trouvé plutôt difficile. Voulait produire une chronologie. Si difficile, en même temps, n'importe quel projet qui produit ce genre de format (JSON) peut facilement placer les contenus sur une timeline. Un projet qui devrait donc continuer à être poussé par la TEI en fournissant un serveur, etc. collecter les besoins des utilisateurs, et identifier ce que peut faire pour la communauté car produit chacun des choses pour la TEI mais qui ne peuvent pas être réutilisés. À un niveau abstrait, produit toujours les mêmes choses encore et encore.

Si vous aviez eut le temps, nombreuses visualisations possibles avec JSON. Mais ne serait-ce qu'avec les GoogleFusion tables, peut aller très loin, car tellement de visualisation possibles. Bien sûr problème de droits pour la publication, mais dans certains cas seulement besoin d'explorer les données.
Chaque outil de visualisation nécessite une sortie particulière, besoin d'un format commun. Si toutes les éditions TEI disposaient des mêmes visualisations, ne présenteraient pas le même intérêt. D'un autre point de vue, besoin de moyens pour communiquer et être compris. Cummings fait remarquer que l'un des premiers problèmes consiste dans le fait que les projets ne mettent généralement pas à disposition leurs fichiers XML-TEI.

Traitement de fichiers en JSON, relativement fatiguant. De fait, XSLT pas très pratique pour traiter du JSON. Pourquoi pas de librairie XSLT pour traiter du JSON ? Sérialisation en JSON prévue pour la version 3.


http://dnovatchev.wordpress.com/2007/07/05/transforming-json/
http://stackoverflow.com/questions/13007280/how-to-convert-json-to-xml-using-xslt
https://github.com/WelcomWeb/Stapling
http://www.bramstein.com/projects/xsltjson/


2e projet
------

Visualisation de fichier ODD
Une manière de montrer ce qu'utilise de la TEI, et ce que n'utilise pas.
Basé sur les membres du module Core.

Une visualisation en réseau de la spécification, qui permet de montrer les relations des éléments entre eux. Changer une description, etc.
[Serait intéressant de pouvoir travailler directement sur le graphe.]

Décidé de travailler sur une visualisation D3 trempa.
Chargement du JSON de la TEI, puis celui d'une customisation réalisé grâce à une XSLT. Créé un système de score sur chaque élément. Si un élément n'est pas modifié en blanc, la taille déterminée par le nombre de valeurs spécifiées, couleur par le nombre d'élément modifié. Déterminer le type d'information que voulait traiter, etc. pris un certain temps. Possibilité de zoomer pour visualiser les choses modifiées. Visualisation géographique par module. Visualisation qui peut donc constituer une bonne aide.

Possibilité de catégoriser par module.
Si ajoute des règles schematron, alors devient complexe à traiter.


La suite
----

Soit considère qu'intéressant de continuer dans cette direction, soit considère qu'il s'agit d'un projet différent qui requière des méthodologies différentes, etc. Remercie que vous adressiez vos documents de travail.
Le premier Hackathon que l'on organise, plutôt un succès. Quelles étapes pour la suite ?
Rédiger un petit paragraphe pour dire l'intérêt de cette voie.
Des questions envisagées dans le cadre de Tapas. Mais pourrait être capable de capter plus de JSON pour faciliter ce travail.  Serait très intéressant de pouvoir disposer de cookbook de manière à ce que les gens n'aient pas l'impression de devoir recommencer depuis zéro.

Pas choisi d'utiliser BaseX ou eXist pour travailler directement sur une preuve de concept. Pas évident que eXist soit scalable sur de grandes sources. Une autre manière de produire du JSON, aurait été d'utiliser JSON.

Explorait avoir des gens qui aient de l'expérience en développement, ne pensait pas avoir le plaisir d'avoir des gens qui travaillent en TEI. Enchanté d'avoir vu comment des personnes avec des niveaux différents et des perspectives différentes ont pu travailler ensemble.
