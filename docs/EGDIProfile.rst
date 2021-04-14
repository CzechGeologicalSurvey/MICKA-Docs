=======================
EGDI Metadata Profile
=======================

|image0|

Methodology for the unified metadata description
of the results of GeoERA projects within
the European Geological Data Infrastructure (EGDI)
with the extension to describe 3D geological models  

================ =========== ========================================
Document version Date        Authors
1.0              29.6. 2018  L. Kondrová
1.1              20.12. 2019 L. Kondrová, Š. Kafka, G. Diepolder
1.2              8.4. 2020   L. Kondrová, Š. Kafka, O. Moravcová,
                             
                             P. Kramolišová, G. Diepolder, U. Stepien
\                            
================ =========== ========================================

TABLE OF CONTENTS

Abstract
========

This document has been created within Work Package 7 of the GeoERA GIP-P
project and defines a unified methodology for a structured metadata
description of the results of GeoERA projects (structured data that will
be included in the European Geological Data Infrastructure (EGDI)) with
the extension to unify the description of 3D geological models.

Used abbreviations
==================

======= ================================================================
EGDI    European Geological Data Infrastructure
GEMET   General environmental multilingual thesaurus
INSPIRE Infrastructure for Spatial Information in the European Community
IR      Implementing Rules of INSPIRE
JRC     Joint Research Center of the European Commission
MD      metadata
MIcKA   MetaInformation Catalogue
======= ================================================================

Executive summary
=================

Metainformation system for the storage of a structured description of
diverse data sources (datasets, services, applications) has formed an
integral part of the EGDI since its establishment. Recently, also 3D
geological models have been produced as another form of project results
which are also intended to be included in the EGDI platform. That
implies a need to define an extended EGDI metadata profile for a unified
description of these models in order to enable an effective search
according to different user-defined parameters.

This proposed metadata profile is compatible with the international
standard EN ISO 19115:2003(E) which is well usable also for the basic
description of a model. In accordance with the rules for the metadata
description of already existing data sources, it is proposed to fill in
the metadata records for models bilingually (national language +
English), which facilitates the cross-border use of the records within
(but not exclusively) the GeoERA consortium. After a consultation with
JRC it is proposed to create the metadata records for 3D geological
models in accordance with the INSPIRE IR (with an extension). In this
first phase it is proposed to describe individual models as datasets,
with the option of a hierarchical aggregation under one project or any
larger work.

A future extension to this metadata profile could be a more detailed
description of the modelling parameters – these would probably have to
be described by another standard because EN ISO 19115 is not suitable
for this.

EGDI Metadata profile 
=====================

Overview of the used metadata elements
--------------------------------------

The EGDI Metadata profile is defined by the EN ISO 19115:2003(E)
metadata elements which are summarized in the table below and described
in detail in chapter `3.2 <#anchor-5>`__.

Table 1: EGDI metadata profile - summary of metadata elements

+----------+----------+----------+----------+----------+----------+
| EGDI     | INSPIRE  | MD       |   Obli   |          |          |
| profile  | profile  | element  | gation/c |          |          |
| nr.      | nr.      | title    | ondition |          |          |
|          |          |          | a        |          |          |
|          |          |          | ccording |          |          |
|          |          |          | to       |          |          |
|          |          |          | d        |          |          |
|          |          |          | escribed |          |          |
|          |          |          | data     |          |          |
|          |          |          | source   |          |          |
|          |          |          | (Maximum |          |          |
|          |          |          | occur    |          |          |
|          |          |          | rence)   |          |          |
+----------+----------+----------+----------+----------+----------+
| “2D”     | 3D model | service  |          |          |          |
| dataset  |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 1        | 1.1      | Resource | [1]      | [1]      | [1]      |
|          |          | title    |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 2        | 1.2      | Resource | [1]      | [1]      | [1]      |
|          |          | abstract |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 3        | 1.3      | Resource | [1]      | [1]      | [1]      |
|          |          | type     |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 4        | 1.4      | Resource | [0.. ]   | [0.. ]   | [0.. ]   |
|          |          | locator  |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 5        | 1.5      | Unique   | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | resource |          |          |          |
|          |          | id       |          |          |          |
|          |          | entifier |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 6.1      | 1.6      | Coupled  | not      | not      | [0.. ]   |
|          |          | resource | ap       | ap       |          |
|          |          |          | plicable | plicable |          |
+----------+----------+----------+----------+----------+----------+
| 6.2      |          | Coupling | not      | not      | [1]      |
|          |          | type     | ap       | ap       |          |
|          |          |          | plicable | plicable |          |
+----------+----------+----------+----------+----------+----------+
| 7        | 1.7      | Resource | [1.. ]   | [1.. ]   | not      |
|          |          | language |          |          | ap       |
|          |          |          |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 8        | 2.1      | Topic    | [1.. ]   | [1.. ]   | not      |
|          |          | category |          |          | ap       |
|          |          |          |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 9        | 2.2      | Service  | not      | not      | [1]      |
|          |          | type     | ap       | ap       |          |
|          |          |          | plicable | plicable |          |
+----------+----------+----------+----------+----------+----------+
| 10.1     | 3.1      | Keyword  | [1.. ]   | [1.. ]   | [1.. ]   |
+----------+----------+----------+----------+----------+----------+
| 10.2     | 3.2      | Ori      | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | ginating |          |          |          |
|          |          | co       |          |          |          |
|          |          | ntrolled |          |          |          |
|          |          | vo       |          |          |          |
|          |          | cabulary |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 11.1     | 4.1      | Ge       | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | ographic |          |          |          |
|          |          | location |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 11.2     |          | Ge       | [0.. ]   | [0.. ]   | [0.. ]   |
|          |          | ographic |          |          |          |
|          |          | id       |          |          |          |
|          |          | entifier |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 12       |          | Pres     | [0.. ]   | [1.. ]   | not      |
|          |          | entation |          |          | ap       |
|          |          | form     |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 13       |          | Edition  | [0.. ]   | [0.. ]   | not      |
|          |          |          |          |          | ap       |
|          |          |          |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 14.1     | 5        | R        | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | eference |          |          |          |
|          |          | date     |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 14.2     | 5.1      | Resource | [0.. ]   | [0.. ]   | [0.. ]   |
|          |          | temporal |          |          |          |
|          |          | extent   |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 15       | 6.1      | Lineage  | [1]      | [1]      | not      |
|          |          |          |          |          | ap       |
|          |          |          |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 16       | 6.2      | Spatial  | [0.. ]   | [0.. ]   | not      |
|          |          | re       |          |          | ap       |
|          |          | solution |          |          | plicable |
|          |          | -        |          |          |          |
|          |          | Scale/   |          |          |          |
|          |          | Distance |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 17.1     | 7.1      | Co       | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | nformity |          |          |          |
|          |          | –        |          |          |          |
|          |          | Speci    |          |          |          |
|          |          | fication |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 17.2     | 7.2      | Co       | [1]      | [1]      | [1]      |
|          |          | nformity |          |          |          |
|          |          | - Degree |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 18.1     | 8.1      | Co       | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | nditions |          |          |          |
|          |          | applying |          |          |          |
|          |          | to       |          |          |          |
|          |          | access   |          |          |          |
|          |          | and use  |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 18.2     | 8.2      | Lim      | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | itations |          |          |          |
|          |          | on       |          |          |          |
|          |          | public   |          |          |          |
|          |          | access   |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 19       | 9.1      | Res      | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | ponsible |          |          |          |
|          |          | party    |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 20       | 12       | Data     | [1]      | [1]      | not      |
|          |          | quality  |          |          | ap       |
|          |          | scope    |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 21       | IOD-1\   | Co       | [1.. ]   | [1.. ]   | [0.. ]   |
|          |          | ordinate |          |          |          |
|          |          | r        |          |          |          |
|          |          | eference |          |          |          |
|          |          | system   |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 22       |          | Vertical | [1]      | [1]      | [0.. ]   |
|          |          | r        |          |          |          |
|          |          | eference |          |          |          |
|          |          | system   |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 23.1     |          | Vertical | not      | [1]      | not      |
|          |          | extent – | ap       |          | ap       |
|          |          | max.     | plicable |          | plicable |
|          |          | model    |          |          |          |
|          |          | depth    |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 23.2     |          | Vertical | not      | [1]      | not      |
|          |          | extent – | ap       |          | ap       |
|          |          | min.     | plicable |          | plicable |
|          |          | model    |          |          |          |
|          |          | depth    |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 23.3     |          | Vertical | not      | [1]      | not      |
|          |          | extent   | ap       |          | ap       |
|          |          | r        | plicable |          | plicable |
|          |          | eference |          |          |          |
|          |          | system   |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 24       | IOD-3\   | Dist     | [1.. ]   | [1.. ]   | not      |
|          |          | ribution |          |          | ap       |
|          |          | format   |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 25       | IOD-6\   | Spatial  | [1.. ]   | [1.. ]   | not      |
|          |          | repres   |          |          | ap       |
|          |          | entation |          |          | plicable |
|          |          | type     |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 26       |          | Mai      | [0..1]   | [0..1]   | not      |
|          |          | ntenance |          |          | ap       |
|          |          | and      |          |          | plicable |
|          |          | update   |          |          |          |
|          |          | f        |          |          |          |
|          |          | requency |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 27       |          | Purpose  | [0..1]   | [0..1]   | not      |
|          |          |          |          |          | ap       |
|          |          |          |          |          | plicable |
+----------+----------+----------+----------+----------+----------+
| 28.1     | 10.1     | Metadata | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | point of |          |          |          |
|          |          | contact  |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 28.2     | 10.2     | Metadata | [1]      | [1]      | [1]      |
|          |          | date     |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 28.3     | 10.3     | Metadata | [1.. ]   | [1.. ]   | [1.. ]   |
|          |          | language |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 29       | 2.2.1    | File     | [1]      | [1]      | [1]      |
|          |          | id       |          |          |          |
|          |          | entifier |          |          |          |
+----------+----------+----------+----------+----------+----------+
| 30       |          | Parent   | [0..1]   | [0..1]   | not      |
|          |          | id       |          |          | ap       |
|          |          | entifier |          |          | plicable |
+----------+----------+----------+----------+----------+----------+

\ Metadata elements marked with the “IOD” prefix are metadata elements
for interoperability as defined in INSPIRE data specifications

Definition of the individual metadata elements of the profile
-------------------------------------------------------------

Resource title
~~~~~~~~~~~~~~

