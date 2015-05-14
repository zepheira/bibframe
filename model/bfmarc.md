<!---

BIBFRAME MARC is a starting point for customized MARC vocabularies using
the BIBFRAME model and profiles.  It builds off of the BIBFRAME Lite
vocabulary. It is framework conformant to BIBFRAME (and in theory MARC)
and where possible, link-compatible with the US Library of Congress's
BIBFRAME vocabulary, http://bibframe.org/

BIBFRAME MARC is expressed using the Versa data model, which also
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

You'll notice that BIBFRAME MARC terms use a humpCase/HumpCase convention,
which derives from BIBFRAME legacy.

--->

# @docheader

<!---

@base is the default base IRI, used e.g. for resource headers. It
would also be used for properties except that it is overridden by
@property-base

The meta-properties in this file are actually defined by the Versa
data model to support interpretation by Versa modeling tools

@resource-base is another possible override, for resource headers, but
not used here

--->

* @iri:
    * @base: http://bibfra.me/vocab/marc/
    * @property: http://bibfra.me/purl/versa/support
* title: BIBFRAME MARC vocabulary
* @interpretations:
    * scope: @resource

<!---
Extend BIBFRAME Lite Classess
--->

# <http://bibfra.me/vocab/lite/Work>

* properties: contentCategory numeration titles catalogingSource lcCallNumber lcItemNumber nlmCallNumber nlmCallNumber nlmCopyStatement nalCallNumber nalItemNumber nalCopyStatement deweyNumber titleRemainder titleRemainder titleStatement titleNumber titlePart titlePart inclusiveDates formDesignation titleVariation titleVariationRemainder titleVariationDate formerTitle seriesStatement dissertationNote degree grantingInstitution dissertationYear dissertationNote governingAccessNote jurisdictionNote physicalAccess uriNote  remainderOfScale creditsNote citationSource citationCoverage citationLocationWithinSource citationUri typeOfReport periodCovered typeOfComputerFile dateTimePlace dateOfEvent otherEventInformation placeOfEvent summaryExpansion assigningSource intendedAudience intendedAudienceSource geographicCoverage supplement interestLevel readingLevel   locationOfOriginalsDuplicates fundingInformation systemDetails informationRelatingToCopyrightStatus locationOfOtherArchivalMaterial biographicalOrHistoricalData languageNote entityAndAttributeInformation informationAboutDocumentation ownership action awardsNote medium additionalPhysicalForm 

# <http://bibfra.me/vocab/lite/Instance>

* properties: keyTitle issn doi accessibilityNote contentsNote creditsNote lccn legalDeposit isbn otherControlNumber upc lcOverseasAcq publisherNumber issueNumber plateNumber videoRecordingNumber systemControlNumber stockNumber abbreviatedTitle edition musicalPresentation computerFilecharacteristics copyrightDate otherPhysicalDetails size accompanyingMaterial typeOfunit materials publication manufacture distribution production publicationFrequency publicationDateFrequency mediaCategory carrierCategory physicalSubstance dimensions materialsApplied recordingTechnique physicalSupport organizationMethod arrangement hierarchy materialsSpec publicationDesignation reproductionNote representativeFractionOfScale termsGoverningUse authorizedUsers authorization formOfItem bibliographyNote contentsNote dataQuality originalVersionNote immediateSourceOfAcquisition issuingBody cumulativeIndexFindingAids 

# <http://bibfra.me/vocab/lite/Authority>

# <http://bibfra.me/vocab/lite/Person>
* properties: numeration titles 

# <http://bibfra.me/vocab/lite/Organization>
* properties: subordinateUnit 

# <http://bibfra.me/vocab/lite/Meeting>
* properties: locationOfEvent

# <http://bibfra.me/vocab/lite/Topic>
* properties: source generalSubdivision chronologicalSubdivision geographicSubdivision formSubdivision

# <http://bibfra.me/vocab/lite/Form>
* properties: source

<!-- 
Class Refinements 
-->

# Series
* label: Series
* refines: <http://bibfra.me/vocab/lite/Collection>
* description: A Series
* scope: <http://bibfra.me/vocab/marc>

<!-- 
MARC Control Code Code Class refinements of Work
-->

# Books
* label: Books
* description: A work that has bibliographic characterisics. 
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: illustrations targetAudience natureOfContents governmentPublication index literaryForm biographical
* remark: Derived from leader information

# ContinuingResources
* label: Continuing resources
* description: A work that has continuing resource characteristics. 
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: frequency regularity natureOfEntireWork natureOfContents governmentPublication originalAlphabetOrScriptOfTitle entryConvention characteristic
* remark: Derived from leader information

# Music
* label: Music
* description: A work that has music characteristics.
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: formOfComposition formatOfMusic musicParts targetAudience accompanyingMatter literaryTextForSoundRecordings transpositionAndArrangement
* remark: Derived from leader information

# Maps
* label: Maps
* description: A work that has map like characteristics. 
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: relief projection governmentPublication index specialFormatCharacteristics characteristic
* remark: Derived from leader information

# VisualMaterials
* label: Visual materials
* description: A work that has characteristics of visual materials.
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: runtime targetAudience governmentPublication technique characteristic
* remark: Derived from leader information

# ComputerFiles
* label: Computer files
* description: A work that has characteritics of a computer file.
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* properties: targetAudience governmentPublication characteristic
* remark: Derived from leader information

# MixedMaterials
* label: Mixed materials
* description: A work that has characteristics of mixed material.
* refines: <http://bibfra.me/vocab/lite/Work>
* scope: <http://bibfra.me/vocab/marc>
* remark: Derived from leader information

<!--
Control Code Work Type Refinements 
-->

# LanguageMaterial
* label: Language material
* description: Books and continuing resources
* refines: Books
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information

# NotatedMusic
* label: Notated music
* description:  A work that visually represents aurally perceived music through the use of written symbols, including ancient or modern musical symbols.
* refines: Music
* scope: <http://bibfra.me/vocab/marc>
* remark: Derived from leader information

# StillImage
* label: Still image
* description: A single static image, as distinguished from a kinetic image.
* refines: VisualMaterials
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Cartography
* label: Cartography
* description: A work reflecting the science or practice of drawing maps.
* refines: Maps
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information. Coded data elements relating to cartographic material.

# MovingImage
* label: Moving image
* description: A work reflecting a form of entertainment that enacts a story by sound and a sequence of images giving the illusion of continuous movement.
* refines: VisualMaterials
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Audio
* label: Audio
* description: A work of sound, especially when recorded, transmitted, or reproduced.
* refines: Music
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Nonmusical
* label: Nonmusical
* description: A work produced by noise, as opposed to continuous and regular vibrations.
* refines: Music
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Sounds
* label: Sounds
* description: A work produced by continuous and regular vibrations, as opposed to noise.
* refines: Music
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Multimedia
* label: Multimedia
* description: A work using more than one medium of expression or communication.
* refines: VisualMaterials
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Kit
* label: Kit
* description: A set of equipment needed for a specific purpose.
* refines: VisualMaterials
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Software
* label: Software
* description: A program used to direct the operation of a computer, as well as documentation giving instructions on how to use them.
* refines: ComputerFiles
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# ThreeDimensionalObject
* label: Three dimensional object
* description: An object that has height, width and depth, like any object in the real world.
* refines: VisualMaterials
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# Manuscript
* label: Manuscript
* description: A work written by hand, or manually typewritten, as opposed to being mechanically printed or reproduced in some automated way. 
* refines: Books
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

