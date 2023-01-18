# Lise Jaillant PI (française)

http://www.lisejaillant.com

Connecter les personnes US et UK sur IA.

Katie Aske, organisation.

Annalina Caputo, co-PI.

Maria Castrillo

## **Dr Giles Bergel** (University of Oxford / National Library of Scotland) **Title:** *Visual AI and Printed Chapbook Illustrations at the National Library of Scotland* **Einion Gruffudd** (National Library of Wales)

Visual Geometry Group

robots.ox.ac.uk/~vgg

https://digital.humanities.ox.ac.uk/people/3198#/

Capt book, partenariat avec Bnf

https://data.nls.uk

https://data.nls.uk/data/digitised-collections/chapbooks-printed-in-scotland/ 3000 Chapbooks océrisés et enrichis par des métadonnées

Gallerie IIIF, etc. mais aussi métadonnées curationnées

Toruver les illustrations avec CNN (EfficientDet)

Match et grouper les illustrations SIFT features

Custom VGG image annotation software LISA

Classer les sujets des blocs avcec CNN (VGG VIC/ResNet)

https://gitlab.com/vgg/lisa pour annotation des listes d’images.

Annotation amnuelle de 337, entrainement pour appliquer aux 20K images. Révisions de 1608 annotations. Réapplication sur 43k images.

Sorties illustrations, etc.

Faux positifs significatifs : icones et marginalia

Identité visuelle claire pour ces contenus à travers le temps.

VGG Image Search Engine VISE très facile à utiliser car fournit des interfaces graphiques. Repère des motifs analogues entre deux images même avec des déformations.

Permit de relpérer réutilisation de blocs à travers le corpus. Y compris à des dates diverses. Mais aussi de blocs de copie. Parfsoi arrangment créatifs.

VGG VIC/ResNet modification par lui-même. Très largement disponible.

robots.ox.ac.uk/~vgg/software/vic/index.html

Moteur de recherche qui intègre Google Image, possible de réentrainer des images. Biais liés à l’utilisation de ImageNet. Possible de réentrainer avec Google Images. Également possible de fournir ses propres images par IIIF.

IA souvent entraînées sur des images couleur. Parfois du mal à classifier des contenus NB.

Pour le moment classification que les bibliothécaires considèrent comme expérimental ou analytique.

Étapes futures

- produire un standard catalogage pour les blocs et leurs impressions
- asigner identification pour les NLS illustrations basées sur ces standards
- métadonnées

Conclusion

Besoin de données bien curationnées. Les outils d’annotation sont toutefois tout aussi importants que les classificateurs. Les modèles génériques fonctionne bien pour les livres mais négatifs.

AI softwoare dev beneficie des cas d’usage y compris préparation des données, etc.

## Enion Gruffudd

**Title:** *Describing the Welsh National Broadcast Archive* 

Archives de la BBC, grande partie numérisée.

Projet qui inclue le public dans la découverte de ce matériau.

- voice2text
- crowdsourcing
- Automated keywords
- Linked data
- online exhibition



## **John Stack** (Science Museum), Title:** *Machine Learning and Cultural Heritage: What Is It Good Enough For?*

V&A propose chose comparable. Propose connexion avec autres projets nationaux de connecter contenus. Question de recherche consiste à savoir dans quelle mesure le passage à l’échelle permet d’améliorer le catalogage des collections.

Lier les collections à Wikidata. Et à travers Wikidata à d’autres choses ou collections.

- Améliorer les interfaces de collections
- améliorer découvrabilité
- liens aux autres sources

AI, LOD, Knowledge Graph

Surtout utilisation de Machine learning

- Easy Wings : processing IDs and URLs (links)
- Disambiguation : adding new links to Wikidata chercher des personnes etx. et voir si peut faire une connexion. Fonctionne bien sur les personnes et les collections d’objets.
- NER Named Entity Recognition

Utilisation knowledge graph pour créer interfaces.

Widget.

**ML fonctionne pour**

Intéressant pour suggérer des possibilités et mettre en lumière des connections.

Identification de tendances et manques

Visualisation étendue et diversité des collections.

Identification contenus en rapport

Travailler à l’échelle