+------------------+-----------------------------------------+-------+
|   EGDI Profile   | Reference number                        | 1     |
+------------------+-----------------------------------------+-------+
| Title            | Resource title                          |       |
+------------------+-----------------------------------------+-------+
| Obligation       | Mandatory                               |       |
+------------------+-----------------------------------------+-------+
| Max. occurence   | [1]                                     |       |
+------------------+-----------------------------------------+-------+
| Comment          |                                         |       |
+------------------+-----------------------------------------+-------+
| INSPIRE IR       | Reference                               | B 1.1 |
+------------------+-----------------------------------------+-------+
| Title            | Resource title                          |       |
+------------------+-----------------------------------------+-------+
| Obligation       | Mandatory                               |       |
+------------------+-----------------------------------------+-------+
| Max. occurence   | [1]                                     |       |
+------------------+-----------------------------------------+-------+
| ISO 19115        | Number                                  | 360   |
+------------------+-----------------------------------------+-------+
| Title            | title                                   |       |
+------------------+-----------------------------------------+-------+
| Definition       | Name by which the cited resource is     |       |
|                  | known.                                  |       |
+------------------+-----------------------------------------+-------+
| XPath            | i                                       |       |
|                  | dentificationInfo[1]/ /citation/ /title |       |
+------------------+-----------------------------------------+-------+
| Data type        | CharacterString                         |       |
+------------------+-----------------------------------------+-------+
| Domain           | Free text                               |       |
+------------------+-----------------------------------------+-------+
| Example          | Detailed structural geological 3D       |       |
|                  | model of the Březový potok candidate    |       |
|                  | site                                    |       |
+------------------+-----------------------------------------+-------+

Resource abstract
~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 2     |
+----------------+-------------------------------------------+-------+
| Title          | Resource abstract                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1]                                       |       |
+----------------+-------------------------------------------+-------+
| Comment        | Abstract should contain a brief           |       |
|                | description of the dataset or how a 3D    |       |
|                | model was created (for ex. “structural    |       |
|                | geological”), information about the used  |       |
|                | software and data inputs                  |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 1.2 |
+----------------+-------------------------------------------+-------+
| Title          | Resource abstract                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1]                                       |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 25    |
+----------------+-------------------------------------------+-------+
| Title          | abstract                                  |       |
+----------------+-------------------------------------------+-------+
| Definition     | Brief narrative summary of the content of |       |
|                | the resource(s).                          |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/ /abstract          |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| Example        | The detailed 3D structural geological     |       |
|                | model of the Březový potok candidate site |       |
|                | summarizes the existing geological        |       |
|                | knowledge at one of the nine sites        |       |
|                | considered for the planned deep           |       |
|                | repository of high-level radioactive      |       |
|                | waste in the Czech Republic.              |       |
|                |                                           |       |
|                | The area of interest is characterized by  |       |
|                | simple geological structure that includes |       |
|                | two lithotectonic units. Metamorphic      |       |
|                | rocks are of Prevariscan protolith, which |       |
|                | was significantly reworked during         |       |
|                | variscan orogeny between c. 350 – 340 Ma  |       |
|                | and magmatic rocks of south-western       |       |
|                | margin of Central Bohemian Plutonic       |       |
|                | Complex which intruded into them at age   |       |
|                | around 345 Ma.                            |       |
|                |                                           |       |
|                | The detailed 3D structural geological     |       |
|                | model of the Březový potok candidate site |       |
|                | was created for SÚRAO (RAWRA) during the  |       |
|                | course of ZL U2304-010 "3D Structural     |       |
|                | Geological Models" solution. The model    |       |
|                | itself was created in MOVE software and   |       |
|                | was submitted to SÚRAO in native MOVE     |       |
|                | format and in 3D PDF format.              |       |
+----------------+-------------------------------------------+-------+

Resource type
~~~~~~~~~~~~~