# ConferencePublication
* label: Conference Publication
* description: A work that is a proceedings, reports, or summaries of a conference
* refines: Books
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information (recast as type)

# Festschrift
* label: Festschrift
* description: A work honoring a respected person, especially an academic, and presented during his or her lifetime.
* refines: Books
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information (recast as type)

<!-- 
Supporting properties from MARC leader codes 
-->

## targetAudience
* label: target audience
* description: Target audience of the Work
* refines: <http://bibfra.me/vocab/lite/audience>
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## biographical
* label: biography type
* description: Indicates what the biographical characteristics are of the work
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## governmentPublication
* label: government publication
* description:  Indicates whether or not the item is published or produced by or for an international, national, state, provincial, or local government agency, or by any subdivision of such a body. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## literaryForm
* label: literary form
* description: Indicates the literary form of an item 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## natureOfContents
* label: nature of contents
* description: Indicates whether a significant part of the item is or contains certain types of material
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## illustrations
* label: illustrations
* description: Indicates the presence of types of illustrations in the work
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## formOfComposition
* label: form of composition
* description: Indicates the form of the conposition
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## formatOfMusic
* label: format of music
* description: Indicates the format of the Music
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## musicParts
* label: music parts
* description: Indicates whether the work being cataloged is, or contains parts.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## accompanyingMatter
* label: accompanying matter
* description: Indicates the contents of program notes and other accompanying material for sound recording, music manuscripts, or notated music
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## literaryTextForSoundRecordings
* label: literary text for sound recordings
* description: Indicates the type of literary text contained in a nonmusical sound recording
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## index
* label: index
* description: Information for this data element is derived from mention of an index in another part of the bibliographic record  
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## formOfItem
* label: form of item
* description: Form of mterial for the item
* scope: <http://bibfra.me/vocab/marc>
* remark: Control Code information 

## transpositionAndArrangement
* label: transposition and arrangement
* description: Indicates whether all or part of the item being cataloged is a transposition and/or arrangement of another work. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## relief
* label: relief
* description: Indicates the relief type specified
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## projection
* label: projection
* description: Indicates the projection used in producing the work. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## specialFormatCharacteristics
* label: special format characteristics
* description: Indicates the special format characteristics of the map.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## runtime
* label: runtime
* description: Indicates the runtime of the moving pictures or videorecordings.
* value: Literal
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## technique 
* label: technique 
* description: Indicates the technique used in creating motion in motion pictures or videorecordings.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## frequency
* label: frequency
* description: Indicates the frequency of a work
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## regularity
* label: regularity
* description: Indicates the regularity of a work
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## natureOfEntireWork
* label: nature of entire work
* description: Indicates the nature of the work
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## originalAlphabetOrScriptOfTitle
* label: original alphabet or script of title
* description: Indicates the original alphabet or script of the language of the title on the source item upon which the key title
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## entryConvention
* label: entry convention
* description: Indicates the type of entry convention.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## characteristic 
* label: characteristic 
* description: a feature or quality belonging typically to a person, place, or thing and serving to identify it
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: property derived from 'typeOf' control code indicators (e.g. typeOfVisualMaterial, typeOfComputerFile, etc.)

<!-- 
Control Code Instance Types - MARC 007
-->

# Map
* label: Map
* description: A diagrammatic representation of an area of land or sea showing physical features, cities, roads, etc.
* properties: specificMaterialDesignation color physicalMedium typeOfReproduction productionReproductionDetails positiveNegativeAspect 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Electronic
* label: Electronic Resource
* description: Item involves a medium intended to be used or processed by a computer.
* remark: Readable and manipulable by a computer
* synonyms: <http://bibframe.org/vocab/Electronic>
* properties: specificMaterialDesignation color dimensions sound imageBitDepth fileFormats qualityAssuranceTargets antecedentSource levelOfCompression reformattingQuality
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Globe
* label: Globe
* description: Item is a globe which is defined as the model of a celestial body, usually the earth or the celestial sphere, depicted on the surface of a sphere.
* properties: specificMaterialDesignation color physicalMedium typeOfReproduction 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# TactileMaterial
* label: Tactile material
* description: Item is tactile material which is defined as material intended to be read or interpreted by touch.
* properties: specificMaterialDesignation classOfBrailleWriting levelOfContraction brailleMusicFormat specialPhysicalCharacteristics 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# ProjectedGraphic
* label: Projected graphic
* description: Item is projected graphic material which is defined as a two-dimensional representation intended to be projected without motion by means of an optical device, for example, a filmstrip, slide, or transparency (includes x-rays).
* properties: specificMaterialDesignation color baseOfEmulsion soundOnMediumOrSeparate mediumForSound dimensions secondarySupportMaterial 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Microform
* label: Microform
* description: Item is a microform. Microform is a generic term for any medium, transparent or opaque, bearing microimages. A microimage is a unit (e.g., a page) of textual, graphic, or computer-generated material that is contained on aperture cards, microfiche, microfilm, micro-opaques, or other microformats and that is too small to be read without magnification. Microforms may be reproductions of existing textual or graphic materials or they may be original publications.
* properties: specificMaterialDesignation positiveNegativeAspect dimensions reductionRatioRange reductionRation color emulsionOnFilm generation baseOfFilm 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# NonprojectedGraphic
* label: Nonprojected graphic
* description: Item is nonprojected graphic material. This is defined generally, as a two-dimensional pictorial representation whether opaque (e.g., print, photoprint, drawing) or transparent, but not intended to be projected for viewing (e.g., a photographic negative).
* properties: specificMaterialDesignation color primarySupportMaterial secondarySupportMaterial 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# MotionPicture
* label: Motion picture
* description: Item is a motion picture, which is defined as a series of still pictures on film, with or without sound, designed to be projected in rapid succession to produce the optical effect of motion.
* properties: specificMaterialDesignation color motionPicturePresentationFormat soundOnMediumOrSeparate mediumForSound dimensions configurationOfPlaybackChannels productionElements positiveNegativeAspect generation baseOfFilm refinedCategoriesOfColor kindOfColorStockOrPrint deteriorationStage completeness filmInspectionDate 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Kit
* label: Kit
* description: Item is a kit, which is defined as a mixture of various components issued as a unit and intended primarily for instructional purposes. No one component is identifiable as the predominant component of the item. Examples are packages of assorted materials, such as a set of K-12 social studies curriculum material (books, workbooks, guides, activities, etc.), or packages of educational test materials (tests, answer sheets, scoring guides, score charts, interpretative manuals, etc.).
* properties: specificMaterialDesignation
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# NotatedMusic
* label: Notated music
* description: Item is notated music, which is defined as graphic, non-realized representations of musical works, both in printed and digitized manifestations. It includes musical scores and/or parts, diagrammatic representations, tablature, instructions for chance compositions, pictures or paintings intended as musical compositions, square note notation, klavirskribo, chant notation, neumes, braille, and other ways of representing the four components of musical sound: pitch, duration, timbre, and loudness. Notated music is often the means for communicating to the performer(s) how the musical work notated therein is to be realized in sound.
* properties: specificMaterialDesignation
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# RemoteSensingImage
* label: Remote-sensing image
* description: Item is a remote-sensing image or remote-sensing map. This is an image produced by a recording device that is not in physical or intimate contact with the object under study.
* properties: specificMaterialDesignation altitudeOfSensor attitudeOfSensor cloudCover platformConstructionType platformUseCategory sensorType dataType
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# SoundRecording
* label: Sound recording
* description: Item is a sound recording, defined as a disc, tape, film, cylinder, or wire on which sound vibrations have been registered so that the sound may be reproduced, or paper rolls on which the notes of a musical composition are represented by perforations in the paper and from which sound can be mechanically produced.
* properties: specificMaterialDesignation speed configurationOfPlaybackChannels grooveWidthPitch dimensions tapeWidth tapeConfiguration kindOfDiscCylinderOrTape kindOfMaterial kindOfCutting specialPlaybackCharacteristics captureAndStorageTechnique 
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Print
* label: Print
* description: Item is text, defined as printed or manuscript language material that is accessible to the naked eye (e.g., a book, a pamphlet, a broadside).
* remark: Generalizes MARC 007 'Text'
* synonyms: <http://bibframe.org/vocab/Print>
* properties: specificMaterialDesignation
* refines: <http://bibfra.me/vocab/lite/Instance>
* scope: <http://bibfra.me/vocab/marc>