Apporter une nouvelle terminologie à côté du catalogue

**Mais**

ML génère du contenu qui nécessite un encadrement ou des contextualisations.

Faux positifs, pas toujours apparents et requiert savoirs de spécialistes.

Notions de collections canonique mise en cause 

comprendre ce que ne peut pas encore faire

approches critique nécessaire.

GitHub.com/TheScienceMuseum/heritage-connector

 www.ai4lam.org



https://collection.sciencemuseumgroup.org.uk/api/objects/co159324

https://ai.harvardartmuseums.org/explore

On the Books corpus

https://github.com/UNC-Libraries-data/OnTheBooks/blob/master/workflow.md

Sur utilisation IIIF et Google

https://docs.google.com/document/d/19eVfnVoirwA462_GltwRLyscDQ6Jby4cW225tpCgdNw/edit#heading=h.ylsw36sxin6j

---

**Room 4:** Developing International Projects. Chair: **Nora McGregor** (The British Library)

Travaillé cours d’introduction IA pour les GLAM. Avec Smithonian. Software Carpentry

https://librarycarpentry.org/

Méthodes pour transférer ce type savoir.

https://instasociety.org Instagram

[10:18] Olivia Dorsey (Guest) Hi! I'm Olivia Dorsey, an Innovation Specialist from the Library of Congress. Working on Computing Cultural Heritage in the Cloud initiative. More tech person than librarian. Am interested in learning more about AI + Machine Learning in DH.

[10:19] Anna Maria Marras (Guest) Anna Maria Marras University of Turin, archaeologist and digital museums expert. I'm currently researching Open Heritage and digital accessibility

[10:18] Thornhill Tamara (TfL Corporate Archives) really interested in AI to extract data from manuscripts and digital documents - particularly unstandardised digital documents

[10:18] Yasamin (Guest) PhD student at University of Miami and the funder of Instasociety.org

[10:17] Ma,Xiaoli Metadata Librarian, University of Florida

[10:17] Thornhill Tamara (TfL Corporate Archives) Archives Manager from Transport for London

[10:17] Paul Jason Perez Paul Perez, I'm an Assistant Prof at the University of the Philippines School of Library and Information Studies. I'm currently researching Open Heritage Data in Philippine Museums

[10:17] NOCKELS Joe Hi I'm Joe Nockels, a PhD researcher at the National Library of Scotland looking at Handwritten Text Recognition.

[10:17] Bart Magnus - meemoo (Guest) I work in the expertise team of meemoo, supporting and advising on digital heritage projects in Flanders (Belgium).

[10:17] Victoria Webb Librarian who works with mixed collections at Wellcome Collection

[10:17] Alexandra Eveleigh I'm the Collections Information Manager at Wellcome Collection in the UK, and an archivist by background

[10:17] Capobianco, James I'm a reference librarian at Houghton Library (Harvard), but also studying Data Science, so really interested in the connection of cultural institutions and AI and ML.

[10:17] Maria Whitaker (Guest) Computer Scientist here. From Indiana University.

[10:19] Christopher Loughnane Visiting Research Scholar in Digital Scholarship at Auburn University. Dual background in librarianship and critical digital/info studies. I chair the Digital Scholarship Interest Group at Auburn and involved in various digital projects including VR and haptic tools. AI noob

## Thomas Padilla

