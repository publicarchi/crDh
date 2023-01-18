# Navigations anthologiques

Marie-Claire Beaulieu

https://excalidraw.com/#room=202e625965365d3a0476,xcM4YBracHRNCxobN8i1Pg

Une collection de poèmes conçue pour être naviguée par des chemins de traverses. Un texte non linéaire. En suivant ces chemins flexibles, le lecteur peut choisir sa propre direction.

D’Arcy Wentworth Thompson. Point de vue mathématique. Zoologiste. Fils d’un professeur de grec. Connaissait de nombreuses langues anciennes.

Amour profond des études classiques. A identifié dans texte antique les espèces lorsque cela était possible. *Glossary of Greek Birds* 

Par ailleurs, publia un scrapbook. 

https://sites.tufts.edu/ancientbirds/

https://perseids-project.github.io/darcy-demo/

Prototyper un rendu de texte non linéaires pour générer de nouvelles questions et manières d’envisager ces textes. 

FCAP, dériver des concepts ontologiques à partir ensemble d’objets. Un ensemble de concepts et voir ce qu’ils partagent.

Récolement des attributs dans un tableau. Puis représentation sous la forme d’un concept Lattice. Attributs en orange, bleu, moment où les concepts partagent des attributs.

https://sites.tufts.edu/ancientbirds/files/2018/06/a-first-course-in-formal-concept-analysis.pdf

FCA4J

https://www.lirmm.fr/fca4j/Introduction.html

Définition des atrtibuts en fonction des questions de recherche. Aimerait à terme que l’utilisateur puisse poser ses propres questions.

https://wonef.pradet.me

## Giuseppe Celano

Opera Adnotata Gaeca (OGA)

External markup pour les hierarchies overlapping.

Opera Graeca Adnotata (OGA) and Opera Latina Adnotata (OLA) are the largest open access and scalable morphosyntactically annotated corpora for Ancient Greek and Latin, respectively. They both adopt a standoff annotation approach whereby tokens and morphological and syntactic labels are connected to each other in a graph structure.

Séparation qui facilite les traitements.

PAULA XML est un standard de facto, il inclue un moteur de recherche ANNIS

https://github.com/korpling/paula-xml

http://pcai049.informatik.uni-leipzig.de:52480/annis3

## Philological Benchmarks for NLP : The Ancient Greek Authorship Attribution Challenge

Kyle P. Johnson

https://kyle-p-johnson.com

https://github.com/cltk/cltk

https://cltk.org

> The Classical Language Toolkit (CLTK) is a Python library offering natural language processing (NLP) for the languages of pre–modern Eurasia. Pre-configured pipelines are available for 19 languages.

Intuition, les nouveaux outils NLP disponibles mais pas d’information quantitative sur le fait qu’ils peuvent répondre à des questions réelles.

Quels aspects de ces algorithmes fonctionnent le mieux, pourquoi ?

Les classicistes ont besoin d’un challenge qui permet à différentes approches algorithmiques d’être comparées au moyen d’un banc d’essai.

Downstream, beaucoup de taggers, etc. Comment aident les classicistes à faire leur travail.

- l’attribution d’auteur répond à ces besoins

Hypothèse : les algoritmes de ML utilisant NLP peuvent distinguer des textes authentiques ou non à l’échelle.

Quelles règles devraient gouverner cette attribution d’auteur : comment comparer les textes, quels aspects pris en compte, etc.

Un ordinateur peut-il distinguer entre deux textes de deux auteurs différenets.

Avec les mêmes fonctionnalité et algo, peut-il le faire entre plusieurs milliers de paires de texte

Est-ce que des fonctionnalités différentes retournes des résultats significativement différents ?

Pre-Modern NLP. Quitté académie. 

| Philology              | NLP                |
| ---------------------- | ------------------ |
| Concordance            | Info. retrieval    |
| Index                  | Info. extraction   |
| Search word in lexicon | Lemmatization      |
| Genre analysis         | Topic modeling     |
| Translation            | POS tagging        |
| Translation            | Dependency parsing |

Nos modèles encodes des tâches restreintes. Il se trouve que les logiciels sont de plus en plus efficaces pour ces tâches.

Nombreuses langues pré-modernes. 219 comptabilités. Des langues qui ne sont plus parlées.

Problème : pluspart des NLP conçus pour les langues vivantes et langues mortes négligées.

CLTK conçu pour cela. Une pipeline NLP.

- NormalizeProcess
- TokenizationProcess
- SentenceProcess
- StopsProcess
- LemmatizationProcess
- ...

Formalisé en une API logicielle formalisée qui permet d’accéder n’importe quel language avec même interface.

Sanity check

- text vs itself
- text same author
- texts same genre
- texts diff genre

Challenge types proper

- textes authentic vs pseudepigrapha
- textes authentic vs forgery

## The Arftermath of Plato : Searching for Traces in Vector Space

Marcus Pöckelmann, Martin Luther University

étude de la réception de Platon dans la littérature grecque ancienne. Citations, paraphrases et intertextualité en général.

Besoin de définir ces termes et développer des outils informatiques pour opérationaliser ces concepts.

Terminé en 2019.

Charlotte Schubert et Kurt Sier (Leipzig)

Utilisation du TLG Thesaurus Linguae Graecae

Coprus très hétérogène et produit sur une longue période.

