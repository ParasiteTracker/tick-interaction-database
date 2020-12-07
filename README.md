## Tick Interaction Database
[![Build Status](https://travis-ci.org/ParasiteTracker/tick-interaction-database.svg)](https://travis-ci.org/ParasiteTracker/tick-interaction-database)  [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:seltmann/tick-interaction-database)](http://globalbioticinteractions.org/?accordingTo=globi:seltmann/tick-interaction-database) 

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
  * **sourceVerbatimName** : An OTU, morphospecies or other designation of the taxon.
  * **sourceFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * **sourceCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : common or vernacular name.
  * **sourceSexName** [DWC:sex](http://rs.tdwg.org/dwc/terms/sex) : The sex of the biological individual(s) represented in the Occurrence.
  * **sourceSexID**  : Identifer for the sex name.
  * **sourceLifeStageName** [DWC:sex](http://rs.tdwg.org/dwc/terms/lifeStage) : TThe age class or life stage of the biological individual(s) at the time the Occurrence was recorded.
  * **sourceAssociatedSequences** [DWC:sex](http://rs.tdwg.org/dwc/terms/associatedSequences) : 	list (concatenated and separated) of identifiers (publication, global unique identifier, URI) of genetic sequence information associated with the Occurrence.
  * **interactionTypeId** : Identifier for the interaction type.
  * **interpretedInteractionTypeName** : The name or term applied to the identifier of the interaction type as reported by the linked ontology.
  * **isNegated** : This field is presently not supported in GloBI. It is intended to relate that a specific interaction was explicitly not observed.
  * **interactionTypeName** : interaction type (ex. eats, piercing). The name of the interaction type should be the name as it is listed in the original text, which is not always the name of the term it is mapped to. As long as the definition to the mapping is compatible with the ```interactionTypeName```, it is usable as a ```interactionTypeId```.
  * **targetBodyPartName**  : The specific name of the target body part. The name of the body part should be the name as it is listed in the original text, which is not always the name of the term it is mapped to. As long as the definition to the mapping is compatible with the ```targetBodyPartName```, it is usable as a ```targetBodyPartId```.
  * **targetBodyPartId**  : Identifer for the body part name.
  * **experimentalConditionName**  : ("in nature" - most common)
  * **experimentalConditionId** : 
  * **targetTaxonId** [DWC:scientificNameID](http://rs.tdwg.org/dwc/terms/scientificNameID) : An identifier for the nomenclatural (not taxonomic) details of a scientific name.
  * **targetTaxonName** [DWC:scientificName](http://rs.tdwg.org/dwc/terms/scientificName) : The lowest level taxonomic rank that can be determined.
  * **targetVerbatimName** : An OTU, morphospecies or other designation of the taxon.
  * **targetFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * **targetCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : common or vernacular name.
  * **targetLifeStageName** [DWC:sex](http://rs.tdwg.org/dwc/terms/lifeStage) : TThe age class or life stage of the biological individual(s) at the time the Occurrence was recorded.
  * **targetAssociatedSequences** [DWC:sex](http://rs.tdwg.org/dwc/terms/associatedSequences) : 	list (concatenated and separated) of identifiers (publication, global unique identifier, URI) of genetic sequence information associated with the Occurrence.
  * **country** [DWC:country](http://rs.tdwg.org/dwc/terms/country) : The name of the country or major administrative unit in which the Location occurs.
  * **stateProvince** [DWC:stateProvince](http://rs.tdwg.org/dwc/terms/stateProvince) : The name of the next smaller administrative region than country (state, province, canton, department, region, etc.) in which the Location occurs.
  * **county** [DWC:county](http://rs.tdwg.org/dwc/terms/county) : The full, unabbreviated name of the next smaller administrative region than stateProvince (county, shire, department, etc.) in which the Location occurs.
  * **verbatimLocality** [DWC:locality](http://rs.tdwg.org/dwc/terms/verbatimLocality) : The specific description of the place. Less specific geographic information can be provided in other geographic terms (higherGeography, continent, country, stateProvince, county, municipality, waterBody, island, islandGroup). This term may contain information modified from the original to correct perceived errors or standardize the description.
  * **locality** [DWC:locality](http://rs.tdwg.org/dwc/terms/locality) : The specific description of the place. Less specific geographic information can be provided in other geographic terms (higherGeography, continent, country, stateProvince, county, municipality, waterBody, island, islandGroup). This term may contain information modified from the original to correct perceived errors or standardize the description.
  * **habitat** [DWC:habitat](http://rs.tdwg.org/dwc/terms/habitat) : category or description of the habitat in which the Event occurred.
  * **decimalLatitude** [DWC:decimalLatitude](http://rs.tdwg.org/dwc/terms/decimalLatitude) : 	The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive.
  * **decimalLongitude** [DWC:decimalLongitude](http://rs.tdwg.org/dwc/terms/decimalLongitude) : The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive.
  * **coordinateUncertaintyInMeters** [DWC:http://rs.tdwg.org/dwc/terms/coordinateUncertaintyInMeters](https://dwc.tdwg.org/terms/#dwc:coordinateUncertaintyInMeters) : The horizontal distance (in meters) from the given decimalLatitude and decimalLongitude describing the smallest circle containing the whole of the Location. Leave the value empty if the uncertainty is unknown, cannot be estimated, or is not applicable (because there are no coordinates). Zero is not a valid value for this term.
  * **georeferenceRemarks** [DWC:http://rs.tdwg.org/dwc/terms/georeferenceRemarks](https://dwc.tdwg.org/terms/#dwc:georeferenceRemarks) : Notes or comments about the spatial description determination, explaining assumptions made in addition or opposition to the those formalized in the method referred to in georeferenceProtocol.
  * **minimumElevationInMeters** [DWC:minimumElevationInMeters](http://rs.tdwg.org/dwc/terms/minimumElevationInMeters) : do not add zeros, if only one elevation add to maximumElevationInMeters
  * **maximumElevationInMeters** [DWC:maximumElevationInMeters](http://rs.tdwg.org/dwc/terms/maximumElevationInMeters) : do not add zeros, if only one elevation add to maximumElevationInMeters
  * **verbatimEventDate** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate) : The verbatim original representation of the date and time information for an Event.
  * **eventDate** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/eventDate) : The date-time or interval during which an Event occurred.
  * **eventTime** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/eventTime) : The time or interval during which an Event occurred.
  * **otherTraits** : key:value list (delimited by semicolons) for describing other traits. These include body size, nesting behavior, and any other traits that are not considered biotic interactions.
  * **containsTaxonTreatment** : Does the paper contain taxon treatments? A taxon treatment is the scientific description of a taxon including a Latinized name of the nominate taxon, followed by one or several elements such as references to older literature citing this taxon and putting it in relation to the new information about the taxon being presented in the paper.
  * **TreatmentBankIdentifier** : The identifer for the taxon treatment from [TreatmentBank](http://plazi.org/resources/treatmentbank/). A paper with a taxon treatment will need to be looked up in TreatmentBank for the TreatmentBank identifier.
  * **referenceDoi** : This field was not populated in this dataset.
  * **referenceCitation**  : The reference for the interaction.
  * **referenceType**  : The type of reference.
  * **primarySource**  : Is the reference the primary source for the observation (TRUE/FALSE)? If it is not, include the primary source citation in the notes.
  * **primarySourceReference** : If the reviewed article is not the primary source of the information (recorded as FALSE in primarySource) the citation for the primarySource is included here. If the reviewed article is the primary source this field is left blank.
  * **enteredBy**  : The person entering the data.
  * **notes**  : Notes about the database entry.


### Contribute
Literature used in this project is recorded on each record. If you have a new paper to add, please submit a [new github issue](https://github.com/ParasiteTracker/tick-interaction-database/issues/new).


