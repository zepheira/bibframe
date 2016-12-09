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
New bf lite terms from AAS Location data
-->

## city

* label: locality
* description: Incorporated municipality or city, usually governed by a mayor and a board of aldermen or councilmen.
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

## region

* label: state
* description: Type of polity, state, or region that is an organized political community living under a single system of government.
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

## country

* label: country
* description: Nation with its own government, occupying a particular territory.
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# givenName

* label: first name
* description: First name of a Person, also known as forename.
* synonyms: <http://schema.org/givenName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# familyName

* label: country
* description: Last name of a Person, also known as surname. 
* synonyms: <http://schema.org/familyName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# gender

* label: gender
* description: Gender of the person. While male (M) and female (F) may be used, other text strings are also acceptable for people who do not identify as a binary gender.
* synonyms: <http://schema.org/gender>
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# alternativeName

* label: alternative name
* description: Alias for a Person. 
* synonyms: <http://schema.org/alternateName>
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# alternativeFamilyName

* label: alternative last name
* description: Alias last name for a Person. 
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

# alternativeGivenName

* label: alternative given name
* description: Alias first name for a Person. 
* value: Literal
* scope: <http://bibfra.me/vocab/lite/>

<!-- 
Existing bf lite terms to be used for AAS data
-->
<http://bibfra.me/vocab/lite/dateStart>

<http://bibfra.me/vocab/lite/dateEnd>

<http://bibfra.me/vocab/lite/note>

<http://bibfra.me/vocab/lite/name>

<http://bibfra.me/vocab/lite/dateBirth>

<http://bibfra.me/vocab/lite/dateDeath>

<http://bibfra.me/vocab/lite/Organization>
* note: use for Firms

<http://bibfra.me/vocab/lite/title>
* note: use for Place of Publication

<http://bibfra.me/vocab/lite/date>
* note: use for Year of Publication

<http://bibfra.me/vocab/lite/authorityLink>

<http://bibfra.me/vocab/lite/related>

<http://bibfra.me/vocab/lite/memberOf>

<!-- 
Existing bf lite + marc terms to be used for AAS data
-->

<http://bibfra.me/vocab/marc/volume>

<http://bibfra.me/vocab/marc/issueNumber>

<http://bibfra.me/vocab/marc/lccn>

<http://bibfra.me/vocab/lite/image>

<!-- 
New bf lite + aas terms
-->

# SourceCard

* label: Source Card
* description: Card that documents the sources used to gather information about a person.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trade

* label: trade
* description: Skilled job, typically one requiring manual skills and special training.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## printer

* label: printer
* description: Person whose job or business is printing.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## race

* label: race
* description: Fact or condition of belonging to a racial division or group; the qualities or characteristics associated with this.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## Firm

* label: Firm
* refines: <http://bibfra.me/vocab/lite/Organization>
* description: Person whose job or business is printing.
* value: Literal
* scope: <http://bibfra.me/vocab/aas>
* note: THIS IS A PLACEHOLDER, USE <http://bibfra.me/vocab/lite/Organization> FOR NOW

## mwaBibId

* label: mwa bib id
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## oclcNumber

* label: oclc number
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## aasAuthorityId

* label: aas authority id
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## capturedDuring

* label: captured during
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedIn

* label: served in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## graduatedFrom

* label: graduated from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## presidentOf

* label: president of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## brotherOf

* label: brother of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## hangedFor

* label: hanged for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## marriedTo

* label: married to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sonOf

* label: son of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sisterOf

* label: sister of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## daughterOf

* label: daughter of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## arrestedFor

* label: arrested for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## removedTo

* label: removed to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## learnedTo

* label: learned to 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## moved

* label: moved
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## residedIn

* label: resided in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## killed

* label: 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## describedAs

* label: described as
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## shipwrecked

* label: shipwrecked
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ransomedFrom

* label: ransomed from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## enslavedBy

* label: enslaved by
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## disappearedFrom

* label: disappeared from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedFor

* label: imprisoned for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedBy

* label: imprisoned by
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedOn

* label: served on
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## foughtIn

* label: fought in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## indebtedTo

* label: indebted to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## explored

* label: explored
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## shot

* label: shot
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## murdered

* label: murdered
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## hangedAt

* label: hanged at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## settledIn

