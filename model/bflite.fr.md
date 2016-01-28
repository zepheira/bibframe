<!--

BIBFRAME Lite est un commencement pour les BIBFRAME vocabulaires customizés.
Cést un cadre qui se conforme à BIBFRAME et fonctionnel avec liens comme le
vocabulaire de la bibliothèque nationale des États Unis.
http://bibframe.org/

-->

# @docheader

* @iri:
    * @base: http://bibfra.me/vocab/lite/
    * @property: http://bibfra.me/purl/versa/support
* @language: fr

# Resource

* label: ressource
* description: Entité Générique; Ce qu'on doit décrire

## label

* label: étiquette
* description: Nom élémentaire de la ressource

## prefLabel

* label:  étiquette préférée
* refines: label
* description: Plus préféré des noms possibles de la ressource
* scope: <http://bibfra.me/vocab/lite>

## description

* label: description
* description: Description de la ressource
* remark: Peut comprendre, mais sans s'y limiter: un résumé, une table des matières, une représentation graphique ou une explication de la ressource.

## image

* label: image
* description: IRI vers une image de la ressource

## link

* label: lien
* description: IRI vers d'une autre ressource

## rightsStatement

* label: déclaration de droits
* description: Déclaration des droits d'utilisation de la ressource

## controlCode

* label: Numéro ou code de contrôle
* description: chaîne alphanumérique ou indicateur utilisé pour trouver et identifier la ressource
* remark: Identifiant selon les pratiques de codage locales

## related
* label: lié
* description: Autre ressource relatif à celle-ci

## language
* label: langue
* description: Langue relatif à la ressource

# LanguageCategory
* label: Catégorie des langues
* description: Liste des langues
* remark: Vocabulaire contrôlé.

