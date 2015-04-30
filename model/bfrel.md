<!---

BIBFRAME RELATION is a starting point for customized MARC Relator vocabularies using
the BIBFRAME model and profiles.  It builds off of the BIBFRAME Lite
vocabulary. It is framework conformant to BIBFRAME (and in theory MARC)
and where possible, link-compatible with the US Library of Congress's
BIBFRAME vocabulary, http://bibframe.org/

BIBFRAME RELATION is expressed using the Versa data model, which also
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

You'll notice that BIBFRAME RELATION terms use a humpCase/HumpCase convention,
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
    * @base: http://bibfra.me/vocab/relation/
    * @property: http://bibfra.me/purl/versa/support
* title: BIBFRAME RELATION vocabulary
* @interpretations:
    * scope: @resource

<!--- 
Work to Work relationships 
-->

## continues
* label: continues
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/continues>
* description: Work that is continued by the content of a later work under a new title.
* scope: <http://bibfra.me/vocab/relation>

## continuesInPart
* label: continues in part
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/continuesInPart>
* description: Work that split into two or more separate works with new titles.
* scope: <http://bibfra.me/vocab/relation>

## supersedes
* label: supersedes
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/supersedes>
* description: Earlier work whose content has been replaced by a later work, usually because the later work contains updated or new information.
* scope: <http://bibfra.me/vocab/relation>

## supersedesInPart
* label: supersedes in part
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/supersedesInPart>
* description: Earlier work whose content has been partially replaced by a later work, usually because the later work contains updated or new information.
* scope: <http://bibfra.me/vocab/relation>

## unionOf
* label: union of
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/unionOf>
* description: One of two or more works which came together to form a new work.
* scope: <http://bibfra.me/vocab/relation>

## absorbed
* label: absorbed
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/absorbed>
* description: Work that has been incorporated into another Work
* scope: <http://bibfra.me/vocab/relation>

## absorbedInPart
* label: absorbed in part
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/absorbedInPart>
* description: Work that has been partially incorporated into another work.
* scope: <http://bibfra.me/vocab/relation>

## separatedFrom
* label: separated from
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/separatedFrom>
* description: Work that spun off a part of its content to form a new work.
* scope: <http://bibfra.me/vocab/relation>

## continueBy
* label: continue by
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/continueBy>
* description: Work whose content continues an earlier work under a new title.
* scope: <http://bibfra.me/vocab/relation>

## continuedInPartBy
* label: continued in part by
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/continuedInPartBy>
* description: Work part of whose content separated from an earlier work to form a new work.
* scope: <http://bibfra.me/vocab/relation>

## supersededBy
* label: superseded by
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/supersededBy>
* description: Later Work used in place of an earlier work, usually because the later work contains updated or new information.
* scope: <http://bibfra.me/vocab/relation>

## supersededInPartBy
* label: superseded in part by
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/supersededInPartBy>
* description: Later Work used in part in place of an earlier work, usually because the later work contains updated or new information.
* scope: <http://bibfra.me/vocab/relation>

## absorbedBy
* label: absorbed by
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/absorbedBy>
* description: Work that incorporates another work.
* scope: <http://bibfra.me/vocab/relation>

## absorbed in part by
* label: absorbedInPartBy
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/absorbedInPartBy>
* description: Work that has been partially incorporated into another work.
* scope: <http://bibfra.me/vocab/relation>

## splitInto
* label: split into
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/splitInto>
* description: One of two or more works resulting from the division of an earlier work into separate works.
* scope: <http://bibfra.me/vocab/relation>

## mergedWith
* label: merged with
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/mergedToForm>
* description: One of two or more works that come together to form a new work.
* scope: <http://bibfra.me/vocab/relation>

## changedBackTo
* label: changed back to
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/>
* description: Work that has been changed back into another work.
* scope: <http://bibfra.me/vocab/relation>

## hasPart
* label: has part
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/hasPart>
* description: Resource that is included either physically or logically contained in the described resource
* scope: <http://bibfra.me/vocab/relation>

## isPartOf
* label: is part of
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/partOf>
* description: Resource in which the described resource is physically or logically contained.
* scope: <http://bibfra.me/vocab/relation>

## hasEquivalent
* label: equivalence
* refines: <http://bibfra.me/vocab/lite/related>
* description: Eembodies the same as the resource being described.
* synonyms: <http://bibframe.org/vocab/hasEquivalent>
* scope: <http://bibfra.me/vocab/relation>

## isDerivativeOf
* label: is derivative of
* description: Source resource is a modification of the target resource.
* refines: <http://bibfra.me/vocab/lite/related>
* synonyms: <http://bibframe.org/vocab/derivativeOf>
* scope: <http://bibfra.me/vocab/relation>

## hasDerivative
* label: has derivative
* refines: <http://bibfra.me/vocab/lite/related>
* description: Target resource is a modification of the source resource. 
* synonyms: <http://bibframe.org/vocab/hasDerivative>
* scope: <http://bibfra.me/vocab/relation>

## hasExpression
* label: has expression
* refines: <http://bibfra.me/vocab/lite/related>
* description: Resource has a related expression. 
* remark: For use to connect Works under FRBR/RDA rules.
* synonyms: <http://bibframe.org/vocab/hasExpression>
* scope: <http://bibfra.me/vocab/relation>

## isAdaptationOf
* label: is adaptation of
* refines: isDerivativeOf
* description: Source resource is an adaptation of the target resource. 
* synonyms: <http://schema.org/vocab/adaptationOf>
* scope: <http://bibfra.me/vocab/relation>

## hasAdaptation
* label: has adaptation
* refines: hasDerivative
* description: Trarget resource is an adaptation of the source resource. 
* scope: <http://bibfra.me/vocab/relation>

## isBasedOn
* label: is based on
* refines: isDerivativeOf
* description: Source resource is based on the target resource. 
* synonyms: <http://schema.org/vocab/basedOn>
* scope: <http://bibfra.me/vocab/relation>

## hasBasis
* label: has basis
* refines: hasDerivative
* description: Trarget resource is the basis of the source resource. 
* scope: <http://bibfra.me/vocab/relation>

## isTranslationOf
* label: is translation of
* refines: isDerivativeOf
* description: Work that has been translated, i.e., the text expressed in a language different from that of the original work.
* synonyms: <http://bibframe.org/vocab/translationOf>
* scope: <http://bibfra.me/vocab/relation>

## hasTranslation
* label: has translation
* refines: hasDerivative
* synonyms: <http://bibframe.org/vocab/translation> <http://schema.org/vocab/hasTranslation>
* description: Work that translates the text of the source entity into a language different from that of the original.
* scope: <http://bibfra.me/vocab/relation>

## isEditionOf
* label: is edition of
* refines: isDerivativeOf
* description: Source resource is a particular version of a target resource that has been revised or created.
* scope: <http://bibfra.me/vocab/relation>

## hasEdition
* label: has edition
* refines: hasDerivative
* synonyms: <http://bibframe.org/vocab/otherEdition>
* description: Target resource is a particular version of a source resource that has been revised or created.
* scope: <http://bibfra.me/vocab/relation>