# Videorecording
* label: Videorecording
* description: Item is a videorecording, defined as a recording on which visual images, usually in motion and accompanied by sound, have been registered. It is designed for playback by means of a television set.
* refines: <http://bibfra.me/vocab/lite/Instance>
* properties: specificMaterialDesignation color videorecordingFormat soundOnMediumOrSeparate mediumForSound dimensions configurationOfPlaybackChannels
* scope: <http://bibfra.me/vocab/marc>

<!---
Properties applicable to instance types - MARC 007
--->

## altitudeOfSensor
* label: altitude of sensor
* description: General position of the sensor relative to to the object under study.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## attitudeOfSensor
* label: attitude of sensor
* description: General angle of the device from which the remote-sensing image is made.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## antecedentSource
* label:  antecedent source
* description: Information about the source of a digital file important to the creation, use and management of digitally reformatted materials. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## baseOfFilm
* label: base of film
* description: Safety base film is a comparatively nonflammable film base that meets ISO requirements for a safety base. On some film, the phrase safety film appears on the edge of motion pictures. Nitrate film base is a highly flammable film base that does not meet the ISO requirements for safety base film.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## brailleMusicFormat
* label: braille music format
* description: Three-character code that indicates the braille music format of the item. The music formats are the way measures, sections, parts, and related information, such as words, are presented in relation to each other. Up to three formats may be indicated, left justified in order of predominance. If fewer than three codes are assigned, the codes are left justified and unused positions contain blanks (#). 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## classOfBrailleWriting
* label: class of braille writing
* description: Family of braille to which the item belongs. This is not the particular braille code, but the type of braille code used, representing different types of written symbols. Up to two braille types may be indicated, or the cataloging agency can choose to encode only the predominate type. Multiple codes are coded in order of predominance, if any. If fewer than two codes are assigned, the codes are left justified and unused positions contain blanks (#).
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## cloudCover
* label: cloud cover
* description: Amount of cloud cover that was present when a remote-sensing image was made.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## color
* label: color
* description: Color characteristics
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## emulsionOnFilm
* label: emulsion on film
* description:  Type of light-sensitive material on the film. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## primarySupportMaterial
* label: primary support material
* description: Type of material used for the support or base on which an image is printed or executed. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## secondarySupportMaterial
* label: secondary support material
* description: Type of material (other than normal museum matting) to which the primary support (007/04) is attached. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## baseOfEmulsion
* label: base of emulsion
* description:  Type of material for the base of the emulsion of a photonegative, filmstrip, slide, or transparency. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## completeness
* label: completeness
* description:  Whether the film is part of a complete production or is a preliminary or post-production element. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## configurationOfPlaybackChannels
* label: configuration of playback channels
* description: Configuration of playback channels for the sound portion of a motion picture. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## grooveWidthPitch
* label: groove width / pitch
* description: Width of the groove of the recording for discs or the pitch of the groove for cylinders.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## dataType
* label: data Type
* description: Spectral, acoustic, or magnetic characteristics of the data received by the device producing the remote-sensing image. It can be used to indicate both the wave length of radiation measured and the type of sensor used to measure it. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## deteriorationStage
* label: deterioration stage
* description:  Level of deterioration of the motion picture film. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## dimensions
* label: dimensions
* description:  Width of a motion picture. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## tapeWidth 
* label: Tape width 
* description: width of the tape.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## tapeConfiguration
* label: tape configuration
* description: Configuration of the tape.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## kindOfDiscCylinderOrTape
* label: kind of disc cylinder or tape
* description: kind of disc cylinder or tape
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## kindOfMaterial 
* label: kind of material 
* description: Kind of material used in the manufacture of sound recordings (both instantaneous and mass-produced).
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## kindOfCutting 
* label: kind of cutting 
* description: Kind of cutting of the grooves used on a disc.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## specialPlaybackCharacteristics 
* label: special playback characteristics 
* description: Playback characteristics for sound recordings, including special equipment or equalization necessary for proper playback. This code is not used to indicate special processes used during recording unless those processes must be applied during playback. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## captureAndStorageTechnique
* label: capture and storage technique
* description: How the sound was originally captured and stored. Re-releases of recordings should be coded for the original capture and storage technique, even though such re-releases may have been enhanced using another technique.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## fileFormats
* label: file formats
* description: Whether the file(s) which comprise the electronic resource are of the same format or type for digitally reformatted materials. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## filmInspectionDate
* label: filmInspectionDate
* description: Six characters that indicate the most recent film inspection date; the date is recorded in the pattern ccyymm (century/year/month). A hyphen is used for any unknown portion of the date. Six fill characters (||||||) are used if no attempt is made to code these character positions. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## generation
* label: generation
* description: How far away from the original material the item is (e.g., the actual negative film or original videotape in the camera). Generation data is used to evaluate the quality of available copies, to make preservation decisions, and to identify materials available for viewing and research. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## imageBitDepth
* label: image bit depth
* description: Exact bit depth of the scanned image(s) that comprise the electronic resource, or a three-character alphabetic code which indicates that the exact bit depth cannot be recorded. Since only exact bit depth is useful, coding should not include missing digits represented by hyphens (-). 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## kindOfColorStockOrPrint
* label: kind of color stock or print
* description:  Type of color film stock or color print the item represents. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## levelOfCompression
* label: level of compression
* description:  Kind of compression the electronic resource has been subjected to. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## reformattingQuality
* label: reformatting quality
* description: Reformatting quality of the electronic resource; an overall assessment of the physical quality of the electronic resource in relation to its intended use. It can be used to judge the level of quality of a file, and an institution's commitment to maintain its availability over time. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## levelOfContraction
* label: level of contraction
* description: Whether contractions are used.
* value: Liteal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## mediumForSound
* label: medium for sound
* description: Specific medium used to carry the sound of an item (whether the sound is on the projected graphic or separate) and the type of sound playback required for the item. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## motionPicturePresentationFormat
* label: motion picture presentation format
* description:  Presentation format for motion pictures. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## physicalMedium
* label: physical medium
* description:  Material out of which the cartographic item is made. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## platformConstructionType
* label: platform construction type
* description: Type of construction of the platform serving as the base for the remote-sensing device. For the purposes of this data element, "platform" refers to any structure that serves as a base, not only flat surfaces. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## platformUseCategory
* label: platform use category
* description: Primary use intended for the platform specified in platform construction type.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## positiveNegativeAspect
* label: positive negative aspect
* description:  Whether the film is positive or negative. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## productionElements
* label: production elements
* description:  Whether the film is part of a complete production or is a preliminary or post-production element. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## qualityAssuranceTargets
* label: quality assurance targets
* description: Whether quality assurance targets have been included appropriately at the time of reformatting/creation of the electronic resource. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## refinedCategoriesOfColor
* label: refined categories of color
* description: More specific color characteristics of the moving image
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## sensorType
* label: sensor type
* description: For the recording mode of the remote-sensing device, specifically, whether the sensor is involved in the creation of the transmission it eventually measures.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## sound
* label: sound
* description:  Whether the production of sound is an integral part of an electronic resource. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## soundOnMediumOrSeparate
* label: sound on medium or separate
* description:  Whether the sound is on or is separate from the projected graphic (i.e., on the accompanying material). 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## specialPhysicalCharacteristics
* label: special physical characteristics
* description: Other special physical characteristics about the braille.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## specificMaterialDesignation
* label: specific material designation
* description: Special class of tactile materialspecific material to which the item belongs.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## speed
* label: speed
* description: Playback speed of the sound recording.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## specialPlaybackCharacteristics
* label: special playback characteristics
* description: Playback characteristics for sound recordings, including special equipment or equalization necessary for proper playback. This code is not used to indicate special processes used during recording unless those processes must be applied during playback. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## typeOfReproduction
* label: type of reproduction
* description:  Whether the cartographic item is a facsimile or other type of reproduction. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## productionReproductionDetails 
* label: production reproduction details 
* description:  Photographic technique used to produce the cartographic item.  
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## positiveNegativeAspect 
* label: positive negative aspect 
* description:  Positive/negative aspect of the photocopy or film of the cartographic item. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information

## videorecordingFormat
* label: videorecording format
* description:  Videotape or videodisc recording format. 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>
* remark: Control code information


<!---
Define MARC additional properties used to describe Works / Expressions (Works)
--->

## contentCategory
* label: content category
* synonyms: <http://bibframe.org/vocab/contentCategory>
* description: Categorization reflecting the fundamental form of communication in which the content is expressed and the human sense through which it is intended to be perceived.
* value: IRI
* scope: <http://bibfra.me/vocab/marc>

## mediaCategory
* label: media category
* synonyms: <http://bibframe.org/vocab/mediaCategory>
* description: Categorization reflecting the general type of intermediation device required to view, play, run, etc., the content of a resource.
* value: IRI
* scope: <http://bibfra.me/vocab/marc>

## carrierCategory
* label: carrier category
* synonyms: <http://bibframe.org/vocab/carrierCategory>
* description: Categorization reflecting the format of the storage medium and housing of a carrier.
* value: IRI
* scope: <http://bibfra.me/vocab/marc>

## lccn
* label: lccn
* synonyms: <http://bibframe.org/vocab/lccn>
* refines: <http://bibfra.me/vocab/lite/controlCode>
* description:  Library of Congress Control Number, which identifies the instance.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## issn
* label: issn
* synonyms: <http://bibframe.org/vocab/issn>
* refines: <http://bibfra.me/vocab/lite/controlCode>
* description: An issn number associated with an instance
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## isbn
* label: isbn
* synonyms: <http://bibframe.org/vocab/issn>
* refines: <http://bibfra.me/vocab/lite/controlCode>
* description: An issn number associated with an instance
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## doi
* label: doi
* synonyms: <http://bibframe.org/vocab/doi>
* refines: <http://bibfra.me/vocab/lite/controlCode>
* description: A DOI (Digital Object Identifier) associated with an Instance
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

<!--
Notes notes notes
-->

## accessibilityNote
* label: accessibility note
* synonyms: <http://bibframe.org/vocab/contentAccessabilityNote>
* refines: <http://bibfra.me/vocab/lite/note>
* description: Content that assists those with a sensory impairment for greater understanding of content, e.g., labels, captions.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## contentsNote
* label: contents note
* synonyms: <http://bibframe.org/vocab/contentsNote>
* refines: <http://bibfra.me/vocab/lite/note>
* description: List of subunits of the resource.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## creditsNote
* label: credits note
* synonyms: <http://bibframe.org/vocab/creditsNote>
* refines: <http://bibfra.me/vocab/lite/note>
* description: Credits for persons or organizations who have participated in the creation and/or production of the resource.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## awardsNote
* label: awards note
* desciption: Information on awards associated with the described resource.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/awardNote>
* scope: <http://bibfra.me/vocab/marc>

## additionalPhysicalForm
* label: additional physical form
* desciption: Resource that is manifested in another physical carrier. 
* value: Literal
* remark: A note about a different format (physical or digital) in which the described item is available. Equivalent to MARC 530 subfield a, additional physical form available note. 
* refines: 
* synonyms: <http://bibframe.org/vocab/otherPhysicalFormat>
* scope: <http://bibfra.me/vocab/marc>

## assigningSource

* label: assigning source
* desciption: Organization code or name of the agency or other source (e.g., journal or newspaper) that supplied the data (summary, review, abstract, content advice statement, etc.) recorded.
* value: Literal
* remark: Equivalent to assigning source, subfield c of MARC 520 field summary, etc. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## authorization

* label: authorization
* desciption: The source of the authority for a restriction.
* value: Literal
* remark: Equivalent to authorization, subfield e of MARC field 506 restrictions on access note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## authorizedUsers

* label: authorized users
* desciption: The class of users or specific individuals for whom legal, physical or procedural restrictions imposed on use do not apply. 
* value: Literal
* remark: Equivalent to authorization, subfield e of MARC field 506 restrictions on access note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## bibliographyNote

* label: bibliography note
* desciption: A note about a bibliography, discography, filmography, webliography, and/or other bibliographic references in an item.
* value: Literal
* remark: Equivalent to bibliography, etc. subfield a of MARC field 504, the bibliography, etc. note. 
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## biographicalOrHistoricalData

* label: biographical or historical data
* desciption: A note providing biographical information about an individual or administrative information of an organization.
* value: Literal
* remark: Equivalent to biographical or historical data, subfield a of MARC field 545. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## citationCoverage

* label: citation coverage
* desciption: The dates of the source. 
* value: Literal
* remark: Equivalent to coverage of source, subfield b of MARC field 510 citation/references note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## citationLocationWithinSource

* label: citation location within source
* desciption: A citationLocationWithinSource
* value: Literal
* remark: Equivalent to location within source, subfield c of MARC field 510 citation/references note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## citationSource
* label: citation source
* desciption: Source of citation. 
* value: Literal
* remark: Equivalent to name of source, subfield a of MARC field 510 citation/references note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## citationUri
* label: citationUri
* desciption: The Uniform Resource Identifier (URI) that provides electronic access data in a standard syntax to an electronic bibliography cited or to the citation within an electronic bibliography.
* value: Literal
* remark: Equivalent to uniform resource identifier, subfield u of MARC field 510 citation/references note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## contentsNote
* label: contents note
* desciption: List of resources contents or subunits. 
* value: Literal
* remark: Equivalent to formatted contents note, subfield a of MARC field 505.  
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/contentsNote>
* scope: <http://bibfra.me/vocab/marc>



## cumulativeIndexFindingAids 

* label: cumulative index finding aids
* desciption: A note identifying the availability of cumulative indexes or finding aids whose primary focus is the described material.
* value: Literal
* remark: Equivalent to cumulative index/finding aids note, subfield a of MARC field 555. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

<!-- 
extracted 
-->

## abbreviatedTitle
* label: abbreviated title
* description: Title as abbreviated for indexing or identification.
* value: Literal
* remark: Equivalent to MARC 210 subfield a, abbreviated title.  
* refines: <http://bibfra.me/vocab/lite/title >
* synonyms: <http://bibframe.org/vocab/abbreviatedTitle>
* scope: <http://bibfra.me/vocab/marc>

## accompanyingMaterial
* label: accompanying material
* description: Resource that has an accompanying resource that adds to it.
* value: Literal
* remark: Equivalent to MARC 300 physical description subfield e, accompanying material.
* synonyms: <http://bibframe.org/vocab/accompaniedBy>
* scope: <http://bibfra.me/vocab/marc>

## action 
* label: action
* description: An act or thing done. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## arrangement
* label: arrangement
* description: Information about the organization and arrangement of a collection of items. For instance, for computer files, organization and arrangement information may be the file structure and sort sequence of a file; for visual materials, this information may be how a collection is arranged.
* value: Literal
* remark: Equivalent to arrangement subfield b of MARC field 351.
* synonyms: <http://bibframe.org/vocab/Arrangement>
* scope: <http://bibfra.me/vocab/marc>

<!-- 
SUGGESTED REMOVAL NEEDS DISCUSSION 
-->

## carrierMARCSource 
* label: carrierMARCSource
* description: MARC code that identifies the source of the term or code used to record the content type information.
* value: Literal
* remark: Equivalent to subfield 2 of MARC field 338. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

<!-- 
NEEDS FURTHER DISCUSSION G SAYS KEEP V SAYS REMOVE 
-->

## catalogingSource 
* label: cataloging source
* description: Source or origin of cataloging work. 
* value: Literal
* remark: Equivalent to original cataloging agency, subfield a of MARC field 040 cataloging source. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## chronologicalSubdivision
* label: chronological subdivision
* description: A chronologicalSubdivision
* value: Literal
* remark: Equivalent to chronological subdivision, any subfield y found in the MARC 6xx fields.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## computerFilecharacteristics
* label: computer file characteristics
* description: Computer file characteristics that include the type of file (e.g., software, text file) and the number of records, statements, etc. (e.g., 1300 records, 5821 bytes).
* value: Literal
* remark: Equivalent to computer file characteristics, subfield a of MARC field 256. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## copyrightDate
* label: copyright date
* description: Date associated with a claim of protection under copyright or a similar regime.
* value: Literal
* remark: Equivalent to date of production, publication, distribution, manufacture, or copyright notice, subfield c of MARC field 264 (with 2nd indicator 4).
* refines: 
* synonyms: <http://bibframe.org/vocab/copyrightDate>
* scope: <http://bibfra.me/vocab/marc>

## creditsNote
* label: credits note
* description: Credits for persons or organizations, other than members of the cast, who have participated in the creation and/or production of the resource.
* value: Literal
* remark: Equivalent to MARC field 508, creation/production credits note. 
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/creditsNote>
* scope: <http://bibfra.me/vocab/marc>

## dataQuality
* label: data quality
* description: A note on the general assessment of the quality of the data set constituting the item. Used primarily for cartographic materials.
* value: Literal
* remark: Equivalent to MARC field 514, data quality note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## dateOfEvent
* label: date of event
* description: Date, time or period of an event. 
* value: Literal
* remark: Equivalent to subfield d of MARC field 518, date/time and place of an event note. 
  refines: 
* synonyms: <http://bibframe.org/vocab/eventDate>
* scope: <http://bibfra.me/vocab/marc>

## dateTimePlace
* label: date time place
* description: A note on the date, time, or place of an event. 
* value: Literal
* remark: Equivalent to subfield a of MARC field 518, date/time and place of an event note.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## degree
* label: degree
* description: Degree the author was awarded. 
* value: Literal
* remark: Equivalent to degree type, subfield b of MARC field 502. 
* refines: 
* synonyms: <http://bibframe.org/vocab/dissertationDegree>
* scope: <http://bibfra.me/vocab/marc>

## deweyNumber
* label: dewey number
* description: Dewey Decimal Classification number used for subject access.
* value: Literal
* remark: Equivalent to subfield a of MARC field 082, Dewey Classification Number. 
* refines: 
* synonyms: <http://bibframe.org/vocab/classificationDdc>
* scope: <http://bibfra.me/vocab/marc>

## dimensions
* label: dimensions
* description: Measurements of the carrier or carriers and/or the container of a resource.
* value: Literal
* remark: Equivalent to dimensions, subfield c of MARC field 300 physical description. 
* refines: 
* synonyms: <http://bibframe.org/vocab/dimensions>
* scope: <http://bibfra.me/vocab/marc>

## reductionRatioRange 
* label: reductionRatioRange 
* description: reductionRatioRange 
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## reductionRation
* label: reductionRation
* description: reductionRation
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## dissertationID
* label: dissertation ID
* description: Identifier assigned to a dissertation for identification purposes.
* value: Literal
* remark: Equivalent to dissertation identifier, subfield o of MARC field 502 dissertation note. 
* refines: 
* synonyms: <http://bibframe.org/vocab/dissertationIdentifier>
* scope: <http://bibfra.me/vocab/marc>

## dissertationNote
* label: dissertation note
* description: Textual information about the dissertation.
* value: Literal
* remark: Equivalent to subfield g of MARC field 502 dissertation note. 
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/dissertationNote>
* scope: <http://bibfra.me/vocab/marc>

## dissertationYear
* label: dissertation year
* description: Year degree awarded.
* value: Literal
* remark: Equivalent to subfield d of MARC field 502 dissertation note.
* refines: <http://bibfra.me/vocab/lite/date>
* synonyms: <http://bibframe.org/vocab/dissertationYear>
* scope: <http://bibfra.me/vocab/marc>

## distribution
* label: distribution
* description: Information relating to distribution of an instance.
* value: Literal
* remark: Equivalent to MARC field 264 with 2nd indicator 2.
* refines: <http://bibfra.me/vocab/lite/provision>
* synonyms: <http://bibframe.org/vocab/distribution>
* scope: <http://bibfra.me/vocab/marc>

## edition
* label: edition
* description: Edition statement, information identifying the edition or version of the resource.
* value: Literal
* remark: Equivalent to edition statement, MARC field 250. 
* refines: 
* synonyms: <http://bibframe.org/vocab/edition>
* scope: <http://bibfra.me/vocab/marc>

## entityAndAttributeInformation
* label: entity attribute information
* description: A note about the information content of the data set, including the entity types, their attributes, and the domains from which the attribute values may be assigned.
* value: Literal
* remark: Equivalent to MARC field 552, entity and attribute information note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## form
* label: form
* description: Standardized terms used to group certain kinds of materials.
* value: Literal
* remark: Equivalent to subfield k, form subheading, used with MARC fields 240, 243 and 700. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## formDesignation
* label: form designation
* description: Class or genre to which a Work or Instance belongs. Used for archival materials. 
* value: Literal
* remark: Equivalent to form subheading subfield k of MARC field 245. 
* refines: 
* synonyms: <http://bibframe.org/vocab/formDesignation>
* scope: <http://bibfra.me/vocab/marc>

## formSubdivision
* label: form subdivision
* description: A specific kind or genre of material defined by the thesaurus being used.
* value: Literal
* remark: Equivalent to form subdivision, subfield v used with the MARC 6xx fields. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## formerTitle
* label: former title
* description: A former title proper used to represent all former titles proper of a continuing resource (serial or integrating resource).
* value: Literal
* remark: Equivalent to MARC field 247, former title. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## formerTitleComplexity
* label: former title complexity
* description: A note that expresses a complex relationship between varying titles.
* value: Literal
* remark: Equivalent to MARC field 547, former title complexity note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## fundingInformation
* label: funding information
* description: A note about the contract, grant and project numbers when the material results from a funded project.
* value: Literal
* remark: Equivalent to MARC field 536, funding information note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## generalSubdivision
* label: general subdivision
* description: A generalSubdivision
* value: Literal
* remark: Equivalent to general subdivision, subfield x in the MARC 6xx fields.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## geographicCoverage
* label: geographic coverage
* description: Geographic entities covered by the resource.
* value: Literal
* remark: Equivalent to geographic coverage MARC field 522. 
* refines: 
* synonyms: <http://bibframe.org/vocab/geographicCoverageNote>
* scope: <http://bibfra.me/vocab/marc>

## geographicSubdivision
* label: geographic subdivision
* description: A geographicSubdivision
* value: Literal
* remark: Equivalent to geographical subdivision, subfield z used with the MARC 6xx fields.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## governingAccessNote
* label: governing access note
* description: A note about the restrictions imposed on access to the described materials. For example, limited distribution for published works or restricted sections of archival collections. 
* value: Literal
* remark: Equivalent to MARC field 506 restrictions on access note. 
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## grantingInstitution
* label: granting institution
* description: Name of degree granting institution.
* value: Literal
* remark: Equivalent to subfield c of MARC field 502, dissertation note.
* refines: 
* synonyms: <http://bibframe.org/vocab/dissertationInstitution>
* scope: <http://bibfra.me/vocab/marc>

## hierarchy
* label: hierarchy
* description: The hierarchical position of the resources relative to each other.
* value: Literal
* remark: Equivalent to hierarchical level, subfield c of MARC field 351 organization and arrangement of materials. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## immediateSourceOfAcquisition
* label: immediate source of acquisition
* description: Information about the circumstances (e.g., source, date, method) under which the resource was directly acquired.
* value: Literal
* refines: 
* remark: Equivalent to subfield a of MARC field 541.
* synonyms: <http://bibframe.org/vocab/immediateAcquisition>
* scope: <http://bibfra.me/vocab/marc>

## inclusiveDates
* label: inclusive dates
* description: The time period during which the described materials were created. Often used for archival materials. 
* value: Literal
* remark: Equivalent to inclusive dates subfield f of MARC 245 title statement. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## informationAboutDocumentation
* label: information about documentation
* description: A note on the documentation of the described materials, such as code or field books that describe a dataset. 
* value: Literal
* remark: Equivalent to subfield a of MARC 556 information about documentation note.   
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## informationRelatingToCopyrightStatus
* label: information relating to copyright status
* description: Information about the item that can be used to determine copyright status.
* value: Literal
* remark: Equivalent to subfield a of MARC field 542 information relating to copyright status. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## intendedAudience
* label: intended audience
* description: Information that identifies the specific intended or target audience or intellectual level for which the content described item is considered appropriate. Used to record interest and motivation levels and special learner characteristics.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/IntendedAudience>
* scope: <http://bibfra.me/vocab/marc>

## intendedAudienceSource
* label: intended audience source
* description: The name or abbreviation of the agency or entity assigning the target audience note. 
* value: Literal
* remark: Equivalent to source subfield b of MARC field 521 target audience note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## interestLevel
* label: interest level
* description: The interest level of the work. For example, high school interest level. 
* value: Literal
* remark: Equivalent to interest level, subfield b of MARC field 526 study program information note.  
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## isbn
* label: isbn
* description: International Standard Book Number.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/isbn>
* scope: <http://bibfra.me/vocab/marc>

## issn
* label: issn
* description: International Standard Serial Number identifier.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/issn>
* scope: <http://bibfra.me/vocab/marc>

## issueNumber
* label: issue number
* description: Number used to identify the issue designation or serial identification, assigned by a publisher to a sound recording.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/issueNumber>
* scope: <http://bibfra.me/vocab/marc>

## issuingBody
* label: issuing body
* description: A note referring to current and former issuing bodies, including notes containing compiling, editing, or translating information that involves an issuing body. 
* value: Literal
* remark: Equivalent to MARC field 550 issuing body note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## jurisdictionNote
* label: jurisdiction note
* description: The name of a person, an institution or a function or position within the institution by whom or which the terms governing access are imposed and/or enforced and to whom the restriction may be appealed.
* value: Literal
* remark: Equivalent to jurisdiction subfield b of MARC field 506 restrictions on access note. 
* refines: <http://bibfra.me/vocab/lite/note >
* synonyms: <http://bibframe.org/vocab/Jurisdiction>
* scope: <http://bibfra.me/vocab/marc>

## keyTitle
* label: key title
* description: Unique title for a continuing resource that is assigned by the ISSN International Center in conjunction with an ISSN.
* value: Literal
* remark: Equivalent to MARC field 222 key title. 
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: <http://bibframe.org/vocab/keyTitle>
* scope: <http://bibfra.me/vocab/marc>

## languageNote
* label: language note
* description: Note concerning the language of the material or its parts.
* value: Literal
* remark: Equivalent to MARC field 546 language note. 
* refines: <http://bibfra.me/vocab/lite/note >
* synonyms: <http://bibframe.org/vocab/languageNote>
* scope: <http://bibfra.me/vocab/marc>

## lcCallNumber
* label: LC call number
* description: Library of Congress Call Number. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## lcItemNumber
* label: LC item number
* description: Library of Congress Item Number.
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## lcOverseasAcq
* label: LC acquisition program
* description: Identification number assigned by the Library of Congress to works acquired through one of its overseas acquisition programs.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/lcOverseasAcq>
* scope: <http://bibfra.me/vocab/marc>

## lccn
* label: lccn
* description: Library of Congress Control Number, which identifies the resource description.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/lccn>
* scope: <http://bibfra.me/vocab/marc>

## legalDate
* label: legal date
* description: Date of legal work or promulgation of a law, or signing of a treaty.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/legalDate>
* scope: <http://bibfra.me/vocab/marc>

## legalDeposit
* label: legal deposit
* description: Number assigned to a copyright or legal deposit, which Identifies a resource description.	
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/legalDeposit>
* scope: <http://bibfra.me/vocab/marc>

## locationOfEvent
* label: location of event
* description: The location at which an event occurred.
* value: Literal
* remark: Equivalent to location of event subfield c of MARC fields 610, 611 and 650. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## locationOfOriginalsDuplicates
* label: location of originals duplicates
* description: The note about the repository that has custody over the originals or duplicates of the described materials. Used to point users to originals or duplicates located in off-site locations. 
* value: Literal
* remark: Equivalent to MARC field 535 location of originals/duplicates note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## locationOfOtherArchivalMaterial
* label: location of other archival material
* description: A note for the name and address of the custodian of the archival materials related to the described materials by provenance, specifically by having been, at a previous time, a part of the same collection or record group. Used to point users to related archival materials in other repositories.  
* value: Literal
* remark: Equivalent to MARC field 544 location of other archival materials note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## manufacture
* label: manufacture
* description: Information relating to manufacture of an instance.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/provision>
* synonyms: <http://bibframe.org/vocab/manufacture>
* scope: <http://bibfra.me/vocab/marc>

## materials
* label: materials
* description: The part of the described materials to which the field applies.
* value: Literal
* remark: Equivalent to subfield 3 of MARC field 300 physical description. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## materialsApplied
* label: materials applied
* description: The physical substance applied to the material base (e.g., ink, oil, paint, tempera or a specific photographic emulsion such as albumen).
* value: Literal
* remark: Equivalent to materials applied to surface subfield c of MARC field 340. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## materialsSpec
* label: materials spec
* description: Distinguishes a subset of the described materials.
* value: Literal
* remark: Equivalent to materials specified, subfield 3 of MARC field 351 organization and arrangement of materials. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## medium
* label: medium 
* description: The particular form of storage for digitized information, such as magnetic tape or disc.
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## musicalPresentation
* label: musicalPresentation
* description: The title and statement of responsibility of a musical presentation. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nalCallNumber
* label: NAL call number
* description: NAL Call Number. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nalCopyStatement
* label: NAL copy statement
* description: NAL Copy Statement. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nalItemNumber
* label: NAL item number
* description: NAL Item Number
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nameOfPart
* label: name of part
* description:  The name designation of a part/section of a work.
* value: Literal
* remark: Equivalent to subfield p of MARC field 630 subject added entry uniform title. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nlmCallNumber
* label: NLM call number
* description: NLM Call Number. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nlmCopyStatement
* label: NLM copy statement
* description: NLM Copy Statement. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## nlmItemNumber
* label: NLM item number
* description: NLM Item Number. 
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## numeration
* label: numeration
* description: A Roman numeral alone or a Roman numeral and a subsequent part of a forename.
* value: Literal
* remark: Equivalent to numeration subfield b of MARC fields 100, 600 and 700. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## organizationMethod
* label: organization method 
* description: Pattern of organization or arrangement of materials within a unit.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/materialArrangement>
* scope: <http://bibfra.me/vocab/marc>

## originalVersionNote

* label: original version note
* description: A note that describes the original production of a work. 
* value: Literal
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/originalVersion>
* scope: <http://bibfra.me/vocab/marc>

## otherControlNumber

* label: other control number
* description: Standard numbers or codes published on an item that cannot be accommodated by other control number terms. 
* value: Literal
* remark: Equivalent to MARC field 024 other standard identifier. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## otherEventInformation

* label: other event information
* description: Other information related to the date or place of the event.
* value: Literal
* remark: Equivalent to other event information, subfield o of MARC field 518 date/time and place of an event note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## size
* label: size
* description: The size of the Instance.
* value: Literal
* scope: <http://bibfra.me/vocab/marc>

## otherPhysicalDetails

* label: other physical details
* description: Further characteristics of an item.
* value: Literal
* remark: Equivalent to other physical details, subfield b of MARC field 300 physical description. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## ownership
* label: ownership
* description: A note about the ownership and custodial history of the described materials from the time of their creation to the time of their accession 
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/custodialHistory.html>
* scope: <http://bibfra.me/vocab/marc>

## performerNote

* label: performerNote
* description: Information about the participants, players, narrators, presenters, or performers.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: <http://bibframe.org/vocab/performerNote>
* scope: <http://bibfra.me/vocab/marc>

## periodCovered
* label: period covered
* description: The time period covered by the resource. 
* value: Literal
* remark: Equivalent to period covered subfield b of MARC field 513 type of report and period covered note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## physicalAccess

* label: physical access
* description: Any current arrangements required for physical access. Arrangements may change. 
* value: Literal
* remark: Equivalent to physical access provisions subfield c of MARC field 506 restrictions on access note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## physicalSubstance

* label: physical substance
* description: Physical description information for an item that requires technical equipment for its use or an item that has special conservation or storage needs.
* value: Literal
* remark: Equivalent to material base and configuration subfield a of MARC field 340 physical medium. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## physicalSupport

* label: physical support
* description: The physical material on which or in which records are mounted, bound or otherwise supported.
* value: Literal
* remark: Equivalent to support subfield e of MARC field 340 physical medium. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## placeOfEvent

* label: place of event
* description: Place of an event. 
* value: Literal
* remark: Equivalent to place of an event subfield p MARC field 518 date/time and place of an event. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## plateNumber

* label: plate number
* description: The plate number assigned by the publisher. Often the plate number is at the bottom of each page of music or on the title page.
* value: Literal
* remark: Equivalent to 1st indicator 2 in MARC field 028 publisher number. 
* refines: 
* synonyms: <http://bibframe.org/vocab/musicPlate>
* scope: <http://bibfra.me/vocab/marc>

## production

* label: production
* description: Information relating to production of an instance.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/provision>
* synonyms: <http://bibframe.org/vocab/production>
* scope: <http://bibfra.me/vocab/marc>

## publication

* label: publication
* description: Information relating to publication of an instance.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/provision>
* synonyms: <http://bibframe.org/vocab/publication>  <http://purl.org/dc/elements/1.1/publisher>
* scope: <http://bibfra.me/vocab/marc>

## publicationDateFrequency

* label: publication date frequency
* description: Date of current publication frequency.
* value: Literal
* remark: Equivalent to date of current publication frequency subfield b of MARC field 310 current publication frequency.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## publicationDesignation

* label: publication designation
* description: The sequential designation and/or dates of publication. May consist of edition number, issue number, volume number, series of volume numbers or other sequential designations according to the usage of the publisher. 
* value: Literal
* remark: Equivalent to dates of publication and/or sequential designation subfield a of MARC field 362.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## publicationFrequency

* label: publication frequency
* description: A note that describes the frequency of the continuing resource. 
* value: Literal
* remark: Equivalent to current publication frequency subfield a of MARC field 310. 
* refines: 
* synonyms: <http://bibframe.org/vocab/frequency>
* scope: <http://bibfra.me/vocab/marc>

## publisherNumber

* label: publisher number
* description: Number assigned by a publisher that is not one of the specific defined types.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/publisherNumber>
* scope: <http://bibfra.me/vocab/marc>

## readingLevel

* label: reading level
* description: The assigned reading level of the resource. 
* value: Literal
* remark: Equivalent to reading level subfield c of MARC field 526 study program information note.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## recordingTechnique

* label: recording technique
* description: The means or technique used to record the information in or on the material base (e.g., cut, embossed, molded, pressed, punched, thermofax and x-ray).
* value: Literal
* remark: Equivalent to information recording technique subfield d of MARC field 340 physical medium. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## remainderOfScale

* label: remainder of scale
* description: The remainder of the scale note. If the still image or three-dimensional form is not to scale, and this fact is considered important for identification or selection, record that information.
* value: Literal
* remark: Equivalent to remainder of scale note subfield b of MARC field 507 scale note for graphic material. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## representativeFractionOfScale

* label: representative fraction of scale
* description: A note on the representative fraction of scale. 
* value: Literal
* remark: Equivalent to representative fraction of scale note subfield b of MARC field 507 scale note for graphic.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## reproductionNote
* label: reproduction note
* description: A note that identifies the type of reproduction being described.
* value: Literal
* remark: Equivalent to type of reproduction subfield a of MARC field 533 reproduction note. 
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## seriesStatement

* label: series statement
* description: The title proper of the series. 
* value: Literal
* remark: Equivalent to series statement subfield a of MARC field 490 series statement. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## seriesVolume

* label: series volume
* description: The volume number or other sequential designation used in conjunction with the series statement.
* value: Literal
* remark: Equivalent to volume number/sequential designation subfield v of MARC field 490 series statement. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>


## source

* label: source
* description: A MARC code that identifies the source list from which the index term was assigned. 
* value: Literal
* remark: Equivalent to source of term subfield 2 of MARC field 655 index term genre/form. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## stockNumber
* label: stock number
* description: Identification number such as distributor, publisher, or vendor number.
* value: Literal
* remark: Equivalent to stock number subfield a of MARC field 037 source of acquisition.
* refines: 
* synonyms: <http://bibframe.org/vocab/stockNumber>
* scope: <http://bibfra.me/vocab/marc>

## studyProgramName
* label: study program name
* description: The name of the study program that uses the title described.
* value: Literal
* remark: Equivalent to program name subfield a of MARC 526 program of study information note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## subordinateUnit
* label: subordinate unit
* description: Corporate names or corporate subheadings that follow the name of the highest hierarchical unit.
* value: Literal
* remark: Equivalent to subordinate unit subfield b of MARC fields 110, 610 and 710.
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## summary
* label: summary
* description: Description of the content of a resource, such as an abstract, summary, etc..
* value: Literal
* refines:  <http://bibfra.me/vocab/lite/description>
* synonyms: <http://bibframe.org/vocab/summary>
* scope: <http://bibfra.me/vocab/marc>

## summaryExpansion
* label: summary expansion
* description: The text of the abstract, review, summary, etc.
* value: Literal
* remark: Equivalent to summary, etc. subfield a of MARC field 520. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## summaryURI
* label: summary URI
* description: A Uniform Resource Identifier that links to an abstract, review, summary, etc. 
* value: Literal
* remark: Equivalent to subfield u of MARC field 520 summary, etc. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## supplement
* label: supplement
* description: Work that updates or otherwise complements the predominant work.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/supplement>
* scope: <http://bibfra.me/vocab/marc>

## systemControlNumber
* label: system control number
* description: Contains local control numbers that identify the same bibliographic record. Numbers may include local system, accession, or serial control numbers.
* value: Literal
* remark: Equivalent to MARC field 035 system control number. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## systemDetails
* label: system details
* description: A note about the technical information for the item.
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## termsGoverningUse
* label: terms governing use
* description: A note about terms governing the use of the materials after access has been provided. Use for copyrights, film rights, trade restrictions, etc., that restrict the right to exhibit, fictionalize, quote or reproduce.
* value: Literal
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## titleNumber
* label: title number
* description: The number designations of a part/section of an item. 
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## titlePart
* label: title part
* description: The name designation of the part or section of a work. 
* value: Literal
* remark: Equivalent to name of part/section of a work subfield p of MARC fields 240, 243 and 245. 
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## titleRemainder
* label: title remainder
* description: Word, character, or group of words and/or characters that contains the remainder of the title information after the main title.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## titleStatement
* label: statement of responsibility
* description: Transcribed information from the resource identifying the names and possibly functions of Agents responsible for or contributing to the creation of the intellectual or artistic content of the resource. 
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: <http://bibframe.org/vocab/titleStatement>
* scope: <http://bibfra.me/vocab/marc>

## titleVariation
* label: title variation
* description: Title associated with the resource that is different from the main title.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: <http://bibframe.org/vocab/titleVariation>
* scope: <http://bibfra.me/vocab/marc>

## titleVariationDate
* label: title variation date
* description: Date or sequential designation of title variation.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: <http://bibframe.org/vocab/titleVariationDate>
* scope: <http://bibfra.me/vocab/marc>

## titleVariationRemainder
* label: titleVariationRemainder
* description: Date or sequential designation of title variation.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/title>
* synonyms: <http://bibframe.org/vocab/titleVariationDate>
* scope: <http://bibfra.me/vocab/marc>

## titles
* label: titles
* description: Titles and other words associated with a name. 
* value: Literal
* remark: Equivalent to subfield c of MARC field 100 main entry personal name. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>
* remark: Dr, etc. 

## typeOfComputerFile
* label: type of computer file
* description: A note that characterizes the computer file.
* value: Literal
* remark: Equivalent to MARC field 516 type of computer file or data note. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## typeOfReport
* label: type of report
* description: A note about the type of report and the period covered.
* value: Literal
* remark: Equivalent to MARC field 513. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## typeOfunit
* label: type of unit
* description: The type of unit (e.g., box, cubic feet, linear feet, page, or volume) to which the extent of an item relates. Use to identify the configuration of material and how it is stored. Use for archival and rare materials only.
* value: Literal
* remark: Equivalent to type of unit subfield f of MARC field 300 physical description. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## upc
* label: upc
* description: Universal Product Code.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/upc>
* scope: <http://bibfra.me/vocab/marc>

## uriNote
* label: uri note
* description: A note on the Uniform Resource Identifier.
* value: Literal
* refines: <http://bibfra.me/vocab/lite/note>
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## version
* label: version
* description: The version, editions, etc., information.
* value: Literal
* remark: Equivalent to subfield s of MARC fields 240 and 243. 
* refines: 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>

## videoRecordingNumber
* label: video recording number
* description: Number assigned by a publisher to a video recording.
* value: Literal
* refines: 
* synonyms: <http://bibframe.org/vocab/videorecordingNumber>
* scope: <http://bibfra.me/vocab/marc>

## volume
* label: volume
* description: The volume number or other sequential designation used in conjunction with the series statement.
* value: Literal
* remark: Equivalent to volume subfield v of MARC field 830 series added entry uniform title. 
* synonyms: 
* scope: <http://bibfra.me/vocab/marc>