Resource locator
~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 4     |
+----------------+-------------------------------------------+-------+
| Title          | Resource locator                          |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Conditional                               |       |
+----------------+-------------------------------------------+-------+
| Max. occurence |   [0.. ]                                  |       |
+----------------+-------------------------------------------+-------+
| Comment        | Electronic address of the resource, if    |       |
|                | it exists. Recommendation: URL of a       |       |
|                | descriptive web page and/or link to an    |       |
|                | online visualization of the               |       |
|                | dataset/model.                            |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 1.4 |
+----------------+-------------------------------------------+-------+
| Title          | Resource locator                          |       |
+----------------+-------------------------------------------+-------+
| Obligation     |                                           |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [0.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 397   |
+----------------+-------------------------------------------+-------+
| Title          | linkage                                   |       |
+----------------+-------------------------------------------+-------+
| Definition     | Location (address) for on-line access     |       |
|                | using a Uniform Resource Locator address  |       |
|                | or similar addressing scheme.             |       |
+----------------+-------------------------------------------+-------+
| XPath          | distribution                              |       |
|                | Info/ /transferOptions/ /onLine/ /linkage |       |
+----------------+-------------------------------------------+-------+
| Data type      | class                                     |       |
+----------------+-------------------------------------------+-------+
| Domain         | CI_OnlineResource<<DataType>>(B.3.2.5)    |       |
+----------------+-------------------------------------------+-------+
| Example        | http://www.geolog                         |       |
|                | y.cz/extranet-eng/science/earths-crust/3d |       |
+----------------+-------------------------------------------+-------+

Unique resource identifier
~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 5     |
+----------------+-------------------------------------------+-------+
| Title          | Unique resource identifier                |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        | Recommended format is organization ID     |       |
|                | (for ex. domain name) and identifier of   |       |
|                | the dataset defined by the data provider, |       |
|                | for ex.                                   |       |
|                | “http                                     |       |
|                | s://www.domain.org/internal_identifier“   |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 1.5 |
+----------------+-------------------------------------------+-------+
| Title          | Unique resource identifier                |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory for datasets and data set       |       |
|                | series.                                   |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 365   |
+----------------+-------------------------------------------+-------+
| Title          | Identifier                                |       |
+----------------+-------------------------------------------+-------+
| Definition     | value uniquely identifying an object      |       |
|                | within a namespace.                       |       |
+----------------+-------------------------------------------+-------+
| XPath          | iden                                      |       |
|                | tificationInfo[1]/ /citation/ /identifier |       |
+----------------+-------------------------------------------+-------+
| Data type      | MD_Identifier                             |       |
+----------------+-------------------------------------------+-------+
| Domain         | See B.2.7.3 of ISO 19115. The code        |       |
|                | property is required at a minimum, and a  |       |
|                | codeSpace property may be provided.       |       |
+----------------+-------------------------------------------+-------+
| Example        | recommended format:                       |       |
|                | \ h                                       |       |
|                | ttps://www.geology.cz/3D-SURAO-KRAVI_HORA |       |
+----------------+-------------------------------------------+-------+

Coupled resource
~~~~~~~~~~~~~~~~

+----------------------+----------------------+----------------------+
| EGDI Profile         | Reference number     |   6.1                |
+----------------------+----------------------+----------------------+
| Title                | Coupled resource     |                      |
+----------------------+----------------------+----------------------+
| Obligation           | Conditional          |                      |
+----------------------+----------------------+----------------------+
| Max. occurence       | [0.. ]               |                      |
+----------------------+----------------------+----------------------+
| Comment              |                      |                      |
+----------------------+----------------------+----------------------+
| INSPIRE IR           | Reference            | B 1.6                |
+----------------------+----------------------+----------------------+
| Title                | Coupled resource     |                      |
+----------------------+----------------------+----------------------+
| Obligation           |                      |                      |
+----------------------+----------------------+----------------------+
| Max. occurence       | [0.. ]               |                      |
+----------------------+----------------------+----------------------+
| ISO 19119: 2005(E)   | Number               | Element no.9 from    |
|                      |                      | table C.1 in Annex   |
|                      |                      | C.2.2                |
+----------------------+----------------------+----------------------+
| Title                | identification       |                      |
|                      | Info[1]/ /operatesOn |                      |
+----------------------+----------------------+----------------------+
| Definition           | provides information |                      |
|                      | on the datasets that |                      |
|                      | the service operates |                      |
|                      | on                   |                      |
+----------------------+----------------------+----------------------+
| XPath                | identification       |                      |
|                      | Info/SV_ServiceIdent |                      |
|                      | ification/operatesOn |                      |
+----------------------+----------------------+----------------------+
| Attribute class or   | M                    |                      |
| target class of role | D_DataIdentification |                      |
+----------------------+----------------------+----------------------+
| Domain               |                      |                      |
+----------------------+----------------------+----------------------+
| Example              | https://egdi.        |                      |
|                      | geology.cz/record/ba |                      |
|                      | sic/5006a106-d66c-49 |                      |
|                      | 16-87bc-91c80a010817 |                      |
+----------------------+----------------------+----------------------+

+----------------------+----------------------+----------------------+
| EGDI Profile         | Reference number     | 6.2                  |
+----------------------+----------------------+----------------------+
| Title                | Coupling type        |                      |
+----------------------+----------------------+----------------------+
| Obligation           |   Mandatory for      |                      |
|                      | services             |                      |
+----------------------+----------------------+----------------------+
| Max. occurence       | [1]                  |                      |
+----------------------+----------------------+----------------------+
| Comment              |                      |                      |
+----------------------+----------------------+----------------------+
| INSPIRE IR           | Reference            | This element is an   |
|                      |                      | extension to the     |
|                      |                      | INSPIRE profile but  |
|                      |                      | is required by ISO   |
|                      |                      | 19119                |
+----------------------+----------------------+----------------------+
| ISO 19119:           | Number               | 2.4, table 1,        |
| 2005/DAmd1           |                      | element no.3 from    |
|                      |                      | ISO 19119            |
+----------------------+----------------------+----------------------+
| Title                | couplingType         |                      |
+----------------------+----------------------+----------------------+
| Definition           | Type of coupling     |                      |
|                      | between service and  |                      |
|                      | associated data (if  |                      |
|                      | exists).             |                      |
+----------------------+----------------------+----------------------+
| XPath                | identificatio        |                      |
|                      | nInfo/ /CouplingType |                      |
+----------------------+----------------------+----------------------+
| Data type            | code                 |                      |
+----------------------+----------------------+----------------------+
| Domain               | SV_CouplingType      |                      |
|                      | (tight, mixed,       |                      |
|                      | loose)               |                      |
+----------------------+----------------------+----------------------+
| Example              | tight                |                      |
+----------------------+----------------------+----------------------+

Resource language
~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 7     |
+----------------+-------------------------------------------+-------+
| Title          | Resource language                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory - if the data doesn’t include   |       |
|                | any language items, please select the “no |       |
|                | language” option                          |       |
+----------------+-------------------------------------------+-------+
| Max. occurence |   [1..]                                   |       |
+----------------+-------------------------------------------+-------+
| Comment        |                                           |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 1.7 |
+----------------+-------------------------------------------+-------+
| Title          | Resource language                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     |                                           |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [0..]                                     |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 39    |
+----------------+-------------------------------------------+-------+
| Title          | language                                  |       |
+----------------+-------------------------------------------+-------+
| Definition     | Language(s) used within the datasets      |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/ /language          |       |
+----------------+-------------------------------------------+-------+
| Data type      | LanguageCode (ISO/TS 19139)               |       |
+----------------+-------------------------------------------+-------+
| Domain         | Codelist (See ISO/TS 19139) based on      |       |
|                | alpha-3 codes of ISO 639-2. Use only      |       |
|                | three-letter codes from in ISO 639-2/B    |       |
|                | (bibliographic codes), as defined at      |       |
|                | http://www.loc.gov/standards/iso639-2/    |       |
|                |                                           |       |
|                | The list of codes for the GeoERA partners |       |
|                | and EGDI data providers:                  |       |
+----------------+-------------------------------------------+-------+
| Example        | cze                                       |       |
+----------------+-------------------------------------------+-------+

Topic category
~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 8     |
+----------------+-------------------------------------------+-------+
| Title          | Topic category                            |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        | “geoscientificInformation” should be      |       |
|                | filled (plus any other additional         |       |
|                | category, if applicable)                  |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 2.1 |
+----------------+-------------------------------------------+-------+
| Title          | Topic category                            |       |
+----------------+-------------------------------------------+-------+
| Obligation     |                                           |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 41    |
+----------------+-------------------------------------------+-------+
| Title          | topicCategory                             |       |
+----------------+-------------------------------------------+-------+
| Definition     | Main theme(s) of the dataset              |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/ /topicCategory     |       |
+----------------+-------------------------------------------+-------+
| Data type      | MD_TopicCategory                          |       |
+----------------+-------------------------------------------+-------+
| Domain         | Enumeration (See B.5.27 of ISO 19115 or   |       |
|                | Part D 2 of the INSPIRE Implementing      |       |
|                | Rules for Metadata)                       |       |
+----------------+-------------------------------------------+-------+
| Example        | geoscientificInformation                  |       |
+----------------+-------------------------------------------+-------+

Service type
~~~~~~~~~~~~

+--------------------+-----------------------+-----------------------+
| EGDI Profile       | Reference number      | 9                     |
+--------------------+-----------------------+-----------------------+
| Title              | Service type          |                       |
+--------------------+-----------------------+-----------------------+
| Obligation         | Mandatory for         |                       |
|                    | services              |                       |
+--------------------+-----------------------+-----------------------+
| Max. occurence     | [1]                   |                       |
+--------------------+-----------------------+-----------------------+
| Comment            |   Type of service     |                       |
|                    | according to the      |                       |
|                    | INSPIRE service       |                       |
|                    | types, or             |                       |
|                    | determination of      |                       |
|                    | other types of        |                       |
|                    | services (OGC,        |                       |
|                    | ESRI)                 |                       |
+--------------------+-----------------------+-----------------------+
| INSPIRE IR         | Reference             | B 2.2                 |
+--------------------+-----------------------+-----------------------+
| Title              | Spatial data service  |                       |
|                    | type                  |                       |
+--------------------+-----------------------+-----------------------+
| Obligation         |                       |                       |
+--------------------+-----------------------+-----------------------+
| Max. occurence     | [1]                   |                       |
+--------------------+-----------------------+-----------------------+
| ISO 19119: 2005(E) | Number                | Element no.1 in table |
|                    |                       | C.1, Annex C.2.2      |
+--------------------+-----------------------+-----------------------+
| Title              | identification        |                       |
|                    | Info[1]/ /serviceType |                       |
+--------------------+-----------------------+-----------------------+
| Definition         | a service type name   |                       |
|                    | from a registry of    |                       |
|                    | services              |                       |
+--------------------+-----------------------+-----------------------+
| XPath              | identification        |                       |
|                    | Info[1]/ /serviceType |                       |
+--------------------+-----------------------+-----------------------+
| Data type          | GenericName           |                       |
+--------------------+-----------------------+-----------------------+
| Domain             |                       |                       |
+--------------------+-----------------------+-----------------------+
| Example            |  INSPIRE view         |                       |
+--------------------+-----------------------+-----------------------+

Keyword
~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 10.1  |
+----------------+-------------------------------------------+-------+
| Title          | Keyword                                   |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        |   1. One keyword for the INSPIRE theme    |       |
|                | from the INSPIRE registry has to be       |       |
|                | filled.                                   |       |
|                |                                           |       |
|                |   2. GeoERA keywords - at least one       |       |
|                | keyword from the GeoERA thesaurus has to  |       |
|                | be filled.                                |       |
|                |                                           |       |
|                |   3. Project name identifier              |       |
|                |                                           |       |
|                |   4. For INSPIRE data, a keyword for the  |       |
|                | spatial scope from the INSPIRE registry   |       |
|                | (  \ http://inspire.ec.euro               |       |
|                | pa.eu/metadata-codelist/SpatialScope\   ) |       |
|                | will be provided as a URI via             |       |
|                | gmx:Anchor.                               |       |
|                |                                           |       |
|                |   5. For datasets related to              |       |
|                | environmental reporting within INSPIRE    |       |
|                | directive, a Priority dataset keyword is  |       |
|                | mandatory                                 |       |
|                | (from  \ http://inspire.ec.europa.eu      |       |
|                | /metadata-codelist/PriorityDataset\   )   |       |
|                |                                           |       |
|                |   6. Any free keyword can be added, if    |       |
|                | needed. For the filtering purposes of     |       |
|                | harvested metadata records from local     |       |
|                | catalogues, the keyword “EGDI” is         |       |
|                | recommended.                              |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 3.1 |
+----------------+-------------------------------------------+-------+
| Title          | Keyword value                             |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 53    |
+----------------+-------------------------------------------+-------+
| Title          | keyword                                   |       |
+----------------+-------------------------------------------+-------+
| Definition     | Commonly used word(s) or formalised       |       |
|                | word(s) or phrase(s) used to describe the |       |
|                | subject.                                  |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificati                              |       |
|                | onInfo[1]/ /descriptiveKeywords/ /keyword |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| Example        |  1. \                                     |       |
|                |  http://inspire.ec.europa.eu/theme/ge\  ; |       |
|                | Geology                                   |       |
|                |                                           |       |
|                |  2. \ https://dat                         |       |
|                | a.geoscience.earth/ncl/geoera/keyword/568 |       |
|                |                                           |       |
|                |  3. \ http://data.geoscienc               |       |
|                | e.earth/egs/projects/35\ :sup:` [3]_`\  ; |       |
|                | HIKE                                      |       |
|                |                                           |       |
|                |  4. \ http://inspire.ec.europa.e          |       |
|                | u/metadata-codelist/SpatialScope/national |       |
|                |                                           |       |
|                |  5. \ ht                                  |       |
|                | tp://inspire.ec.europa.eu/metadata-codeli |       |
|                | st/PriorityDataset/Boreholes-reco-2014-70 |       |
|                |                                           |       |
|                |  6. EGDI                                  |       |
+----------------+-------------------------------------------+-------+

+----------------+----------------------------------------+----------+
| EGDI Profile   | Reference number                       |   10.1   |
+----------------+----------------------------------------+----------+
| Title          |   Keyword with type “stratum”          |          |
+----------------+----------------------------------------+----------+
| Obligation     | Optional                               |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [0.. ]                                 |          |
+----------------+----------------------------------------+----------+
| Comment        |   A keyword with the defined type      |          |
|                | “stratum” can be added from a          |          |
|                | thesaurus (for ex. GeoERA keyword      |          |
|                | thesaurus or other officially          |          |
|                | registered thesaurus) in the form of   |          |
|                | URI to describe for ex. the modelled   |          |
|                | geological units. For GeoERA products, |          |
|                | keywords must be selected from the     |          |
|                | GeoERA keyword thesaurus.              |          |
+----------------+----------------------------------------+----------+
| INSPIRE IR     | Reference                              | B 3.1    |
+----------------+----------------------------------------+----------+
| Title          | Keyword value                          |          |
+----------------+----------------------------------------+----------+
| Obligation     | Mandatory                              |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| ISO 19115      | Number                                 | 53       |
+----------------+----------------------------------------+----------+
| Title          | keyword                                |          |
+----------------+----------------------------------------+----------+
| Definition     | Commonly used word(s) or formalised    |          |
|                | word(s) or phrase(s) used to describe  |          |
|                | the subject.                           |          |
+----------------+----------------------------------------+----------+
| XPath          | identifica                             |          |
|                | tionInfo[1]/ /descriptiveKeywords/ [ty |          |
|                | pe/ /@codeListValue=’stratum’]/keyword |          |
+----------------+----------------------------------------+----------+
| Data type      | URI (+ CharacterString)                |          |
+----------------+----------------------------------------+----------+
| Domain         | URI                                    |          |
+----------------+----------------------------------------+----------+
| Example        | http://                                |          |
|                | resource.geolba.ac.at/GeologicUnit/736 |          |
+----------------+----------------------------------------+----------+

+----------------+----------------------------------------+----------+
| EGDI Profile   | Reference number                       |   10.1   |
+----------------+----------------------------------------+----------+
| Title          |   Keyword with type “temporal”         |          |
+----------------+----------------------------------------+----------+
| Obligation     | Optional                               |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [0.. ]                                 |          |
+----------------+----------------------------------------+----------+
| Comment        |   A keyword with the defined type      |          |
|                | “temporal” can be added from a         |          |
|                | thesaurus (for ex. GeoERA keyword      |          |
|                | thesaurus or other officially          |          |
|                | registered thesaurus) in the form of   |          |
|                | URI to describe for ex. the modelled   |          |
|                | geological units in the same order as  |          |
|                | the respective stratum keywords.       |          |
+----------------+----------------------------------------+----------+
| INSPIRE IR     | Reference                              | B 3.1    |
+----------------+----------------------------------------+----------+
| Title          | Keyword value                          |          |
+----------------+----------------------------------------+----------+
| Obligation     | Mandatory                              |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| ISO 19115      | Number                                 | 53       |
+----------------+----------------------------------------+----------+
| Title          | keyword                                |          |
+----------------+----------------------------------------+----------+
| Definition     | Commonly used word(s) or formalised    |          |
|                | word(s) or phrase(s) used to describe  |          |
|                | the subject.                           |          |
+----------------+----------------------------------------+----------+
| XPath          | identificat                            |          |
|                | ionInfo[1]/ /descriptiveKeywords/ [typ |          |
|                | e/ /@codeListValue=’temporal’]/keyword |          |
+----------------+----------------------------------------+----------+
| Data type      | URI (+ CharacterString)                |          |
+----------------+----------------------------------------+----------+
| Domain         | URI                                    |          |
+----------------+----------------------------------------+----------+
| Example        | https://data.ge                        |          |
|                | oscience.earth/ncl/geoera/keyword/2231 |          |
+----------------+----------------------------------------+----------+

+----------------+----------------------------------------+----------+
| EGDI Profile   | Reference number                       |   10.1   |
+----------------+----------------------------------------+----------+
| Title          |   Keyword with type “discipline”       |          |
+----------------+----------------------------------------+----------+
| Obligation     | Optional                               |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [0.. ]                                 |          |
+----------------+----------------------------------------+----------+
| Comment        |   A keyword with the defined type      |          |
|                | “discipline” can be added from a       |          |
|                | thesaurus (for ex. GeoERA keyword      |          |
|                | thesaurus or other officially          |          |
|                | registered thesaurus) in the form of   |          |
|                | URI to describe for ex. the modelled   |          |
|                | geological units.                      |          |
+----------------+----------------------------------------+----------+
| INSPIRE IR     | Reference                              | B 3.1    |
+----------------+----------------------------------------+----------+
| Title          | Keyword value                          |          |
+----------------+----------------------------------------+----------+
| Obligation     | Mandatory                              |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| ISO 19115      | Number                                 | 53       |
+----------------+----------------------------------------+----------+
| Title          | keyword                                |          |
+----------------+----------------------------------------+----------+
| Definition     | Commonly used word(s) or formalised    |          |
|                | word(s) or phrase(s) used to describe  |          |
|                | the subject.                           |          |
+----------------+----------------------------------------+----------+
| XPath          | identificatio                          |          |
|                | nInfo[1]/ /descriptiveKeywords/ [type/ |          |
|                | /@codeListValue=’discipline’]/keyword  |          |
+----------------+----------------------------------------+----------+
| Data type      | URI (+ CharacterString)                |          |
+----------------+----------------------------------------+----------+
| Domain         | URI                                    |          |
+----------------+----------------------------------------+----------+
| Example        | https://data.g                         |          |
|                | eoscience.earth/ncl/geoera/keyword/568 |          |
+----------------+----------------------------------------+----------+

Originating controlled vocabulary
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+----------------------------------------+----------+
| EGDI Profile   | Reference number                       |   10.2   |
+----------------+----------------------------------------+----------+
| Title          | Originating controlled vocabulary      |          |
+----------------+----------------------------------------+----------+
| Obligation     |   Conditional – if the keyword comes   |          |
|                | from a controlled thesaurus, citation  |          |
|                | of the thesaurus has to be filled (at  |          |
|                | least the title and reference date     |          |
|                | with the date type).                   |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| Comment        |                                        |          |
+----------------+----------------------------------------+----------+
| INSPIRE IR     | Reference                              | B 3.2    |
+----------------+----------------------------------------+----------+
| Title          | Originating controlled vocabulary      |          |
+----------------+----------------------------------------+----------+
| Obligation     | Conditional. Mandatory for datasets,   |          |
|                | data set series and services related   |          |
|                | directly to INSPIRE.                   |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| ISO 19115      | Number                                 | 55       |
+----------------+----------------------------------------+----------+
| Title          | thesaurusName                          |          |
+----------------+----------------------------------------+----------+
| Definition     | Name of the formally registered        |          |
|                | thesaurus or a similar authoritative   |          |
|                | source of keywords.                    |          |
+----------------+----------------------------------------+----------+
| XPath          | identificationInfo[1]                  |          |
|                | / /descriptiveKeywords/ /thesaurusName |          |
+----------------+----------------------------------------+----------+
| Data type      | CI_Citation                            |          |
+----------------+----------------------------------------+----------+
| Domain         | The following properties are expected: |          |
+----------------+----------------------------------------+----------+
| Example        |  GEMET - INSPIRE themes, version 1.0;  |          |
|                | date: 2008-06-01; date type:           |          |
|                | publication                            |          |
+----------------+----------------------------------------+----------+

Geographic location
~~~~~~~~~~~~~~~~~~~

+----------------+----------------------------------------+----------+
| EGDI Profile   | Reference number                       |   11.1   |
+----------------+----------------------------------------+----------+
| Title          |   Geographic location                  |          |
+----------------+----------------------------------------+----------+
| Obligation     |   Mandatory for datasets, conditional  |          |
|                | for services                           |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ]                                 |          |
+----------------+----------------------------------------+----------+
| Comment        | Defined by the western and eastern     |          |
|                | longitude and southern and northern    |          |
|                | latitude in decimal degrees (2 digits  |          |
|                | precision) in the WGS-84 coordinate    |          |
|                | system.                                |          |
+----------------+----------------------------------------+----------+
| INSPIRE IR     | Reference                              | B 4.1    |
+----------------+----------------------------------------+----------+
| Title          | Geographic bounding box                |          |
+----------------+----------------------------------------+----------+
| Obligation     |                                        |          |
+----------------+----------------------------------------+----------+
| Max. occurence | [1.. ] for datasets and data set       |          |
|                | series                                 |          |
|                |                                        |          |
|                | [0.. ] for services                    |          |
+----------------+----------------------------------------+----------+
| ISO 19115      | Number                                 | 343      |
+----------------+----------------------------------------+----------+
| Title          | EX_GeographicBoundingBox               |          |
+----------------+----------------------------------------+----------+
| Definition     | geographic position of the dataset.    |          |
|                | This is only an approximate            |          |
|                |                                        |          |
|                | reference so specifying the coordinate |          |
|                | reference system is                    |          |
|                |                                        |          |
|                | unnecessary.                           |          |
+----------------+----------------------------------------+----------+
| XPath          | identificationInfo[1]/ /extent/ /geog  |          |
|                | raphicElement/EX_GeographicBoundingBox |          |
+----------------+----------------------------------------+----------+
| Data type      | EX_GeographicExtent                    |          |
+----------------+----------------------------------------+----------+
| Domain         | Lines 344-347 and 340                  |          |
+----------------+----------------------------------------+----------+
| Example        |  11.62 19.19 48.01 51.56               |          |
+----------------+----------------------------------------+----------+

