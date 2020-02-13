---
date: 2015-10-29
tags: cr, conférence, tei, lod


---

# TEI Ontologies SIG, Lyon 2015-10-29

- Emmanuel Château, in charge of various TEI projects, specially interested in the work which have been done by the SIG with representation of TEI in RDF for places and persons.
- Florence Clavaud, in charge of authorities in National french archives, currently participating to an archival ontology
- Kathrin Pindl ? (not Kathryn Tomasek), from MEDEA (Modelling Semantically Enhanced Digital Edition of Accounts)
- Tubingen
- Francesco Beretta, plateform for digital history. Use of CIDOC-CRM but also of TEI text to link historical data with text.
- Vivianne Pouletran, Lyon participating to Persée
- Fabio Ciotti, working on a projet where want to express geographical featurs to make an geographic ontology. Now interested on the fact to ontologize TEI, currently working with collegues on that trying one step beyond. I think this group should try this step.
- Martin Holmes, working on many digital projects in TEI, on the Council.
- Christian-Emil Ore. Working with museum, lexicography, have been engaged on the development of CIDOC-CRM.

There is already a cultural ontology dealing with museum domain and bibliography (CIDO-CRM and FRBR-OO)
Ontology the fact to share conceptualisation, etc.

You may have followed the discussion of this morning, about working on an ontoly. This is not common to ear this here. An other fact, some elements expressing the same thing, so such things that can be expressed in a common way. Working on mappings.
With Øyvind Eide work in TEI in 2009, we have been looking at what is possible to express in TEI. See how much the expressivity of TEI can express CIDOC-CRM.

TEI and cultural heritage ontologies: Exchange of information?
cf. TEI and cultural heritage ontologies: Exchange of information?
Christian-Emil Ore and Øyvind Eide
http://llc.oxfordjournals.org/content/24/2/161.abstract

Extracting information from a catalogue, text with a markup structural, lemmatization, information elements identified and marked up according to a simple information model. Use of Museum database, artefacts, excavations, referential information = get back the information.
Common to tag the text and extract the text, nowadays possible to use RDF dataset.

A fragment of a imaginary report.
ex. identification of elements
Actor
  Relation
​    Event: E1
​      type excavation
​      ...

Doesn’t say that could extract information automaticaly. But focus on how much information could be extract.
Three possible strategies :
- store information as XML-doc
- Store information in the TEI header
- store information in the TEI header as RDF

person provides ifnoramtion abaout an identifiable individual
org   ...
Place ...
event ...
relation describes any kind of relationship or linkage amongst a specified group of participants

Then it’s possible to connect, express a model as CIDOC-CRM in TEI. There are some part in TEI that are more, over, specified in TEI than in other langage. For example for person and place (properties list). Statelike, vs State
Could that have been simplified ?

Introduce a _description_ element
<description type='trait'> etc.

TEI P5 introduces several new useful ontological elements.

Suggested extensions and adjustments :
- introduce an element _conceptualObject_ for conceptual/abstract objects
- introduce an element _physicalObject_ for physical objects
- Extend the scope of _relation_ to the object elements and to events and add the type attribute
- extend the scope of _taxonomy_ to non-textual entities
- Extend the scope of _desc_ to all ontological elements and desc be a super element of the classification element, eg, <age>, will be equal to <desc type='age'>
- consider to state explicitly other equivalences like publisher and <name type='publisher'>

Question on the fact to formalize more this things.
Would be a good idea, but would be add an extra element to TEI elements. The question could be make the TEI tighter by adding formal description to each elements.

For historical reasons the SIG have not made very much project these two last years.
Our aims for the group was to develops proposals for how detailed information about persons (physical and legal), dates, events, places, objects, etc., as well as their information.
Formalisation of TEI element, but didn’t thought at this time that time was came for that.

To do list (mostly not done)
Five suggestion for extending/adapting TEI to enable a 1-1 maping between a subset of CIDOC CRM and the ontological elements in TEI P5.
1. Introdcution of an element for physical objects on the same level as person, places
2. The introduction of an element for abstracts object (cf. work/expression/manifestation in FRBR and motif e.g. Mona Lisa) on the same level as person, places.
3. A 'description' element and a description-like class containing the calsses trait-like
4. ...
5.

Manuscripts ? Books ?
But you can also have a stone inscribed or a sword with an inscription.
Suggestion 2014 (didn’t done)
Go throuht the manuscript module to see what is specific and generic.
64 element in the module
Big work to do, participants welcome
<event>-like elements in history
<origin>
<provenance>
<acquisition>
Suggestion to replace by event and type them.
<custodialHist> et <custEvent> no difference from the ontological point of view

Suppress the ms prefix to identifier, part, physDesc, history, additional, contents

FC One participants evoque a project where they had to describe bindings and manuscripts, for the modelling we needed to customize the TEI on this because it was too specific.
It’s possible to generalize physDesc and specialize under-element.

MH Would you rather prefer to thraw all away ?
There is backwards compatibility issues.
Have been investigating in the manuscript stmt, it would possible to make a clear statement.

EM One participant working with Epidoc, explain that they had many a huge discussion about the conceptual model of what is a manuscript. There would be shortly a ms-fragment. But no under-elements are really specific to manuscripts.

FB Content description identify manuscript or text binding object. The problem is the ms.

FC Would be interesting to review if everything is present there. For an archival point of view, one key thing here is unpresent : how to link a manuscript to an another one, there is not currently a real solution in TEI. listWit but not allright, listRelation possibaly.

It is possible to treat the text in relation in msContents, but in archival context, a sequence. Nothing to express which relation are between texts. Corpus could join them, but it doesn’t express any kind of relation.

Could be possible to distinguish physical objects and the writing itself. If you speak of an physical object distinct of the object your working on.

The proposition to suppress ms prefix was in a way supposed to use this element in other content model like object, etc. The distinct proposition between object and physical object could be resolved with the new element object.

There is a real tradition to describe manuscript with msDesc.
This work would better done form scratch with a whole reflexion on the ontology of TEI.

But this work would take a very long time before to be achieve. It may be difficult to wait this achievement, puting aside this proposition, before this work done ?

Elements to mark part of catalog of TEI.
Important question to decide how to act stategically : or in a pragmatic way with this proposition which are based on a ontological analysis, or work on the whole issue of the TEI ontology. But in a way interesting to work also on the informal ontology expressed by the TEI.

Object proposal
The same thing, because the object could replace the text ! It’s a question about what you call a text. Just to exemplify it, if you take the lecture, etc. it’s an abstract expression not a physical book. My suggestion is to make a more general physical object, or physical object description and see how it could fit with the actual msDescription. It’s also a concrete way to work in the direction proposed by Elena this morning.

We’ll contact you by mail. 
Unfortunatly Sebastian isn’t among us today. I will bring back to him the discussion.