<!--- 
MARC Relator Codes and Terms recast as properties
-->

## appraiser
* label:  appraiser
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## graphictechnician
* label: graphic technician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## abridger
* label: abridger
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: abr
* description: A person, family, or organization contributing to a resource by shortening or condensing the original work but leaving the nature and content of the original work substantially unchanged. For substantial modifications that result in the creation of a new work, see author

## actor
* label: actor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: act
* description: A performer contributing to an expression of a work by acting as a cast member or player in a musical or dramatic presentation, etc.

## adapter
* label: adapter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: adp
* description: A person or organization who 1) reworks a musical composition, usually for a different medium, or 2) rewrites novels or stories for motion pictures or other audiovisual medium.

## addressee
* label: addressee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rcp
* description: A person, family, or organization to whom the correspondence in a work is addressed

## analyst
* label: analyst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: anl
* description: A person or organization that reviews, examines and interprets data or information in a specific area

## animator
* label: animator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: anm
* description: A person contributing to a moving image work or computer program by giving apparent movement to inanimate objects or drawings. For the creator of the drawings that are animated, see artist

## annotator
* label: annotator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ann
* description: A person who makes manuscript annotations on an item

## appellant
* label: appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: apl
* description: A person or organization who appeals a lower court's decision

## appellee
* label: appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ape
* description: A person or organization against whom an appeal is taken

## applicant
* label: applicant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: app
* description: A  person or organization responsible for the submission of an application or who is named as eligible for the results of the processing of the application (e.g., bestowing of rights, reward, title, position)

## appraiser
* label: appraiser
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## architect
* label: architect
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: arc
* description: A person, family, or organization responsible for creating an architectural design, including a pictorial representation intended to show how a building, etc., will look when completed. It also oversees the construction of structures

## arranger
* label: arranger
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: arr
* description: A person, family, or organization contributing to a musical work by rewriting the composition for a medium of performance different from that for which the work was originally intended, or modifying the work for the same medium of performance, etc., such that the musical substance of the original composition remains essentially unchanged. For extensive modification that effectively results in the creation of a new musical work, see composer

## arrangerofmusic
* label: arranger of music
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## artcopyist
* label: art copyist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: acp
* description: A person (e.g., a painter or sculptor) who makes copies of works of visual art

## artdirector
* label: art director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: adi
* description: A person contributing to a motion picture or television production by overseeing the artists and craftspeople who build the sets

## artist
* label: artist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: art
* description: A person, family, or organization responsible for creating a work by conceiving, and implementing, an original graphic design, drawing, painting, etc. For book illustrators, prefer Illustrator [ill]

## artisticdirector
* label: artistic director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ard
* description: A person responsible for controlling the development of the artistic style of an entire production, including the choice of works to be presented and selection of senior production staff

## assignee
* label: assignee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: asg
* description: A person or organization to whom a license for printing or publishing has been transferred

## associatedname
* label: associated name
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: asn
* description: A person or organization associated with or found in an item or collection, which cannot be determined to be that of a Former owner [fmo] or other designated relationship indicative of provenance

## attributedname
* label: attributed name
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: att
* description: An author, artist, etc., relating him/her to a resource for which there is or once was substantial authority for designating that person as author, creator, etc. of the work

## auctioneer
* label: auctioneer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: auc
* description: A person or organization in charge of the estimation and public auctioning of goods, particularly books, artistic works, etc.

## author
* label: author
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aut
* description: A person, family, or organization responsible for creating a work that is primarily textual in content, regardless of media type (e.g., printed text, spoken word, electronic text, tactile text) or genre (e.g., poems, novels, screenplays, blogs). Use also for persons, etc., creating a new work by paraphrasing, rewriting, or adapting works by another creator such that the modification has substantially changed the nature and content of the original or changed the medium of expression

## authorinquotationsortextabstracts
* label: author in quotations or text abstracts
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aqt
* description: A person or organization whose work is largely quoted or extracted in works to which he or she did not contribute directly. Such quotations are found particularly in exhibition catalogs, collections of photographs, etc.

## authorofafterwordcolophonetc
* label: author of afterword, colophon, etc.
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aft
* description: A person or organization responsible for an afterword, postface, colophon, etc. but who is not the chief author of a work

## authorofdialog
* label: author of dialog
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aud
* description: A person or organization responsible for the dialog or spoken commentary for a screenplay or sound recording

## authorofintroductionetc
* label: author of introduction, etc.
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aui
* description: A person or organization responsible for an introduction, preface, foreword, or other critical introductory matter, but who is not the chief author

## authorofscreenplayetc
* label: author of screenplay, etc.
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## autographer
* label: autographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ato
* description: A person whose manuscript signature appears on an item

## bibliographicantecedent
* label: bibliographic antecedent
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ant
* description: A person or organization responsible for a resource upon which the resource represented by the bibliographic description is based. This may be appropriate for adaptations, sequels, continuations, indexes, etc.

## binder
* label: binder
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bnd
* description: A person who binds an item

## bindingdesigner
* label: binding designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bdd
* description: A person or organization responsible for the binding design of a book, including the type of binding, the type of materials used, and any decorative aspects of the binding

## blurbwriter
* label: blurb writer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: blw
* description: A person or organization responsible for writing a commendation or testimonial for a work, which appears on or within the publication itself, frequently on the back or dust jacket of print publications or on advertising material for all media

## bookdesigner
* label: book designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bkd
* description: A person or organization involved in manufacturing a manifestation by being responsible for the entire graphic design of a book, including arrangement of type and illustration, choice of materials, and process used

## bookproducer
* label: book producer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bkp
* description: A person or organization responsible for the production of books and other print media

## bookjacketdesigner
* label: bookjacket designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bjd
* description: A person or organization responsible for the design of flexible covers designed for or published with a book, including the type of materials used, and any decorative aspects of the bookjacket

## bookplatedesigner
* label: bookplate designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bpd
* description: A person or organization responsible for the design of a book owner's identification label that is most commonly pasted to the inside front cover of a book

## bookseller
* label: bookseller
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: bsl
* description: A person or organization who makes books and other bibliographic materials available for purchase. Interest in the materials is primarily lucrative

## bowdlerizer
* label: bowdlerizer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## brailleembosser
* label: braille embosser
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: brl
* description: A person, family, or organization involved in manufacturing a resource by embossing Braille cells using a stylus, special embossing printer, or other device

## broadcaster
* label: broadcaster
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: brd
* description: A person, family, or organization involved in broadcasting a resource to an audience via radio, television, webcast, etc.

## calligrapher
* label: calligrapher
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cll
* description: A person or organization who writes in an artistic hand, usually as a copyist and or engrosser

## cartographer
* label: cartographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ctg
* description: A person, family, or organization responsible for creating a map, atlas, globe, or other cartographic work

## caster
* label: caster
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cas
* description: A person, family, or organization involved in manufacturing a resource by pouring a liquid or molten substance into a mold and leaving it to solidify to take the shape of the mold

## censor
* label: censor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cns
* description: A person or organization who examines bibliographic resources for the purpose of suppressing parts deemed objectionable on moral, political, military, or other grounds