Geographic identifier
~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 11.2                    |
+----------------+-------------------------+-------------------------+
| Title          | Geographic identifier   |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Optional                |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [0.. ]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   The extent of the     |                         |
|                | whole country is        |                         |
|                | selected from           |                         |
|                | the  \ https            |                         |
|                | ://op.europa.eu/en/web/ |                         |
|                | eu-vocabularies/at-data |                         |
|                | set/-/resource/dataset/ |                         |
|                | country\   vocabulary   |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 349                     |
+----------------+-------------------------+-------------------------+
| Title          | geographicIdentifier    |                         |
+----------------+-------------------------+-------------------------+
| Definition     | identifier used to      |                         |
|                | represent a geographic  |                         |
|                | area                    |                         |
+----------------+-------------------------+-------------------------+
| XPath          | iden                    |                         |
|                | tificationInfo/ /extent |                         |
|                | / /geographicElement/ / |                         |
|                |                         |                         |
|                | geographicIdentifier    |                         |
+----------------+-------------------------+-------------------------+
| Data type      | MD_Identifier           |                         |
+----------------+-------------------------+-------------------------+
| Domain         | URI representing the    |                         |
|                | geographic              |                         |
|                | identification of the   |                         |
|                | resource extent         |                         |
+----------------+-------------------------+-------------------------+
| Example        | http://publica          |                         |
|                | tions.europa.eu/resourc |                         |
|                | e/authority/country/CZE |                         |
+----------------+-------------------------+-------------------------+

Presentation form
~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 12                      |
+----------------+-------------------------+-------------------------+
| Title          | Presentation form       |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Mandatory for 3D      |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [1.. ] for 3D         |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   For 3D models choose  |                         |
|                | “model digital” from    |                         |
|                | the codelist. Not       |                         |
|                | applicable for          |                         |
|                | services.               |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 368                     |
+----------------+-------------------------+-------------------------+
| Title          | presentationForm        |                         |
+----------------+-------------------------+-------------------------+
| Definition     | mode in which the       |                         |
|                | resource is represented |                         |
+----------------+-------------------------+-------------------------+
| XPath          | ident                   |                         |
|                | ificationInfo[1]/ /cita |                         |
|                | tion/ /presentationForm |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Class                   |                         |
+----------------+-------------------------+-------------------------+
| Domain         | CI_PresentationFormCode |                         |
|                | (Codelist B.5.4)        |                         |
+----------------+-------------------------+-------------------------+
| Example        | model digital           |                         |
+----------------+-------------------------+-------------------------+

Edition
~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        |   13                    |
+----------------+-------------------------+-------------------------+
| Title          | Edition                 |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Conditional for 3D      |                         |
|                | models – if there       |                         |
|                | are/will be more        |                         |
|                | versions of the model,  |                         |
|                | it is mandatory to fill |                         |
|                | this element            |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [0.. ]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Version number (model |                         |
|                | identifier) and         |                         |
|                | optionally also text    |                         |
|                | description (for ex.    |                         |
|                | relation to previous    |                         |
|                | model versions)         |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 363                     |
+----------------+-------------------------+-------------------------+
| Title          | edition                 |                         |
+----------------+-------------------------+-------------------------+
| Definition     | Version of the cited    |                         |
|                | resource                |                         |
+----------------+-------------------------+-------------------------+
| XPath          | identificationInfo[     |                         |
|                | 1]/ /citation/ /edition |                         |
+----------------+-------------------------+-------------------------+
| Data type      | CharacterString         |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Free text               |                         |
+----------------+-------------------------+-------------------------+
| Example        |  Version 2; based on    |                         |
|                | new geophysical survey  |                         |
+----------------+-------------------------+-------------------------+

 Reference date
~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 14.1                    |
+----------------+-------------------------+-------------------------+
| Title          |   Reference date        |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Mandatory               |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [1.. ]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        | Date of creation must   |                         |
|                | be filled, optionally   |                         |
|                | also other types of     |                         |
|                | reference dates can be  |                         |
|                | added (publication      |                         |
|                | date/date of the last   |                         |
|                | revision).              |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | B 5.4, optionally also  |
|                |                         | B 5.3 or B 5.2          |
+----------------+-------------------------+-------------------------+
| Title          | Date of creation        |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Conditional: At least   |                         |
|                | one temporal reference  |                         |
|                | is required.            |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [0.. ] but at least one |                         |
|                | temporal reference is   |                         |
|                | required.               |                         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 362                     |
+----------------+-------------------------+-------------------------+
| Title          | date                    |                         |
+----------------+-------------------------+-------------------------+
| Definition     | Reference date for the  |                         |
|                | cited resource          |                         |
+----------------+-------------------------+-------------------------+
| XPath          | identificationIn        |                         |
|                | fo[1]/ /citation/ /date |                         |
+----------------+-------------------------+-------------------------+
| Data type      | class                   |                         |
+----------------+-------------------------+-------------------------+
| Domain         | CI_Date (B.3.2.4)       |                         |
|                | <<DataType>>            |                         |
+----------------+-------------------------+-------------------------+
| Example        |  2018-06-30; Date of    |                         |
|                | creation                |                         |
+----------------+-------------------------+-------------------------+

