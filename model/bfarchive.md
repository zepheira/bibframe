<!---

BIBFRAME Archive is a starting point for archival vocabularies using the 
http://bibfra.me model and profiles. It builds off of the BIBFRAME Lite vocabulary. 
It is framework conformant to BIBFRAME and Descriving Archives a Content Standard (DACS). Where possible, the vocabulary is link-compatible with the 
US Library of Congress's BIBFRAME vocabulary, http://bibframe.org/

BIBFRAME Archive is expressed using the Versa data model, which also
allows for full expression in RDF form.  This particular file is in
the Versa Literate syntax, based on the Markdown format

The convention for expressing data models in Versa Literate has each
vocabulary item starting with a new header, A level 1 header for
resource classes and level 2 for properties.  Each has its ID as an
IRI reference (usually relative). Each is then described within its
section's unordered list, given a "label" (display label),
"description" (also for explanatory display), possibly "synonyms" (one
or more loose expression that the resource can be considered a synonym
for another). Resource classes may also have "properties"
(space-separated list of property IDs defined on the
resource). Properties may also have "value" (textual description of
the expected value of the property, perhaps as a relationship to
another resource, or as a data value).

You'll notice that BIBFRAME Archive terms use a humpCase/HumpCase convention,
which derives from BIBFRAME legacy.

-->

# @docheader

<!---

@base is the default base IRI, used e.g. for resource headers. It
would also be used for properties except that it is overridden by
@property-base

The meta-properties in this file are actually defined by the Versa
data model to support interpretation by Versa modeling tools

@resource-base is another possible override, for resource headers, but
not used here

-->

* @iri:
    * @base: http://bibfra.me/vocab/archive/
    * @property: http://bibfra.me/purl/versa/support
* title: BIBFRAME Archive vocabulary
* @interpretations:
    * scope: @resource

<!---
Extend BIBFRAME Lite Classess
--->

# <http://bibfra.me/vocab/lite/Work>
* properties: primary memberOf scopeContent contains

# <http://bibfra.me/vocab/lite/Instance>
* properties: primary memberOf scopeContent contains referenceCode

# <http://bibfra.me/vocab/lite/Authority>

# <http://bibfra.me/vocab/lite/Collection>
* properties: primary memberOf scopeContent contains extent 

# <http://bibfra.me/vocab/lite/Person>
* properties: 

# <http://bibfra.me/vocab/lite/Organization>
* properties: 

# <http://bibfra.me/vocab/lite/Meeting>
* properties: 

# <http://bibfra.me/vocab/lite/Topic>
* properties: 

# <http://bibfra.me/vocab/lite/Form>
* properties: 
    
# <http://bibfra.me/vocab/lite/Event>
* properties: 

# <http://bibfra.me/vocab/lite/Temporal>
* properties:
   
<!-- 
Class Refinements 
-->

# Archive

* label: Archive
* refines: http://bibfra.me/vocab/lite/Place
* synonyms: 
* description: Place to access, curate, and store archival collections of historical documents or records providing information about places, institutions, groups of peoples, events, and creative activity. 
* value: Literal
* properties: 
* scope: <http://bibfra.me/vocab/archive>
* remark:

<!---

Should reading room be a place? I think it should because a multi-unit organization may have different hours of operation for different locations. 

-->

# FindingAid
* label: Finding Aid
* refines: http://bibfra.me/vocab/lite/Instance
* synonyms: 
* description: Work with finding aid characteristics that describes archival collections to give the repository physical and intellectual control over the materials, and assist users in gaining access to and understanding the materials.
* properties: eadId 
* scope: <http://bibfra.me/vocab/archive>
* remark:

# Repository
* label: Repository
* refines: http://bibfra.me/vocab/lite/Organization
* synonyms: 
* description: Name of holding organization or repository. 
* properties: addressRepository 
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Name of Repository Element (2.2) in Describing Archives: a Content Standard, 2nd Edition (2015).

# ArchivalCollection 
* label: Archival Collection
* refines: <http://bibfra.me/vocab/lite/Collection>
* description: Aggregation or gathering of works.
* properties: primary memberOf scopeContent contains extent
* scope: <http://bibfra.me/vocab/archive>

# ArchivalSeries
* label: Archival Series
* refines: <http://bibfra.me/vocab/lite/Series>
* description: Aggregation or gathering of works within an archival collection.
* properties: primary memberOf scopeContent contains
* scope: <http://bibfra.me/vocab/archive>

# ArchivalSubSeries
* label: <http://bibfra.me/vocab/lite/SubSeries>
* refines: Archival Series
* description: Aggregation or gathering of works within a series.
* properties: primary memberOf scopeContent contains
* scope: <http://bibfra.me/vocab/archive>