## chiefelectrician
* label: chief electrician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## choreographer
* label: choreographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: chr
* description: A person responsible for creating or contributing to a work of movement

## cinematographer
* label: cinematographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cng
* description: A person in charge of photographing a motion picture, who plans the technical aspets of lighting and photographing of scenes, and often assists the director in the choice of angles, camera setups, and lighting moods. He or she may also supervise the further processing of filmed material up to the completion of the work print. Cinematographer is also referred to as director of photography. Do not confuse with videographer

## client
* label: client
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cli
* description: A person or organization for whom another person or organization is acting

## collaborator
* label: collaborator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## collectionregistrar
* label: collection registrar
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cor
* description: A curator who lists or inventories the items in an aggregate work such as a collection of items or works

## collector
* label: collector
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: col
* description: A curator who brings together items from various sources that are then arranged, described, and cataloged as a collection. A collector is neither the creator of the material nor a person to whom manuscripts in the collection may have been addressed

## collotyper
* label: collotyper
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: clt
* description: A person, family, or organization involved in manufacturing a manifestation of photographic prints from film or other colloid that has ink-receptive and ink-repellent surfaces

## colorist
* label: colorist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: clr
* description: A person or organization responsible for applying color to drawings, prints, photographs, maps, moving images, etc

## commentator
* label: commentator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cmm
* description: A performer contributing to a work by providing interpretation, analysis, or a discussion of the subject matter on a recording, film, or other audiovisual medium

## commentatorforwrittentext
* label: commentator for written text
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cwt
* description: A person or organization responsible for the commentary or explanatory notes about a text. For the writer of manuscript annotations in a printed book, use Annotator

## compiler
* label: compiler
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: com
* description: A person, family, or organization responsible for creating a new work (e.g., a bibliography, a directory) through the act of compilation, e.g., selecting, arranging, aggregating, and editing data, information, etc

## complainant
* label: complainant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cpl
* description: A person or organization who applies to the courts for redress, usually in an equity proceeding

## complainant-appellant
* label: complainant-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cpt
* description: A complainant who takes an appeal from one court or jurisdiction to another to reverse the judgment, usually in an equity proceeding

## complainant-appellee
* label: complainant-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cpe
* description: A complainant against whom an appeal is taken from one court or jurisdiction to another to reverse the judgment, usually in an equity proceeding

## composer
* label: composer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cmp
* description: A person, family, or organization responsible for creating or contributing to a musical resource by adding music to a work that originally lacked it or supplements it

## compositor
* label: compositor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cmt
* description: A person or organization responsible for the creation of metal slug, or molds made of other materials, used to produce the text and images in printed matter

## conceptor
* label: conceptor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ccp
* description: A person or organization responsible for the original idea on which a work is based, this includes the scientific author of an audio-visual item and the conceptor of an advertisement

## conductor
* label: conductor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cnd
* description: A performer contributing to a musical resource by leading a performing group (orchestra, chorus, opera, etc.) in a musical or dramatic presentation, etc.

## conservator
* label: conservator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: con
* description: A person or organization responsible for documenting, preserving, or treating printed or manuscript material, works of art, artifacts, or other media

## consultant
* label: consultant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: csl
* description: A person or organization relevant to a resource, who is called upon for professional advice or services in a specialized field of knowledge or training

## consultanttoaproject
* label: consultant to a project
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: csp
* description: A person or organization relevant to a resource, who is engaged specifically to provide an intellectual overview of a strategic or operational task and by analysis, specification, or instruction, to create or propose a cost-effective course of action or solution

## contestant
* label: contestant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cos
* description: A person(s) or organization who opposes, resists, or disputes, in a court of law, a claim, decision, result, etc.

## contestant-appellant
* label: contestant-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cot
* description: A contestant who takes an appeal from one court of law or jurisdiction to another to reverse the judgment

## contestant-appellee
* label: contestant-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: coe
* description: A contestant against whom an appeal is taken from one court of law or jurisdiction to another to reverse the judgment

## contestee
* label: contestee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cts
* description: A person(s) or organization defending a claim, decision, result, etc. being opposed, resisted, or disputed in a court of law

## contestee-appellant
* label: contestee-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ctt
* description: A contestee who takes an appeal from one court or jurisdiction to another to reverse the judgment

## contestee-appellee
* label: contestee-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cte
* description: A contestee against whom an appeal is taken from one court or jurisdiction to another to reverse the judgment

## contractor
* label: contractor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ctr
* description: A person or organization relevant to a resource, who enters into a contract with another person or organization to perform a specific

## copier
* label: copier
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## copyrightclaimant
* label: copyright claimant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cpc
* description: A person or organization listed as a copyright owner at the time of registration. Copyright can be granted or later transferred to another person or organization, at which time the claimant becomes the copyright holder

## copyrightholder
* label: copyright holder
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cph
* description: A person or organization to whom copy and legal rights have been granted or transferred for the intellectual content of a work. The copyright holder, although not necessarily the creator of the work, usually has the exclusive right to benefit financially from the sale and use of the work to which the associated copyright protection applies

## corrector
* label: corrector
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: crr
* description: A person or organization who is a corrector of manuscripts, such as the scriptorium official who corrected the work of a scribe. For printed matter, use Proofreader

## correspondent
* label: correspondent
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: crp
* description: A person or organization who was either the writer or recipient of a letter or other communication

## costumedesigner
* label: costume designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cst
* description: A person, family, or organization that designs the costumes for a moving image production or for a musical or dramatic presentation or entertainment

## counterfeiter
* label: counterfeiter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## courtgoverned
* label: court governed
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cou
* description: A court governed by court rules, regardless of their official nature (e.g., laws, administrative regulations)

## courtreporter
* label: court reporter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: crt
* description: A person, family, or organization contributing to a resource by preparing a court's opinions for publication

## coverdesigner
* label: cover designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cov
* description: A person or organization responsible for the graphic design of a book cover, album cover, slipcase, box, container, etc. For a person or organization responsible for the graphic design of an entire book, use Book designer; for book jackets, use Bookjacket designer

## contributor
* label: contributor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ctb
* description: A person, family or organization responsible for making contributions to the resource. This includes those whose work has been contributed to a larger work, such as an anthology, serial publication, or other compilation of individual works. If a more specific role is available, prefer that, e.g. editor, compiler, illustrator

## creator
* label: creator
* refines: <http://bibfra.me/vocab/lite/creator>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cre
* description: A person or organization responsible for the intellectual or artistic content of a resource

## curator
* label: curator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: cur
* description: A person, family, or organization conceiving, aggregating, and/or organizing an exhibition, collection, or other item

## curatorofanexhibition
* label: curator of an exhibition
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## currentowner
* label: current owner
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dancer
* label: dancer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dnc
* description: A performer who dances in a musical, dramatic, etc., presentation

## datacontributor
* label: data contributor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dtc
* description: A person or organization that submits data for inclusion in a database or other collection of data

## datamanager
* label: data manager
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dtm
* description: A person or organization responsible for managing databases or other data sources

## dedicatee
* label: dedicatee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dte
* description: A person, family, or organization to whom a resource is dedicated

