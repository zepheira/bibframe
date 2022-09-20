<!--

BIBFRAME Lite is a starting point for customized BIBFRAME vocabularies
and profiles.  It is framework conformant to BIBFRAME and
link-compatible with the US Library of Congress's BIBFRAME vocabulary,
http://id.loc.gov/ontologies/bibframe/

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

* synonyms: <http://schema.org/Thing>
* label: Resource
* description: Most generic Bibframe entity
* properties: label description image link rightsStatement controlCode related language date audience note authorityLink equivalent
* scope: <http://bibfra.me/vocab/lite>

## label

* synonyms: <http://schema.org/name> <http://www.w3.org/2000/01/rdf-schema#label>
* value: Literal
* label: label
* description: Text string representing the name of resource
* scope: <http://bibfra.me/vocab/lite>

## prefLabel

* synonyms: <http://www.w3.org/2004/02/skos/core#prefLabel>
* value: Literal
* label: preferred label
* refines: label
* description: Preferred human readable label of the resource
* scope: <http://bibfra.me/vocab/lite>

## description

* synonyms: <http://schema.org/description> <http://purl.org/dc/terms/description>
* refines: note
* label: description
* description: Description of the resource
* value: Literal
* remark: Description for example of bibliographic resources may include but is not limited to: an abstract, a table of contents, a graphical representation, or a free-text account of the resource.
* scope: <http://bibfra.me/vocab/lite>

## image

* synonyms: <http://schema.org/image>
* value: IRI
* label: image
* description: IRI that points to an image of the resource
* scope: <http://bibfra.me/vocab/lite>

## link

* synonyms: <http://schema.org/url>
* value: IRI
* label: link
* description: IRI of a resource
* scope: <http://bibfra.me/vocab/lite>

## rightsStatement

* label: rights statement
* synonyms: <http://purl.org/dc/terms/rights>
* value: Literal
* description: Rights statement associated with the origin resource
* scope: <http://bibfra.me/vocab/lite>

## controlCode

* label: control code
* value: Literal
* description: Alphanumeric string or indicator used to find and identify the resource
* remark: A non-IRI based identifier reflecting local or community coding practices
* scope: <http://bibfra.me/vocab/lite>

## related

* label: related
* synonyms: <http://purl.org/dc/terms/related>
* value: Resource
* description: Resource related to the origin resource
* scope: <http://bibfra.me/vocab/lite>

## language

* label: language
* synonyms: <http://id.loc.gov/ontologies/bibframe/language> <http://purl.org/dc/terms/language>
* value: LanguageCategory
* description: Language associated with the resource
* scope: <http://bibfra.me/vocab/lite>

# LanguageCategory
* synonyms: <http://id.loc.gov/ontologies/bibframe/Language>
* label: Language Category
* refines: Category
* description: List of languages
* remark: A controlled vocabulary.
* scope: <http://bibfra.me/vocab/lite>

# Temporal

* label: Temporal
* refines: Authority
* description: Used to denote context for the chronological continued progress of existence and events in the past, present, and future.
* scope: <http://bibfra.me/vocab/lite>

## date

* label: date
* synonyms: <http://id.loc.gov/ontologies/bibframe/date> <http://purl.org/dc/terms/date>
* description: Date associated with the resource
* refines: when
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateStart

* label: start date
* synonyms: <http://schema.org/startDate>
* description: Start date associated with the resource
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateEnd

* label: end date
* synonyms: <http://schema.org/endDate>
* description: End date associated with the resource
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateBirth

* label: birth date
* synonyms: <https://schema.org/birthDate>
* description: Birth date associated with the person
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## dateDeath

* label: death date
* synonyms: <https://schema.org/deathDate>
* description: Death date associated with the person
* value: Literal
* refines: date
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## audience

* label: audience
* value: Literal
* description: Class of user for which the content of a resource is intended, or for whom the content is considered suitable
* remark: A target audience can be formed of people of a certain age group, gender, marital status, etc.. Other groups, although not the main focus, may also be interested. The value of this property is intended to be a code list.
* scope: <http://bibfra.me/vocab/lite>

## note