Courte phrase de Platon concernant l’expérience de l’art et change. Paraphrase d’Aristote. Réorganisation de la phrase. Plusieurs mots se retrouvent dans les deux phrases, de même que des synonymes.  

Autre exemple, peu de mots en commun pourtant il s’agit bine d’une paraphrase.

216 paraphrases de 19 auteurs. Couplés avec les passages correspondant chez Platon 33 doubles.

Outil de visualisation pour documenter les phénomènes.

Plusieurs approches ont été développées

- n-Gramm-Search compare deux œuvres et trouver des phrases communes
- Rütteln (shaking), recherche d’une phrase et exploration interactive
- Fast-RWMD-Search recherche d’une phrase et retour des phrases similaires dans le corpus, plus à la manière de Google.

Comment nous avons mis en place cette dernière approche. Utilisation de Word Embeddings.

Word2vec (Tomas Mikolov et al. 2013)

Méthode qui recherche mots dans les contextes. Méthod of embedding words in a hight-dimentional space, i.e. to assign fature vestons characterizing them. In particular, words are uses in similar contextes should...

Une méthode principalement statistique.

Word Mover’s Distance (Kusner et al. 2015)

Mesure distance entre deux passages textuels avec mouvement minimal cost. Fondé sur l’utilisation des words embedding.

WMD-Search basic idea

Dès lors que mesure de similarité

Brute force approach

- normalisation
- déterminer la longue de la phrase
- traverser toutes les phrases du texte source avec des longueurs similaires. 
  --> Calculer WMD
- sortir les phrases avec le plus faible WMD --> paraphrase candidates.

Interface utilisateur.  Aussi staistiques.

Approche qui s’est avérée utile. Prototypage sur trois projets des collègues.

Possibilité de trouver nouvelles paraphrases.

https://digital-plato.org

Enjeux de performance. Calcul très coûteux. Parallélisation mise en place par l’université. Réduction d’un facteur 10 pour la performance.

Travail sur l’algorithme pour réduire le coût.

Word Mover’s distance sur la proximité. Plusieurs heuristiques publiées par Kusner pour calculer des formes approximatives et réduire temps de calcul.  

- Relaxed Word Mover’s Distance.
- Relaxed Word Mover’s Distance for the next phrase. Shift sliding window to the next word, évite de calculer la distance complètement à nouveau et permet de calculer d‘après les résultats précédents.

S’est apperçu que ces heuristiques pour notre corpus relativement bons et peuvent être traités bien plus rapidement.

Moins de calcul, possibilité précalcul, réutisation et résultast partiels.

Preprocessisng dCache, preload, parallelisation, load balancing

Fishing for Intertextual References

approche traditionnelle

- très ciblée
- des textes prédéfins
- recherche mot cibles
- = pêcher à la canne

Fast-RWMD-Search plus comme pêcher avec un filet. 

- prend tout 
- certains intéressant, d’autres non
- mais beaucoup inatendu

Comme pas le même coût en temps, dernière approche qui laisse plus de liberté pour l’expérimentation.

Tesseract a ajouté des similarités sémantique

## Marianne Reboul

PHD sur les traductions de Homer. Grands corpus 40 traductions. Et besoin de les comparer ce qui était difficile à faire à la main. A donc cherché une manière de le faire automatiquement.

Actuellement cherche à déposer un projet ERC.

Machine Learning and Ancient European Languages. About low-resource data.

--> Voir comment les languages interagissent à travers le temps.

Plusieurs objectifs. A court terme avoir des meilleures systèmes pour analyser les techniques de traduction au cours du temps. Comment créer les données pour entrainer des modèles, etc.

- NLP Classical text toolkit
- Stanza
- ... produit par Thibault Clérisse

Aby finereader. Puis XML et texte, essayait aligner les traductions avec le texte obtenu. Mais séquences souvent variables. Utilisation de stratégies issues de bioinformatiques où cherche à compléter les gap. Fréquent que les traducteurs ne traduisent pas tous les passages des textes ! 

Algorithme qui permet de repérer les trous.

https://github.com/OdysseusPolymetis

https://odysseuspolumetis.github.io/paralogos

WordEmbedding qui peuvent être rpésentés mathématiquement. Chaque terme a sa position dans l’espace en fonction de ses voisins.

Trois directions dans l’espace. Mesure l’angle entre eux si plus petit, similarité. Peut aussi inférer relations entre les vecteurs. Et voir même relation pour un autre mot.

Contextual word vector

https://jalammar.github.io/illustrated-bert/

Utilisés pour classifier les textes. Ils prennent l’ensemble d’un etxte en compte plutôt que le mot et ses voisins.

Peu de données de traduction, pourquoi ne pas utiliser NMT traduction machine. Demande beaucoup de données, mais souvent pas applicable pour les classicistes.

Toutefois, nous avons des données. Ugarit qui propose des données parallèles.

Stratégie possible, Map monolingual models (MUSE and vecmap)

Hypothèse que les langues européennes toutes iso-morphiques.

Chaque fois qu’utilise Word2vec des modèles différents car randomisation. Or comme je veux voir comment vecteurs évoluent dans le temps pb si pas placé au même endroit. POur faire des comparaison, besoin solidité.

- Réduire randoming principles, p. e. en utilisant MLM
- construire des pivots pour rendre les modèles stables et comparables.

Veut essayer de montrer que signification évoluent sous influence sémantique terme latin, etc.