## dedicateeofitem
* label: dedicatee of item
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dedicator
* label: dedicator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dto
* description: A person who writes a dedication, which may be a formal statement or in epistolary or verse form

## defendant
* label: defendant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dfd
* description: A person or organization who is accused in a criminal proceeding or sued in a civil proceeding

## defendant-appellant
* label: defendant-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dft
* description: A defendant who takes an appeal from one court or jurisdiction to another to reverse the judgment, usually in a legal action

## defendant-appellee
* label: defendant-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dfe
* description: A defendant against whom an appeal is taken from one court or jurisdiction to another to reverse the judgment, usually in a legal action

## degreegrantinginstitution
* label: degree granting institution
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dgg
* description: A organization granting an academic degree

## degreegrantor
* label: degree grantor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## degreesupervisor
* label: degree supervisor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dgs
* description: A person overseeing a higher level academic degree

## delineator
* label: delineator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dln
* description: A person or organization executing technical drawings from others' designs

## depicted
* label: depicted
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dpc
* description: An entity depicted or portrayed in a work, particularly in a work of art

## deponent
* label: deponent
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## depositor
* label: depositor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dpt
* description: A current owner of an item who deposited the item into the custody of another person, family, or organization, while still retaining ownership

## designer
* label: designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dsr
* description: A person, family, or organization responsible for creating a design for an object

## designerofbinding
* label: designer of binding
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## designerofbook
* label: designer of book
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## designerofbookjacket
* label: designer of bookjacket
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## designerofcover
* label: designer of cover
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## designerofe-book
* label: designer of e-book
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## designeroftype
* label: designer of type
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## director
* label: director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: drt
* description: A person responsible for the general management and supervision of a filmed performance, a radio or television program, etc.

## directorofphotography
* label: director of photography
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dissertant
* label: dissertant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dis
* description: A person who presents a thesis for a university or higher-level educational degree

## distributionplace
* label: distribution place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dbp
* description: A place from which a resource, e.g., a serial, is distributed

## distributor
* label: distributor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dst
* description: A person or organization that has exclusive or shared marketing rights for a resource

## donor
* label: donor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dnr
* description: A former owner of an item who donated that item to another owner

## draftsman
* label: draftsman
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: drm
* description: A person, family, or organization contributing to a resource by an architect, inventor, etc., by making detailed plans or drawings for buildings, ships, aircraft, machines, objects, etc

## dubiousauthor
* label: dubious author
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: dub
* description: A person or organization to which authorship has been dubiously or incorrectly ascribed

## editor
* label: editor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: edt
* description: A person, family, or organization contributing to a resource by revising or elucidating the content, e.g., adding an introduction, notes, or other critical matter. An editor may also prepare a resource for production, publication, or distribution. For major revisions, adaptations, etc., that substantially change the nature and content of the original work, resulting in a new work, see author

## editorofcompilation
* label: editor of compilation
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: edc
* description: A person, family, or organization contributing to a collective or aggregate work by selecting and putting together works, or parts of works, by one or more creators. For compilations of data, information, etc., that result in new works, see compiler

## editorofmovingimagework
* label: editor of moving image work
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: edm
* description: A person, family, or organization responsible for assembling, arranging, and trimming film, video, or other moving image formats, including both visual and audio aspects

## electrician
* label: electrician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: elg
* description: A person responsible for setting up a lighting rig and focusing the lights for a production, and running the lighting at a performance

## electrotyper
* label: electrotyper
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: elt
* description: A person or organization who creates a duplicate printing surface by pressure molding and electrodepositing of metal that is then backed up with lead for printing

## enactingjurisdiction
* label: enacting jurisdiction
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: enj
* description: A jurisdiction enacting a law, regulation, constitution, court rule, etc.

## encoder
* label: encoder
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## engineer
* label: engineer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: eng
* description: A person or organization that is responsible for technical planning and design, particularly with construction

## engraver
* label: engraver
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: egr
* description: A person or organization who cuts letters, figures, etc. on a surface, such as a wooden or metal plate used for printing

## etcher
* label: etcher
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: etr
* description: A person or organization who produces text or images for printing by subjecting metal, glass, or some other surface to acid or the corrosive action of some other substance

## eventplace
* label: event place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: evp
* description: A place where an event such as a conference or a concert took place

## expert
* label: expert
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: exp
* description: A person or organization in charge of the description and appraisal of the value of goods, particularly rare items, works of art, etc.

## expurgator
* label: expurgator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## eyewitness
* label: eyewitness
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## facsimilist
* label: facsimilist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fac
* description: A person or organization that executed the facsimile

## fielddirector
* label: field director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fld
* description: A person or organization that manages or supervises the work done to collect raw data or do research in an actual setting or environment (typically applies to the natural and social sciences)

## filmdirector
* label: film director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fmd
* description: A director responsible for the general management and supervision of a filmed performance

## filmdistributor
* label: film distributor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fds
* description: A person, family, or organization involved in distributing a moving image resource to theatres or other distribution channels

## filmeditor
* label: film editor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: flm
* description: A person who, following the script and in creative cooperation with the Director, selects, arranges, and assembles the filmed material, controls the synchronization of picture and sound, and participates in other post-production tasks such as sound mixing and visual effects processing.  Today, picture editing is often performed digitally.

## filmproducer
* label: film producer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fmp
* description: A producer responsible for most of the business aspects of a film

## filmmaker
* label: filmmaker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fmk
* description: A person, family or organization responsible for creating an independent or personal film. A filmmaker is individually responsible for the conception and execution of all aspects of the film

## firstparty
* label: first party
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fpy
* description: A person or organization who is identified as the only party or the party of the first party. In the case of transfer of rights, this is the assignor, transferor, licensor, grantor, etc. Multiple parties can be named jointly as the first party

## forger
* label: forger
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: frg
* description: A person or organization who makes or imitates something of value or importance, especially with the intent to defraud

## formerowner
* label: former owner
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fmo
* description: A person, family, or organization formerly having legal possession of an item

## funder
* label: funder
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: fnd
* description: A person or organization that furnished financial support for the production of the work

## geographicinformationspecialist
* label: geographic information specialist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: gis
* description: A person responsible for geographic information system (GIS) development and integration with global positioning system data

## geospatialinformationspecialist
* label: geospatial information specialist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## graphictechnician
* label: graphic technician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## honoree
* label: honoree
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: hnr
* description: A person, family, or organization honored by a work or item (e.g., the honoree of a festschrift, a person to whom a copy is presented)

## honouree
* label: honouree
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: honoree

## honoureeofitem
* label: honouree of item
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## host
* label: host
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: hst
* description: A performer contributing to a resource by leading a program (often broadcast) that includes other guests, performers, etc. (e.g., talk show host)

## hostinstitution
* label: host institution
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: his
* description: An organization hosting the event, exhibit, conference, etc., which gave rise to a resource, but having little or no responsibility for the content of the resource

## supporting
* label: host, supporting
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## hosthouseelectrician
* label: house electrician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## illuminator
* label: illuminator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ilu
* description: A person providing decoration to a specific item using precious metals or color, often with elaborate designs and motifs