* label: note
* value: Literal
* description: Additional descriptive information associated with the resource
* scope: <http://bibfra.me/vocab/lite>

# Authority

* label: Authority
* refines: Resource
* description: Credible, curated description of a person, place or thing
* properties: name nameAlternative
* scope: <http://bibfra.me/vocab/lite>

## name
* label: name
* value: Literal
* description: Name of an authority
* refines: label
* scope: <http://bibfra.me/vocab/lite>

## equivalent 
* synonyms: <http://schema.org/sameAs>
* label: equivalent
* value: IRI
* description: actionable IRI linking to a Real World Object. 
* refines: link
* scope: <http://bibfra.me/vocab/lite>

## authorityLink

* label: authority link
* value: IRI
* refines: link
* description: Actionable IRI linking to an authoritative controlled vocabulary
* remark: Example identifiers include VIAF, LCNAF, ISNI, ORCID, etc.
* scope: <http://bibfra.me/vocab/lite>

# Identifier

* label: Identifier
* synonyms: <http://id.loc.gov/ontologies/bibframe/Identifier>
* refines: Resource
* description: A string or number that identifies either a unique resource or class of resources.
* properties: name link
* scope: <http://bibfra.me/vocab/lite>
* remark: Example identifiers include ISBN, ISSN, and MESH.

# Item

* label: Item
* synonyms: <http://id.loc.gov/ontologies/bibframe/Item>
* refines: Resource
* description: An Item represents a specific, individual, material embodiment of a distinct intellectual or artistic creation. 
* properties: heldBy itemizes
* scope: <http://bibfra.me/vocab/lite>

## itemizes

* label: itemizes
* synonyms: <http://id.loc.gov/ontologies/bibframe/itemOf>
* description: Instance for which the described Item is an example
* value: Instance
* scope: <http://bibfra.me/vocab/lite>

## heldBy

* label: held by
* synonyms: <http://id.loc.gov/ontologies/bibframe/heldBy>
* value: Agent
* description: Agent holding the item or from which it is available.
* scope: <http://bibfra.me/vocab/lite>

# Library 

* label: Library
* synonyms: <http://schema.org/Library>
* refines: Organization
* description: Organization responsible for the care of a collection of literary, musical, artistic, or reference materials, such as books, manuscripts, recordings, or films
* scope: <http://bibfra.me/vocab/lite>

# Museum

* label: Museum
* synonyms: <http://schema.org/Library>
* refines: Organization
* description: Organization that holds artifacts and other objects of scientific, artistic, cultural, historical, or other importance
* scope: <http://bibfra.me/vocab/lite>

# Archive

* label: Archive
* synonyms: <https://schema.org/ArchiveOrganization>
* refines: Organization
* description: Organization responsible for the documents, photos, rare books, and artifacts selected for access and preservation
* scope: <http://bibfra.me/vocab/lite>

# Work

* label: Work
* synonyms: <http://id.loc.goc/ontologies/bibframe/Work>
* refines: Resource
* description: A distinct intellectual or artistic creation
* properties: creator contributor title subject genre
* scope: <http://bibfra.me/vocab/lite>

## title

* label: title
* synonyms: <http://purl.org/dc/terms/title>
* description: Title of the resource
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## titleAlternative

* label: title alternative
* refines: title
* description: Alternative title of the resource
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## creator

* label: creator
* synonyms: <http://schema.org/creator> <http://purl.org/dc/terms/creator>
* value: Agent
* refines: contributor
* description: Entity (or entities) responsible with the creation of the origin resource
* scope: <http://bibfra.me/vocab/lite>

## contributor

* label: contributor
* value: Agent
* synonyms: <http://schema.org/contributor> <http://purl.org/dc/terms/contributor>
* description: Entity (or entities) who contribute to the origin resource
* scope: <http://bibfra.me/vocab/lite>

## subject
* label: subject
* value: Concept
* synonyms: <http://id.loc.gov/ontologies/bibframe/subject> <http://purl.org/dc/terms/subject>
* description: Index term, subject term, subject heading, or descriptor, a term for information retrieval which captures the essence of the topic of a resource
* remark: The 'about-ness' of a work
* scope: <http://bibfra.me/vocab/lite>

