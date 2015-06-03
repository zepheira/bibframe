<!--

BIBFRAME Lite is a starting point for customized BIBFRAME vocabularies
and profiles.  It is framework conformant to BIBFRAME and
link-compatible with the US Library of Congress's BIBFRAME vocabulary,
http://bibframe.org/

BIBFRAME Lite is expressed using the Versa data model, which also
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

You'll notice that BIBFRAME terms use a humpCase/HumpCase convention,
which derives from BIBFRAME legacy.

-->

# @docheader

<!--

@base is the default base IRI, used e.g. for resource headers. It
would also be used for properties except that it is overridden by
@property-base

The meta-properties in this file are actually defined by the Versa
data model to support interpretation by Versa modeling tools

@resource-base is another possible override, for resource headers, but
not used here

-->

* @iri:
    * @base: http://bibfra.me/vocab/lite/
    * @property: http://bibfra.me/purl/versa/support
* @interpretations:
    * scope: @resource
    * highlight: @resourceset
* title: BIBFRAME Lite vocabulary
* highlight: Work Instance Event Authority Annotation

# Resource

* synonyms: <http://bibframe.org/vocab/Resource> <http://schema.org/Thing>
* label: Resource
* description: A conceptual resource
* properties: label description image link rightsStatement controlCode related language date audience note authorityLink
* scope: <http://bibfra.me/vocab/lite>

## label

* synonyms: <http://bibframe.org/vocab/label> <http://schema.org/name> <http://www.w3.org/2000/01/rdf-schema#label>
* value: Literal
* label: label
* description: A text string representing the name of resource.
* scope: <http://bibfra.me/vocab/lite>

## prefLabel

* synonyms: <http://www.w3.org/2004/02/skos/core#prefLabel>
* value: Literal
* label: prefered label
* refines: label
* description: The prefered human readable label of the resource.
* scope: <http://bibfra.me/vocab/lite>

## description

* synonyms: <http://bibframe.org/vocab/description> <http://schema.org/description> <http://purl.org/dc/elements/1.1/description>
* value: Literal
* label: description
* description: A description of the resource.
* scope: <http://bibfra.me/vocab/lite>

## image

* synonyms: <http://bibframe.org/vocab/image> <http://schema.org/image>
* value: IRI
* label: image
* description: The IRI of an image of the resource.
* scope: <http://bibfra.me/vocab/lite>

## link

* synonyms: <http://bibframe.org/vocab/link> <http://schema.org/url>
* value: IRI
* label: link
* description: The IRI of a resource.
* scope: <http://bibfra.me/vocab/lite>

## rightsStatement

* label: rights statement
* synonyms: <http://purl.org/dc/elements/1.1/rights>
* value: literal
* description: A rights statement associated with the origin resource.
* scope: <http://bibfra.me/vocab/lite>

## controlCode

* label: control code
* value: Literal
* description: An alphanumeric string or indicator used to find and identify the resource.
* remark: A non-IRI based identifier reflecting local or community coding practices
* scope: <http://bibfra.me/vocab/lite>

## related

* label: related
* synonyms: <http://purl.org/dc/elements/1.1/related>
* value: Resource
* description: A resource related to the origin resource.
* scope: <http://bibfra.me/vocab/lite>

## language

* label: language
* synonyms: <http://bibframe.org/vocab/language> <http://purl.org/dc/elements/1.1/language>
* value: IRI
* description: A language associated with the resource.
* scope: <http://bibfra.me/vocab/lite>

## date

* label: date
* description: The date associated with the resource.
* value: Literal
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateStart
* label: start date
* synonyms: <http://schema.org/startDate>
* description: The start date associated with the resource.
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateEnd
* label: end date
* synonyms: <http://schema.org/endDate>
* description: The end date associated with the resource.
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## audience

* label: audience
* value: Literal
* description: Class of user for which the content of a resource is intended, or for whom the content is considered suitable.
* remark: A target audience can be formed of people of a certain age group, gender, marital status, etc.. Other groups, although not the main focus, may also be interested. The value of this property is intended to be a code list. 
* scope: <http://bibfra.me/vocab/lite>

## note

* label: note
* value: Literal
* description: Additional descriptive information associated with the resource.
* scope: <http://bibfra.me/vocab/lite>

# Authority 

* label: Authority
* synonyms: <http://bibframe.org/vocab/Authority>
* refines: Resource
* description: A credible, curated description of a person, place or thing.
* properties: name nameAlternative
* scope: <http://bibfra.me/vocab/lite>

## name
* label: name
* value: Literal
* description: The name of an authority.
* refines: label
* scope: <http://bibfra.me/vocab/lite>

## nameAlternative
* label: alternative name
* value: Literal
* description: The alternative name of an authority.
* refines: name
* scope: <http://bibfra.me/vocab/lite>

## authorityLink