## illustrator
* label: illustrator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ill
* description: A person, family, or organization contributing to a resource by supplementing the primary content with drawings, diagrams, photographs, etc. If the work is primarily the artistic content created by this entity, use artist or photographer

## imprimatur
* label: imprimatur
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## inscriber
* label: inscriber
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ins
* description: A person who has written a statement of dedication or gift

## instructor
* label: instructor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## instrumentalist
* label: instrumentalist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: itr
* description: A performer contributing to a resource by playing a musical instrument

## interviewee
* label: interviewee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ive
* description: A person, family or organization responsible for creating or contributing to a resource by responding to an interviewer, usually a reporter, pollster, or some other information gathering agent

## interviewer
* label: interviewer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ivr
* description: A person, family, or organization responsible for creating or contributing to a resource by acting as an interviewer, reporter, pollster, or some other information gathering agent

## inventor
* label: inventor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: inv
* description: A person, family, or organization responsible for creating a new device or process

## issuingbody
* label: issuing body
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: isb
* description: A person, family or organization issuing a work, such as an official organ of the body

## jointauthor
* label: joint author
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## judge
* label: judge
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: jud
* description: A person who hears and decides on legal matters in court.

## jurisdictiongoverned
* label: jurisdiction governed
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: jug
* description: A jurisdiction governed by a law, regulation, etc., that was enacted by another jurisdiction

## labdirector
* label: lab director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## laboratory
* label: laboratory
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lbr
* description: An organization that provides scientific analyses of material samples

## laboratorydirector
* label: laboratory director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ldr
* description: A person or organization that manages or supervises work done in a controlled setting or environment

## landscapearchitect
* label: landscape architect
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lsa
* description: An architect responsible for creating landscape works. This work involves coordinating the arrangement of existing and proposed land features and structures

## lead
* label: lead
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: led
* description: A person or organization that takes primary responsibility for a particular activity or endeavor. May be combined with another relator term or code to show the greater importance this person or organization has regarding that particular role. If more than one relator is assigned to a heading, use the Lead relator only if it applies to all the relators

## lender
* label: lender
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: len
* description: A person or organization permitting the temporary use of a book, manuscript, etc., such as for photocopying or microfilming

## libelant
* label: libelant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lil
* description: A person or organization who files a libel in an ecclesiastical or admiralty case

## libelant-appellant
* label: libelant-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lit
* description: A libelant who takes an appeal from one ecclesiastical court or admiralty to another to reverse the judgment

## libelant-appellee
* label: libelant-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lie
* description: A libelant against whom an appeal is taken from one ecclesiastical court or admiralty to another to reverse the judgment

## libelee
* label: libelee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lel
* description: A person or organization against whom a libel has been filed in an ecclesiastical court or admiralty

## libelee-appellant
* label: libelee-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: let
* description: A libelee who takes an appeal from one ecclesiastical court or admiralty to another to reverse the judgment

## libelee-appellee
* label: libelee-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lee
* description: A libelee against whom an appeal is taken from one ecclesiastical court or admiralty to another to reverse the judgment

## librettist
* label: librettist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lbt
* description: An author of a libretto of an opera or other stage work, or an oratorio

## licensee
* label: licensee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lse
* description: A person or organization who is an original recipient of the right to print or publish

## licensor
* label: licensor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lso
* description: A person or organization who is a signer of the license, imprimatur, etc

## lightingdesigner
* label: lighting designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lgd
* description: A person or organization who designs the lighting scheme for a theatrical presentation, entertainment, motion picture, etc.

## lithographer
* label: lithographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ltg
* description: A person or organization who prepares the stone or plate for lithographic printing, including a graphic artist creating a design directly on the surface from which printing will be done.

## lyricist
* label: lyricist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: lyr
* description: An author of the words of a non-dramatic musical work (e.g. the text of a song), except for oratorios

## manufactureplace
* label: manufacture place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mfp
* description: The place of manufacture (e.g., printing, duplicating, casting, etc.) of a resource in a published form

## manufacturer
* label: manufacturer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mfr
* description: A person or organization responsible for printing, duplicating, casting, etc. a resource

## marbler
* label: marbler
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mrb
* description: The entity responsible for marbling paper, cloth, leather, etc. used in construction of a resource

## markupeditor
* label: markup editor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mrk
* description: A person or organization performing the coding of SGML, HTML, or XML markup of metadata, text, etc.

## masterelectrician
* label: master electrician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## medium
* label: medium
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: med
* description: A person held to be a channel of communication between the earthly world and a world

## metadatacontact
* label: metadata contact
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mdc
* description: A person or organization primarily responsible for compiling and maintaining the original description of a metadata set (e.g., geospatial metadata set)

## metal-engraver
* label: metal-engraver
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mte
* description: An engraver responsible for decorations, illustrations, letters, etc. cut on a metal surface for printing or decoration

## minutetaker
* label: minute taker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mtk
* description: A person, family, or organization responsible for recording the minutes of a meeting

## moderator
* label: moderator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mod
* description: A performer contributing to a resource by leading a program (often broadcast) where topics are discussed, usually with participation of experts in fields related to the discussion

## monitor
* label: monitor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mon
* description: A person or organization that supervises compliance with the contract and is responsible for the report and controls its distribution. Sometimes referred to as the grantee, or controlling agency

## motionpictureeditor
* label: motion picture editor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## movingimageworkeditor
* label: moving image work editor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## musiccopyist
* label: music copyist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mcp
* description: A person who transcribes or copies musical notation

## musicaldirector
* label: musical director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: msd
* description: A person who coordinates the activities of the composer, the sound editor, and sound mixers for a moving image production or for a musical or dramatic presentation or entertainment

## musician
* label: musician
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: mus
* description: A person or organization who performs music or contributes to the musical content of a work when it is not possible or desirable to identify the function more precisely

## narrator
* label: narrator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: nrt
* description: A performer contributing to a resource by reading or speaking in order to give an account of an act, occurrence, course of events, etc

## observer
* label: observer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## onlooker
* label: onlooker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## onscreenpresenter
* label: onscreen presenter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: osp
* description: A performer contributing to an expression of a work by appearing on screen in nonfiction moving image materials or introductions to fiction moving image materials to provide contextual or background information. Use when another term (e.g., narrator, host) is either not applicable or not desired

## opponent
* label: opponent
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: opn
* description: A person or organization responsible for opposing a thesis or dissertation

## organizer
* label: organizer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: orm
* description: A person, family, or organization organizing the exhibit, event, conference, etc., which gave rise to a resource

## organizerofmeeting
* label: organizer of meeting
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## originator
* label: originator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: org
* description: A person or organization performing the work, i.e., the name of a person or organization associated with the intellectual content of the work. This category does not include the publisher or personal affiliation, or sponsor except where it is also the corporate author

## other
* label: other
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: oth
* description: A role that has no equivalent in the MARC list.

## owner
* label: owner
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: own
* description: A person, family, or organization that currently owns an item or collection, i.e.has legal possession of a resource

## panelist
* label: panelist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pan
* description: A performer contributing to a resource by participating in a program (often broadcast) where topics are discussed, usually with participation of experts in fields related to the discussion