# Temporal
* label: Temporal
* description: Dénotation de contexte chronologique des événements relatif à la ressource (dans le passé, le présent et l'avenir).

## date
* label: date
* description: Date relatif à la ressource.
* remark: Conseillé d'utiliser ISO 8601

## dateStart
* label: date de début
* description: Date de début relatif à la ressource
* remark: Conseillé d'utiliser ISO 8601

## dateEnd
* label: date de fin
* description: Date de fin relatif à la ressource
* remark: Conseillé d'utiliser ISO 8601

## dateBirth
* label: date de naissance
* description: Date de naissance relatif à la personne
* remark: Conseillé d'utiliser ISO 8601

## dateDeath
* label: date de la mort
* description: Date de décès relatif à la personne
* remark: Conseillé d'utiliser ISO 8601

## audience
* label: public prévu
* description: Classe d'utilisateur à lequel le contenu d'une ressource est destinée ou pour lesquels le contenu est jugé comme convenable
* remark: Peut être formé de personnes d'un certain groupe d'âge, sexe, état matrimonial, etc. l'objet de cette propriété devrait être une liste de code.

## note
* label: note
* description: Information supplémentaire relatif à la ressource

# Authority
* label: Autorité
* description: Description organisée et crédible d'une personne organisée, lieu ou chose

## name
* label: nom
* description: Nom de la ressource autorisée

## nameAlternative
* label: nom alternatif
* description: Nom alternatif de la ressource autorisée

## authorityLink
* label: lien autorisé
* description: Lien résolu relatif à la ressource autorisée
* remark: Quelquechose comme VIAF, LCNAF, ISNI, ORCID, etc.

# Work
* label: œuvre
* description: Création distincte, intellectuelle ou artistique

## title
* label: titre
* description: Titre de la ressource

## titleAlternative
* label: titre alternatif
* description: Titre alternatif de la ressource

## description
* label: description
* description: Description de la ressource
* remark: Description par exemple des ressources bibliographiques peut comprendre, mais sans s'y limiter: un résumé, une table des matières, une représentation graphique ou un texte libre de la ressource.

## creator
* label: créateur
* description: entité (ou les entités) responsables de la création de la ressource de l'origine

## contributor
* label: contributeur
* description: entité (ou les entités) qui contribuent à la ressource de l'origine

## subject
* label: sujet
* description: Indice terme, sous réserve terme, Vedette, ou descripteur, un terme de recherche d'information qui capture l'essence du sujet d'une ressource
* remark: La «volte-ness» d'une œuvre

## genre
* label: genre
* description: Catégorie de composition artistique caractérisé par des similitudes dans la forme, le style, ou du sujet
* remark: Le 'Ness est-' d'une œuvre

# Agent
* label: Agent
* description: Entité (par exemple, personne, organisation, etc.) associée à une ressource

## email
* label: adresse e-mail
* description: Adresse qui identifie une boîte e-mail pour les messages qui sont livrés à un agent

# Person
* label: Personne
* description: individuel (vie, mort, vampires, ou fictif) par rapport à une ressource

# Organization
* label: Organisation
* description: Unité de personnes, par exemple, une institution, une association ou personne morale

# Meeting
* label: Réunion
* description: réunion formelle de personnes à un usage particulier

# Family
* label: Famille
* description: unité sociale liés par la naissance, le mariage, l'adoption, l'union civile, ou relation similaire

# Place
* label: Lieu
* description: Emplacement géographique

# Category
* label: Catégorie
* description: Liste des choses considérées comme ayant des caractéristiques particulières partagées
* remark: Un vocabulaire contrôlé.

# Topic
* label: Topic
* description: terme Sujet décrivant un concept général, événement ou un objet

# Form
* label: Formulaire
* description: Catégorie ou genre qui décrit ce que la ressource est

# Concept
* label: Concept
* description: Terme décrivant le sujet, aboutness, une idée ou notion de ressource

# Instance
* label: Instance
* description: réalisation individuelle d'un travail

## instantiates
* label: instantiates
* description: Travailler la ressource instantie ou manifestes
* remark: Pour l'utilisation de connecter les instances pour Travaux dans la structure BIBFRAME.

## focus
* label: focus
* description: entité sous-jacente ou focale associée à un concept
* remark: Souvent, l'accent est l'entité principale associée à un concept.

## subFocus
* label: subfocus
* description: Qualifier ou modificateur utilisé pour décrire une entité sous-jacente focale supplémentaire associée à un concept.
* remark: Souvent les entités suivent fois l'objectif principal associé à un concept.

## provision
* label: disposition
* description: fournisseur associé à la porteuse
* remark: Connexion à des détails tels que le lieu, le nom et / ou des informations à jour relatives à la publication, impression, distribution, une émission, la libération, ou la production d'une instance.

## copyright
* label: le droit d'auteur
* description: cas du droit d'auteur associé à l'instance

## format
* label: le format
* description: Format de l'instance

## medium
* label: moyen
* description: moyenne de l'instance

## extent
* label: mesure
* description: Nombre de pages physiques, des volumes, des cassettes, temps total de lecture, etc., de chaque type d'unité

## dimensions
* label: dimensions
* description: Mesure de la taille

# ProviderEvent
* label: fournisseur de l'événement
* description: événement associé à la publication, impression, distribution, une émission, la libération ou la production d'une instance

# CopyrightEvent
* label: le droit d'auteur de l'événement
* description: cas du droit d'auteur associé à la propriété intellectuelle d'une instance.

## license
* label: licence
* description: licence associée à l'événement de l'homme associé à un travail

## copyrightAgent
* label: agent de droits d'auteur
* description: Agent associé à l'auteur d'une instance

## copyrightPlace
* label: copyright lieu
* description: Lieu associé à l'auteur d'une instance

## copyrightDate
* label: date de fournisseur
* description: Date associé à l'auteur d'une instance

## copyrightNote
* label: note de copyright
* description: note associée avec le droit d'auteur d'une instance

## providerAgent
* label: agent de fournisseur
* description: Agent associé à la publication, impression, distribution, une émission, la libération ou la production d'une instance

## providerPlace
* label: prestataire lieu
* description: Lieu associé à la publication, impression, distribution, une émission, la libération ou la production d'une instance

## providerDate
* label: date de fournisseur
* description: Date associé à la publication, impression, distribution, une émission, la libération ou la production d'une instance

## providerNote
* label: fournisseur Note
* description: note associée à la publication, impression, distribution, une émission, la libération ou la production d'une instance

# Event
* label: Événement
* description: occurrence significative ou passe

## who
* label: qui
* description: Personne ou chose liée à un événement

## what
* label: ce
* description: Ressource liée à un événement

## where
* label: où
* description: Lieu associé à un événement

## when
* label: lorsque
* description: Date associée à un événement
* remark: Recommandé ISO 8601 Date

## why
* label: pourquoi
* description: Concept associé à un événement

# Annotation
* label: Annotation
* description: Annotation, fournit des informations lâchement sur une ressource

## annotator
* label: annotateur
* description: Agent associé à l'annotation

## body
* label: corps
* description: Corps d'une annotation

## target
* label: la cible
* description: cible d'une annotation

# Collection
* label: Collection
* description: Agrégation ou le ramassage des œuvres

## primary
* label: travail principal
* description: travaux primaire associée à une collection

## memberOf
* label: membre du
* description: membre d'une collection

## isVersionOf
* label: est une version de
* description: Agent associé à l'annotation
