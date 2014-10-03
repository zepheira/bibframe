<!--
BIBFRAME Lite is a starting point for customized BIBFRAME vocabularies and profiles.
It is framework conformant to BIBFRAME and link-compatible with the US Library of Congress's
BIBFRAME vocabulary, http://bibframe.org/

BIBFRAME Lite is expressed using the Versa data model, which also allows for full expression in RDF form.
This particular file is in the Versa Literate syntax, based on the Markdown format
<https://daringfireball.net/projects/markdown/basics>.

The convention for expressing data models in Versa Literate has each vocabulary item starting with a new header,
A level 1 header for resource classes and level 2 for properties.  Each has its ID as an IRI reference
(usually relative). Each is then described within its section's unordered list, given a "label" (display label),
"description" (also for explanatory display), possibly "synonyms" (one or more loose expression that the resource
can be considered a synonym for another). Resource classes may also have "properties" (space-separated list of
property IDs defined on the resource). Properties may also have "value" (textual description of the expected
value of the property, perhaps as a relationship to another resource, or as a data value).

You'll notice that BIBFRAME Lite terms use a humpCase/HumpCase convention, which derives from BIBFRAME legacy.

-->

# @docheader

<!--
@base is the default base IRI, used e.g. for resource headers. It would also be used for properties except that it is
overridden by @property-base

The meta-properties in this file are actually defined by the Versa data model to support interpretation by Versa modeling tools

@resource-base is another possible override, for resource headers, but not used here
-->

* @base: http://bibfra.me/vocab/
* @property-base: http://bibfra.me/purl/versa/support
* title: Lite version of BIBFRAME vocabulary

# Resource

* synonyms: http://bibframe.org/vocab/Resource http://schema.org/Thing
* label: Resource
* description: Conceptual Resource
* properties: label description image link

## property

* description: a relationship between two resources or a resource and literal data
* label: property

## label

* value: Literal
* label: label
* description: Label of the item

## description

* value: Literal
* label: description
* description: Short description of the item

## image

* value: IRI
* label: Image
* description: IRI of an image of the item

## link

* value: IRI
* label: Link
* description: IRI of the item

# Authority 

* label: Authority
* description: Authority Resource
* properties: authorityLink

## authorityLink

* label: Authority Link
* value: IRI
* remark: Link to an authority identifier (VIAF, LCNAF, ISNI, ORCID, etc.)

# Work

* label: Work
* refines: Resource
* description: Most generic kind of creative work, including bibliographic resources, movies, photographs, software programs, etc.
* properties: creator contributor title description subject note

## title

* label: Title
* description: Title of the Work.

## description

* label: Description
* description: Description of the Work.

## creator

* value: Agent 
* label: Creator
* description: Entity (or entities) primarily associated with the creation of the work.

## contributor

* value: Agent 
* label: Contributor
* description: Entity (or entities) associated with the creation of the work.

## subject

* label: Subject
* value: Authority

# Agent

* refines: Authority
* label: Agent

# Person

* refines: Agent
* label: Person

# Organization

* refines: Agent
* label: Organization

# Place

* refines: Authority
* label: Place
* description: Physical location

# Meeting

* refines: Authority
* label: Meeting
* description: Gathering of persons for a purpose.

# Topic 

* refines: Authority
* label: Topic
* description: Topic

# Family

* refines: Authority
* label: Family
* description: Family of people

# Instance

* refines: Resource
* label: Instance
* definition: Carrier or instantiation associated with a Conceptual Work
* properties: instanceOf provider note

## instantiates

* label: Instantiates
* value: Work

## provider

* value: ProviderEvent
* label: provider
* description: Provider associated with the carrier.

# ProviderEvent

* refines: Event
* label: Provider Event
* properties: providerAgent providerPlace providerDate providerNote

## providerAgent

* label: Provider Agent
* refines: who
* value: Agent

## providerPlace

* label: Provider Place
* refines: where
* value: Place

## providerDate

* label: Provider Date
* refines: when

## providerNote

* label: Provider Note
* refines: why

## note

* label: Note

# Event

* label: Event
* refines: Resource
* properties: who what where when why

## who

* label: Who

## what

* label: What

## where

* label: Where

## when

* label: When

## why

* label: Why

# Annotation

* label: Annotation
* refines: Resource
* description: Annotation, provides for loosely attached information about a resource
* properties: annotated annotator body target

## annotated

* label: Annotated
* description: Date of the annotation

## annotator

* label: Annotator
* value: Agent
* description: Agent associated with the annotation

## body

* label: Body
* value: Resource

## target

* label: Target
* value: Resource