.. _section-1:

Resource temporal extent
~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 14.2  |
+----------------+-------------------------------------------+-------+
| Title          | Resource temporal extent                  |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Optional                                  |       |
+----------------+-------------------------------------------+-------+
| Max. occurence |   [0.. ]                                  |       |
+----------------+-------------------------------------------+-------+
| Comment        | This element should be filled if the      |       |
|                | resource has a temporal extent (either as |       |
|                | a time instant, or a range of dates of    |       |
|                | validity).                                |       |
|                |                                           |       |
|                |   In case the time period is open-ended   |       |
|                | with either the start or the end date     |       |
|                | unknown, the elements gml:startPosition   |       |
|                | or gml:endPosition may be used with an    |       |
|                | empty value and the attribute             |       |
|                | indeterminatePosition with value          |       |
|                | "unknown". If the temporal extent is      |       |
|                | on-going, the gml:endPosition may be used |       |
|                | with an empty value and the attribute     |       |
|                | indeterminatePosition with value "now".   |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 5.1 |
+----------------+-------------------------------------------+-------+
| Title          | Temporal extent                           |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Conditional: At least one temporal        |       |
|                | reference is required.                    |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [0.. ] but at least one temporal          |       |
|                | reference is required.                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 337   |
+----------------+-------------------------------------------+-------+
| Title          | temporalElement                           |       |
+----------------+-------------------------------------------+-------+
| Definition     | provides temporal component of the extent |       |
|                | of the referring object                   |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo/ /extent/ /t           |       |
|                | emporalElement/ /EX_TemporalExtent/extent |       |
+----------------+-------------------------------------------+-------+
| Data type      | Association                               |       |
+----------------+-------------------------------------------+-------+
| Domain         | EX_TemporalExtent (B.3.1.3)               |       |
+----------------+-------------------------------------------+-------+
| Example        |  2002-01-30 - now                         |       |
+----------------+-------------------------------------------+-------+

.. _section-2:

Lineage
~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 15    |
+----------------+-------------------------------------------+-------+
| Title          | Lineage                                   |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1]                                       |       |
+----------------+-------------------------------------------+-------+
| Comment        |   Description of the history of           |       |
|                | processing and/or the overall quality of  |       |
|                | the dataset, including information on the |       |
|                | input data, SW used, if the data/model    |       |
|                | has been approved etc. Not applicable for |       |
|                | services.                                 |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 6.1 |
+----------------+-------------------------------------------+-------+
| Title          | Lineage                                   |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory for data sets and data set      |       |
|                | series                                    |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1]                                       |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 83    |
+----------------+-------------------------------------------+-------+
| Title          | statement                                 |       |
+----------------+-------------------------------------------+-------+
| Definition     | general explanation of the data           |       |
|                | producer’s knowledge about the lineage of |       |
|                | a dataset                                 |       |
+----------------+-------------------------------------------+-------+
| XPath          | dataQualityInfo/ /lineage/ /statement     |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| Example        |  Detailed model is a specification of the |       |
|                | regional model, with emphasis put on the  |       |
|                | central part containing the exploratory   |       |
|                | area. The model itself was created in     |       |
|                | MOVE software and was submitted in native |       |
|                | MOVE format and in 3D PDF format.         |       |
+----------------+-------------------------------------------+-------+

Spatial resolution
~~~~~~~~~~~~~~~~~~

+----------------+--------------------------------------+------------+
| EGDI Profile   | Reference number                     | 16         |
+----------------+--------------------------------------+------------+
| Title          |   Spatial resolution –               |            |
|                | Scale/Distance                       |            |
+----------------+--------------------------------------+------------+
| Obligation     |   Conditional – mandatory, if the    |            |
|                | scale or spatial resolution can be   |            |
|                | determined                           |            |
+----------------+--------------------------------------+------------+
| Max. occurence | [0.. ]                               |            |
+----------------+--------------------------------------+------------+
| Comment        |   It’s possible to indicate a range  |            |
|                | of scales for which the data/model   |            |
|                | can be usable (repeatable item)      |            |
+----------------+--------------------------------------+------------+
| INSPIRE IR     | Reference                            | Part B 6.2 |
+----------------+--------------------------------------+------------+
| Title          | Spatial resolution                   |            |
+----------------+--------------------------------------+------------+
| Obligation     |                                      |            |
+----------------+--------------------------------------+------------+
| Max. occurence | [0.. ]                               |            |
+----------------+--------------------------------------+------------+
| ISO 19115      | Number                               | 38         |
+----------------+--------------------------------------+------------+
| Title          | spatialResolution                    |            |
+----------------+--------------------------------------+------------+
| Definition     | factor which provides a general      |            |
|                | understanding of the density of      |            |
|                |                                      |            |
|                | spatial data in the dataset          |            |
+----------------+--------------------------------------+------------+
| XPath          | id                                   |            |
|                | entificationInfo/ /spatialResolution |            |
+----------------+--------------------------------------+------------+
| Data type      | Class                                |            |
+----------------+--------------------------------------+------------+
| Domain         | MD_Resolution <<Union>> (B.2.2.5)    |            |
+----------------+--------------------------------------+------------+
| Example        | 50000                                |            |
|                |                                      |            |
|                | 100 m                                |            |
+----------------+--------------------------------------+------------+

Conformity – Specification
~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 17.1  |
+----------------+-------------------------------------------+-------+
| Title          |   Conformity - specification              |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        |   Citation of the implementing rules      |       |
|                | adopted according to the Article 7,       |       |
|                | section 1 of the 2007/2/ES Directive      |       |
|                | (INSPIRE). If the dataset or data set     |       |
|                | series are not within the scope of        |       |
|                | INSPIRE, fill in the citation of the      |       |
|                | Directive and then the element 17.2 will  |       |
|                | have the value “false”.                   |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 7.1 |
+----------------+-------------------------------------------+-------+
| Title          | Specification                             |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1] understood in the context of a        |       |
|                | conformity statement when reported in the |       |
|                | metadata – there may be more than one     |       |
|                | conformity statement.                     |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 130   |
+----------------+-------------------------------------------+-------+
| Title          | specification                             |       |
+----------------+-------------------------------------------+-------+
| Definition     | citation of the product specification or  |       |
|                | user requirement against which data is    |       |
|                | being evaluated.                          |       |
+----------------+-------------------------------------------+-------+
| XPath          | data                                      |       |
|                | QualityInfo/ /report/DQ_DomainConsistency |       |
|                | /                                         |       |
|                | result/DQ_ConformanceResult/specification |       |
+----------------+-------------------------------------------+-------+
| Data type      | CI_Citation                               |       |
+----------------+-------------------------------------------+-------+
| Domain         | The following properties are expected:    |       |
+----------------+-------------------------------------------+-------+
| Example        | COMMISSION REGULATION (EU) No 1089/2010   |       |
|                | of 23 November 2010 implementing          |       |
|                | Directive 2007/2/EC of the European       |       |
|                | Parliament and of the Council as regards  |       |
|                | interoperability of spatial data sets and |       |
|                | services                                  |       |
|                |                                           |       |
|                |  Reference date: 2010-12-08               |       |
|                |                                           |       |
|                |  Type: publication                        |       |
+----------------+-------------------------------------------+-------+

Conformity - Degree
~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 17.2  |
+----------------+-------------------------------------------+-------+
| Title          |   Conformity - Degree                     |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1]                                       |       |
+----------------+-------------------------------------------+-------+
| Comment        |   True = conformant, False =              |       |
|                | non-conformant, Blank field = not         |       |
|                | evaluated                                 |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 7.2 |
+----------------+-------------------------------------------+-------+
| Title          | Degree                                    |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1] Understood in the context of a        |       |
|                | conformity statement when reported in the |       |
|                | metadata – there may be more than one     |       |
|                | conformity statement.                     |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 132   |
+----------------+-------------------------------------------+-------+
| Title          | Pass                                      |       |
+----------------+-------------------------------------------+-------+
| Definition     | indication of the conformance result      |       |
+----------------+-------------------------------------------+-------+
| XPath          | dataQualityInfo/ /report/ /result/ /pass  |       |
+----------------+-------------------------------------------+-------+
| Data type      | Boolean                                   |       |
+----------------+-------------------------------------------+-------+
| Domain         |                                           |       |
+----------------+-------------------------------------------+-------+
| Example        | false                                     |       |
+----------------+-------------------------------------------+-------+

Conditions applying to access and use
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 18.1  |
+----------------+-------------------------------------------+-------+
| Title          | Conditions applying to access and use     |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        | Description of the Conditions applying to |       |
|                | access and use of the model; information  |       |
|                | about fees, if applicable (text           |       |
|                | description or a URL of a descriptive     |       |
|                | document).                                |       |
|                |                                           |       |
|                |   Description of licences related to the  |       |
|                | model – fill in the element “Use          |       |
|                | Constraints” = „otherRestrictions“ and in |       |
|                | the element otherConstraints fill in the  |       |
|                | information about licensing or a URL of a |       |
|                | descriptive document (for ex. URL of a CC |       |
|                | license).                                 |       |
|                |                                           |       |
|                |   If no conditions apply, fill in “no     |       |
|                | conditions apply” and if the conditions   |       |
|                | are unknown, fill in “conditions unknown” |       |
|                | (from the INSPIRE                         |       |
|                | codelist  \ http                          |       |
|                | ://inspire.ec.europa.eu/metadata-codelist |       |
|                | /ConditionsApplyingToAccessAndUse\   ).   |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 8.1 |
+----------------+-------------------------------------------+-------+
| Title          | Conditions applying to access and use     |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 71    |
+----------------+-------------------------------------------+-------+
| Title          | useConstraints                            |       |
+----------------+-------------------------------------------+-------+
| Definition     | constraints applied to assure the         |       |
|                | protection of privacy or intellectual     |       |
|                | property, and any special restrictions or |       |
|                | limitations or                            |       |
|                |                                           |       |
|                | warnings on using the resource or         |       |
|                | metadata                                  |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/                    |       |
|                |  /resourceConstraints/MD_LegalConstraints |       |
|                | /otherConstraints                         |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 72    |
+----------------+-------------------------------------------+-------+
| Title          | otherConstraints                          |       |
+----------------+-------------------------------------------+-------+
| Definition     | other restrictions and legal              |       |
|                | prerequisites for accessing and using the |       |
|                | resource or metadata                      |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]                     |       |
|                | / /resourceConstraints/ /otherConstraints |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| Example        | Other restrictions;                       |       |
|                |                                           |       |
|                | http://inspire.ec.e                       |       |
|                | uropa.eu/metadata-codelist/ConditionsAppl |       |
|                | yingToAccessAndUse/conditionsUnknown\  ;  |       |
|                |                                           |       |
|                | conditions to access and use unknown      |       |
+----------------+-------------------------------------------+-------+

