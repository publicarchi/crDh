# Bert for Humanists Projects

4 juin 2021

BERT et les modèles similaires ont largement révolutionné le champ du traitement automatique des langues. Comment en faire bénéficier les DH et comment apports des dh.

http://bit.ly/BERT-for-Humanists (https://melaniewalsh.github.io/BERT-for-Humanists/)

http://bit.ly/BERT-Humanists-Workshop

https://docs.google.com/document/d/1FreCUwtZVsekEvSwIQMh-G7N4GPQFHsLeXhCXzXT1xY/edit

Malanie Walsh, Maria Antoniak, David Mimno

https://mimno.infosci.cornell.edu/

## What is BERT

BERT Bidirectional Encoder Representations from Transformers, is an NLP model that is trained on a very large amout of textual data and can understand...

Voir un exemple

Word vectors : one point per vocabulary item

Manière d’envisager le texte et d’envisager les mots comme des vecteurs. Dans BERT au lieu de donner une position dans le vocabulaire, donne une position pour chaque instance d’un mot dans le texte source.

Exemple la nature de la philosophie, un point qui représente cette instance spécique du mot dans un contexte. Prend ensuite chaque token de mot dans un vecteur. D’autres instances du mot art et nature dans le texte. Exemple autres instances qui semblent se diviser en plusieurs grands clusters.

Distinction verbe et nom.

Pourquoi les spécialistes de NLP très excités par BERT. Beaucoup dominé le champ car rend le champ meilleur.

Autre exemple de Topic model, caractérisé par termes à haute prévalence, voit que ce topic baisse à une certaine période. Témoigne de l’intérêt de la communauté dans le domaine.

Melanie Walsh, gens des DH très intéressés car champ encore émergeant. David Bermann group à Bamman et Patrick Burns modèle pour les textes en latin, possibilité de trouver des passages similaires basés sur le contexte. A prouvé que fonctionne pour les textes fictionnels en anglais. Résultats prometteur pour la reconnaissance des entités nomées NER et co-reference (Bamman, etc.). 

Cf. biblio sur le site.

### Pourquoi beaucoup de critiques à l’égar de BERT ou de grands modèles de langues similaires.

BERT implémenté dans Google Search, intéressant de voir ces modèles implméntés si rapidement. En même temps pose des questions éthiques et des craintes. 

- Modèles qui peuvent incorporer des biais racistes ou sexistes
- peuvent être difficiles à interprétés
- larges et consommateurs de ressources computationnelles, environnementales ou financières
- souvent des données d’entraînement pauvrement documentés

Garder ces critiques à l’esprit lorsque l’on travaille avec ces modèles.

Références sur les dangers dans la biblio.

### Comment BERT fonctionne-t-il ?

En concevant ce tutoriel, très attentifs au niveau de connaissance que veut délivrer en distinguant ce qui peut concerner l’application pratique et la théorie.

Quelques éléments clefs qui peuvent permettre de rendre les choses plus claires. 

Model parameters

Inside the model are millions of numbers that dertermine how we process inputs.

Training a model

Settig the numbers in the matrices for a model.

Vector

A list of numbers in a coordinate system (x,y)

Souvent visualisé comme des points ou des flèches.

Matrix

Une tabel de nombre. Multiplier une matrice de temps de vecteur...

BERT transforme le texte en vecteurs.

Nous avons des textes avec des syntaxes compliquées et des sémantiques qui embarquent beaucoup d’information, mais il est difficile d’accéder à la signification computationnellement.

Les vecteurs sont des listes de valeurs dans un système coordonné, ils sont faciles à traiter computationnellement, mais en eux-même sont déprouvus de toute signification.

BERT transforme le texte en vercteurs (à la fois les mots individuels et les passages complets).

Pose chaque mot dans une case, pour chacun sort un vecteur comme position spécifique. Tous les autres mots dans la phrase disposent aussi d’un vecteur qui seront placés ailleurs dans l’espace. Mais sur la base du contexte de ces mots. Multiplication de matrices qui sont une manière de transformer série de word vecteurs en matrices qui contiennent de la sémantique.

### Explorer BERT word embeddings à partir d’une collection de poésie

cf. Links

https://colab.research.google.com/drive/192YOj8N9isRsEvOQwaI2WZ3pRSlUgAYb?usp=sharing#scrollTo=ygmgQSrFUgIj

https://colab.research.google.com/drive/1r_eoi8CMea_a3YjWC1M4EmTqKMGVMbzQ?usp=sharing

https://colab.research.google.com

https://colab.research.google.com/drive/192YOj8N9isRsEvOQwaI2WZ3pRSlUgAYb?usp=sharing

### Représentation plus formelle

Comprendre fonctionnement interme. Figures.

Perceptron : the most basic classifier : an equiation that takes an input vector and returns 0 or 1

Layer : One step of a neural netwok, possibly many perceptrons in parallel

Transformer : A class of NLP model that builds representations of words in parallel. BErt is an exemple

Attention

Diagrammes souvent présentés. Parcourir le processus qui intervient quand alimente avec du texte.

Un texte d’entrée que tokenize, ceux-ci convertis en vecteurs à partir embedding Learned during pre-training. Ajoute vecteurs de positions. Ensuite entre dans premier des blocs d’encodage. Ceux-ci occupent une place importante dans ce système. Ces encodeurs très vastes, tonnes de nombre contenus, rendent le modèle difficile à comprendre, et donc implémenter, mais opérations simples.

Multiplication des vecteurs par poids (attention). Ajout et normalisation. Niveau de perceptrons (feed forward) car passe les valeurs en arrière sur un grand ensemble de perceptron. Tonnes mais chaque un simple système de machine learning. Puis ajouts et normalisations. 

