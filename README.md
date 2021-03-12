## Tick Interaction Database
[![Build Status](https://travis-ci.org/ParasiteTracker/tick-interaction-database.svg)](https://travis-ci.org/ParasiteTracker/tick-interaction-database)  [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:ParasiteTracker/tick-interaction-database)](http://globalbioticinteractions.org/?accordingTo=globi:ParasiteTracker/tick-interaction-database) 

[```Citation```](#Citation) / [```Interaction Types```](#interaction-types) / [```Data Definitions```](#data-definitions) / [```Included Resources```](#included-resources) /  [```Data Issues```](#data-issues) / [```Summary```](#summary)


### Description

The tick-interaction-database is a repository for interaction and ecological trait data about ticks. The observations are from the literature and focused on tick hosts, which are important vectors of many arthropod borne pathogens. This is part of the [Terrestrial Parasite Tracker](http://parasitetracker.org/).

This GitHub repository was cloned from [globalbioticinteractions/template-dataset](https://github.com/globalbioticinteractions/template-dataset), which includes a blank interactions.tsv, README and globi.json. GloBI requires that the interactions.tsv be called interactions.tsv and for the globi.json file to exist. Some column headers of inteteractions.tsv file was modified from the cloned template, but follow the naming conventions.

### Citation

Seltmann, K. (2020). TID: A project to share biotic interaction and ecological trait data about ticks. UC Santa Barbara: Cheadle Center for Biodiversity and Ecological Restoration.

### Funding

The tick-interaction-database is funded by the National Science Foundation award "Collaborative Research: Digitization TCN: Digitizing collections to trace parasite-host associations and predict the spread of vector-borne disease," Award numbers [DBI:1901932](https://nsf.gov/awardsearch/showAward?AWD_ID=1901932) and [DBI:1901926](https://nsf.gov/awardsearch/showAward?AWD_ID=1901926).

### BioticInteraction Types

The biotic species interactions in this dataset were mapped to terms in the Relations Ontology (RO). Biotic interactions are best viewed through [Global Biotic Interactions](https://www.globalbioticinteractions.org/)

interactionTypeName | interactionTypeId | description
--- | --- | --- |
has host |http://purl.obolibrary.org/obo/RO_0002454|X 'has host' y if and only if: x is an organism, y is an organism, and x can live on the surface of or within the body of y|
(biotically) interacts with | http://purl.obolibrary.org/obo/RO_0002437 | An interaction relationship in which at least one of the partners is an organism and the other is either an organism or an abiotic entity with which the organism interacts.


### Other Properties

propertyTypeName | propertyTypeId
--- | --- |
in nature | http://purl.obolibrary.org/obo/ENVO_01001226
male | http://purl.obolibrary.org/obo/FBcv_0000333
female | http://purl.obolibrary.org/obo/FBcv_0000334

### otherTraits
Presently, otherTraits are listed as a key:value list (delimited by semicolons). These include body size, nesting behavior, and any other traits that are not considered biotic interactions. Trait terms are following [Encyclopedia of Life - TraitBank](https://eol.org/traitbank). Traits are defined as being either from the source or target taxon. They can be sourceGeneralObservation/targetGeneralObservation, which indicate overall study results, or sourceCommonKnowledge/targetCommonKnowledge, which indicates general knowledge about the taxon.

 
### Data Definitions

The definitions of the columns used in the interactions.tsv dataset are described here. If these correspond with Darwin Core they are mapped to those classes. Some of the columns in the template were unused.

  * **InteractionID** : An non-unique identifier that links two interactions as part of the same observation in the dataset.
  * **basisOfRecord** [DWC:BasisOfRecord](http://rs.tdwg.org/dwc/terms/basisOfRecord) : The specific nature of the data record. For literature use LiteratureRecord.
  * **interactionText** : The phrase or phrases copied verbatim from the text that describe the interaction.
  * **sourceTaxonId** [DWC:scientificNameID](http://rs.tdwg.org/dwc/terms/scientificNameID) : An identifier for the nomenclatural (not taxonomic) details of a scientific name.
  * **sourceTaxonName** [DWC:scientificName](http://rs.tdwg.org/dwc/terms/scientificName) : The lowest level taxonomic rank that can be determined.
  * **sourceFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * **sourceCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : common or vernacular name.
  * **sourceSexName** [DWC:sex](http://rs.tdwg.org/dwc/terms/sex) : The sex of the biological individual(s) represented in the Occurrence.
  * **sourceLifeStageName** [DWC:sex](http://rs.tdwg.org/dwc/terms/lifeStage) : TThe age class or life stage of the biological individual(s) at the time the Occurrence was recorded.
  * **interactionTypeId** : Identifier for the interaction type. This is the term that is the interpreted term of the interaction found in the paper.
  * **interactionTypeName** : interaction type (ex. eats, piercing). The name of the interaction type should be the name as it is listed in the original text, which is not always the name of the term it is mapped to. As long as the definition to the mapping is compatible with the ```interactionTypeName```, it is usable as a ```interactionTypeId```.
  * **isNegated** : This field is presently not supported in GloBI. It is intended to relate that a specific interaction was explicitly not observed.
  * **targetTaxonName** [DWC:scientificName](http://rs.tdwg.org/dwc/terms/scientificName) : The lowest level taxonomic rank that can be determined.
  * **targetFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * **targetCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : common or vernacular name.
  * **targetLifeStageName** [DWC:sex](http://rs.tdwg.org/dwc/terms/lifeStage) : TThe age class or life stage of the biological individual(s) at the time the Occurrence was recorded.
  * **higherGeography** [DWC:country](http://rs.tdwg.org/dwc/terms/higherGeography) : The name of the continent in which the Location occurs.
  * **enteredBy**  : The person entering the data.
  * **notes**  : Notes about the database entry.
  * **containsTaxonTreatment** : Does the paper contain taxon treatments? A taxon treatment is the scientific description of a taxon including a Latinized name of the nominate taxon, followed by one or several elements such as references to older literature citing this taxon and putting it in relation to the new information about the taxon being presented in the paper.
  * **TreatmentBankIdentifier** : The identifer for the taxon treatment from [TreatmentBank](http://plazi.org/resources/treatmentbank/). A paper with a taxon treatment will need to be looked up in TreatmentBank for the TreatmentBank identifier.
  * **referenceDoi** : This field was not populated in this dataset.
  * **referenceCitation**  : The reference for the interaction.


### Contribute
Literature used in this project is recorded on each record. If you have a new paper to add, please submit a [new github issue](https://github.com/ParasiteTracker/tick-interaction-database/issues/new).