## genre
* label: genre
* value: Form
* synonyms: <http://id.loc.gov/ontologies/bibframe/genreForm>
* description: Category of artistic composition characterized by similarities in form, style, or subject matter
* remark: The 'is-ness' of a work
* scope: <http://bibfra.me/vocab/lite>

# Agent
* label: Agent
* refines: Authority
* synonyms: <http://id.loc.gov/ontologies/bibframe/Agent> <http://xmlns.com/foaf/0.1/Agent>
* description: Entity (e.g. person, organization, etc.) associated with a resource
* properties: email placeAssociated placeResidence address
* scope: <http://bibfra.me/vocab/lite>

## email
* synonyms: <http://schema.org/email>
* label: e-mail address
* description: Address that identifies an email box to which email messages are delivered to an agent
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## placeAssociated
* label: associated place 
* description: The place associated with an agent. 
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## placeResidence
* label: place of residence 
* description: The agent's place of residence.
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## placeBirth
* label: place of birth
* description: The agent's place of birth.
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## placeDeath
* label: place of death 
* description: The agent's place of death.
* value: Place
* scope: <http://bibfra.me/vocab/lite>

# Person
* label: Person
* refines: Agent
* synonyms: <http://id.loc.gov/ontologies/bibframe/Person>
* description: Individual (alive, dead, undead, or fictional) in relation to a resource
* properties: dateBirth dateDeath placeBirth placeDeath gender givenName familyName nameAlternative gender
* scope: <http://bibfra.me/vocab/lite>

# Organization
* label: Organization
* refines: Agent
* synonyms: <http://id.loc.gov/ontologies/bibframe/Organization>
* description: Unit of people, e.g., an institution, an association, or corporate body
* properties: dateStart dateEnd subOrganization nameAlternative 
* scope: <http://bibfra.me/vocab/lite>

## subOrganization
* label: sub organization
* refines: related
* synonyms: <http://schema.org/subOrganization>
* description: A relationship between two organizations where the first includes the second, e.g., as a subsidiary.
* scope: <http://bibfra.me/vocab/lite>

# Meeting
* label: Meeting
* refines: Agent
* synonyms: <http://id.loc.gov/ontologies/bibframe/Meeting>
* description: Formal gathering of people for a particular purpose
* properties: dateStart dateEnd
* scope: <http://bibfra.me/vocab/lite>

# Family
* label: Family
* refines: Agent
* synonyms: <http://id.loc.gov/ontologies/bibframe/Family>
* description: Social unit related by birth, marriage, adoption, civil union, or similar relationship
* properties: dateStart dateEnd
* scope: <http://bibfra.me/vocab/lite>

# Place
* label: Place
* synonyms: <http://schema.org/Place>
* refines: Authority
* synonyms: <http://id.loc.gov/ontologies/bibframe/Place>
* description: Geographic location
* scope: <http://bibfra.me/vocab/lite>

# Category
* label: Category
* refines: Resource
* synonyms: <http://schema.org/Enumeration>
* description: List of things regarded as having particular shared characteristics
* remark: A controlled vocabulary.
* scope: <http://bibfra.me/vocab/lite>

# Topic
* label: Topic
* refines: Authority
* synonyms: <http://id.loc.gov/ontologies/bibframe/Topic>
* description: Subject term describing a general concept, event or object
* scope: <http://bibfra.me/vocab/lite>

# Form
* label: Form
* refines: Category
* description: Category or genre that describes what the resource is
* scope: <http://bibfra.me/vocab/lite>

# Concept
* label: Concept
* refines: Resource
* synonyms: <http://www.w3.org/2009/08/skos-reference/skos.html#Concept>
* description: Term describing the subject, aboutness, idea or notion of a resource
* properties: focus subFocus
* scope: <http://bibfra.me/vocab/lite>

# Instance
* refines: Resource
* label: Instance
* synonyms: <http://id.loc.gov/ontologies/bibframe/Instance>
* description: A material embodiment of a distinct intellectual or artistic creation. 
* properties: contributor title instantiates extent provider copyright dimensions format medium 
* scope: <http://bibfra.me/vocab/lite>

