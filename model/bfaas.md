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

# <http://bibfra.me/vocab/lite/Person>
* properties: race

<!-- 
New bf lite + aas terms
-->

# SourceCard

* label: Source Card
* description: Card that documents the sources used to gather information about a person.
* properties: sourceOf
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sourceFor

* label: source of
* description: Source of information about a Person.
* synonyms: <http://bibfra.me/vocab/lite/related>
* remark: Used to connect Source Cards to people.
* properties: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## printer

* label: printer
* description: Person whose job or business is printing.
* value: Agent
* scope: <http://bibfra.me/vocab/aas>

## race

* label: race
* description: Fact or condition of belonging to a racial division or group; the qualities or characteristics associated with this.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## firm

* label: firm
* refines: <http://bibfra.me/vocab/lite/Organization>
* description: Organization whose job or business is printing.
* value: Organization
* scope: <http://bibfra.me/vocab/aas>
* note: THIS IS A PLACEHOLDER, USE <http://bibfra.me/vocab/lite/Organization> FOR NOW

## aasAuthorityId

* label: aas authority id
* description: American Antiquarian Society authority ID. 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## capturedDuring

* label: captured during
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedIn

* label: served in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## graduatedFrom

* label: graduated from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## presidentOf

* label: president of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## brotherOf

* label: brother of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## hangedFor

* label: hanged for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## marriedTo

* label: married to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sonOf

* label: son of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sisterOf

* label: sister of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## daughterOf

* label: daughter of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## arrestedFor

* label: arrested for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## removedTo

* label: removed to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## learnedTo

* label: learned to 
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## moved

* label: moved
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## residedIn

* label: resided in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## killed

* label: killed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## describedAs

* label: described as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## shipwrecked

* label: shipwrecked
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ransomedFrom

* label: ransomed from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## enslavedBy

* label: enslaved by
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## disappearedFrom

* label: disappeared from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedFor

* label: imprisoned for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedBy

* label: imprisoned by
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedOn

* label: served on
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## foughtIn

* label: fought in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## indebtedTo

* label: indebted to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## explored

* label: explored
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## shot

* label: shot
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## murdered

* label: murdered
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## hangedAt

* label: hanged at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## settledIn

* label: settled in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fatherOf

* label: father of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## nephewOf

* label: nephew of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedIn

* label: lived in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## retiredFrom

* label: retired from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## grandsonOf

* label: grandson of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedFor

* label: studied for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## baptised

* label: baptised
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## admittedTo

* label: admitted to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## retiredTo

* label: retired to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## workedFor

* label: worked for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## learned

* label: learned
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## formed

* label: formed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## joined

* label: joined
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## impressed

* label: impressed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## attended

* label: attended
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trainedAs

* label: trained as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedIn

* label: studied in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## founderOf

* label: founder of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## relativeOf

* label: relative of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## received

* label: received
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ordained

* label: ordained
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trusteeOf

* label: trustee of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## purchased

* label: purchased
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## bought

* label: bought
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## committedTo

* label: committed to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## banishedFrom

* label: banished from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studied

* label: 
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## left

* label: left
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## changed

* label: changed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## interestedIn

* label: interested in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## promotedTo

* label: promoted to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## convertedTo

* label: converted to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## leaderOf

* label: leader of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## halfBrotherOf

* label: half brother of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## uncleOf

* label: uncle of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## owned

* label: owned
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## adoptedBy

* label: adopted by
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## brotherInLawOf

* label: brother-in-law of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## visited

* label: visited
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## cameTo

* label: came to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## became

* label: became
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## buried

* label: buried
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## at

* label: at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## committedSuicide

* label: committed suicide
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## advertisedIn

* label: advertised in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## onASeaVoyage

* label: on a sea voyage
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## organized

* label: organized
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## licensed to preach

* label: 
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedAt

* label: studied at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## returned

* label: returned
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## rented

* label: rented
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## opened

* label: opened
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedAt

* label: educated at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travelledIn

* label: travelled in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## usedPseudynom

* label: used pseudynom
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## connectedTo

* label: connected to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## assistantTo

* label: assistant to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## unmarried

* label: unmarried
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## from

