---
date: 2022-04-11
tags: deepLearning, IA
---



## “New Tools for Old Documents – Layout Analysis and OCR with Deep Learning and Heuristics”

**Clemens Neudecker,** Berlin State Library, Berlin, Germany

https://www.kbr.be/en/agenda/dhs-layout-analysis/

Berlin State Librayr, établie en 1661 sous le Royaume de Pruse. Une des bibliothèques les plus importnetes d’allemange. Membre de SPK Prussian Cultural Heritage Foundation.

NUmérisiation in-house depuis 2007. Plus de 20M de pages numériquesée.

Quartor.ai une plateforme pour des solutions de contenus intelligents. BMBF 2019

SBB responsable du sous-projet 10 "AI for digitized cultural heritage"

https://qurator-data.de/

https://github.com/qurator-spk

https://qurator.ai/partner/staatsbibliothek-zu-berlin/

Document Layout Analysis for Text Recognition

Documents haute qualités reconnus pour des élements textuels. State of the art OCR à partir de lignes segmentées.

## Eynollah 

analyse de mise en page. Retourne Page-XML, identification des régions de textes et des lignes de textes.

Entraîné pour ResNet50-U-Net model pour pixel-wise segmentation. 

Prmeière itéartion pure ML

2d itération hybridismes ML + Heuristics.

améliore la reconnaissance des lignes et ordre de lecture.

https://github.com/qurator-spk/eynollah

Plusieurs ML models utilisés en coordination. Flux de données.

Image scaling and optimization. Prendre des images de hautes qualités puis réduction résolution. Pour entraîner les données.

Réduction du bruit de la page précédente.

Ensuite première classification des régions de la page.

Cas arabe, etc.

