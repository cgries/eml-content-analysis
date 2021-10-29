---
title: FAIR analysis
---

# Analyzing metadata for different FAIR criteria

[FAIR - findable, accessible, interoperable, reusable,](https://www.go-fair.org/fair-principles/) as first suggested by Wilkinson et al. 2016 ^[Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). https://doi.org/10.1038/sdata.2016.18] is a framework for understanding quality of metadata in terms of making data usable for somebody who was not directly involved in the sampling.

EDI has implemented the EML schema for metadata and a congruence checker which together already assure a high degree of metadata quality. As the community develops more guidelines for metadata quality it may become interesting for a research site or project to evaluate their overall performance in this area.

The [Research Data Alliance (RDA)](https://www.rd-alliance.org/) has developed guidelines for evaluating FAIR, [the FAIR data maturity model](https://zenodo.org/record/3909563#.YXwWp57MKUk). This framework is fairly general and research communities need to expand on with more specific community level criteria. [DataONE](https://www.dataone.org/) has taken the initiative to develop such [criteria for data in the DataONE community](https://github.com/NCEAS/metadig-checks). 

| FAIR | RDA | DataONE | EDI repository implementation | EML schema | EDI congruence checker |
|-------|-------|-------|-------|-------|-------|
| F | Metadata is identified by a persistent identifier | metadata identifier present |  | required | yes |
| F | Data is identified by a persistent identifier | entity identifier present |  |  | no |
| F | Metadata is identified by a globally unique identifier | metadata identifier present |  | required | yes |
| F | Data is identified by a globally unique identifier | entity identifier present |  |  | no |
| F |  | entity identifierType present |  |  | no |
| F | Rich metadata is provided to allow discovery | resource titleLength sufficient |  |  | yes |
| F |  | resource publicationDate present |  |  | yes |
| F |  | resource creator present |  | required | yes |
| F |  | resource creatorIdentifier present |  |  | no |
| F |  | resource abstractLength sufficient |  |  | yes |
| F |  | resource keywords present |  |  | yes |
| F |  | resource keywords controlled |  |  | no |
| F |  | resource keywordType present |  |  | no |
| F |  | resource publicationDate timeframe |  |  | no |
| F |  | resource revisionDate present |  | not in EML = latest publication date | no |
| F |  | resource spatialExtent present |  |  | yes |
| F |  | geographic description present |  | required with spatialExtent | yes |
| F |  | resource taxonomicExtent present |  |  | yes |
| F |  | resource temporalExtent present |  |  | yes |
| F | Metadata includes the identifier for the data | entity identifier present |  |  | no |
| F | Metadata is offered in such a way that it can be harvested and indexed |  | D1 member node, PASTA+ API, schema.org |  |  |
|  |  |  |  |  |  |
| A | Metadata contains information to enable the user to get access to the data | entity distributionURL resolvable |  |  | yes |
| A |  | resource accessControlRules present |  |  | no |
| A |  | resource distributionContact present |  | required | yes |
| A |  | resource distributionContactIdentifier present |  |  | no |
| A |  | resource publisher present | is EDI |  |  |
| A |  | resource publisherIdentifier present | EDI's ROR |  |  |
| A |  | resource serviceLocation present |  | not in EML | PASTA+ API |
| A |  | resource serviceProvider present |  | not in EML | PASTA+ API |
| A | Metadata can be accessed manually (i.e. with human intervention) | resource landingPage present | EDI provided |  |  |
| A | Data can be accessed manually (i.e. with human intervention) | entity distributionURL resolvable |  |  | yes |
| A | Metadata identifier resolves to a metadata record | metadata identifier resolvable |  |  | no |
| A | Data identifier resolves to a digital object |  |  |  |  |
| A | Metadata is accessed through standardised protocol |  | yes |  |  |
| A | Data is accessible through standardised protocol |  | yes |  |  |
| A | Data can be accessed automatically (i.e. by a computer program) |  | yes |  |  |
| A | Metadata is accessible through a free access protocol |  | yes |  |  |
| A | Data is accessible through a free access protocol |  | yes |  |  |
| A | Data is accessible through an access protocol that supports authentication and authorisation |  | yes |  |  |
| A | Metadata is guaranteed to remain available after data is no longer available |  |  |  |  |
|  |  |  |  |  |  |
| I | Metadata uses knowledge representation expressed in standardised format |  | LTER vocabulary |  |  |
| I | Data uses knowledge representation expressed in standardised format |  |  | EML entity |  |
| I |  | entity format present |  |  | yes |
| I |  | entity name present |  | required | yes |
| I |  | entity type present |  | encoded | yes |
| I |  | entity checksum present |  |  | yes |
| I |  | entity attributeName differs from description |  |  | yes |
| I |  | entity attributeNames unique |  |  | yes |
| I |  | entity attributeDefinition present |  |  | no |
| I |  | entity attributeDefinition sufficient |  |  | no |
| I |  | entity attributeStorageType present |  |  | no |
| I | Metadata uses machine-understandable knowledge representation |  |  | LTER vocabulary in SKOS |  |
| I | Data uses machine-understandable knowledge representation |  | data models |  |  |
| I | Metadata uses FAIR-compliant vocabularies |  | LTER vocabulary |  |  |
| I | Data uses FAIR-compliant vocabularies |  |  |  |  |
| I | Metadata includes references to other metadata |  |  |  |  |
| I | Data includes references to other data |  |  |  |  |
| I | Metadata includes references to other data |  |  |  |  |
| I | Data includes qualified references to other data |  |  |  |  |
| I | Metadata includes qualified references to other metadata |  |  |  |  |
| I | Metadata include qualified references to other data |  |  |  |  |
|  |  |  |  |  |  |
| R | Plurality of accurate and relevant attributes are provided to allow reuse | entity format nonproprietary |  |  |  |
| R |  | entity attributeDomain present |  |  |  |
| R |  | entity attributeUnits present |  | required | yes |
| R |  | entity attributeMeasurementScale present |  | required | yes |
| R |  | entity attributePrecision present |  |  |  |
| R |  | entity description present |  | required | yes |
| R |  | entity qualityDescription present |  |  |  |
| R | Metadata includes information about the licence under which the data can be reused | resource license present |  |  |  |
| R | Metadata refers to a standard reuse licence |  |  |  |  |
| R | Metadata refers to a machine-understandable reuse licence |  |  |  |  |
| R | Metadata includes provenance information according to community-specific standards | provenance processStepCode present |  |  |  |
| R |  | provenance sourceEntity present |  |  |  |
| R |  | provenance trace present |  | not in EML |  |
| R |  | resource methods present |  |  | yes |
| R | Metadata includes provenance information according to a cross-community language |  |  |  |  |
| R | Metadata complies with a community standard |  |  | EML | yes |
| R | Data complies with a community standard |  |  |  |  |
| R | Metadata is expressed in compliance with a machine-understandable community standard |  |  | EML | yes |
| R | Data is expressed in compliance with a machine-understandable community standard |  |  |  |  |