* label: from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## elderOf

* label: elder of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## cameFrom

* label: came from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedFor

* label: educated for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedAs

* label: served as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## associatedWith

* label: associated with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## lostAtSea

* label: lost at sea
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## stewardOf

* label: steward of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## namedFor

* label: named for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## returnedTo

* label: returned to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedWith

* label: studied with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## partnersWith

* label: partners with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## widowOf

* label: widow of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## halfSisterOf

* label: half sister of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## in 

* label: in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## filedFor

* label: filed for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## agentOf

* label: agent of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedNear

* label: lived near
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## built

* label: built
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## workedIn

* label: worked in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## established

* label: established
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedOn

* label: lived on
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## triedFor

* label: tried for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fledTo

* label: fled to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## activeIn

* label: active in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## proscribed

* label: proscribed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ranFor

* label: ran for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## wentTo

* label: went to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## friendsWith

* label: friends with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## prosecutedFor

* label: prosecuted for
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travelledWith

* label: travelled with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travellingCompanionOf

* label: travelling companion of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## enlistedIn

* label: enlisted in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## capturedBy

* label: captured by
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## issued

* label: issued
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## broughtTo

* label: brought to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## greatGrandsonOf

* label: great grandson of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## author

* label: author
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livingIn

* label: living in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## movedTo

* label: moved to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## subscriber

* label: subscriber
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedAt

* label: lived at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedAs

* label: educated as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## operated

* label: operated
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## oneOf

* label: one of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## inCommandOf

* label: in command of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## knownAs

* label: known as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## renounced

* label: renounced
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trainedIn

* label: trained in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedIn

* label: imprisoned in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## exiled

* label: exiled
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fatherOf

* label: father of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sent

* label: sent
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sailed

* label: sailed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travellingAbroad

* label: travelling abroad
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## bankrupt

* label: bankrupt
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## landedAt

* label: landed at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## wentInto

* label: went into
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## went

* label: went
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## jailed

* label: jailed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## taken

* label: taken
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## takenTo

* label: taken to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## inADuelWith

* label: in a duel with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## motherOf

* label: motherOf
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## confirmed

* label: confirmed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## entered

* label: entered
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## drownedIn

* label: drowned in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## missingIn

* label: missing in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## was

* label: was
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## raised

* label: raised
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## kept

* label: kept
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## released

* label: released
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## buriedIn

* label: buried in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## christened

* label: christened
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## admittedAs

* label: admitted as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## killedIn

* label: killed in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sentencedTo

* label: sentenced to 
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## pardoned

* label: pardoned
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## married

* label: married
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## published

* label: published
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## escapedFrom

* label: escaped from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## with

* label: with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## triedTo

* label: tried to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## resigned

* label: resigned
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sold

* label: sold
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## divorcedFrom

* label: divorced from
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## had

* label: had
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## supported

* label: supported
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## voyaged

* label: voyaged
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## connectedWith

* label: connected with
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travelling

* label: travelling
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## residentOf

* label: resident of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## appearedIn

* label: appeared in
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## underConfinementAs

* label: under confinement as
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## bequeathed

* label: bequeathed
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## deeded

* label: deeded
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## proprietor

* label: proprietor
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## grandfatherOf

* label: grandfather of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## entertained

* label: entertained
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## patronOf

* label: patron of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## gave

* label: gave
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## vicePresidentOf

* label: vice president of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## delegate

* label: delegate
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## layReader

* label: lay reader
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## espoused

* label: espoused
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sentTo

* label: sent to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedBy

* label: educated by
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sonInLawOf

* label: son in law of
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## expelledFrom

* label: expelled from 
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## emigrated

* label: emigrated
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## becameA

* label: became a
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## made

* label: made
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## placedAt

* label: placed at
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## played

* label: played
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## insured

* label: insured
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## invented

* label: invented
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## born

* label: born
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## engagedTo

* label: engaged to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## removedTo

* label: removed to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livingOn

* label: living on
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## electedTo

* label: elected to
* description: 
* synonyms: <http://bibfra.me/vocab/lite/related>
* value: Literal
* scope: <http://bibfra.me/vocab/aas>
