<!--

NOTE: Sample translation template for supporting localization of
Bibframe Lite vocabulary. Text between { } are intended for translation. "{" "}"
delimeters should be removed after translation.

-->

<!--

{ BIBFRAME Lite is a starting point for customized BIBFRAME vocabularies
and profiles.  It is framework conformant to BIBFRAME and
link-compatible with the US Library of Congress's BIBFRAME vocabulary, 
http://bibframe.org/ }

-->

# @docheader

* @iri:
    * @base: http://bibfra.me/vocab/lite/
    * @property: http://bibfra.me/purl/versa/support
* @language: { en }

# Resource

* label: { Resource }
* description: { Most generic Bibframe entity }

## label

* label: { label }
* description: { Text string representing the name of resource }

## prefLabel

* label: { preferred label }
* description: { Preferred human readable label of the resource }

## description

* label: { description }
* description: { Description of the resource }
* remark: { Description for example of bibliographic resources may include but is not limited to: an abstract, a table of contents, a graphical representation, or a free-text account of the resource. }

## image

* label: { image }
* description: { IRI that points to an image of the resource }

## link

* label: { link }
* description: { IRI of a resource }

## rightsStatement

* label: { rights statement }
* description: { Rights statement associated with the origin resource }

## controlCode

* label: { control code }
* description: { Alphanumeric string or indicator used to find and identify the resource }
* remark: { A non-IRI based identifier reflecting local or community coding practices }

## related

* label: { related }
* description: { Resource related to the origin resource }

## language

* label: { language }
* description: { Language associated with the resource }

# LanguageCategory

* label: { Language Category }
* description: { List of languages }
* remark: { A controlled vocabulary. }

# Temporal

* label: { Temporal }
* description: { Used to denote context for the chronological continued progress of existence and events in the past, present, and future. }

## date

* label: { date }
* description: { Date associated with the resource }
* remark: { Recommended ISO 8601 date }

## dateStart

* label: { start date }
* description: { Start date associated with the resource }
* remark: { Recommended ISO 8601 date }

## dateEnd

* label: { end date }
* description: { End date associated with the resource }
* remark: { Recommended ISO 8601 date }

## dateBirth

* label: { birth date }
* description: { Birth date associated with the person }
* remark: { Recommended ISO 8601 date }

## dateDeath

* label: { death date }
* description: { Death date associated with the person }
* remark: { Recommended ISO 8601 date }

## audience

* label: { audience }
* description: { Class of user for which the content of a resource is intended, or for whom the content is considered suitable }

## note

* label: { note }
* description: { Additional descriptive information associated with the resource }

# Authority

* label: { Authority }
* description: { Credible, curated description of a person, place or thing }

## name

* label: { name }
* description: { Name of an authority }

## nameAlternative

* label: { alternative name }
* description: { Alternative name of an authority }

## authorityLink

* label: { authority link }
* description: { Actionable IRI linking to an authoritative controlled vocabulary }
* remark: { Example identifiers include VIAF, LCNAF, ISNI, ORCID, etc. }

# Work

* label: { Work }
* description: { A distinct intellectual or artistic creation }

## title

* label: { title }
* description: { Title of the resource }

## titleAlternative

* label: { title alternative }
* description: { Alternative title of the resource }

## creator

* label: { creator }
* description: { Entity (or entities) responsible with the creation of the origin resource }

## contributor

* label: { contributor }
* description: { Entity (or entities) who contribute to the origin resource }

## subject

* label: { subject }
* description: { Index term, subject term, subject heading, or descriptor, a term for information retrieval which captures the essence of the topic of a resource }
* remark: { The 'about-ness' of a work }

## genre

* label: { genre }
* description: { Category of artistic composition characterized by similarities in form, style, or subject matter }
* remark: { The 'is-ness' of a work }

# Agent

* label: { Agent }
* description: { Entity (e.g. person, organization, etc.) associated with a resource }

## email

* label: { e-mail address }
* description: { Address that identifies an email box to which email messages are delivered to an agent }

# Person

* label: { Person }
* description: { Individual (alive, dead, undead, or fictional) in relation to a resource }

# Organization

* label: { Organization }
* description: { Unit of people, e.g., an institution, an association, or corporate body }

# Meeting

* label: { Meeting }
* description: { Formal gathering of people for a particular purpose }

# Family

* label: { Family }
* description: { Social unit related by birth, marriage, adoption, civil union, or similar relationship }

# Place

* label: { Place }
* description: { Geographic location }

# Category

* label: { Category }
* description: { List of things regarded as having particular shared characteristics }
* remark: { A controlled vocabulary. }

# Topic

* label: { Topic }
* description: { Subject term describing a general concept, event or object }

# Form

* label: { Form }
* description: { Category or genre that describes what the resource is }

# Concept

* label: { Concept }
* description: { Term describing the subject, aboutness, idea or notion of a resource }

# Instance

* label: { Instance }
* description: { Individual embodiment of a Work }

## instantiates

* label: { instantiates }
* description: { Work the resource instantiates or manifests }
* remark: { For use to connect Instances to Works in the BIBFRAME structure. }

## focus

* label: { focus }
* description: { Underlying or focal entity associated with a concept }
* remark: { Often times the focus is the primary entity associated with a Concept. }

## subFocus

* label: { subfocus }
* description: { Qualifier or modifer used to describe an additional underlying focal entity associated with a concept. }
* remark: { Often times subfocus entities follow the primary focus associated with a Concept. }

## provision

* label: { provision }
* description: { Provider associated with the carrier }
* remark: { Connection to details such as the place, name, and/or date information relating to the publication, printing, distribution, issue, release, or production of an Instance. }

## copyright

* label: { copyright }
* description: { Copyright event associated with the Instance }

## format

* label: { format }
* description: { File format or physical medium of an instance. }

## medium

* label: { medium }
* description: { Medium of the Instance }

## extent

* label: { extent }
* description: { Number of physical pages, volumes, cassettes, total playing time, etc., of of each type of unit }

## dimensions

* label: { dimensions }
* description: { Measurement of size }

# ProviderEvent

* label: { Provider Event }
* description: { Event associated with the publication, printing, distribution, issue, release or production of an Instance }

# CopyrightEvent

* label: { Copyright Event }
* description: { Copyright event associated with the intellectual property of an instance. }

## license

* label: { license }
* description: { License associated with the rights event associated with a Work }

## copyrightAgent

* label: { copyright agent }
* description: { Agent associated with the copyright of an instance }

## copyrightPlace

* label: { copyright place }
* description: { Place associated with the copyright of an instance }

## copyrightDate

* label: { provider date }
* description: { Date associated with the copyright of an instance }

## copyrightNote

* label: { copyright note }
* description: { Note associated with the copyright of an instance }

## providerAgent

* label: { provider agent }
* description: { Agent associated with the publication, printing, distribution, issue, release or production of an Instance }

## providerPlace

* label: { provider place }
* description: { Place associated with the publication, printing, distribution, issue, release or production of an Instance }

## providerDate

* label: { provider date }
* description: { Date associated with the publication, printing, distribution, issue, release or production of an Instance }

## providerNote

* label: { provider note }
* description: { Note associated with the publication, printing, distribution, issue, release or production of an Instance }

# Event

* label: { Event }
* description: { Significant occurrence or happening }

## who

* label: { who }
* description: { Person or thing related to an Event }

## what

* label: { what }
* description: { Resource related to an Event }

## where

* label: { where }
* description: { Place associated with an Event }

## when

* label: { when }
* description: { Date associated with an Event }
* remark: { Recommended ISO 8601 date }

## why

* label: { why }
* description: { Concept associated with an Event }

# Annotation

* label: { Annotation }
* description: { Annotation, provides for loosely attached information about a resource }

## annotator

* label: { annotator }
* description: { Agent associated with the annotation }

## body

* label: { body }
* description: { Body of an annotation }

## target

* label: { target }
* description: { Target of an annotation }

# Collection

* label: { Collection }
* description: { Aggregation or gathering of works }

## primary

* label: { primary work }
* description: { Primary work associated with a Collection }

## memberOf

* label: { member of }
* description: { Member of a Collection }

## isVersionOf

* label: { is version of }
* description: { Work of which this is a version }
