<!---

BIBFRAME American Antiquarian Society (AAS) is a starting point for vocabularies 
intended to describe the history of printing rare materials using the 
BIBFRAME model and profiles. It builds off of the BIBFRAME Lite vocabulary. 
It is framework conformant to BIBFRAME where applicable, and where possible, link-compatible with the 
US Library of Congress's BIBFRAME vocabulary, http://www.loc.gov/bibframe/docs/index.html.

BIBFRAME AAS is expressed using the Versa data model, which also
allows for full expression in RDF form.  This particular file is in
the Versa Literate syntax, based on the Markdown format
<https://daringfireball.net/projects/markdown/basics>.

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

You'll notice that BIBFRAME Rare terms use a humpCase/HumpCase convention,
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
    * @base: http://bibfra.me/vocab/aas/
    * @property: http://bibfra.me/purl/versa/support
* title: BIBFRAME American Antiquarian Society vocabulary
* @interpretations:
    * scope: @resource

<!---
Extend BIBFRAME Lite Classess
--->

# <http://bibfra.me/vocab/lite/Place>
* properties: locationID

# <http://bibfra.me/vocab/lite/Person>
* properties: trade


<!-- 
From AAS Location data
-->

# City

* label: City
* refines: <http://bibfra.me/vocab/lite/Place>
* description: Incorporated municipality, usually governed by a mayor and a board of aldermen or councilmen.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

# State

* label: State
* refines: <http://bibfra.me/vocab/lite/Place>
* description: Type of polity that is an organized political community living under a single system of government.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

# Country

* label: Country
* refines: <http://bibfra.me/vocab/lite/Place>
* description: Nation with its own government, occupying a particular territory.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

<!-- 
From AAS Trade data
-->

## trade

* label: trade
* description: Skilled job, typically one requiring manual skills and special training.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>


# 

* label: 
* refines: <http://bibfra.me/vocab/lite/>
* synonyms: 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>
* remark: 
* properties:




