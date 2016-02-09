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
* properties: scopeContent contains

# <http://bibfra.me/vocab/lite/Collection>
* properties: extent 
   
## contains
* label: contains
* description: Part of relationship
* scope: <http://bibfra.me/vocab/archive>

<!-- 
Class Refinements 
-->

# Archive

* label: Archive
* refines: http://bibfra.me/vocab/lite/Place
* description: Place to access, curate, and store archival collections of historical documents or records providing information about places, institutions, groups of peoples, events, and creative activity. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>

<!---

Should reading room be a place? I think it should because a multi-unit organization may have different hours of operation for different locations. 

-->

# FindingAid
* label: Finding Aid
* refines: <http://bibfra.me/vocab/lite/Instance>
* description: Document used to give the repository physical and intellectual control over the materials, and assist users in gaining access to and understanding archival collections.
* properties: eadId 
* scope: <http://bibfra.me/vocab/archive>

# Repository
* label: Repository
* refines: <http://bibfra.me/vocab/lite/Organization>
* description: Organization that stores and manages archival materials. 
* properties: addressRepository 
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Name of Repository Element (2.2) in Describing Archives: a Content Standard, 2nd Edition (2015).

# Box
* label: Box
* refines: <http://bibfra.me/vocab/archive/Item>
* description: Box that contains archival materials. 
* properties: contains
* scope: <http://bibfra.me/vocab/archive>

# Folder
* label: Folder
* refines: <http://bibfra.me/vocab/archive/Item>
* description: Folder that contains archival materials. 
* properties: contains
* scope: <http://bibfra.me/vocab/archive>

<!---

New classes to BF Lite + Archives (not in BF Lite). 

-->

# Item
* label: Item
* refines: <http://bibfra.me/vocab/lite/Instance>
* description: Archival item or object. 
* properties: scopeContent referenceCode
* scope: <http://bibfra.me/vocab/archive>

# File
* label: File
* refines: <http://bibfra.me/vocab/archive/Item>
* description: Digital or object. A File is a sequence of binary data and is described by some accompanying metadata. The metadata typically includes at least basic technical metadata (size, content type, modification date, etc.), but can also include properties related to preservation, digitization process, provenance, etc.
* scope: <http://bibfra.me/vocab/archive>
* remark: Equivalent to pcdm:File.

<!---

Supporting properties from DACS

-->

## arranger
* label: arranger
* refines: <http://bibfra.me/vocab/lite/contributor>
* description: Person who works to provide access to archival collections of historical documents or records providing information about places, institutions, groups of peoples, events, and creative activity. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>

## addressRepository 
* label: repository address
* description: Address of holding organization or repository. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Location of Repository Element (2.2) in Describing Archives: a Content Standard, 2nd Edition (2015).

## eadId
* label: ead identifier
* refines: <http://bibfra.me/vocab/lite/controlCode>
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
* description: A local or repository identifier for archival collection, box, folder or item. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Reference Code Element 2.1 in Describing Archives: a Content Standard, 2nd Edition (2015). At the highest levels of description, this is oftentimes known as the collection number, e.g., UARS745 for University Archives Record Series #745.

## extent
* label: extent
* description: Used to identify and describe the physical or logical extent and the medium of the unit of description. Oftentimes measured in linear shelf space or cubic storage space of the unit of description, or the amount of digital files and storage space.
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Extent Element 2.5 in in Describing Archives: a Content Standard, 2nd Edition (2015). 


## scopeContent
* label: scope and content
* refines: <http://bibfra.me/vocab/lite/note>
* description: Scope and content note. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Scope and Content Element 3.1 in Describing Archives: a Content Standard, 2nd Edition (2015).


## accessConditions
* label: conditions governing access
* refines: <http://bibfra.me/vocab/lite/note>
* description: Note on conditions for accessing an archival collection. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Scope and Conditions Governing Access Element 4.1 in Describing Archives: a Content Standard, 2nd Edition (2015).


<!---

Elements below are oncluded in BF Lite but need updated descriptions for the BF Lite + Archives layer.
NOTE: This is best done at the profile layer rather than the vocabulary layer

# title
* label: title
* refines: http://bibfra.me/vocab/lite/title
* description: Title of an archival collection, box, folder or item. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Title Element 2.3 in Describing Archives: a Content Standard, 2nd Edition (2015).

# date
* label: date
* refines: http://bibfra.me/vocab/lite/date
* description: Date of an archival collection, box, folder or item. 
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Date Element 2.4 in Describing Archives: a Content Standard, 2nd Edition (Updated March 2015).

# creator
* label: extent
* refines: --use something on the relator level instead of refining? 
* description: Creator of an archival item or group of items.
* value: Literal
* scope: <http://bibfra.me/vocab/archive>

# language
* label: language
* refines: http://bibfra.me/vocab/lite/note
* description: Language or script of the archival material.
* value: Literal
* scope: <http://bibfra.me/vocab/archive>
* remark: Equevalent to Languages and Scripts of the Material Element 4.5 in Describing Archives: a Content Standard, 2nd Edition (2015).

Not from DACS but needs updated description:

## donor

* label: donor
* refines: <http://bibfra.me/vocab/lite/contributor>
* description: Person who donates an archival collection of documents or records providing information about themselves, places, institutions, groups of peoples, events, and creative activity.
* value: Literal
* scope: <http://bibfra.me/vocab/archive>

--->