# Box
* label: Box
* refines: <http://bibfra.me/vocab/lite/Instance>
* description: Box that contains archival materials. 
* properties: primary memberOf scopeContent contains referenceCode
* scope: <http://bibfra.me/vocab/archive>

# Folder
* label: Folder
* refines: <http://bibfra.me/vocab/lite/Instance>
* description: Folder that contains archival materials. 
* properties: primary memberOf scopeContent contains referenceCode
* scope: <http://bibfra.me/vocab/archive>

<!---

New classes to BF Lite + Archives (not in BF Lite). 

-->

# Item
* label: Item
* refines: 
* description: Archival item or object. 
* properties: primary memberOf scopeContent referenceCode
* scope: <http://bibfra.me/vocab/archive>

# File
* label: file
* refines: <http://bibfra.me/vocab/lite/archive/Item>
* description: Digital or object. A File is a sequence of binary data and is described by some accompanying metadata. The metadata typically includes at least basic technical metadata (size, content type, modification date, etc.), but can also include properties related to preservation, digitization process, provenance, etc.
* properties: primary memberOf scopeContent referenceCode
* scope: <http://bibfra.me/vocab/archive>
* remark: Equivalent to pcdm:File.


<!---

Supporting properties from DACS

-->

## arranger
* label: arranger
* refines: <http://bibfra.me/vocab/lite/contributor>
* synonyms: 
* description: Person who works to provide access to archival collections of historical documents or records providing information about places, institutions, groups of peoples, events, and creative activity. 
* value: Literal
* properties: 
* scope: <http://bibfra.me/vocab/archive>
* remark:

## addressRepository 
* label: repository address
* refines: http://bibfra.me/vocab/lite/address
* synonyms: 
* description: Address of holding organization or repository. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Location of Repository Element (2.2) in Describing Archives: a Content Standard, 2nd Edition (2015).

## eadId
* label: ead identifier
* refines: <http://bibfra.me/vocab/lite/controlCode>
* synonyms: 
* description: Designates a unique code for a particular EAD finding aid document.
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equivalent to EAD ID <eadid>

<!---

Terms below are mapped from DACS Multilevel Required elements:

-->

## referenceCode
* label: reference code
* refines: <http://bibfra.me/vocab/lite/controlCode>
* synonyms: 
* description: A local or repository identifier for archival collection, box, folder or item. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Reference Code Element 2.1 in Describing Archives: a Content Standard, 2nd Edition (2015). At the highest levels of description, this is oftentimes known as the collection number, e.g., UARS745 for University Archives Record Series #745.

## extent
* label: extent
* refines: 
* synonyms: 
* description: Used to identify and describe the physical or logical extent and the medium of the unit of description. Oftentimes measured in linear shelf space or cubic storage space of the unit of description, or the amount of digital files and storage space.
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Extent Element 2.5 in in Describing Archives: a Content Standard, 2nd Edition (2015). 


## scopeContent
* label: scope and content
* refines: http://bibfra.me/vocab/lite/note
* synonyms: 
* description: Scope and content note. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Scope and Content Element 3.1 in Describing Archives: a Content Standard, 2nd Edition (2015).


## accessConditions
* label: conditions governing access
* refines: http://bibfra.me/vocab/lite/note
* synonyms: 
* description: Note on conditions for accessing an archival collection. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Scope and Conditions Governing Access Element 4.1 in Describing Archives: a Content Standard, 2nd Edition (2015).


<!---

Elements below are oncluded in BF Lite but need updated descriptions for the BF Lite + Archives layer.

# title
* label: title
* refines: http://bibfra.me/vocab/lite/title
* synonyms: 
* description: Title of an archival collection, box, folder or item. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Title Element 2.3 in Describing Archives: a Content Standard, 2nd Edition (2015).

# date
* label: date
* refines: http://bibfra.me/vocab/lite/date
* synonyms: 
* description: Date of an archival collection, box, folder or item. 
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Date Element 2.4 in Describing Archives: a Content Standard, 2nd Edition (Updated March 2015).

# creator
* label: extent
* refines: --use something on the relator level instead of refining? 
* synonyms: 
* description: Creator of an archival item or group of items.
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>


# language
* label: language
* refines: http://bibfra.me/vocab/lite/note
* synonyms: 
* description: Language or script of the archival material.
* value: Literal
* properties:  
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Languages and Scripts of the Material Element 4.5 in Describing Archives: a Content Standard, 2nd Edition (2015).

Not from DACS but needs updated description:

## donor

* label: donor
* refines: <http://bibfra.me/vocab/lite/contributor>
* synonyms: 
* description: Person who donates an archival collection of documents or records providing information about themselves, places, institutions, groups of peoples, events, and creative activity.
* value: Literal
* properties: 
* scope: <http://bibfra.me/vocab/archive>
* remark:

--->