Limitations on public access
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 18.2  |
+----------------+-------------------------------------------+-------+
| Title          | Limitations on public access              |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        |   Description of a reason of a limitation |       |
|                | on public access to a dataset or a        |       |
|                | service according to the Article 13 of    |       |
|                | the 2007/2/ES Directive. Fill in the      |       |
|                | element “Access Constraints” =            |       |
|                | „otherRestrictions“ and in the element    |       |
|                | otherConstraints fill in the information  |       |
|                | about limitations on access (for INSPIRE  |       |
|                | data, choose from the INSPIRE             |       |
|                | codelist                                  |       |
|                | \ http://inspire.ec.europa.eu/metadata-c  |       |
|                | odelist/LimitationsOnPublicAccess\   ).   |       |
|                |                                           |       |
|                |   If there are no limitations, fill in    |       |
|                | “no limitations to public access”         |       |
|                | (  \ http://insp                          |       |
|                | ire.ec.europa.eu/metadata-codelist/Limita |       |
|                | tionsOnPublicAccess/noLimitations\   from |       |
|                | the INSPIRE codelist).                    |       |
|                |                                           |       |
|                |   You can also mark the data as “open     |       |
|                | data” in this element.                    |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 8.2 |
+----------------+-------------------------------------------+-------+
| Title          | Limitations on public access              |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 70    |
+----------------+-------------------------------------------+-------+
| Title          | accessConstraints                         |       |
+----------------+-------------------------------------------+-------+
| Definition     | access constraints applied to assure the  |       |
|                | protection of privacy or intellectual     |       |
|                | property, and any special restrictions or |       |
|                | limitations on obtaining the resource.    |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/ /resourceConstrai  |       |
|                | nts/MD_LegalConstraints/accessConstraints |       |
+----------------+-------------------------------------------+-------+
| Data type      | MD_RestrictionCode                        |       |
+----------------+-------------------------------------------+-------+
| Domain         | Codelist (strictly limited to the value   |       |
|                | defined in B.5.24 of ISO 19115)           |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 72    |
+----------------+-------------------------------------------+-------+
| Title          | otherConstraints                          |       |
+----------------+-------------------------------------------+-------+
| Definition     | other restrictions and legal              |       |
|                | prerequisites for accessing and using the |       |
|                | resource or metadata.                     |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]                     |       |
|                | / /resourceConstraints/ /otherConstraints |       |
+----------------+-------------------------------------------+-------+
| Data type      | CharacterString                           |       |
+----------------+-------------------------------------------+-------+
| Domain         | Free text                                 |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 74    |
+----------------+-------------------------------------------+-------+
| Title          | classification                            |       |
+----------------+-------------------------------------------+-------+
| Definition     | name of the handling restrictions on the  |       |
|                | resource.                                 |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/                    |       |
|                |  /resourceConstraints/MD_LegalConstraints |       |
|                | /classification                           |       |
+----------------+-------------------------------------------+-------+
| Data type      | MD_ClassificationCode                     |       |
+----------------+-------------------------------------------+-------+
| Domain         | Codelist (See B.5.11 of ISO 19115)        |       |
+----------------+-------------------------------------------+-------+
| Example        | htt                                       |       |
|                | p://inspire.ec.europa.eu/metadata-codelis |       |
|                | t/LimitationsOnPublicAccess/noLimitations |       |
+----------------+-------------------------------------------+-------+

 Responsible party
~~~~~~~~~~~~~~~~~

+----------------+-------------------------------------------+-------+
| EGDI Profile   | Reference number                          | 19    |
+----------------+-------------------------------------------+-------+
| Title          | Responsible party                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     |   Minimum required information – name of  |       |
|                | the organization, name of the author of   |       |
|                | the dataset/model, email address, role    |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| Comment        |   The organization name should be filled  |       |
|                | in English and it is recommended to add   |       |
|                | its abbreviation in the parantheses at    |       |
|                | the end. Organization or person who is    |       |
|                | the primary provider of the dataset or    |       |
|                | service will have the role “custodian”.   |       |
|                | The custodian has the right to commission |       |
|                | other organization to create the data     |       |
|                | source – this organization will have the  |       |
|                | role “originator” or “author” (in case of |       |
|                | enforcing the intellectual property       |       |
|                | rights to the data source). All           |       |
|                | institutions or organizations that buy or |       |
|                | take over the rights to use the data      |       |
|                | source will have the role “user”.         |       |
+----------------+-------------------------------------------+-------+
| INSPIRE IR     | Reference                                 | B 9.1 |
+----------------+-------------------------------------------+-------+
| Title          | Responsible party                         |       |
+----------------+-------------------------------------------+-------+
| Obligation     | Mandatory                                 |       |
+----------------+-------------------------------------------+-------+
| Max. occurence | [1.. ]                                    |       |
+----------------+-------------------------------------------+-------+
| ISO 19115      | Number                                    | 29    |
+----------------+-------------------------------------------+-------+
| Title          | pointOfContact                            |       |
+----------------+-------------------------------------------+-------+
| Definition     | identification of, and means of           |       |
|                | communication with, person(s) and         |       |
|                | organization(s) associated with the       |       |
|                | resource(s)                               |       |
+----------------+-------------------------------------------+-------+
| XPath          | identificationInfo[1]/ /pointOfContact    |       |
+----------------+-------------------------------------------+-------+
| Data type      | CI_ResponsibleParty                       |       |
+----------------+-------------------------------------------+-------+
| Domain         | The following properties are expected:    |       |
+----------------+-------------------------------------------+-------+
| Example        |   Radioactive Waste Repository            |       |
|                | Authority  \  \  \   (SÚRAO)              |       |
|                |                                           |       |
|                |  Dlážděná 6, Praha 1, 110 00, Czech       |       |
|                | Republic                                  |       |
|                |                                           |       |
|                | gis@surao.cz                              |       |
|                |                                           |       |
|                |  role: custodian                          |       |
|                |                                           |       |
|                |   Czech Geological Survey (CGS)           |       |
|                |                                           |       |
|                |  Klárov 3, Praha 1, 118 21, Czech         |       |
|                | Republic                                  |       |
|                |                                           |       |
|                | metadata@geology.cz                       |       |
|                |                                           |       |
|                |  role: originator                         |       |
+----------------+-------------------------------------------+-------+

Data quality scope
~~~~~~~~~~~~~~~~~~

+----------------+-----------------------------------------+---------+
| EGDI Profile   | Reference number                        |   20    |
+----------------+-----------------------------------------+---------+
| Title          | Data quality scope                      |         |
+----------------+-----------------------------------------+---------+
| Obligation     |   Mandatory                             |         |
+----------------+-----------------------------------------+---------+
| Max. occurence | [1]                                     |         |
+----------------+-----------------------------------------+---------+
| Comment        |   Denomination if the data quality      |         |
|                | information is applied to the whole     |         |
|                | dataset or only its part (object class, |         |
|                | attributes, …). Not applicable for      |         |
|                | services.                               |         |
+----------------+-----------------------------------------+---------+
| INSPIRE IR     | Reference                               | 3.1.4.1 |
+----------------+-----------------------------------------+---------+
| Title          | Scope                                   |         |
+----------------+-----------------------------------------+---------+
| Obligation     | Mandatory                               |         |
+----------------+-----------------------------------------+---------+
| Max. occurence | [1]                                     |         |
+----------------+-----------------------------------------+---------+
| ISO 19115      | Number                                  | 79/139  |
+----------------+-----------------------------------------+---------+
| Title          | level                                   |         |
+----------------+-----------------------------------------+---------+
| Definition     | hierarchical level of the data          |         |
|                | specified by the scope                  |         |
+----------------+-----------------------------------------+---------+
| XPath          | dataQualityInfo/ /scope/                |         |
+----------------+-----------------------------------------+---------+
| Data type      | Class                                   |         |
+----------------+-----------------------------------------+---------+
| Domain         | MD_ScopeCode <<CodeList>> (B.5.25)      |         |
+----------------+-----------------------------------------+---------+
| Example        | dataset                                 |         |
+----------------+-----------------------------------------+---------+

.. _section-3:

Coordinate reference system
~~~~~~~~~~~~~~~~~~~~~~~~~~~

+------------------+------------------------+------------------------+
|   EGDI Profile   | Reference number       | 21                     |
+------------------+------------------------+------------------------+
| Title            | Coordinate reference   |                        |
|                  | system                 |                        |
+------------------+------------------------+------------------------+
| Obligation       |   Mandatory for        |                        |
|                  | datasets, optional for |                        |
|                  | services               |                        |
+------------------+------------------------+------------------------+
| Max. occurence   |   [1.. ]               |                        |
+------------------+------------------------+------------------------+
| Comment          | Description of the     |                        |
|                  | coordinate reference   |                        |
|                  | system(s) used in the  |                        |
|                  | dataset (EPSG code and |                        |
|                  | URL).                  |                        |
+------------------+------------------------+------------------------+
| INSPIRE IR       | Reference              | Metadata for           |
|                  |                        | interoperability (1)   |
+------------------+------------------------+------------------------+
| Title            | Coordinate Reference   |                        |
|                  | System                 |                        |
+------------------+------------------------+------------------------+
| Obligation       | Mandatory              |                        |
+------------------+------------------------+------------------------+
| Max. occurence   | [1.. ]                 |                        |
+------------------+------------------------+------------------------+
| ISO 19115        | Number                 | 13                     |
+------------------+------------------------+------------------------+
| Title            | referenceSystemInfo    |                        |
+------------------+------------------------+------------------------+
| Definition       | description of the     |                        |
|                  | spatial and temporal   |                        |
|                  | reference systems used |                        |
|                  | in the dataset         |                        |
+------------------+------------------------+------------------------+
| XPath            | ref                    |                        |
|                  | erenceSystemInfo/ /ref |                        |
|                  | erenceSystemIdentifier |                        |
+------------------+------------------------+------------------------+
| Data type        | Association            |                        |
+------------------+------------------------+------------------------+
| Domain           | MD_ReferenceSystem     |                        |
|                  | (B.2.7)                |                        |
+------------------+------------------------+------------------------+
| Example          |  code: \ ht            |                        |
|                  | tp://www.opengis.net/d |                        |
|                  | ef/crs/EPSG/0/5514\  ; |                        |
|                  | EPSG 5514              |                        |
+------------------+------------------------+------------------------+

Vertical reference system
~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 22                      |
+----------------+-------------------------+-------------------------+
| Title          | Vertical reference      |                         |
|                | system                  |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Mandatory for 3D      |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1]                     |                         |
+----------------+-------------------------+-------------------------+
| Comment        | Description of the      |                         |
|                | vertical reference      |                         |
|                | system used in the      |                         |
|                | dataset (EPSG code and  |                         |
|                | URL).                   |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile but     |
|                |                         | uses the same metadata  |
|                |                         | elements as the element |
|                |                         | “Coordinate reference   |
|                |                         | system”                 |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 13                      |
+----------------+-------------------------+-------------------------+
| Title          | referenceSystemInfo     |                         |
+----------------+-------------------------+-------------------------+
| Definition     | description of the      |                         |
|                | spatial and temporal    |                         |
|                | reference systems used  |                         |
|                | in the dataset          |                         |
+----------------+-------------------------+-------------------------+
| XPath          | r                       |                         |
|                | eferenceSystemInfo/ /re |                         |
|                | ferenceSystemIdentifier |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Association             |                         |
+----------------+-------------------------+-------------------------+
| Domain         | MD_ReferenceSystem      |                         |
|                | (B.2.7)                 |                         |
+----------------+-------------------------+-------------------------+
| Example        |  code:                  |                         |
|                | http://www.opengis.n    |                         |
|                | et/def/crs/EPSG/0/5705; |                         |
|                | EPSG 5705               |                         |
+----------------+-------------------------+-------------------------+

Model vertical extent
~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 23.1                    |
+----------------+-------------------------+-------------------------+
| Title          | Minimum                 |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Conditional for 3D    |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1]                     |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Fill in the           |                         |
|                | numerically smaller     |                         |
|                | vertical limit of the   |                         |
|                | model interlinked with  |                         |
|                | the reference system in |                         |
|                | element 23.3 (local     |                         |
|                | system or a defined     |                         |
|                | vertical coordinate     |                         |
|                | system). If you want to |                         |
|                | describe the model      |                         |
|                | depth in a local        |                         |
|                | system, choose Local    |                         |
|                | (EPSG code 1049) and    |                         |
|                | enter positive value (Z |                         |
|                | axis is in the          |                         |
|                | direction from the      |                         |
|                | surface to the Earth’s  |                         |
|                | core).                  |                         |
|                |                         |                         |
|                |   Conditional in the    |                         |
|                | context of the whole    |                         |
|                | element 23 – if the     |                         |
|                | 23.1 element is filled, |                         |
|                | than 23.2 and 23.3 must |                         |
|                | also be filled.         |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 355                     |
+----------------+-------------------------+-------------------------+
| Title          | minimumValue            |                         |
+----------------+-------------------------+-------------------------+
| Definition     | lowest vertical extent  |                         |
|                | contained in the        |                         |
|                | dataset                 |                         |
+----------------+-------------------------+-------------------------+
| XPath          | identificationInfo[1    |                         |
|                | ]/ /extent/ /verticalEl |                         |
|                | ement/EX_VerticalExtent |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Real                    |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Real                    |                         |
+----------------+-------------------------+-------------------------+
| Example        | 500                     |                         |
+----------------+-------------------------+-------------------------+

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 23.2                    |
+----------------+-------------------------+-------------------------+
| Title          | Maximum                 |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Conditional for 3D    |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1]                     |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Fill in the           |                         |
|                | numerically larger      |                         |
|                | vertical limit of the   |                         |
|                | model interlinked with  |                         |
|                | the reference system in |                         |
|                | element 23.3 (local     |                         |
|                | system or a defined     |                         |
|                | vertical coordinate     |                         |
|                | system). If you want to |                         |
|                | describe the model      |                         |
|                | depth in a local        |                         |
|                | system, choose Local    |                         |
|                | (EPSG code 1049) and    |                         |
|                | enter positive value (Z |                         |
|                | axis is in the          |                         |
|                | direction from the      |                         |
|                | surface to the Earth’s  |                         |
|                | core).                  |                         |
|                |                         |                         |
|                |   Conditional in the    |                         |
|                | context of the whole    |                         |
|                | element 23 – if the     |                         |
|                | 23.2 element is filled, |                         |
|                | than 23.1 and 23.3 must |                         |
|                | also be filled.         |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 356                     |
+----------------+-------------------------+-------------------------+
| Title          | maximumValue            |                         |
+----------------+-------------------------+-------------------------+
| Definition     | highest vertical extent |                         |
|                | contained in the        |                         |
|                | dataset                 |                         |
+----------------+-------------------------+-------------------------+
| XPath          | identificationInfo[1    |                         |
|                | ]/ /extent/ /verticalEl |                         |
|                | ement/EX_VerticalExtent |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Real                    |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Real                    |                         |
+----------------+-------------------------+-------------------------+
| Example        |  2500                   |                         |
+----------------+-------------------------+-------------------------+

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 23.3                    |
+----------------+-------------------------+-------------------------+
| Title          | Vertical extent         |                         |
|                | reference system        |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Conditional for 3D    |                         |
|                | models                  |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1]                     |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   The vertical          |                         |
|                | reference system that   |                         |
|                | is used in the vertical |                         |
|                | extent elements (EPSG   |                         |
|                | code and URL). It can   |                         |
|                | be a local system       |                         |
|                | (depth from the         |                         |
|                | surface) – EPSG 1049.   |                         |
|                |                         |                         |
|                | Mandatory, if elements  |                         |
|                | 23.1 and 23.2 are       |                         |
|                | filled.                 |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 13                      |
+----------------+-------------------------+-------------------------+
| Title          | referenceSystemInfo     |                         |
+----------------+-------------------------+-------------------------+
| Definition     | description of the      |                         |
|                | spatial and temporal    |                         |
|                | reference systems used  |                         |
|                | in the dataset          |                         |
+----------------+-------------------------+-------------------------+
| XPath          | r                       |                         |
|                | eferenceSystemInfo/ /re |                         |
|                | ferenceSystemIdentifier |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Association             |                         |
+----------------+-------------------------+-------------------------+
| Domain         | MD_ReferenceSystem      |                         |
|                | (B.2.7)                 |                         |
+----------------+-------------------------+-------------------------+
| Example        |  http://www.opengis.n   |                         |
|                | et/def/crs/EPSG/0/1049  |                         |
+----------------+-------------------------+-------------------------+

Distribution format
~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 24                      |
+----------------+-------------------------+-------------------------+
| Title          | Distribution format     |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Mandatory             |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [1.. ]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   The value can be      |                         |
|                | either selected from    |                         |
|                | the INSPIRE codelist,   |                         |
|                | or entered as a         |                         |
|                | freetext (especially in |                         |
|                | the case of specialized |                         |
|                | modelling SW). This     |                         |
|                | element will be given   |                         |
|                | as a URI via gmx:Anchor |                         |
|                | for the name of the     |                         |
|                | distribution format     |                         |
|                | <gmd:name>              |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | Metadata for            |
|                |                         | interoperability (3)    |
+----------------+-------------------------+-------------------------+
| Title          | Encoding                |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Mandatory               |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1.. ]                  |                         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 271                     |
+----------------+-------------------------+-------------------------+
| Title          | distributionFormat      |                         |
+----------------+-------------------------+-------------------------+
| Definition     | provides a description  |                         |
|                | of the format of the    |                         |
|                | data to be distributed  |                         |
+----------------+-------------------------+-------------------------+
| XPath          | distributionIn          |                         |
|                | fo/ /distributionFormat |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Association             |                         |
+----------------+-------------------------+-------------------------+
| Domain         | MD_Format (B.2.10.4)    |                         |
+----------------+-------------------------+-------------------------+
| Example        |  http://inspire         |                         |
|                | .ec.europa.eu/media-typ |                         |
|                | es/application/gml+xml; |                         |
|                | gml+xml                 |                         |
+----------------+-------------------------+-------------------------+

Spatial Representation Type
~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 25                      |
+----------------+-------------------------+-------------------------+
| Title          | Spatial representation  |                         |
|                | type                    |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Mandatory             |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [1.. ]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        | Not applicable for      |                         |
|                | services.               |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | Chapter. 8 INSPIRE Data |
|                |                         | Specification on … –    |
|                |                         | Guidelines              |
+----------------+-------------------------+-------------------------+
| Title          | Data Identification –   |                         |
|                | Spatial Representation  |                         |
|                | Type                    |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Mandatory. Optional for |                         |
|                | themes from annex I/5   |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [0.. ]                  |                         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 37                      |
+----------------+-------------------------+-------------------------+
| Title          | sp                      |                         |
|                | atialRepresentationType |                         |
+----------------+-------------------------+-------------------------+
| Definition     | method used to          |                         |
|                | spatially represent     |                         |
|                | geographic information  |                         |
+----------------+-------------------------+-------------------------+
| XPath          | identificationInfo/ /sp |                         |
|                | atialRepresentationType |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Class                   |                         |
+----------------+-------------------------+-------------------------+
| Domain         | MD_Spatia               |                         |
|                | lRepresentationTypeCode |                         |
|                | <<CodeList>> (B.5.26)   |                         |
+----------------+-------------------------+-------------------------+
| Example        | tin                     |                         |
+----------------+-------------------------+-------------------------+

Maintenance and Update Frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 26                      |
+----------------+-------------------------+-------------------------+
| Title          | Maintenance and Update  |                         |
|                | Frequency               |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   Optional              |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [0..1]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   If the desired        |                         |
|                | interval is not present |                         |
|                | in the                  |                         |
|                | mainte                  |                         |
|                | nanceAndUpdateFrequency |                         |
|                | codelist, fill in the   |                         |
|                | value “unknown” and in  |                         |
|                | the                     |                         |
|                | userDefi                |                         |
|                | nedMaintenanceFrequency |                         |
|                | element fill the        |                         |
|                | appropriate interval in |                         |
|                | accordance with the ISO |                         |
|                | 8601:                   |                         |
|                | P<number><period>,      |                         |
|                | where period is Y –     |                         |
|                | year, M-month, D-day,   |                         |
|                | H-hour, for ex. “P5Y”   |                         |
|                | denominates the period  |                         |
|                | of 5 years.             |                         |
|                |                         |                         |
|                | Not applicable for      |                         |
|                | services.               |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 30                      |
+----------------+-------------------------+-------------------------+
| Title          | resourceMaintenance     |                         |
+----------------+-------------------------+-------------------------+
| Definition     | provides information    |                         |
|                | about the frequency of  |                         |
|                | resource updates, and   |                         |
|                | the scope of those      |                         |
|                | updates                 |                         |
+----------------+-------------------------+-------------------------+
| XPath          | iden                    |                         |
|                | tificationInfo/ /resour |                         |
|                | ceMaintenance/ /mainten |                         |
|                | anceAndUpdateFrequency, |                         |
|                | případně                |                         |
|                |                         |                         |
|                | ident                   |                         |
|                | ificationInfo/ /resourc |                         |
|                | eMaintenance/ /userDefi |                         |
|                | nedMaintenanceFrequency |                         |
+----------------+-------------------------+-------------------------+
| Data type      | Class                   |                         |
+----------------+-------------------------+-------------------------+
| Domain         | MD_M                    |                         |
|                | aintenanceFrequencyCode |                         |
|                |                         |                         |
|                | <<CodeList>> (B.5.18),  |                         |
|                | TM_PeriodDuration       |                         |
+----------------+-------------------------+-------------------------+
|  Example       |  unknown, P3Y           |                         |
+----------------+-------------------------+-------------------------+

