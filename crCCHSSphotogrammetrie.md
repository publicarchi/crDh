---
date: 2021-02-19
tags: compute Canada, photogrammétrie, 3D
---



## crCCHSS High Performance Photogrammetry for Academic Research on HPC clusters

Katie Champman, Tassie Gniady (Indiana Univeristy)

Pervasive technology institute, Indiana University

Photogrammetrie

- est une méthode pour extraire des modèles (3D) d’un objet, un environnement ou un terrain à partir d’un ensemble de photographies en deux dimentions (2D)
- applicable à un grand nombre de disciplines académiques : patrimoine, architecture, histoire de l’art
- high computational algorithm

Ernie Pyle Statue Example

- localisation des points depuis lesquelles les photographies prises
- 3D wire frame of the model
- resulting texture mapped 3D model

https://itconnections.iu.edu/2018/11/avl-photogrammetry.php

Première étape alignement et génération des nuages de points

Deuxième étape construction des nuages de points denses

Build Mesh (generate a polygonal model)

Enfin, Build texture

Outils existants

- Commerciaux : Metashape (discount éducatif) and RealityCapture (prohibitif)
- Open source : COLMAP, Meshlab, MVE, OpenMVG, OpenMVS, VisualSFM and MicMac

Travaillent avec Metashape car disponible sur Mac ou Windows, mais aussi Linux. N’ont trouvé qu’aucun logiciel open source aussi robuste ou bons que les outils commerciaux.

Utilisation de sciptes pour automatiser les tâches. Informations pour les queues, etc.

Exemple de processing avec Metashape. Commence par ajouter un répertoire de photographies, jpg, png. Photographies prises avec une table tournante. Photos prises avec une règle pour l’échelle.

Importation des masques. Plusieurs options possibles. L’applique à toutes les photographies.

Alignement des photographies, logiciel qui va chercher correspondance et appliquer le masque aux points clefs afin de positionner les images où celles-ci doivent se trouver. Obtient un premier nuage de point qui produit une première estimation de ce que doit obtenir.

S’assurer que la boîte comprendr bien toutes les parties du modèle que veut traiter. On créée ensuite un nuage de point dense. Ici peut appliquer colorisation. Cette étape est coûteuse en traitement informatique. 216 000 points mais encore des espaces entre ces nuages de points.

L’étape suivante faire un polygonal mesh puis triangular mesh pour finaliser la production du model. Pas très long et peut être réalisé de manière interactive assez facilement. Pas besoin de scripts parallèle. Obtient maintenant un solid mesh : une figure solide. Pas encore complètement lisse mais le logiciel va pouvoir régler cela. Si s’approche de très près, le modèle comprend des milliers de petits triangles.

La dernière étape consiste à appliquer une texture sur cette mesh. Lors de l’exportation donc plusieurs fichiers à patager ensemble (trois).

Le nombre de détails que peut obtenir avec la photogramétrie parfois très surprenant. Une fois que l’objet est numérisé, il devient possible de partager le modèle sur une plateforme comme sketchfab. Plusieurs formats possibles pour le partage ou l’impression.

Option de générer un rapport avec des statistiques sur la génération du modèle. Information utile pour l’archive pour comparer les modèles ou les résultats.

GPU enable option avec le logiciel. Mieux de l’activité. Toutes les étapes pas encore GPU enable mais prévu pour les prochaines étapes. Lorsque pas de GPU, utiliser processus CPU.

---

Benchmarking datasets pour regarder comment accélérer les options.

- Statue céramique
- statue bronze université
- site archéologique

Nombre d’iamges considérablement plus élevé pour les grands objets. Petit objet obtient rapidement suffisamment d’objets 63 images suffisantes. Parfois certaines plus d’informations utile que d’autres

Pour grande scupluture : 389 photographies. Plus d’informations utiles par photographie.

Pour le site archéologique, 2617 images utilisées. Photographies prises sur un mat, souvent une goPro. Le plus gros ensemble de donné qu’a pu utilisé. Pour nous intéressant de voir ce que pouvait permettre le processing parallèle.

Karst system, node type IBM NeXtScale, Intel Xeon E5-2650 v2 * 2, 16 core, RAM 32 GB

BigRed II, XE6, AMD Opteron, Abu Dhabi * 2, 32 core, RM 64 GB

Carbonate, Lenovo NeXtScale nx360 M5 server, Intel Xeon E5-2680 v3 * 2, 24 core, 256 GB

Carbonate beaucoup plus efficace mais temps d’attente plus long.

Temps de traitement, carbonate, de 11 minutes à 8 minutes pour statuette en medium et 35 à 19 en high, 241 à 62 pour sculpture en medium, 893 à ??? en hight, site 285 à 199. Pas capable de computer avec 2 nœuds (perte de mémoire)

Comment déterminer nombre le plus approprié de nœuds à demander. Benchmark destiné à évaluer besoins les plus appropriés. Pour des petits ensemble de données, parallélisation qui ralentit.

Toutes les tâches pas parallélisables. Construire les modèles pas parallélisables, autres traiteemnts oui. Build the dense cloud le plus coûteux, or parallélisable. Donc utile de l’avoir.

Ces résultats d’utilisation un peu anciennes. Aujourd’hui réduit utilisation avec Covid. Mais moyenne utilisation 140, median 27 minutes, max 1800 minutes.

Travaille pour étendre technologies employées.

XSEDE Use Case

Utilisation de Blender pour session photogrammétique virtuelle puis passé dans Metashape. Permet de déterminer stratégies pour produire données où intégrité des données importantes. Determiner points utiles pour capture initiale de l’objet.

Nouveau sous groupe IU3D

https://iu3d.sitehost.iu.edu/iu3d/

Matterport scanning, Lidar, etc. cf. https://matterport.com/

https://sketchfab.com/IU3D

Lilly Library

Toutes captations en RAW même si process en JPG car pense que par la suite amélioration des traitements peut être possible. Machine à écrire et parties fines des chaires difficiles à numériser pour la statue.

Exemple extraction d’une gravure japonaise, extraction des différents plans et extrusion pour produire un modèle imprimable. Idée avoir touchabilité.

3Dstudio Max, and extracts information. Possibile utiliser blocs de fondactions.

 

## Discussion

Travail sur les meilleures pratiques pour les métadonnées. Mais il n’y a pas encore de format standardisé. Certaines personnes ont travaillé sur des standards utilisant XML, d’autres LOD. Mais jusqu’à présent pas de standard qui se soit dégagé.

Possible d’utiliser des photographies anciennes pour faire ce traitement comme les logiciels sont de plus en plus tolérants.

## Logiciels

### Commerciaux : 

- Metashape (discount éducatif)
  https://www.agisoft.com/
- RealityCapture (prohibitif)
  https://www.capturingreality.com

### Open source

- COLMAP

  https://colmap.github.io/
  BSD

- Meshlab
  https://www.meshlab.net/

- MVE
  https://www.gcc.tu-darmstadt.de/home/proj/mve/

- OpenMVG
  https://github.com/openMVG/openMVG

- OpenMVS
  http://cdcseacave.github.io/openMVS/

- VisualSFM
  http://ccwu.me/vsfm/

- MicMac
  https://micmac.ensg.eu





