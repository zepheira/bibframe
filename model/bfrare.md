<!---

BIBFRAME Rare is a starting point for rare materials vocabularies using the 
BIBFRAME model and profiles. It builds off of the BIBFRAME Lite vocabulary. 
It is framework conformant to BIBFRAME, the DCRM principles of construction, 
RDA where applicable. and where possible, link-compatible with the 
US Library of Congress's BIBFRAME vocabulary, http://bibframe.org/

BIBFRAME Rare is expressed using the Versa data model, which also
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
    * @base: http://bibfra.me/vocab/dcrmb/
    * @property: http://bibfra.me/purl/versa/support
* title: BIBFRAME DCRM(B) vocabulary
* @interpretations:
    * scope: @resource


## titleProper

* label: title proper
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: 
* description: The proper title
* value: Literal
* scope: <http://bibfra.me/vocab/dcrmb>
* remark: Required element.

## datePublication

* label: date publication
* refines: <http://bibfra.me/vocab/lite/providerDate>
* description: The date of publication.
* value: Literal
* scope: <http://bibfra.me/vocab/dcrmb>
* remark: Required element. Recommended ISO 8601 date.

## signature

* label: signature
* refines: <http://bibfra.me/vocab/lite/note>
* description: Lists or summaries of signatures often printed at the end of early printed books.
* value: Literal
* scope: <http://bibfra.me/vocab/dcrmb>