Nombreux blocs de ce type. Nombreux encodeurs supplémentaures. C’est de là que proviennent les vecteurs de mots.

Convert to number of classes (linear layer)

Convert to probability distribution (softmax)

### Cycle de vie d’un modèle BERT

Comme ces modèles très gros et coûteux à entraîner, ils ont un cycle de vie. Un modèle BERT consiste en 400M de nombres. D’où viennent-ils ? pourquoi changent-ils ?

Pre-training, gradually improve parameters by looping over large datasets. --> wikipedia, self-published novels, etc.

Encode de nouveau document. Prendre les entrées, produire des sorties, mais ne pas changer les modèles du paramètres. Ex. ajout de poèmes.

Fine-tuning : gradually improve parameters for a new purpose by looping over smaller datasets.

Production use. Take new imputs, produce outputs, make non change to parameters. Genre classification, etc.

### Comment a été entraîné ?

Pour chaque segment essaye de prédire quel terme doit venir.

Comment utiliser BERT avec ou sans fine-tuning.

Comme utiliser un mixer sur lequel peut placer plusieurs adapateurs spécifiques à différentes tâches.

Mapping words and sentences to vectors, which we can use directly ex. Measure word similarity

Or we can add task-specific methods

### How do I actually use Bert ?

Comment fait entrer son preopre texte dans BERT.

Bonne nouvelle, Beaucoup d’outils déjà existant ! 

Même si formidables, pas forcément faciles d’accès pour ceux qui ont peu de familiarité avec NLP. Idée du tutorial faciliter.

HuggingFace qui produit librairies Python pour NLP pour transformers

- très commodes
- beaucoup de documentation
- beaucoup de modèles parmi lesquels BERT et GPT-2, cahngement de modèle facile
- beaucoup de datasets
- communauté très active

Nécessite connaissance librairies de deepl learning comme Pytorch, ou documentation suppose que les cas d’utilisations comme analyse de sentiments. Datastes traditionnels.

### Can I work with BERT/HuggingFace on my laptop ?

Oui mais avec des modifications et des caveats

Risque d’être très lent et probablement pas la situation idéale.

C’est la raison pour laquelle introduire la notion de GPU. Graphic processing unit, un circuit électornique spécialisé poru la computation.

Permet parallel processing, souvent utilisé pour tâches graphiques consommatrices.

Si pas accès, possible utiliser Google Colab Notebooks, des documents interactifs pour programmation, similaire de Jupyter. Offre accès gratuit et payant à des GPUs.

Pour utiliser GPUs avec Colab, besoin .to('cuda') quand charge les modèles pré-entraînés. CUDA est une plateforme de computation parallèle créée par NVDIA.

DistilBert

Une version plus simples de BERT qui peut être utilse pour travailler localement. Peut aussi fine-tune ce modèle.

### BERT Models Beyond English

Nombreux modèles développés pour d’autres langues. Nombre d’entre eux accessibles par HuggingFace https://huggingface.co/models

Mais peut être difficile de déterminer quel modèle le plus approprié pour travailler sur vos données ou selon vos objectifs.

FWIW, ERNIE is a very good BERT-like model for Chinese

Very pro puns myself. CamemBERT is a good French model

Italian BERT is ALBERTO :)

### Previewing a few BERT & HuggingFace Basics

Formater le texte dans un format compréhensible pour BERT.

Quaque séquence entrée 512 tokes

- petites séquences qui doivent être *padded* (add special tokens)
- longer sequences...

BERT Special Tokens

[CLS] au début de tous documents

[SEP] entre chaque phrase

[PAD] ajouté à la fin documents

\# pour certains mots

Ignore les sauts de ligne. Que perd-on quand supprime cela ?

Overview doc with slides link: http://bit.ly/BERT-Humanists-Workshop

Ne peut pas déterminer la tokenisation.

https://paperswithcode.com/method/wordpiece

https://www.dropbox.com/scl/fi/w9w2bs55o0fm1upl2hrhz/BERT-for-Humanists-Annotated-Bibliography.paper?dl=0&rlkey=7qtjce0tilgg42sn7kywwqloh

https://huggingface.co/

https://melaniewalsh.github.io/BERT-for-Humanists/

### Note book

### Use Case pour fine-tuning

Imaginer que ensemble de textes de recentions et veut prédire étiquettes de genre pour explorer à quel point ces étiquettes sont adaptées.

Un exemple de tache supervisée et fine-tuned.

NLP "Tasks"

Classification : single category,, genre prediction sentiment prediction

text generation : tokens, translation, autocomplétion

Retrieval : similarity score, search

Tagging : one category... pour étiquetage discours

### Distinction pre-training et fine-tuning

Pour le moment seulement utilisé le modèle pré-entrainé. Après pré-entrainement sur un grand corpus possible de fine-tuning it pour un plus petit ensemble de données ou des tâches spécialisées.

Architecture pre-training

- transformer architecture : a stack of encoders
- deux tâches de pré-entraitement : masked word prediction / next sentence prediction
- training data include the BooksCorpus (800M words) (Zhu et al., 2015) et English Wikipedia (2,500M mots)
- ...

Preparing your data for fine-tuning

- converter lables vers integers plutôt que chaînes
- couper données en entrainement, tests, ensemble évaluations
- utiliser BERT Tokenizer pour convertir les données ...
- torch dataset...

Fine-tuning, partie où utilise se propses données.

Met à jour BERT pour vos données et optionnemelent vos tâches de classification.

Ajouter nouevlels couches qui contiennnt classification

Utilisation GPU ?...

The Bert Fine-tuning "Recipe" with HuggingFace

1. Formater les données
2. Load a pre-trained Bert
3. Fine tune
4. ..

Voir le doc

Comment apprend de ces nombres

comme nb ML modèle apprentissage avec un alog **gradient descent**

Csqses

Un