* label: settled in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fatherOf

* label: father of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## nephewOf

* label: nephew of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedIn

* label: lived in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## retiredFrom

* label: retired from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## grandsonOf

* label: grandson of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedFor

* label: studied for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## baptised

* label: baptised
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## admittedTo

* label: admitted to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## retiredTo

* label: retired to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## workedFor

* label: worked for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## learned

* label: learned
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## formed

* label: formed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## joined

* label: joined
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## impressed

* label: impressed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## attended

* label: attended
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trainedAs

* label: trained as
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedIn

* label: studied in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## founderOf

* label: founder of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## relativeOf

* label: relative of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## received

* label: received
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ordained

* label: ordained
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trusteeOf

* label: trustee of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## purchased

* label: purchased
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## bought

* label: bought
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## committedTo

* label: committed to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## banishedFrom

* label: banished from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studied

* label: 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## left

* label: left
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## changed

* label: changed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## interestedIn

* label: interested in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## promotedTo

* label: promoted to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## convertedTo

* label: converted to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## leaderOf

* label: leader of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## halfBrotherOf

* label: half brother of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## uncleOf

* label: uncle of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## owned

* label: owned
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## adoptedBy

* label: adopted by
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## brotherInLawOf

* label: brother-in-law of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## visited

* label: visited
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## cameTo

* label: came to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## became

* label: became
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## buried

* label: buried
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## at

* label: at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## committedSuicide

* label: committed suicide
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## advertisedIn

* label: advertised in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## onASeaVoyage

* label: on a sea voyage
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## organized

* label: organized
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## licensed to preach

* label: 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedAt

* label: studied at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## returned

* label: returned
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## rented

* label: rented
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## opened

* label: opened
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedAt

* label: educated at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travelledIn

* label: travelled in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## usedPseudynom

* label: used pseudynom
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## connectedTo

* label: connected to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## assistantTo

* label: assistant to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## unmarried

* label: unmarried
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## from

* label: from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## elderOf

* label: elder of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## cameFrom

* label: came from
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedFor

* label: educated for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## servedAs

* label: served as
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## associatedWith

* label: associated with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## lostAtSea

* label: lost at sea
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## stewardOf

* label: steward of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## namedFor

* label: named for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## returnedTo

* label: returned to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## studiedWith

* label: studied with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## partnersWith

* label: partners with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## widowOf

* label: widow of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## halfSisterOf

* label: half sister of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## in 

* label: in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## filedFor

* label: filed for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## agentOf

* label: agent of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedNear

* label: lived near
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## built

* label: built
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## workedIn

* label: worked in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## established

* label: established
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedOn

* label: lived on
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## triedFor

* label: tried for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fledTo

* label: fled to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## activeIn

* label: active in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## proscribed

* label: proscribed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## ranFor

* label: ran for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## wentTo

* label: went to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## friendsWith

* label: friends with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## prosecutedFor

* label: prosecuted for
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travelledWith

* label: travelled with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travellingCompanionOf

* label: travelling companion of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## enlistedIn

* label: enlisted in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## capturedBy

* label: captured by
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## issued

* label: issued
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## broughtTo

* label: brought to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## greatGrandsonOf

* label: great grandson of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## author

* label: author
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livingIn

* label: living in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## movedTo

* label: moved to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## subscriber

* label: subscriber
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## livedAt

* label: lived at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## educatedAs

* label: educated as
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## operated

* label: operated
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## oneOf

* label: one of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## inCommandOf

* label: in command of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## knownAs

* label: known as
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## renounced

* label: renounced
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## trainedIn

* label: trained in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## imprisonedIn

* label: imprisoned in
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## exiled

* label: exiled
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## fatherOf

* label: father of
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sent

* label: sent
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## sailed

* label: sailed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## travellingAbroad

* label: travelling abroad
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## bankrupt

* label: bankrupt
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## landedAt

* label: landed at
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## wentInto

* label: went into
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## went

* label: went
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## jailed

* label: jailed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## taken

* label: taken
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## takenTo

* label: taken to
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## inADuelWith

* label: in a duel with
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## motherOf

* label: motherOf
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## confirmed

* label: confirmed
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## 

* label: 
* description: 
* value: Literal
* scope: <http://bibfra.me/vocab/aas>

## 

* label: 
* description: 
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




