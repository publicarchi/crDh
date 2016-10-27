# CR Software Carpentry, 27 octobre 2016

Software Carpentry est une initiative pour rendre disponible les technologies numériques pour les personnes issues de domaines où l’utilisation technique de l’ordinateur n’est pas habituelle ou bien ne fait pas parti du cursus classique.

Cela implique un certain nombre d’outils pédagogiques. Utilisation de post-it pour communiquer sur l'apprentissage comme les post-it. Encourage les participants à travailler en équipe et à s’entre-aider les uns les autres.

http://swcarpentry.github.io/swc-releases/2015.08/shell-novice/

http://pad.software-carpentry.org/SWC-UDEM-OCT27

Shell qui sert à communiquer avec l’ordinateur, à donner des commandes et aussi voir les sorties de l’ordinateur. Nous allons utiliser toute la mâtinée l’exemple d’une chercheuse qui dispose de données qu’elle voudrait analyser. Ces données se trouvent dans le répertoire data. L’idée c’est que le chercheur disposent de milliers de fichiers et elle a besoin d’automatiser ses traitements pour ne pas avoir à tapper des milliers de commandes. Le shell constitue un ensemble d’outils qui permettent d'automatiser des tâches répétitives, et même créer de petits scripts formant des petits logiciels pour automatiser les opérations.

Lorsque l’on se trouve dans le shell on observe un signe indiquant que l’ordinateur attend votre commande.

`whoami` Permet de connaître son nom d’utilisateur selon l’ordinateur. On peut avoir plusieurs comptes sur une même machine. `whoami` est un logiciel que l’on exécute en tapant la commande, et l’ordinateur fournit l’information dans la sortie. C’est un programme que l’on exécute en tapant une commande, son exécution renvoie éventuellement une sortie.

`pwd` est une autre commande très utile car elle permet de connaître le chemin du répertoire où l’on se trouve "print working directory". C’est une commande très utile car il est souvent facile de se perdre dans l’arborescence des répertoires. Et pour supprimer un fichier, il convient habituellement de bien s’assurer que l’on se trouve au bon endroit car sous Linux il est difficile de récupérer un fichier détruit.

Sous mac, on a un home directory qui utilise le nom d’usager. Important de comprendre la notion de répertoire personnel. Ici on dispose d’une arborescence de répertoires et sous-répertoires où les branches seraient les dossiers et les feuilles les fichiers, et la racine serait le répertoire qui contient tous les autres. On peut donc très souvent avoir des niveaux très imbriqués d’arborescence, mais l’idée est toujours la même : on a des répertoires qui contiennent d’autres répertoires ou des fichiers.

`ls` est une commande destinée à présenter le contenu d’un répertoire. Par défaut, le terminal ne présente pas forcément de coloration syntaxiques ou de conventions pour distinguer les répertoires des fichiers.


Pour accéder à plus d’information, on peut utiliser un argument. Il s’agit d’ajouter quelque choseà une commande pour modifier son comportement.

`ls -F` permet d’indiquer la nature de ces entités et de distinguer les fichiers des répertoires en ajoutant un "/" à la fin du nom des répertoires.

Les commandes Linux se tapent toujours en minuscules, pour les noms de fichiers on doit éviter l’utilisation des espaces et des diacritiques car certains de ces outils ont été créés dans les années 60.

`cd` permet d’aller d’un répertoire à l’autre "change directory". On tape "cd" puis utilise un espace pour indiquer au terminal que ce qui suit est un argument. On peut ici lister les répertoires. On se rend dans le répertoire de `nelle/`, puis on peut utiliser la commande `pwd` pour afficher le chemin.

Il existe de très nombreux raccourcis dans la ligne de commande. L’un des raccourcis très utiles. Par exemple pour revenir dans le répertoire du dessus, on pourrait très bien retaper l’ensemble du chemin. Mais cela ne serait pas très pratique.

`cd ..` permet de se rendre dans le répertoire parent.

`cd` sans argument va à la racine de l’utilisateur.

`ls -a` l’option a permet d’afficher les fichiers cachés. Souvent ces fichiers sont des fichiers de configuration. Beaucoup de logiciels peuvent créer leur propres fichiers cachés. Souvent, il s'agit de fichiers textes. Cette option affiche également le chemin vers le répertoire parent `..`, mais aussi le répertoire courant `.`

Afin d’éviter les fautes de frappes dans le terminal, on peut utiliser l’auto-complétion. En commençant à tapper le nom du répertoire, puis en tapant sur la touche "tabulation", on obtient l’auto-complétion. Lorsqu’il existe plusieurs choix, l'ordinateur liste les choix.

On se rend dans le répertoire contenant les données de l’océan pacifique `~/shell-novice/users/nelle/north-pacific-gyre/2012-07-03` et on liste les fichiers. Ce répertoire contient des fichiers de données.

L’extension est censée indiquer la nature du fichier. Mais notez que ce n’est pas parceque vous renommez l’extension que vous allez pouvoir convertir le fichier ! Nommez donc vos fichiers de manière cohérente.