* label: authority link
* synonyms: <http://bibframe.org/vocab/hasAuthority> <http://schema.org/sameAs>
* value: IRI
* refines: link
* description: Actionable IRI linking to an authoritative controlled vocabulary.
* remark: Example identifiers include VIAF, LCNAF, ISNI, ORCID, etc.
* scope: <http://bibfra.me/vocab/lite>

# Work

* label: Work
* synonyms: <http://bibframe.org/vocab/Work>
* refines: Resource
* description: A distinct intellectual or artistic creation.
* properties: creator contributor title subject genre
* scope: <http://bibfra.me/vocab/lite>

## title

* label: title
* synonyms: <http://purl.org/dc/elements/1.1/title>
* description: Title of the resource.
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## titleAlternative

* label: title alternative
* refines: title
* description: Alternative title of the resource.
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## description

* label: description
* description: Description of the resource.
* value: Literal
* remark: Description for example of bibliographic resources may include but is not limited to: an abstract, a table of contents, a graphical representation, or a free-text account of the resource.
* scope: <http://bibfra.me/vocab/lite>

## creator

* label: creator
* synonyms: <http://bibframe.org/vocab/creator> <http://purl.org/dc/elements/1.1/creator>
* value: Agent 
* refines: contributor
* description: Entity (or entities) responsible with the creation of the origin resource
* scope: <http://bibfra.me/vocab/lite>

## contributor

* label: contributor
* value: Agent 
* synonyms: <http://bibframe.org/vocab/contributor> <http://purl.org/dc/elements/1.1/contributor>
* description: Entity (or entities) who contribute to the origin resource
* scope: <http://bibfra.me/vocab/lite>

## subject
* label: subject
* value: Concept
* synonyms: <http://bibframe.org/vocab/subject> <http://purl.org/dc/elements/1.1/subject>
* description: Index term, subject term, subject heading, or descriptor, a term for information retrieval which captures the essence of the topic of a resource. 
* remark: The 'about-ness' of a work
* scope: <http://bibfra.me/vocab/lite>

## genre
* label: genre
* value: Form
* synonyms: <http://bibframe.org/vocab/genre>
* description: A category of artistic composition characterized by similarities in form, style, or subject matter.
* remark: The 'is-ness' of a work
* scope: <http://bibfra.me/vocab/lite>

# Agent
* label: Agent
* refines: Authority
* synonyms: <http://bibframe.org/vocab/Agent>
* description: An entity (e.g. person, organization, etc.) associated with a resource. 
* scope: <http://bibfra.me/vocab/lite>

# Person
* label: Person
* refines: Agent
* synonyms: <http://bibframe.org/vocab/Person>
* description: An individual (alive, dead, undead, or fictional) in relation to a resource.
* scope: <http://bibfra.me/vocab/lite>

# Organization
* label: Organization
* refines: Agent
* synonyms: <http://bibframe.org/vocab/Organization>
* description: A unit of people, e.g., an institution, an association, or corporate body.
* scope: <http://bibfra.me/vocab/lite>

# Meeting
* label: Meeting
* refines: Agent
* synonyms: <http://bibframe.org/vocab/Meeting>
* description: A formal gathering of people for a particular purpose.
* scope: <http://bibfra.me/vocab/lite>

# Family
* label: Family
* refines: Agent
* synonyms: <http://bibframe.org/vocab/Family>
* description: A social unit related by birth, marriage, adoption, civil union, or similar relationship.
* scope: <http://bibfra.me/vocab/lite>

# Place
* label: Place
* refines: Authority
* synonyms: <http://bibframe.org/vocab/Place>
* description: Geographic location.
* scope: <http://bibfra.me/vocab/lite>

# Category
* label: Category
* refines: Resource
* synonyms: <http://schema.org/Enumeration> <http://bibframe.org/vocab/Category>
* description: A list of things regarded as having particular shared characteristics.
* remark: A controlled vocabulary. 
* scope: <http://bibfra.me/vocab/lite>

# Topic 
* label: Topic
* refines: Authority
* synonyms: <http://bibframe.org/vocab/Topic>
* description: Subject term describing a general concept, event or object. 
* scope: <http://bibfra.me/vocab/lite>

# Form
* label: Form
* refines: Category
* description: Category or genre that describes what the resource is.
* scope: <http://bibfra.me/vocab/lite>

# Concept
* label: Concept
* refines: Resource
* synonyms: <http://www.w3.org/2009/08/skos-reference/skos.html#Concept>
* description: Term describing the subject or aboutness of a resource. An idea or notion. 
* properties: focus
* scope: <http://bibfra.me/vocab/lite>

# Instance
* refines: Resource
* label: Instance
* synonyms: <http://bibframe.org/vocab/Instance>
* description: An individual embodiment of a Work.
* properties: contributor title instantiates extent provision copyright dimensions format medium 
* scope: <http://bibfra.me/vocab/lite>

## instantiates
* synonyms: <http://bibframe.org/vocab/instanceOf>
* label: instantiates
* description: The Work this resource instantiates or manifests. 
* remark: For use to connect Instances to Works in the BIBFRAME structure.
* refines: related
* value: Work
* scope: <http://bibfra.me/vocab/lite>

