# Pierre Willaime, Ouvroir 1er novembre 2023

3 personnes en ligne

12 en local

Mission MSH Lorraine autour d’une plateforme de publication de souerces numériques.

Modélisation des Connaissances.

Logiciel libre, sous licence GPL qui peut être étendu par des modules et qui est initialement conçu pour publier des bibliothèques numériques.

Il n’y a pas d’usages recommandés du logiciel qui n’est pas conçu pour des usages particuliers. On peut notamment l’utiliser pour la constitution de bases de données prosopographiques. Le logiciel est développé par une équipe de développeurs aux US, CHNM, Université George Mason, et depuis par un consortium Digital Scholar. 

Une équipe professionnelle dirigée par Sharon Leon, développent un logiciel libre qui peut être modifié par plusieurs personnes.

- Omeka Classic 2008
- Omeka-S 2017

Un développmenet communautaire international en France et aux US. Pourquoi deux versions ? 

Omeka Classic initialement conçu autour de l’individu. Développé avec le Framework PHP Zend. Une version 2. La version 3, renommée pour rendre compte des changements majeurs intervenus dans le logiciel.

Omeka-S est plus axé sur les institutions, il est possible de créer plusieurs projets avec une seule instance. Les standards du web sémantic sont mieux intégrés dans le logiciel. Le S pour multi-site. Nouveau Framework php Laminas.

L’utilisation de Classic est toujours pertinente, mais suppose la réalisation de choix. Cathédrale et le bazar. Logiciel codé de manière cohérente et avec une unité, et un code protéïforme. Omeka un peu des deux.

Il s’agit d’un logiciel très facile à prendre en main. Mais il peut être comparé avec d’autres solutions comme Heurist. Il est très facile de créer des bases de données avec le logiciel. On peut décrire des entités intellectuelles en les associant à des médias.

On fait ça en respectant des standards. Possible d’importer des ontologies. Possible d’entrer les données Omeka. Mieux d’exporter les données et les traiter avec des logiciels particuliers.

C’est donc un logiciel que l’on peut considérer comme un couteau-suisse qui fait beaucoup de choses mais pour des tâches spécialisées, peut être plus pertinent d’utiliser des logiciels spécialisés.

Ce choix est adapté aux BDD car dans une bdd, ne sait pas nécessairement à l’avance ce que veut faire. C’est de tester diverses choses. Lors de l’installation d’omega, on arrive sur une interface d’administration qui peut être francisée, créaion possible d’un formualire. Demande de titre, et de description. La partie droite de l’interface pour une ressource permet d’utiliser des vocabulaires dès lorsqu’ils sont compatibles avec les standards du web sémantique.

Le travail implique de définir quelle est l’entité intellectuelle décrite en choisissant l’ontologie nécessaire pour le projet. On peut aller très loin dans la description ou créer une ontologie à peu de frais.

Intégration d’un module de géolocalisation. Possible d’utiliser des fonds classiques, pour une géolocalisation à façon, peut être mieux d’aller vers QGis.

Question d’imports

Par défaut, on peut avoir l’impression que le logiciel permet de ne rien importé. La base est conçue pour créer des modèles de resources. On peut créer des modèles spécifiques pour décrire un contenu. L’interface graphique permet de créer le modèle de ressource de manière relativement fine.

Par exemple, ici créée une entité historique. Bibliographic ontologie. Foaf, etc. Après avoir choisi des champs dans un référentiel, il est possible de renommer les champs dès lors que l’on s’assure bien de la compatibilité de son système.

En ce qui concerne l’identité, il existe des bases de données pertinentes qui peuvent être intéressantes. On peut par exemple aller piocher dans un référentiel d’autorités. Value-suggest et flux de données.

Possibilité d’exprimer l’incertitude. Pour importer des données, il faut installer un module comme CDV Import, etc. Ici un module maintenu par un ecollègue français. L’installation des modules est assez simple, un zip à déposer sur le serveur.

ODS

Projet INHA, Digital Muret, INHA. Possibilité importer les données directement si les données sont partagées.

Possibilité de connecter l’API Omeka pour importer les données. Côté interopérable et ouvert. Pas possible de faire ça avec d’autres logiciels.

Site Omeka-Classic réalisation sur des arhcives de mathématicien. Archives Bourbaki. Interface Omeka Classic un peu différente, mais projet qui exemplifie l’idée de décrire des entités intellectuelles. Ici un collectif qui écrit sous un nom collectif.

Nombreux documents à gérer avec des informations de versions. On a donc un corpus numérisé. Parfois pas de documents numérisés, mais possible de créer des entités intellectuelles pour lier identité existente avec une entité absente.

Le logiciel permet de créer des relations. Avec des propriétés. Ici relations typées avec Item relation. Ici créées manuellement sans être alignées par un référentiel. Un projet qui date de 2012. Pas fait le choix de passer à Omeka-S.

