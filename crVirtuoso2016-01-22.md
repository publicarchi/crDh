
# Jennifer Drouin, Shakespeare au/in Québec: Building a bilingual, open-access database and critical anthology in collaboration with the Internet Shakespeare Editions

Partenariat
- Renaissance edition
- Queens’s men Editions

Contribuer à l’économie canadienne en diffusant éditions canadiennes. Annoter pour illuminer textes dans le contexte québécois.
23 non imprimés et donc pas accessibles.
12 imprimés, mais aucun n’a encore fait l’objet d’une édition critique.

Canadian Adaptations of Shakespeare Project incluera revues des adaptations scéniques, cinématographiques ou autres.
2 en anglais, mais toutes les pièces en français.

DRE et QME différences
Theory of Shakespearean Adaptation, inclue réécriture textuelle qui réengagent directement le texte. Exclue certain nombre de choses.

Chronology of Québécois adaptations of Shakespeare, 1960-2013.
Adaptation qui révèle discours nationaliste, question du langage en 70, 90 gender diversity.
Jeu sur les codes nationalistes, anti ecclésiastique, etc.

Michel Garneau, publie Macbeth traduit en québécois, tradaptation. Approximation d’un dialecte 18e.

Adaptation du Roi Lear. Figure des cousins batards pour représenter québécois et canadiens.

90’s explosion des adaptations incluant adaptation par femmes queer. Nombre considérable des textes produits à cette époque. Diversité des voix. Focus sur la parole des femmes ou des minorités comme migrants. Position du sujet, intersectionnalité. 

Nouvelle génération d’adaptation qui engagent dialogue avec le texte originale en accordant une place particulière à la pluralité culturelle et sociale.
Peu focalisent femme, etc.

Variation dans le corpus à la fois en termes de formes ou de contenus.
Parfois fondées sur plusieurs sources ou bien une seule. Réflexions biographiques sur la vie de Shakespeare.

Markup en TEI à la différence de pdf qui ne permet pas manipulation du texte.

Texte adapté sera collationné avec éditions anglaises en utilisant TLN moderne édition de ISE
Toutes allusions historiques et politiques seront relevées et annotées par des notes historiques.
Correction des spellings, possibilité de conserver texte avec TEI, = à la fois production d’un texte intégral et grand public.

Premier texte encodé le plus complexe pour révéler ensemble de problème auxquels pourra ensuite être confrontés.
Henry V où jeu avec politiques contemporains Trudeau, etc. Voir son livre où 20aine de page d’analyse sur le sujet.

Exemple d’encodage
\<l\> pour les vers, xml:id sur chaque.
\<ref\> pour notes avec @target #fn pour les notes critiques
name pour marquer les personnages
Liens externes et internes. Liens vers Google Maps pour premiers lieux d’interprétation.
Note vers source secondaires.

Markup pour croiser sources
\<sp\> avec @who et @ana pour encoder les dialogues et speakers.
utilisation de @prev et @part
\<addspan\> et span element pour passages pour créer des popup avec @from et @to
Utilisation numérotation de l’édition moderne pour correspondance.

Intertexte pour les textes non Shakespeariens ou Shakespeariens.
\<spanGrp\> pour regrouper les passages FLQ avec lien vers les textes originaux.

Composant de base de données
Plusieurs milliers d’articles et programmes.
Gérés dans 16 tables de 2 à 12 colonnes de données. La plupart sont liés avec des clefs externes entre elles. Par exemple pour table des pièces, etc.
Sans doute également besoin d’ajouter une table pour les compendium outre les adaptations.

Interface en cours pour ajout d’entrées, etc.
7 types entrées : performances, artefacts ou collection, series, compagnies, personnes, théâtre ou contributeur.
Formulaire de saisie jusqu’à 33 champs.

Essaye de pouvoir de mapper avec SIP
[http://internetshakespeare.uvic.ca][1]

## Discussion

TEI limiting pour liage
éléments et attributs, comment distinction des niveaux d’intervention sur le texte. Manque les instructions scéniques, mais comme les ajoutait dans le texte devait pouvoir les distinguer. Correction de la grammaire car parfois seulement rédigé pour la production mais non pas pour l’édition. @resp mais pas attribut global dans la TEI.

Comment prend en charge adaptations bilingues ? Quelle langue pour l’édition critique ?

Quel futur pour ce projet ?
Adaptations de Shakespeare au Québec très important.
En novembre une adaptation majeure. 

[1]:	http://internetshakespeare.uvic.ca