***Thomas Padilla*** is Director of Information Systems and Technology Strategy at the [Center for Research Libraries.](https://www.crl.edu/)

http://www.thomaspadilla.org

Consortium de bibliothèques de recherche en amérique du Nord initialement consacré au partage de journaux numériques dans un contexte ouvert.

Thomas engagé sur l’ouverture des collections.

PI collections as data, établir des guidelines pour rendre les collections computationnelles. 12 collections ouvertes de cette manière.

2019, produit un rapport Responsible operation sur IA. Focalisation sur la morale et les implications éthiques de l’utlisation de l’informatique.

Nicole Coleman, https://library.stanford.edu/people/cnc

https://collectionsasdata.github.io/statement/

Consortium de bibliothèques de recherche créé 1949.

Aeolian Network

GLAM potentiel distinctif dans le contexte des GLAM

Non Scalability in IA. Déterminer si l‘échelle justife le cout.

The Mushroom at the End of the World. Anna Lowenhaupt Tsing On NonScalability

Question de la précision. 

Ruines de la forêts. Cultivés par des migrants. Quand quelque chose paraît disponible, se poser la question de toutes les couches inférieures.

The Next Generation AI, from language to models to sclae.

Directive européenne, régulation of the European parlement IA

Michael Veale, Demystifying the Draft EU Artificial Intelligence Act. Bien d’avoir critique.

Infromation Maintenance as a Practice of Care. Maintenance forme fondamentale de l’innovation qui supporte information et communautés.

Maintainers, The Information, D. Olson, J. Meyerson, M. A. Parsons, J. Castro, M. Lassere, D. J. Wright, et al. 2019. « Information Maintenance as a Practice of Care », juin. https://doi.org/10.5281/zenodo.3236410.



Padilla, Thomas. 2016. « Humanities Data in the Library: Integrity, Form, Access ». *D-Lib Magazine* 22 (3/4). https://doi.org/10.1045/march2016-padilla.



———. 2019. « Responsible Operations: Data Science, Machine Learning, and AI in Libraries ». OCLC Research Position Paper. OCLC. Consulté le 7 juillet 2021. https://doi.org/10.25333/xk7z-9g97.



Padilla, Thomas, Laurie Allen, Hannah Frost, Sarah Potvin, Elizabeth Russey Roke, et Stewart Varner. 2019. « Always Already Computational: Collections as Data ». Final report. Collections as Data. Consulté le 7 juillet 2021. https://doi.org/10.5281/zenodo.3152935.



Padilla, Thomas G. 2018. « Collections as data: Implications for enclosure ». *College & Research Libraries News* 79 (6) : 296. https://doi.org/10.5860/crln.79.6.296.



Maintainers, The Information, D. Olson, J. Meyerson, M. A. Parsons, J. Castro, M. Lassere, D. J. Wright, et al. 2019. « Information Maintenance as a Practice of Care », juin. https://doi.org/10.5281/zenodo.3236410.

Padilla, Thomas. 2016. « Humanities Data in the Library: Integrity, Form, Access ». *D-Lib Magazine* 22 (3/4). https://doi.org/10.1045/march2016-padilla.

———. 2019. « Responsible Operations: Data Science, Machine Learning, and AI in Libraries ». OCLC Research Position Paper. OCLC. Consulté le 7 juillet 2021. https://doi.org/10.25333/xk7z-9g97.

Padilla, Thomas, Laurie Allen, Hannah Frost, Sarah Potvin, Elizabeth Russey Roke, et Stewart Varner. 2019. « Always Already Computational: Collections as Data ». Final report. Collections as Data. Consulté le 7 juillet 2021. https://doi.org/10.5281/zenodo.3152935.

Padilla, Thomas G. 2018. « Collections as data: Implications for enclosure ». *College & Research Libraries News* 79 (6) : 296. https://doi.org/10.5860/crln.79.6.296.

https://www.gov.uk/government/groups/ai-council

https://cogx.live/agenda-2021/

**Avoir jeu de données pour compétition dans le domaine patrimonial**

Downie, J Stephen, HathiTrust volontaire

https://www.forbes.com/sites/gilpress/2021/06/16/andrew-ng-launches-a-campaign-for-data-centric-ai/?sh=67994e9674f5

https://www.music-ir.org/mirex/wiki/MIREX_HOME

## Table ronde

**17:00** **–** **17:30:** Roundtable. Chair: **Dr Katherine Aske** (Loughborough University).

**Title:** *Roundtable discussion with the AEOLIAN Project Team*: **Dr Lise Jaillant**, **Dr Annalina Caputo**, **Glen Worthey** (University of Illinois), **Prof. Claire Warwick** (Durham University), **Prof. J. Stephen Downie** (University of Illinois), **Dr Paul Gooding** (Glasgow University), and **Ryan Dubnicek** (University of Illinois).

Claire Warwick

https://www.ucl.ac.uk/information-studies/claire-warwick

Paul Gooding

https://www.gla.ac.uk/schools/humanities/staff/paulgooding/

Glen pour les US

Lise Jaillant, réseau