## instantiates
* synonyms: <http://id.loc.gov/ontologies/bibframe/instanceOf>
* label: instantiates
* description: Work the resource instantiates or manifests
* remark: For use to connect Instances to Works in the BIBFRAME structure.
* refines: related
* value: Work
* scope: <http://bibfra.me/vocab/lite>

## focus
* label: focus
* synonyms: <http://xmlns.com/foaf/0.1/focus>
* description: Underlying or focal entity associated with a concept
* remark: Often times the focus is the primary entity associated with a Concept.
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## subFocus
* label: subfocus
* description: Qualifier or modifer used to describe an additional underlying focal entity associated with a concept.
* remark: Often times subfocus entities follow the primary focus associated with a Concept.
* refines: focus
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## provider
* label: provider
* synonyms: <http://id.loc.gov/ontologies/bibframe/provisionActivity>
* value: ProviderEvent
* description: Provider associated with the carrier
* remark: Connection to details such as the place, name, and/or date information relating to the publication, printing, distribution, issue, release, or production of an Instance.
* scope: <http://bibfra.me/vocab/lite>

## copyright
* label: copyright
* value: CopyrightEvent
* description: Copyright event associated with the Instance
* scope: <http://bibfra.me/vocab/lite>

## format
* label: format
* synonyms: <http://id.loc.gov/ontologies/bibframe/carrier> <http://purl.org/dc/terms/format>
* description: File format or physical medium of an instance.
* value: IRI
* scope: <http://bibfra.me/vocab/lite>

## medium
* synonyms: <http://id.loc.gov/ontologies/bibframe/media>
* label: medium
* value: IRI
* description: Medium of the Instance
* scope: <http://bibfra.me/vocab/lite>

## extent

* synonyms: <http://id.loc.gov/ontologies/bibframe/extent>
* label: extent
* value: Literal
* description: Number of physical pages, volumes, cassettes, total playing time, etc., of of each type of unit
* scope: <http://bibfra.me/vocab/lite>

## dimensions

* synonyms: <http://id.loc.gov/ontologies/bibframe/dimensions>
* label: dimensions
* value: Literal
* description: Measurement of size
* scope: <http://bibfra.me/vocab/lite>

# ProviderEvent
* synonyms: <http://id.loc.gov/ontologies/bibframe/ProvisionActivity>
* label: Provider Event
* refines: Event
* description: Event associated with the publication, printing, distribution, issue, release or production of an Instance
* properties: providerAgent providerPlace providerDate providerNote
* scope: <http://bibfra.me/vocab/lite>

# CopyrightEvent

* refines: Event
* synonyms: <http://id.loc.gov/ontologies/bibframe/CopyrightRegistration>
* label: Copyright Event
* description: Copyright event associated with the intellectual property of an instance.
* properties: license copyrightAgent copyrightPlace copyrightDate copyrightNote
* scope: <http://bibfra.me/vocab/lite>

## license

* label: license
* synonyms: <http://creativecommons.org/ns#license>
* description: License associated with the rights event associated with a Work
* value: Resource
* scope: <http://bibfra.me/vocab/lite>

## copyrightAgent

* label: copyright agent
* synonyms:
* description: Agent associated with the copyright of an instance
* refines: who
* value: Agent
* scope: <http://bibfra.me/vocab/lite>

## copyrightPlace

* label: copyright place
* refines: where
* description: Place associated with the copyright of an instance
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## copyrightDate

* label: copyright date
* synonyms: <http://id.loc.gov/ontologies/bibframe/copyrightDate>
* description: Date associated with the copyright of an instance
* refines: date
* scope: <http://bibfra.me/vocab/lite>

## copyrightNote

* label: copyright note
* description: Note associated with the copyright of an instance
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## providerAgent

* label: provider agent
* description: Agent associated with the publication, printing, distribution, issue, release or production of an Instance
* refines: who
* value: Agent
* scope: <http://bibfra.me/vocab/lite>

## providerPlace

* label: provider place
* refines: where
* description: Place associated with the publication, printing, distribution, issue, release or production of an Instance
* value: Place
* scope: <http://bibfra.me/vocab/lite>

## providerDate

