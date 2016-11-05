# CR Software Carpentry, 27 octobre 2016



## Feed back

Prévoir un temps de présentation des participants et des intervenants.

Mieux indiquer les objectifs des exercices et ce qui est attendu.

Mieux utiliser les feed back utilisateurs avec le pad.



## notes

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

Par défaut l’ordre de sortie de la commande `ls` est alphabétique. L’option `-r` donne la liste dans l’ordre inverse.

`mkdir` créer un répertoire

Pour obtenir la taille du fichier, on utilise l’option `-s`ou `-sh`

Supprimer un fichier `rm`, supprimer un répertoire `rm -R`. L’option `-i` permet de sécuriser la commande. On peut d’ailleurs facilement configurer son shell pour que la commande s’exécute nécessairement avec cette option.

Utilisation de caractères joker `*` : exemple `rm *.txt`

Pour renommer un répertoire, on utilise la commande `mv`, `cp` pour copier des fichier ou des répertoires. On peut bien évidemment ici utiliser des caractères génériques. Dans une commande de ce type, la dernière valeur est le nom du répertoire cible.

`wc` Obtenir le nombre de ligne d’un fichier texte. Faire un "word count", l’option `-l` permet de ne s’intéresser qu’aux lignes. Si je veux voir le nombre de ligne dans chaque fichier en fonction d’un type, on utilise un caractère générique.

Pour écrire la sortie d’une commande dans un fichier, on utilise, un signe `>`.

La commande `cat` affiche dans la sortie le contenu textuel d’un document.

`sort -n` trier les éléments dans la sortie. On peut enchaîner les commandes avec des pipes `|` qui sont des "pipes" ou des "redirections" ou "embranchements".

`wc -l *.pdb | sort -n | head -1`

La logique des commandes unix consiste à produire des programmes très simples que vous pouvez combiner pour produire des choses intelligentes. 

`wc -l *.* | sort -n | tail -5`

`ls *Z.txt`

`wc -l *A.txt *Z.txt` en mettant les deux sur la ligne

`wc -l *[AB].txt` avec une expression régulière, une manière de désigner un motif.

### Exercices sur les embranchements

`wc -l < NENE01729A.txt` permet de rediriger l’entrée standard. La différence avec `wc -l NENE01729A.txt` est que l’on aura pas le nom de fichier, seulement le résultat.

`>>` apend, ajouter à la fin. 

`echo hello >> out.txt`

`cat out.txt`

`echo hello >> out.txt`

`cat out.txt`



Si l’on voulait renommer successivement chacun des fichier en leur ajoutant un suffixe, la commande `mv *.bat *postfix.bat` ne fonctionnerait pas. On va devoir utiliser une boucle.

```bash
for filename in basilisk.dat unicorn.dat

do 

  head -3 $filename

  done
```

Une bonne manière de faire est de mettre tout cela dans un fichier et d’en faire un script afin de pouvoir le réutiliser. On créée un fichier texte avec l’extension `sh`.

Pour l’exécuter `sh script.sh`

Il existe des variables prédéfinies pour le script. $1 = premier argument, $2 = deuxième argument.

`sh script.sh basilisk.dat unicorn.dat`

On peut donc maintenant utiliser des caractères génériques.



## Premiers pas sur les serveurs de Calcul, Nikolai Sergueev

Calcul Québec à l’université de Montréal, présentation concernant la première connexion sur les serveurs de calcul. Objectifs : vous familiariser avec le calcul informatique de pointe et son vocabulaire. Apprendre à utiliser une grappe de calcul.

Du code qui fonctionne parfois mal sur son ordinateur et peut avoir besoin de plus de puissance, et donc accès à des machines spécifiques. Avec cette présentation, on va apprendre à utiliser une grappe de calcul.

- Transfert de fichier
- Calcul informatique de pointe
  - composantes d’un ordinateur et d’une grappe de calcul
  - types de parallélisme (tâches séquentielles versus tâches parallèles)
  - Calcul Canada et Calcul Québec
- Utilisation du système de modules
- Exécuter des tâches

### Transfert de fichiers

Le transfert de fichier est très important car avant de réaliser n’importe quelle tâche de calcul, vous allez avoir besoin de transférer les données sur lesquelles vous voulez travailler. Il existe de nombreux outils de transfert en fonction de la nature des données sur lesquelles vous voulez travailler.

On va surtout parler de la commande `scp` qui est un peu l’équivalent de la commande Linux `cp`mais elle fonctionne entre plusieurs machines différentes. 