## focus
* label: focus
* synonyms: <http://xmlns.com/foaf/0.1/focus>
* description: The underlying or focal entity associated with a concept.
* remark: Often times the focus is the primary entity associated with a pre-coordinated subject heading.
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## provision
* label: provision
* synonyms: <http://bibframe.org/vocab/provider>
* value: ProviderEvent
* description: Provider associated with the carrier.
* remark: Connection to details such as the place, name, and/or date information relating to the publication, printing, distribution, issue, release, or production of an Instance.
* scope: <http://bibfra.me/vocab/lite>

## copyright
* label: copyright
* value: CopyrightEvent
* description: Copyright event associated with the instance.
* scope: <http://bibfra.me/vocab/lite>

## format
* label: format
* synonyms: <http://bibframe.org/vocab/format>
* description: Format of the Instance.
* value: IRI
* scope: <http://bibfra.me/vocab/lite>

## medium
* label: medium
* value: IRI
* description: The medium of the Instance.
* scope: <http://bibfra.me/vocab/lite>

## extent

* synonyms: <http://bibframe.org/vocab/extent>
* label: extent
* value: Literal
* description: Number of physical pages, volumes, cassettes, total playing time, etc., of of each type of unit.
* scope: <http://bibfra.me/vocab/lite>

## dimensions

* synonyms: <http://bibframe.org/vocab/dimensions>
* label: dimensions
* value: Literal
* description: A measure of the size of its covering properties. 
* scope: <http://bibfra.me/vocab/lite>

# ProviderEvent

* refines: Event
* label: Provider Event
* description: Event associated with the publication, printing, distribution, issue, release or production of an instance.
* properties: providerAgent providerPlace providerDate providerNote
* scope: <http://bibfra.me/vocab/lite>

# CopyrightEvent

* refines: Event
* label: Copyright Event
* description: Copyright event associated with the intellectual property of an instance.
* properties: license
* scope: <http://bibfra.me/vocab/lite>

## license

* label: license
* synonyms: <http://creativecommons.org/ns#license>
* description: License associated with the rights event associated with a Work.
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## providerAgent

* label: provider agent
* synonyms: <http://bibframe.org/vocab/providerName>
* description: Agent associated with the publication, printing, distribution, issue, release or production of an instance.
* refines: who
* value: Agent
* scope: <http://bibfra.me/vocab/lite>

## providerPlace

* label: provider place
* refines: where
* description: Place associated with the publication, printing, distribution, issue, release or production of an instance.
* synonyms: <http://bibframe.org/vocab/providerPlace>
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## providerDate

* label: provider date
* synonyms: <http://bibframe.org/vocab/providerDate>
* description: Date associated with the publication, printing, distribution, issue, release or production of an instance.
* refines: when
* scope: <http://bibfra.me/vocab/lite>

## providerNote

* label: provider note
* description: A note associated with the publication, printing, distribution, issue, release or production of an instance.
* refines: why
* value: 
* scope: <http://bibfra.me/vocab/lite>

# Event

* label: Event
* refines: Resource
* properties: who what where when why
* description: A significant occurrence or happening
* scope: <http://bibfra.me/vocab/lite>

## who

* label: who
* description: Person or thing related to an Event 
* value: Agent
* scope: <http://bibfra.me/vocab/lite>

## what

* label: what
* description: Resource related to an Event 
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## where

* label: where
* description: Place associated with an Event 
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## when

* label: when
* description: Date associated with an Event 
* value: Literal
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## why

* label: why
* refines: note  
* description: Concept associated with an Event 
* value: Concept
* scope: <http://bibfra.me/vocab/lite>

# Annotation

* label: Annotation
* refines: Resource
* synonyms: <http://bibframe.org/vocab/Annotation>
* description: Annotation, provides for loosely attached information about a resource
* properties: annotator body target
* scope: <http://bibfra.me/vocab/lite>

## annotator

* label: annotator
* synonyms: <http://bibfra.me/vocab/annotator>
* value: Agent
* description: Agent associated with the annotation
* scope: <http://bibfra.me/vocab/lite>

## body

* synonyms: <http://bibfra.me/vocab/body>
* label: body
* value: Resource
* description: Body of an annotation
* scope: <http://bibfra.me/vocab/lite>

## target

* synonyms: <http://bibfra.me/vocab/target>
* label: target
* value: Resource
* description: Target of an annotation
* scope: <http://bibfra.me/vocab/lite>

# Collection 
* label: Collection
* refines: Work
* description: An aggregation of works
* properties: primary memberOf
* scope: <http://bibfra.me/vocab/lite>

## primary
* label: primary work
* value: Work
* description: Primary work associated with a Collection
* scope: <http://bibfra.me/vocab/lite>

## memberOf
* label: member of
* value: Work
* description: Member of a Collection
* scope: <http://bibfra.me/vocab/lite>
