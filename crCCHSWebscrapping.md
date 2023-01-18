# crCCHSWebscrapping

https://ubc-library-rc.github.io/intro-web-scraping/slides/what-is-scraping.html#/

https://ubc-library-rc.github.io/intro-web-scraping/slides/website-structure.html#/

https://ubc-library-rc.github.io/intro-web-scraping/content/understanding-a-website.html

Joe Melanson

Webscrapping, automatisation des tâches.

- si tâche répétitive
- données faciles
- si veut le faire plusieurs fois à des temps 

Mais peu utile si single task.

Peuvent automatiser tâche de plusieurs manières. Identifier la tâche à visiter. Définir l’information à recherche, profondeur, et fréquence.

Souvent sur des sites de news. 

Utile de différentier du crawling qui analyse en masse le web pour produire des index. Scrapping est une tâche plus spécifique et ciblées (informations de contacts, prix, identification de ces informations).

Certains sites interdisent le web scaping avec un `robots.txt` file

http://locomostrip.com/comic/179

Est-ce que le scraping est la meilleure option ?

- facile à copier coller, automatisation des tâches répétables.
- Vérifier que export option ?
- Est-ce qu’il y a une API, parfois pas toujours les points d’entrée que veut, et public key qui peuvent limiter ce à quoi accès

Considérations éthiques.

Ce n’est pas parce que quelque est en ligne que vous pouvez utiliser ces données. Savoir si vous pouvez accéder à ces données. 

Voir s’il existe des restrictions concernant ce que peut faire avec les données. Voir aussi dans quelle mesure va overloading le serveur web ? Les pratiques de scraping doivent respecter les règles d’accès au site, souvent renseignées dans le fichier robots.txt

## Jeremy Buhler (how to)

Besoin de comprendre structuration des pages. Exemple d’un outil dans le navigateur. Seulement besoin de comprendre à quoi ressemble un élément html. Ici dans la boîte noire vous avez un élément HTML avec balise ouvrante, fermante. Parfois peut être utile d’identifier les attributs comme des désignation de classes, ou des id ou encore des title que peut utiliser pour indiquer ensuite au webscraper quoi utiliser.

Recommande Chrome pour ce workshop, mais laplupart des navigateurs modernes offre une option d’inspection qui permet de visualiser comment un contenu est structuré.

Exemple avec Data Miner, pas forcément meilleur outil mais permet de ne pas avoir à se poser trop de question.

https://dataminer.io/

Plugin, nécessite de créer un compte. Peut produire sa propre recette ou utiliser des recettes déjà existantes. Une recette est la dénomination dans DataMiner d’une méthode pour scrapper les données.

Possible d’enregistrer le contenu sous la forme d’un simple fichier CSV.