## papermaker
* label: papermaker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ppm
* description: A person or organization responsible for the production of paper, usually from wood, cloth, or other fibrous material

## patentapplicant
* label: patent applicant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pta
* description: A person or organization that applied for a patent

## patentholder
* label: patent holder
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pth
* description: A person or organization that was granted the patent referred to by the item

## patentinventor
* label: patent inventor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## patentee
* label: patentee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## patron
* label: patron
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pat
* description: A person or organization responsible for commissioning a work. Usually a patron uses his or her means or influence to support the work of artists, writers, etc. This includes those who commission and pay for individual works

## performer
* label: performer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prf
* description: A person contributing to a resource by performing music, acting, dancing, speaking, etc., often in a musical or dramatic presentation, etc. If specific codes are used, [prf] is used for a person whose principal skill is not known or specified

## performerofresearch
* label: performer of research
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## permittingagency
* label: permitting agency
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pma
* description: An organization (usually a government agency) that issues permits under which work is accomplished

## photographer
* label: photographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pht
* description: A person, family, or organization responsible for creating a photographic work

## plaintiff
* label: plaintiff
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ptf
* description: A person or organization who brings a suit in a civil proceeding

## plaintiff-appellant
* label: plaintiff-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ptt
* description: A plaintiff who takes an appeal from one court or jurisdiction to another to reverse the judgment, usually in a legal proceeding

## plaintiff-appellee
* label: plaintiff-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pte
* description: A plaintiff against whom an appeal is taken from one court or jurisdiction to another to reverse the judgment, usually in a legal proceeding

## platemaker
* label: platemaker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: plt
* description: A person, family, or organization involved in manufacturing a manifestation by preparing plates used in the production of printed images and/or text

## printerof
* label: plates, printer of
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## platespraeses
* label: praeses
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pra
* description: A person who is the faculty moderator of an academic disputation, normally proposing a thesis and participating in the ensuing disputation

## presenter
* label: presenter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pre
* description: A person or organization mentioned in an “X presents” credit for moving image materials and who is associated with production, finance, or distribution in some way.  A vanity credit;  in early years, normally the head of a studio

## preservationist
* label: preservationist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## printer
* label: printer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prt
* description: A person, family, or organization involved in manufacturing a manifestation of printed text, notated music, etc., from type or plates, such as a book, newspaper, magazine, broadside, score, etc

## printerofplates
* label: printer of plates
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pop
* description: A person or organization who prints illustrations from plates.

## printmaker
* label: printmaker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prm
* description: A person or organization who makes a relief, intaglio, or planographic printing surface

## processcontact
* label: process contact
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prc
* description: A person or organization primarily responsible for performing or initiating a process, such as is done with the collection of metadata sets

## producer
* label: producer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pro
* description: A person, family, or organization responsible for most of the business aspects of a production for screen, audio recording, television, webcast, etc. The producer is generally responsible for fund raising, managing the production, hiring key personnel, arranging for distributors, etc.

## producerofbook
* label: producer of book
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## productioncompany
* label: production company
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prn
* description: An organization that is responsible for financial, technical, and organizational management of a production for stage, screen, audio recording, television, webcast, etc.

## productiondesigner
* label: production designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prs
* description: A person or organization responsible for designing the overall visual appearance of a moving image production

## productionmanager
* label: production manager
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pmn
* description: A person responsible for all technical and business matters in a production

## productionpersonnel
* label: production personnel
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prd
* description: A person or organization associated with the production (props, lighting, special effects, etc.) of a musical or dramatic presentation or entertainment

## productionplace
* label: production place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prp
* description: The place of production (e.g., inscription, fabrication, construction, etc.) of a resource in an unpublished form

## programmer
* label: programmer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prg
* description: A person, family, or organization responsible for creating a computer program

## projectdirector
* label: project director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pdr
* description: A person or organization with primary responsibility for all essential aspects of a project, has overall responsibility for managing projects, or provides overall direction to a project manager

## promoter
* label: promoter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## proofreader
* label: proofreader
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pfr
* description: A person who corrects printed matter. For manuscripts, use Corrector [crr]

## provider
* label: provider
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: prv
* description: A person or organization who produces, publishes, manufactures, or distributes a resource if specific codes are not desired (e.g. [mfr], [pbl])

## publicationplace
* label: publication place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pup
* description: The place where a resource is published

## publisher
* label: publisher
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pbl
* description: A person or organization responsible for publishing, releasing, or issuing a resource

## publishingdirector
* label: publishing director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: pbd
* description: A person or organization who presides over the elaboration of a collective work to ensure its coherence or continuity. This includes editors-in-chief, literary editors, editors of series, etc.

## puppeteer
* label: puppeteer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ppt
* description: A performer contributing to a resource by manipulating, controlling, or directing puppets or marionettes in a moving image production or a musical or dramatic presentation or entertainment

## radiodirector
* label: radio director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rdd
* description: A director responsible for the general management and supervision of a radio program

## radioproducer
* label: radio producer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rpc
* description: A producer responsible for most of the business aspects of a radio program

## recipient
* label: recipient
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## recordingengineer
* label: recording engineer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rce
* description: A person contributing to a resource by supervising the technical aspects of a sound or video recording session

## recordist
* label: recordist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rcd
* description: A person or organization who uses a recording device to capture sounds and/or video during a recording session, including field recordings of natural sounds, folkloric events, music, etc.

## redaktor
* label: redaktor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: red
* description: A person or organization who writes or develops the framework for an item without being intellectually responsible for its content

## renderer
* label: renderer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ren
* description: A person or organization who prepares drawings of architectural designs (i.e., renderings) in accurate, representational perspective to show what the project will look like when completed

## reporter
* label: reporter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rpt
* description: A person or organization who writes or presents reports of news or current events on air or in print

## repository
* label: repository
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rps
* description: An organization that hosts data or material culture objects and provides services to promote long term, consistent and shared use of those data or objects

## researchteamhead
* label: research team head
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rth
* description: A person who directed or managed a research project

## researchteammember
* label: research team member
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rtm
* description: A person who participated in a research project but whose role did not involve direction or management of it

## researcher
* label: researcher
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: res
* description: A person or organization responsible for performing research

## respondent
* label: respondent
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rsp
* description: A person or organization who makes an answer to the courts pursuant to an application for redress (usually in an equity proceeding) or a candidate for a degree who defends or opposes a thesis provided by the praeses in an academic disputation

## respondent-appellant
* label: respondent-appellant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rst
* description: A respondent who takes an appeal from one court or jurisdiction to another to reverse the judgment, usually in an equity proceeding

## respondent-appellee
* label: respondent-appellee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rse
* description: A respondent against whom an appeal is taken from one court or jurisdiction to another to reverse the judgment, usually in an equity proceeding

## responsibleparty
* label: responsible party
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rpy
* description: A person or organization legally responsible for the content of the published material

## restager
* label: restager
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rsg
* description: A person or organization, other than the original choreographer or director, responsible for restaging a choreographic or dramatic work and who contributes minimal new content

## restorationist
* label: restorationist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rsr
* description: A person, family, or organization responsible for the set of technical, editorial, and intellectual procedures aimed at compensating for the degradation of an item by bringing it back to a state as close as possible to its original condition