* label: provider date
* description: Date associated with the publication, printing, distribution, issue, release or production of an Instance
* refines: date
* scope: <http://bibfra.me/vocab/lite>

## providerNote

* label: provider note
* description: Note associated with the publication, printing, distribution, issue, release or production of an Instance
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

# Event

* label: Event
* synonyms: <http://id.loc.gov/ontologies/bibframe/Event> <http://schema.org/Event>
* refines: Resource
* properties: who what where when why
* description: Significant occurrence or happening
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
* remark: Recommended ISO 8601 date
* scope: <http://bibfra.me/vocab/lite>

## why

* label: why
* description: Concept associated with an Event
* value: Concept
* scope: <http://bibfra.me/vocab/lite>

# Annotation

* label: Annotation
* refines: Resource
* synonyms: <http://www.w3.org/ns/oa#Annotation>
* description: Annotation, provides for loosely attached information about a resource
* properties: body target source
* scope: <http://bibfra.me/vocab/lite>

## body

* synonyms: <http://www.w3.org/ns/oa#hasBody>
* label: body
* value: Literal
* description: Body of an annotation
* scope: <http://bibfra.me/vocab/lite>

## target

* synonyms: <http://www.w3.org/ns/oa#hasTarget>
* label: target
* value: Resource
* description: Target of an annotation
* scope: <http://bibfra.me/vocab/lite>

## source

* synonyms: <http://www.w3.org/ns/oa#hasSource>
* label: source
* value: Resource
* description: Source of an annotation
* scope: <http://bibfra.me/vocab/lite>

# Collection
* label: Collection
* synonyms: <http://id.loc.gov/ontologies/bibframe/Collection>
* refines: Work
* description: Aggregation or gathering of works
* remark: In the case of Archives, a collection reflects the body of archival materials relating to a person, family, or organization. Includes materials collected to focus on a particular topic, event, person, place, etc. 
* properties: primary memberOf
* scope: <http://bibfra.me/vocab/lite>

# Series
* label: Series
* refines: <http://bibfra.me/vocab/lite/Collection>
* description: Set of related resources, especially of a specified kind
* scope: <http://bibfra.me/vocab/lite>

# List
* label: List
* refines: <http://bibfra.me/vocab/lite/Collection>
* description: An ordered / unordered group of related resources
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

## isVersionOf

* label: is version of
* synonyms: <http://bibfra.me/vocab/isVersionOf>
* value: Work
* description: Work of which this is a version
* scope: <http://bibfra.me/vocab/lite>

<!-- 
New bf lite terms from American Antiquarian Society Project
-->

# PostalAddress

* label: Postal Address
* synonyms: <http://schema.org/postalAddress>
* description: A postal / mailing address
* properties: street city region country zipcode
* scope: <http://bibfra.me/vocab/lite>

## address 

* label: address
* synonyms: <http://schema.org/address>
* description: A physical address
* value: PostalAddress
* scope: <http://bibfra.me/vocab/lite>

## street

* label: street address
* synonyms: <http://schema.org/streetAddress>
* description: The street address
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## city

* label: locality
* synonyms: <http://schema.org/addressLocality>
* description: Incorporated municipality or city, usually governed by a mayor and a board of aldermen or councilmen.
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## region

* label: state
* synonyms: <http://schema.org/addressRegion>
* description: Type of polity, state, or region that is an organized political community living under a single system of government.
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## country

* label: country
* synonyms: <http://schema.org/addressCountry>
* description: Nation with its own government, occupying a particular territory.
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## zipcode

* label: zipcode
* synonyms: <http://schema.org/postalcode>
* description: The postal code
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## givenName

* label: given name
* description: First name of a Person, also known as forename.
* synonyms: <http://schema.org/givenName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## familyName

* label: family name
* description: Last name of a Person, also known as surname. 
* synonyms: <http://schema.org/familyName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## gender

* label: gender
* description: Gender of the person. While male (M) and female (F) may be used, other text strings are also acceptable for people who do not identify as a binary gender.
* synonyms: <http://schema.org/gender>
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

## nameAlternative

* label: alternative name
* description: Alias for a resource.
* synonyms: <http://schema.org/alternateName> <http://bibframe.org/vocab/lite/alternativeName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite>