Cette commande fonctionne très bien dans la plupart des cas, mais peut se révéler insuffisante lorsque l’on doit transférer de très grandes quantités de données sur l’internet. Dans ce cas, on peut utiliser deux logiciels, **BBCP** pour le transfert parallèle ou **Globus** qui est utilisé partout sur Calcul Québec et Calcul Canada. L’avantage de ce dernier logiciel est qu’aucune configuration n’est à faire et il offre une interface web conviviale, option d’envoi de courriel à la fin du transfert et possibilité de partage avec d’autres utilisateurs.

https://globus.computecanada.ca

Si vous disposez d’un compte Globus, vous pouvez l’utiliser, sinon créez un compte sur Globes.

https://globus.computecanada.ca/globus-app/transfer est la fenêtre de transfert de fichiers. Vous devez configurer les point de chute sur les deux serveurs.

Lors de la création du compte, on a la possibilité de créer sa machine locale. On peut définir deux machines différentes mais nous allons configurer sa machine personnelle comme point d’entrée. "Get Globes Connect Personnal".

Renseigner un nom pour votre machine personnelle. Puis "Generate Setup Key". Copiez la clef dans le presse-papier et téléchargez le fichier d’installation. Exécuter le script d’installation, puis lancez le logiciel et copiez la clef.

Dans les préférences de Globus, vous pouvez définir des répertoires partagés.

Choisir les points d'accès, sélectionner son point d’accès local. De l’autre côté choisir "colosse". Renseigner les mot-de-passe et codes d’accès. Une fois le transfert effectué un courriel de confirmation du transfert est adressé.

### Calcul informatique de pointe

Qu’est-ce que le CIP Calcul informatique de pointe

Il n’y a pas véritablement de définition officielle du Calcul informatique de pointe. Selon notre définition à Calcul Québec, toute utilisation intensive des ressources informatiques, ou qui est limité par les ressources disponibles.

Usage intensif de ressources ? temps d’exécution, calcul, stockage, mémoire, etc.

Domaines traditionnels : dynamique moléculaire, astronomie et astrophysique, mécanique des fluides (CFD). Mais de plus en plus aussi des domaines non-traditionnels : assemblages du génomes, rendus vidéo et analyse d’image, sciences humaines numériques, analyse de données géospatiales, etc.

### Calcul Canada et Calcul Québec

Et la différence entre les deux. Calcul Canada, une organisation de quatre divisions régionales. WestGrid, Compute Ontorio, Calcul Québec et Acenet.

Calcul Québec est un regroupement de plusieurs universités pour du Calcul de pointe, ressources de calcul et de stockage. Il existe beaucoup de besoin de calcul et de stockage qui sont assurés avec Calcul Québec. Plusieurs grapes de calcul : Briarée à l’université de Montréal, Colosse à Laval, Guillimin à McGill, Mammouth à l’Université de Sherbrooke.

Dès lors, que vous êtes associés à une université québécoise ou canadienne, vous pouvez utiliser ces ressources. Au total, la grille offre plus de 60 000 cœurs de calcul, 300 accélérateurs (GPU etc.) , 200 To de mémoire vive, 8 000 To de stokage sur disque.

Plus de 40 analystes, administrateurs systèmes et gestionnaires. cf. le site www.calculquebec.ca pour obtenir des détails d’information sur les serveurs, les politiques d’utilisation des ressources et d’utilisation des serveurs https://wiki.calculquebec.ca

Les composantes d’un ordinateur.

Espace de travail (scratch) local | Mémoires vive | Cœurs | infiniband pour permettre aux cœurs d’interagir entre eux, les accélérateurs sont des cartes qui servent à augmenter la vitesse d’exécution de votre code. Le système utilise en général ethernet.

Exemple d’un nœud de Colosse. Plusieurs CPU, mémoires vives et modules.

Calcul Québec offre des service différents en fonction des besoins. Si l’on compare un ordinateur personnel à un nœud de calcul, ce dernier présente plus de processeurs, beaucoup plus de mémoire vive, beaucoup plus de stockage, au lieu du wifi utilisation de GigE et Infiniband. Carte graphique professionnelle, File d’attente.

2 à 4 processeurs sur un ordinateur personnel, 8 à 32 processeurs

4 Go à 16 Go, etc.

Grappe de Calcul, on transfère une tâche depuis un client par l’intermédiaire d’internet au nœud frontal de la grappe de la calcul, cette tâche est acheminée par ethernet et Inifiband vers le stockage (home, project, scratch), ou les nœud par un ordonnanceur.