## reviewer
* label: reviewer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rev
* description: A person or organization responsible for the review of a book, motion picture, performance, etc.

## rubricator
* label: rubricator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: rbr
* description: A person or organization responsible for parts of a work, often headings or opening parts of a manuscript, that appear in a distinctive color, usually red

## scenarist
* label: scenarist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sce
* description: A person or organization who is the author of a motion picture screenplay, generally the person who wrote the scenarios for a motion picture during the silent era

## scientificadvisor
* label: scientific advisor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sad
* description: A person or organization who brings scientific, pedagogical, or historical competence to the conception and realization on a work, particularly in the case of audio-visual items

## screenwriter
* label: screenwriter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: aus
* description: An author of a screenplay, script, or scene

## scribe
* label: scribe
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: scr
* description: A person who is an amanuensis and for a writer of manuscripts proper. For a person who makes pen-facsimiles, use Facsimilist [fac]

## sculptor
* label: sculptor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: scl
* description: An artist responsible for creating a three-dimensional work by modeling, carving, or similar technique

## secondparty
* label: second party
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: spy
* description: A person or organization who is identified as the party of the second part. In the case of transfer of right, this is the assignee, transferee, licensee, grantee, etc. Multiple parties can be named jointly as the second party

## secretary
* label: secretary
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sec
* description: A person or organization who is a recorder, redactor, or other person responsible for expressing the views of a organization

## seller
* label: seller
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sll
* description: A former owner of an item who sold that item to another owner

## setdesigner
* label: set designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: std
* description: A person who translates the rough sketches of the art director into actual architectural structures for a theatrical presentation, entertainment, motion picture, etc. Set designers draw the detailed guides and specifications for building the set

## setting
* label: setting
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: stg
* description: An entity in which the activity or plot of a work takes place, e.g. a geographic place, a time period, a building, an event

## signer
* label: signer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sgn
* description: A person whose signature appears without a presentation or other statement indicative of provenance. When there is a presentation statement, use Inscriber [ins].

## singer
* label: singer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sng
* description: A performer contributing to a resource by using his/her/their voice, with or without instrumental accompaniment, to produce music. A singer's performance may or may not include actual words

## sounddesigner
* label: sound designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sds
* description: A person who produces and reproduces the sound score (both live and recorded), the installation of microphones, the setting of sound levels, and the coordination of sources of sound for a production

## speaker
* label: speaker
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: spk
* description: A performer contributing to a resource by speaking words, such as a lecture, speech, etc. 

## sponsor
* label: sponsor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: spn
* description: A person, family, or organization sponsoring some aspect of a resource, e.g., funding research, sponsoring an event

## sponsoringbody
* label: sponsoring body
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## stagedirector
* label: stage director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sgd
* description: A person or organization contributing to a stage resource through the overall management and supervision of a performance

## stagemanager
* label: stage manager
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: stm
* description: A person who is in charge of everything that occurs on a performance stage, and who acts as chief of all crews and assistant to a director during rehearsals

## standardsbody
* label: standards body
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: stn
* description: An organization responsible for the development or enforcement of a standard

## stereotyper
* label: stereotyper
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: str
* description: A person or organization who creates a new plate for printing by molding or copying another printing surface

## storyteller
* label: storyteller
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: stl
* description: A performer contributing to a resource by relaying a creator's original story with dramatic or theatrical interpretation

## supportinghost
* label: supporting host
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: sht
* description: A person or organization that supports (by allocating facilities, staff, or other resources) a project, program, meeting, event, data objects, material culture objects, or other entities capable of support

## supposedname
* label: supposed name
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## surveyor
* label: surveyor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: srv
* description: A person, family, or organization contributing to a cartographic resource by providing measurements or dimensional relationships for the geographic area represented

## teacher
* label: teacher
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tch
* description: A performer contributing to a resource by giving instruction or providing a demonstration

## technicaldirector
* label: technical director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tcd
* description: A person who is ultimately in charge of scenery, props, lights and sound for a production

## technicaldraftsman
* label: technical draftsman
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## televisiondirector
* label: television director
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tld
* description: A director responsible for the general management and supervision of a television program

## televisionproducer
* label: television producer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tlp
* description: A producer responsible for most of the business aspects of a television program

## testifier
* label: testifier
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## thesisadvisor
* label: thesis advisor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: ths
* description: A person under whose supervision a degree candidate develops and presents a thesis, mémoire, or text of a dissertation

## transcriber
* label: transcriber
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: trc
* description: A person, family, or organization contributing to a resource by changing it from one system of notation to another. For a work transcribed for a different instrument or performing group, see Arranger [arr]. For makers of pen-facsimiles, use Facsimilist [fac]

## translator
* label: translator
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: trl
* description: A person or organization who renders a text from one language into another, or from an older form of a language into the modern form

## typedesigner
* label: type designer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tyd
* description: A person or organization who designs the type face used in a particular item

## typesetter
* label: typesetter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## typographer
* label: typographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: tyg
* description: A person or organization primarily responsible for choice and arrangement of type used in an item. If the typographer is also responsible for other aspects of the graphic design of a book (e.g., Book designer [bkd]), codes for both functions may be needed

## universityplace
* label: university place
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: uvp
* description: A place where a university that is associated with a resource is located, for example, a university where an academic dissertation or thesis was presented

## videographer
* label: videographer
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: vdg
* description: A person in charge of a video production, e.g. the video recording of a stage production as opposed to a commercial motion picture. The videographer may be the camera operator or may supervise one or more camera operators. Do not confuse with cinematographer

## vocalist
* label: vocalist
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## voiceactor
* label: voice ctor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: vac

## witness
* label: witness
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wit
* description: Use for a person who verifies the truthfulness of an event or action.

## woodengraver
* label: wood engraver
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wde
* description: A person or organization who makes prints by cutting the image in relief on the end-grain of a wood block

## woodcutter
* label: woodcutter
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wdc
* description: A person or organization who makes prints by cutting the image in relief on the plank side of a wood block

## writerofaccompanyingmaterial
* label: writer of accompanying material
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wam
* description: A person or organization who writes significant material which accompanies a sound recording or other audiovisual material

## writerofaddedcommentary
* label: writer of added commentary
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wac
* description: A person, family, or organization contributing to an expression of a work by providing an interpretation or critical explanation of the original work

## writerofaddedlyrics
* label: writer of added lyrics
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wal
* description: A writer of words added to an expression of a musical work. For lyric writing in collaboration with a composer to form an original work, see lyricist

## writerofaddedtext
* label: writer of added text
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wat
* description: A person, family, or organization contributing to a non-textual resource by providing text for the non-textual work (e.g., writing captions for photographs, descriptions of maps).

## writerofintroduction
* label: writer of introduction
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: win
* description: A person, family, or organization contributing to a resource by providing an introduction to the original work

## writerofpreface
* label: writer of preface
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wpr
* description: A person, family, or organization contributing to a resource by providing a preface to the original work

## writerofsupplementarytextualcontent
* label: writer of supplementary textual content
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>
* synonyms: wst
* description: A person, family, or organization contributing to a resource by providing supplementary textual content (e.g., an introduction, a preface) to the original work