Des exemples où formulaire connecté à un Omeka pour la saisie, sans avoir recours à PHP.

Pour les archives Henri Poincaré, besoin de fournir description pour Incipit. eu besoin de créer un modèle de document. Destinatiare, destinateur. Lien vers un contenu interne ou externe pour relier les documents entre eux.

Projet dans lequel n’utilise pas du tout la TEI. Deux raisons principales, un choix que l’on a fait. Pour éditer un texte en TEI, doit procéder à la transcription d’un document en utilisant un modèle d’encodage pour éditer numériquement le texte. Ici s’est demandé si pertinent. Initialement un projet réalisé en LateX avant transformation en HTML. Cette chaîne de traitement était assez lourde et difficile à maintenir. Les chercheurs n’avaient pas la main sur l’édition. Un seul chercheur qui avait les compétences techniques et pas d’ingénieur recruté sur ça.

Quand le projet a évolué se posait sans cesse la question de savoir comment développer un projet accessible à tous, y compris des utilisateurs peu familiers de l’informatique. Lorsque Omeka-S est sorti, l’idée de pouvoir proposer aux chercheurs de faire des correction. Ou alors devait recruter quelqu’un.

Aspect intellectuel important aussi. Voulait-on faire une édition ? Plutôt non, des domaines de recherche 19e 20e, bien sûr des enjeux de transcription. Mais ce qui nous intéressait moins l’édition du contenu que de pouvoir proposer des capacités de recherche après coup. Le travail s’est donc principalement concentré sur les métadonnées.

Possibilité d’articuler le logiciel avec d’autres. Exemple Tropy.

Pas de prise en charge de contenus XML-TEI, ou prise en charge très limitée. Limitations techniques liées à l’environnement PHP.

Lorsque l’on développe une ontologie, on peut créer des propriétés complexes, et hiérarchiques. Mais ces contraintes et cet héritage est présenté à plat dans l’interface d’Omeka, ce qui ne permet pas de pouvoir complètement profiter de la richesse de l’ontologie dans le formulaire.

Cf. article. 

Travail avec des scripts pour appliquer ontologie. Ce qui a permis de générer une interface d’interogation SPARQL pour permettre une interrogation fine du corpus. Nicolas Lasolle, développement d’outils d’extrapolation pour proposer autres résultats.

https://exploration.henripoincare.fr

Caractère séparé de la gestion des données et leur exploitation. Exemple qui fonctionne.

Importation qui permet mapping des ressources et alignement.

L’association est liée à la question de la pérennisation des projets. Les HN ne sont plus toutes jeunes, les projets meurent. Besoin de préserver les métadonnées, les développements (avantage logiciel libre). Mais ce dont a également besoin pour que les projets ne meurent pas, c’est que les données soient réutilisables. Usage de référentiels d’autorités idRef, Geonames, etc.

Entrée et sortie libres des (méta)données : API, OAI-PMH, SPARQL, IIIF, CSV.

Traitements techniques interopérables et reproductibles (ex. IIIF).

Mais également besoin de préserver les logiciels. Actuellement deux versions de logiciels. Comment gère-t-on les deux versions. Des archives du code. Mais ne suffit pas.

Pour que le site reste, besoin de prendre en compte l’évolution des logiciels. L’évolution des logiciels est inéluctable. Et voit bien entre les deux versions, ne peut pas seulement mettre à jour. Des logiques différentes.

Réponse qu’envisage, celle de la constitution de communautés. Risques d’abandons. Chercheurs quittant le site. Possibilité de générer un site statique mais risque de perte : dépendance PHP ou faille de sécurité.

- Communauté autour d’un logiciel/outil/technologie.
- comme lien entre des usagers aux profils variés
- comme facteur de résilience et d’adaptabilité face aux changements.

La communauté est un facteur de résilience, même en cas d’évolutions majeure possibilité de répondre évolutions aux 

AUFO, d’abord groupe informel. Journées en 2016. Journées à Poitiers 2019, Nancy, etc. Aujourd’hui événement annuel. Structuré en loi 1901 depuis 2020.

Bureau de 6 personnes et deux chargés de mission. Liste de 198 abonnés. 

Faire le lien entre les disciplines et les métiers. En France des IGE, et des développeurs. Métiers différentiés avec des compétences différentes. Bibliothécaires et monde de la culture. Logiciel qui lie donc des personnes différentes et communauté pour interaction.

Communauté qui a évité sission entre deux logiciels et amotri les évolutions techniques.

Permet aussi de réfléchir aux usages. Car un outil difficile. 

Définir aussi un endroit où discuter du développement.

Eruditlhor

NoCode

Articulation avec d’autres logciels : image, biblio, etc.

OAI PHM - ORE, etc.

Question sur expositions numériques

Alternatives avec Arches

Version API ? quelles perspectives ?