On peut aussi avoir un local sur les nœuds. Scratch parallèle ensemble de stockage partageable sur l’ensemble du nœuds. Il n’y a pas de système de sauvegarde, c’est un stockage temporaire sur un disque très rapide.

Il existe une limite utilisateur concernant le nombre de cœur 

### Tâches

Tâches séquentielles

Tâches parallèles

ssh user12@colosse1.calculquebec.ca

- `msub solution.sh` (la commande msub est spécialiste à colosse, Bérari qsub )
- `qstat -u user12` pour accéder aux statistiques d’exécution

## Utilisation du système de modules

Un module est un fichier de configuration qui rend disponible une version précise d’une application ou bibliothèque dans la session d’un usager. 

Il y a de nombreux logiciels installés sur les machines, mais on n’a pas toujours besoin de tous pour l’exécution d’une tâche. Les modules sont chargés en fonction des besoins de notre tâche.

Plusieurs centaines d’usagers qui ont autant de besoins différentes, mais qui exécutent des tâches sur les mêmes serveurs.

Pour passer de mathlab2 à mathlab3, il suffit de charger le module dont on a besoin. Cela permet donc d’avoir plusieurs versions d’un logiciel.

Utilisation de la manière suivante

- `module <sous-commande> <paramètre>`
- `module avail` liste tous les modules disponibles sur la grappe.
- `module load apps/a`
- `module list`
- `module purge` mais reste les modules par défauts `module --force purge`

Il est possible d’ajouter les modules que l’on charge dans son .bashrc ou son .bash_profile

### Fichier de soumission

Comment écrire son fichier de soumission, le fichier pbs

Un fichier de soumission contient une entête destinée à l’ordonnanceur et le code à exécuter.

Les lignes qui débutent par #PBS décrivent les ressources à utiliser

```bash
#PBS -l walltime="3:00:00"
#PBS -l nodes=1:ppn=8
```

Souvent ne connait pas le temps d’exécution. Avec un modèle inconnu, demande le temps maximum, puis choisit plus intelligemment le temps exigé. Votre code doit être parallélisé.

Les conditions d’exécution de votre programme sont généralement indiquées dans le manuel. Sinon regarder des Benchmarks. Ne sert pas toujours d’ajouter des processeurs car le coût des communications entre processeur peut devenir trop coûteux. Il y a en quelque sorte un point d’inflexion.

On doit aussi indiquer dans le fichier le compte de projet.

voir vos projets ici https://ccdb.computecanada.ca/

En appelant le script, on peut vérifier la file d’attente, vérifier une tâche et modifier ou annuler une tâche.

C’est séquentiel, donc il va exécuter le travail l’un après l’autre.

dans le 2e exemple, le `&` sert à dire de continuer malgré le wait. Le wait sert à exécuter la tâche en arrière fond.

Exécution en parallèle avec `parallel` mais `mpiexec` supporte plusieurs méthodes, parallel et mpi. Pour paralleliser en mpi, cela implique une modification du code.

### Exécuter des tâches

vous êtes l’utilisateur, vous transmettez la tâche bien préparée. Il y a une priorité entre les tâches qui est réglée par l’ordonnanceur en fonction de leur horaire, de leur priorité et de l’accès aux ressources.

Lorsque vous ordonnancez une tâche, vous faite une demande d’affectation de puissance de calcul. Il y a une politique d’rorodnnacement avec des privilèges des accès selon les modalités définies par le comité d’allocation des ressource.

Plus vous calculez, plus votre priorité diminue, moins vous calculez, plus elle augmente.

Les limites d'affectation de ressources sont ici

https://docs.computecanada.ca/wiki/Compute_Canada_Documentation

Entre 20 et 30 cœur par année, par serveur.

Chaque serveur a des limites de resources qui sont variables d’un ordinateur à l’autre. Nb de cœur, durée maximum des tâches.

### Conseils

Demander uniquement les resources nécessaires, pas plus.

- temps d’exécution
- Nombre de nœuds/cœurs/mémoires

Votre application ne s’exécutera pas significativement plus rapidement sur un superordinateur. à moins que le code n’ait été conçu spécialement.



Nombreuses formations à calculquébec.

http://calculquebec.eventbrite.ca/

Chaque année renouveler le compte. Et pour les professeur demande de publications liées au Compte.

support@calculquebec.ca