## abr
* label: abr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## act
* label: act
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## adp
* label: adp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rcp
* label: rcp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## anl
* label: anl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## anm
* label: anm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ann
* label: ann
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## apl
* label: apl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ape
* label: ape
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## app
* label: app
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## arc
* label: arc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## arr
* label: arr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## acp
* label: acp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## adi
* label: adi
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## art
* label: art
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ard
* label: ard
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## asg
* label: asg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## asn
* label: asn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## att
* label: att
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## auc
* label: auc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aut
* label: aut
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aqt
* label: aqt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aft
* label: aft
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aud
* label: aud
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aui
* label: aui
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ato
* label: ato
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ant
* label: ant
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bnd
* label: bnd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bdd
* label: bdd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## blw
* label: blw
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bkd
* label: bkd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bkp
* label: bkp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bjd
* label: bjd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bpd
* label: bpd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## bsl
* label: bsl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## brl
* label: brl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## brd
* label: brd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cll
* label: cll
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ctg
* label: ctg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cas
* label: cas
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cns
* label: cns
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## chr
* label: chr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cng
* label: cng
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cli
* label: cli
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cor
* label: cor
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## col
* label: col
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## clt
* label: clt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## clr
* label: clr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cmm
* label: cmm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cwt
* label: cwt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## com
* label: com
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cpl
* label: cpl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cpt
* label: cpt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cpe
* label: cpe
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cmp
* label: cmp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cmt
* label: cmt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ccp
* label: ccp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cnd
* label: cnd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## con
* label: con
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## csl
* label: csl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## csp
* label: csp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cos
* label: cos
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cot
* label: cot
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## coe
* label: coe
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cts
* label: cts
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ctt
* label: ctt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cte
* label: cte
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ctr
* label: ctr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ctb
* label: ctb
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cpc
* label: cpc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cph
* label: cph
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## crr
* label: crr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## crp
* label: crp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cst
* label: cst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cou
* label: cou
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## crt
* label: crt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cov
* label: cov
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cre
* label: cre
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## cur
* label: cur
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dnc
* label: dnc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dtc
* label: dtc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dtm
* label: dtm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dte
* label: dte
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dto
* label: dto
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dfd
* label: dfd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dft
* label: dft
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dfe
* label: dfe
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dgg
* label: dgg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dgs
* label: dgs
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dln
* label: dln
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dpc
* label: dpc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dpt
* label: dpt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dsr
* label: dsr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## drt
* label: drt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dis
* label: dis
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dbp
* label: dbp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dst
* label: dst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dnr
* label: dnr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## drm
* label: drm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## dub
* label: dub
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## edt
* label: edt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## edc
* label: edc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## edm
* label: edm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## elg
* label: elg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## elt
* label: elt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## enj
* label: enj
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## eng
* label: eng
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## egr
* label: egr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## etr
* label: etr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## evp
* label: evp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## exp
* label: exp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fac
* label: fac
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fld
* label: fld
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fmd
* label: fmd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fds
* label: fds
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## flm
* label: flm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fmp
* label: fmp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fmk
* label: fmk
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fpy
* label: fpy
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## frg
* label: frg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fmo
* label: fmo
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## fnd
* label: fnd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## gis
* label: gis
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## hnr
* label: hnr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## hst
* label: hst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## his
* label: his
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ilu
* label: ilu
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ill
* label: ill
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ins
* label: ins
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## itr
* label: itr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ive
* label: ive
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ivr
* label: ivr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## inv
* label: inv
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## isb
* label: isb
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## jud
* label: jud
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## jug
* label: jug
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lbr
* label: lbr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ldr
* label: ldr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lsa
* label: lsa
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## led
* label: led
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## len
* label: len
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lil
* label: lil
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lit
* label: lit
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lie
* label: lie
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lel
* label: lel
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## let
* label: let
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lee
* label: lee
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lbt
* label: lbt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lse
* label: lse
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lso
* label: lso
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lgd
* label: lgd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ltg
* label: ltg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## lyr
* label: lyr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mfp
* label: mfp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mfr
* label: mfr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mrb
* label: mrb
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mrk
* label: mrk
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## med
* label: med
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mdc
* label: mdc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mte
* label: mte
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mtk
* label: mtk
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mod
* label: mod
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mon
* label: mon
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mcp
* label: mcp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## msd
* label: msd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## mus
* label: mus
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## nrt
* label: nrt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## osp
* label: osp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## opn
* label: opn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## orm
* label: orm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## org
* label: org
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## oth
* label: oth
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## own
* label: own
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pan
* label: pan
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ppm
* label: ppm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pta
* label: pta
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pth
* label: pth
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pat
* label: pat
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prf
* label: prf
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pma
* label: pma
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pht
* label: pht
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ptf
* label: ptf
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ptt
* label: ptt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pte
* label: pte
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## plt
* label: plt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pra
* label: pra
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pre
* label: pre
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prt
* label: prt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pop
* label: pop
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prm
* label: prm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prc
* label: prc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pro
* label: pro
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prn
* label: prn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prs
* label: prs
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pmn
* label: pmn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prd
* label: prd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prp
* label: prp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prg
* label: prg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pdr
* label: pdr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pfr
* label: pfr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## prv
* label: prv
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pup
* label: pup
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pbl
* label: pbl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## pbd
* label: pbd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ppt
* label: ppt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rdd
* label: rdd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rpc
* label: rpc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rce
* label: rce
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rcd
* label: rcd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## red
* label: red
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ren
* label: ren
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rpt
* label: rpt
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rps
* label: rps
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rth
* label: rth
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rtm
* label: rtm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## res
* label: res
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rsp
* label: rsp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rst
* label: rst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rse
* label: rse
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rpy
* label: rpy
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rsg
* label: rsg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rsr
* label: rsr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rev
* label: rev
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## rbr
* label: rbr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sce
* label: sce
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sad
* label: sad
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## aus
* label: aus
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## scr
* label: scr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## scl
* label: scl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## spy
* label: spy
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sec
* label: sec
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sll
* label: sll
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## std
* label: std
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## stg
* label: stg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sgn
* label: sgn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sng
* label: sng
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sds
* label: sds
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## spk
* label: spk
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## spn
* label: spn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sgd
* label: sgd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## stm
* label: stm
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## stn
* label: stn
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## str
* label: str
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## stl
* label: stl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## sht
* label: sht
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## srv
* label: srv
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tch
* label: tch
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tcd
* label: tcd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tld
* label: tld
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tlp
* label: tlp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## ths
* label: ths
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## trc
* label: trc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## trl
* label: trl
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tyd
* label: tyd
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## tyg
* label: tyg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## uvp
* label: uvp
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## vdg
* label: vdg
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## vac
* label: vac
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wit
* label: wit
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wde
* label: wde
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wdc
* label: wdc
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wam
* label: wam
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wac
* label: wac
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wal
* label: wal
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wat
* label: wat
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## win
* label: win
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wpr
* label: wpr
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

## wst
* label: wst
* refines: <http://bibfra.me/vocab/lite/contributor>
* scope: <http://bibfra.me/vocab/relation>