Purpose
~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 27                      |
+----------------+-------------------------+-------------------------+
| Title          | Purpose                 |                         |
+----------------+-------------------------+-------------------------+
| Obligation     |   optional              |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [0..1]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Summary of purposes   |                         |
|                | for which the data      |                         |
|                | source was created      |                         |
|                | (internal project       |                         |
|                | identifier, scope, type |                         |
|                | of data/model, …).      |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 26                      |
+----------------+-------------------------+-------------------------+
| Title          | purpose                 |                         |
+----------------+-------------------------+-------------------------+
| Definition     | summary of the          |                         |
|                | intentions with which   |                         |
|                | the resource(s) was     |                         |
|                | developed               |                         |
+----------------+-------------------------+-------------------------+
| XPath          | ident                   |                         |
|                | ificationInfo/ /purpose |                         |
+----------------+-------------------------+-------------------------+
| Data type      | CharacterString         |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Free text               |                         |
+----------------+-------------------------+-------------------------+
| Example        |  Project nr. 321560     |                         |
+----------------+-------------------------+-------------------------+

Metadata point of contact
~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------+------------------------------------------+--------+
| EGDI Profile   | Reference number                         | 28.1   |
+----------------+------------------------------------------+--------+
| Title          | Metadata point of contact                |        |
+----------------+------------------------------------------+--------+
| Obligation     |   Minimum required information – name of |        |
|                | the organization (name should be filled  |        |
|                | in English and it is recommended to add  |        |
|                | its abbreviation in the parantheses at   |        |
|                | the end), email address, role            |        |
+----------------+------------------------------------------+--------+
| Max. occurence | [1.. ]                                   |        |
+----------------+------------------------------------------+--------+
| Comment        |   Role must be “pointOfContact” at least |        |
|                | for one organization.                    |        |
+----------------+------------------------------------------+--------+
| INSPIRE IR     | Reference                                | B 10.1 |
+----------------+------------------------------------------+--------+
| Title          | Metadata point of contact                |        |
+----------------+------------------------------------------+--------+
| Obligation     | Mandatory                                |        |
+----------------+------------------------------------------+--------+
| Max. occurence | [1.. ]                                   |        |
+----------------+------------------------------------------+--------+
| ISO 19115      | Number                                   | 8      |
+----------------+------------------------------------------+--------+
| Title          | contact                                  |        |
+----------------+------------------------------------------+--------+
| Definition     | party responsible for the metadata       |        |
|                | information.                             |        |
+----------------+------------------------------------------+--------+
| XPath          | contact                                  |        |
+----------------+------------------------------------------+--------+
| Data type      | CI_ResponsibleParty                      |        |
+----------------+------------------------------------------+--------+
| Domain         | The following properties are expected:   |        |
+----------------+------------------------------------------+--------+
| Example        |  Czech Geological Survey (CGS)           |        |
|                |                                          |        |
|                | metadata@geology.cz                      |        |
|                |                                          |        |
|                |  role: point of contact                  |        |
+----------------+------------------------------------------+--------+

Metadata date
~~~~~~~~~~~~~

============== ==================================== ======
EGDI Profile   Reference number                     28.2
Title            Metadata date                      
Obligation       Mandatory                          
Max. occurence [1]                                  
Comment        Date stamp is created automatically. 
INSPIRE IR     Reference                            B 10.2
Title          Metadata date                        
Obligation     Mandatory                            
Max. occurence [1]                                  
ISO 19115      Number                               9
Title          dateStamp                            
Definition     Date that the metadata was created.  
XPath          dateStamp                            
Data type      Date                                 
Domain         ISO 8601                             
Example        2018-06-30                           
============== ==================================== ======

Metadata language
~~~~~~~~~~~~~~~~~

+----------------+------------------------------------------+--------+
| EGDI Profile   | Reference number                         | 28.3   |
+----------------+------------------------------------------+--------+
| Title          |   Metadata language                      |        |
+----------------+------------------------------------------+--------+
| Obligation     |   Mandatory                              |        |
+----------------+------------------------------------------+--------+
| Max. occurence |   [1.. ]                                 |        |
+----------------+------------------------------------------+--------+
| Comment        |   It is mandatory to have metadata       |        |
|                | records for GeoERA projects in English + |        |
|                | optionally in national language.         |        |
+----------------+------------------------------------------+--------+
| INSPIRE IR     | Reference                                | B 10.3 |
+----------------+------------------------------------------+--------+
| Title          | Metadata language                        |        |
+----------------+------------------------------------------+--------+
| Obligation     | Mandatory                                |        |
+----------------+------------------------------------------+--------+
| Max. occurence | [1]                                      |        |
+----------------+------------------------------------------+--------+
| ISO 19115      | Number                                   | 3      |
+----------------+------------------------------------------+--------+
| Title          | language                                 |        |
+----------------+------------------------------------------+--------+
| Definition     | Language used for documenting metadata.  |        |
+----------------+------------------------------------------+--------+
| XPath          | language                                 |        |
+----------------+------------------------------------------+--------+
| Data type      | LanguageCode (ISO/TS 19139)              |        |
+----------------+------------------------------------------+--------+
| Domain         | Codelist (See ISO/TS 19139) based on     |        |
|                | alpha-3 codes of ISO 639-2. Use only     |        |
|                | three-letter codes from in ISO 639-2/B   |        |
|                | (bibliographic codes), as defined at     |        |
|                | http://www.loc.gov/standards/iso639-2/   |        |
|                |                                          |        |
|                | The list of codes for the 23 official EU |        |
|                | languages is:                            |        |
+----------------+------------------------------------------+--------+
| Example        | cze                                      |        |
+----------------+------------------------------------------+--------+

File identifier
~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 29                      |
+----------------+-------------------------+-------------------------+
| Title          | File identifier         |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Mandatory               |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [1]                   |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Identifier of the     |                         |
|                | metadata file in the    |                         |
|                | form of automatically   |                         |
|                | generated UUID          |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | 2.2.1 (Technical        |
|                |                         | Guidance for the        |
|                |                         | implementation of       |
|                |                         | INSPIRE dataset and     |
|                |                         | service metadata based  |
|                |                         | on ISO/TS 19139:2007)   |
+----------------+-------------------------+-------------------------+
| Title          | File identifier         |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Mandatory               |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence | [1]                     |                         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 2                       |
+----------------+-------------------------+-------------------------+
| Title          | fileIdentifier          |                         |
+----------------+-------------------------+-------------------------+
| Definition     | unique identifier for   |                         |
|                | this metadata file      |                         |
+----------------+-------------------------+-------------------------+
| XPath          | fileIdentifier          |                         |
+----------------+-------------------------+-------------------------+
| Data type      | CharacterString         |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Free text               |                         |
+----------------+-------------------------+-------------------------+
| Example        | 00d32154-1656           |                         |
|                | -4fcc-9ddd-6dbe9a1baeb0 |                         |
+----------------+-------------------------+-------------------------+

Parent identifier
~~~~~~~~~~~~~~~~~

+----------------+-------------------------+-------------------------+
| EGDI Profile   | Reference number        | 30                      |
+----------------+-------------------------+-------------------------+
| Title          | Parent identifier       |                         |
+----------------+-------------------------+-------------------------+
| Obligation     | Optional                |                         |
+----------------+-------------------------+-------------------------+
| Max. occurence |   [0..1]                |                         |
+----------------+-------------------------+-------------------------+
| Comment        |   Identifier of the     |                         |
|                | parent metadata file    |                         |
|                | (for ex. if a dataset   |                         |
|                | belongs to a data set   |                         |
|                | series). Not applicable |                         |
|                | for services.           |                         |
+----------------+-------------------------+-------------------------+
| INSPIRE IR     | Reference               | This element is an      |
|                |                         | extension to the        |
|                |                         | INSPIRE profile         |
+----------------+-------------------------+-------------------------+
| ISO 19115      | Number                  | 5                       |
+----------------+-------------------------+-------------------------+
| Title          | parentIdentifier        |                         |
+----------------+-------------------------+-------------------------+
| Definition     | file identifier of the  |                         |
|                | metadata to which this  |                         |
|                | metadata is a subset    |                         |
|                |                         |                         |
|                | (child)                 |                         |
+----------------+-------------------------+-------------------------+
| XPath          | parentIdentifier        |                         |
+----------------+-------------------------+-------------------------+
| Data type      | CharacterString         |                         |
+----------------+-------------------------+-------------------------+
| Domain         | Free text               |                         |
+----------------+-------------------------+-------------------------+
| Example        | 00d32154-1656           |                         |
|                | -4fcc-9ddd-6dbe9a1baeb0 |                         |
+----------------+-------------------------+-------------------------+

References
==========

-  EN ISO 19115 Geographic Information – Metadata, 2003 Czech National Metadata Profile, version 4.2 (5.2.2020, TWG Metadata)  
-  EC Directive 2007/2/EC (INSPIRE)
-  EC REGULATION No 1205/2008 (Metadata) Technical Guidelines for implementing dataset and service metadata based on ISO/TS 19139:2007, version 2.0.1, 2017-03-02  

.. [1]
   The final form of the URI for the project vocabularies was not
   established at the time of publication of this document but will look
   similarly to the provided example

.. [2]
   The final form of the URI for the project vocabularies was not
   established at the time of publication of this document but will look
   similarly to the provided example

.. [3]
   The final form of the URI for the project vocabularies was not
   established at the time of publication of this document but will look
   similarly to the provided example

.. |image0| image:: _static/images/EGDIProfile/Pictures/1000000000000FB000000FB0DB6852BC5C06E692.jpg
   :width: 2.277cm
   :height: 2.277cm
