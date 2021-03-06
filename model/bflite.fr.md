<!--

BIBFRAME Lite est un commencement pour les BIBFRAME vocabulaires customizés.
Cést un cadre qui se conforme à BIBFRAME et fonctionnel avec liens comme le
vocabulaire de la bibliothèque nationale des États Unis.
http://bibframe.org/

BIBFRAME constitue un fondement pour l’avenir de la description bibliographique adaptée à la fois au Web et, plus largement, au monde de réseaux interconnectés. Le vocabulaire Bibframe Lite fournit un ensemble de classes et de propriétés offrant une structure de base pour un modèle de données à couches multiples permettant à une telle description bibliographique.  

-->

# @docheader

* @iri:
    * @base: http://bibfra.me/vocab/lite/
    * @property: http://bibfra.me/purl/versa/support
* @language: fr

# Resource

* label: Ressource
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

* label: numéro ou code de contrôle
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
* label: public cible
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
* label: variante de nom
* description: Nom alternatif de la ressource autorisée

## authorityLink
* label: lien autorisé
* description: Lien résolu relatif à la ressource autorisée
* remark: Quelquechose comme VIAF, LCNAF, ISNI, ORCID, etc.

# Work
* label: Œuvre
* description: Création distincte, intellectuelle ou artistique

## title
* label: titre
* description: Titre de la ressource

## titleAlternative
* label: variante de titre
* description: Titre alternatif de la ressource

## creator
* label: créateur
* description: Entité primaire par quel la ressource etait originalement créé

## contributor
* label: contributeur
* description: Entité qui a fait contribution à la création originale de la ressource

## subject
* label: sujet
* description: Terme d'indice, sujet, ou description, un terme de rechercher d'information qui capture l'essence du sujet d'une ressource

## genre
* label: genre
* description: Catégorie de composition artistique caractérisé par des similitudes dans la forme, le style, ou du sujet

# Agent
* label: Agent
* description: Entité (par exemple, personne, organisation, etc.)

## email
* label: e-mail
* description: Adresse pour livraison des messages à un agent ou entité

# Person
* label: Personne
* description: Être humain, individu (vie, mort, morts-vivants, ou fictif)

# Organization
* label: Organisation
* description: Collectivité; Groupement, à caractère public ou non, de personnes, par exemple, une institution, une association ou personne morale

# Meeting
* label: Réunion
* description: Assemblée formelle de personnes

# Family
* label: Famille
* description: Unité sociale liés par la naissance, le mariage, l'adoption, l'union civile, ou relation similaire

# Place
* label: Lieu
* description: Endroit déterminé; emplacement géographique

# Category
* label: Catégorie
* description: Classe dans laquelle on répartit des ressources, des êtres de même nature
* remark: Conseillé d'utiliser les vocabulaires contrôlés

# Topic
* label: Thème
* description: Motif, sujet

# Form
* label: Forme
* description: Catégorie ou genre qui décrit la façon dont la ressource est présenté

# Concept
* label: Concept
* description: Terme décrivant un sujet, idée ou notion de la ressource

# Instance
* label: Instance
* description: Réalisation individuelle d'un œuvre

## instantiates
* label: manifeste
* description: Rends évident, représente la réalité d'un œuvre qu'un utilisateur puisse y accéder
* remark: Utilisé pour connecter les œuvre et instances dans la structure BIBFRAME.

## focus
* label: focus
* description: Centre d’intérêt d'un concept

## subFocus
* label: subfocus
* description: Facette d’intérêt parmi les aspects possible d'un concept

## provision
* label: disposition
* description: fournisseur de la porteur d'information
* remark: Détails tels que le lieu, le temps, et le nom relatives à la publication, impression, distribution, émission, libération, ou production d'une instance.

## copyright
* label: le droit d'auteur
* description: L’ensemble des droits dont dispose un auteur ou ses ayants droit (héritiers, sociétés de production) sur des œuvres de l’esprit originales et des droits corrélatifs du public à l'utilisation et à la réutilisation de ces œuvres sous certaines conditions

## format
* label: format
* description: Format de fichier ou support physique d'une instance

## medium
* label: médium
* description: Système de communication par lequel l'instance est exprimée

## extent
* label: mesure
* description: Nombre de pages physiques, des volumes, des cassettes, temps total de lecture, etc., de chaque type d'unité

## dimensions
* label: dimensions
* description: Mesure de la taille

# ProviderEvent
* label: Évènement relatif à l’instance
* description: Publication, impression, distribution, une émission, la libération ou la production d'une instance

# CopyrightEvent
* label: Événement relatif au droit d'auteur
* description: cas du droit d'auteur associé à la propriété intellectuelle d'une instance.

## license
* label: licence
* description: Conditions sous lequel on peut utiliser une instance

## copyrightAgent
* label: agent de droits d'auteur
* description: Agent qui représente le droit d'auteur

## copyrightPlace
* label: copyright lieu
* description: Lieu relatif au droit d'auteur

## copyrightDate
* label: date de copyright
* description: Date relatif au droit d'auteur

## copyrightNote
* label: note de copyright
* description: Note qui donne information relatif au droit d'auteur

## providerAgent
* label: agent associé à l’instance
* description: Agent associé à la publication, impression, distribution, émission, libération ou production d'une instance

## providerPlace
* label: lieu associé à l’instance
* description: Lieu associé à la publication, impression, distribution, émission, libération ou production d'une instance

## providerDate
* label: date associée à l’instance
* description: Date associé à la publication, impression, distribution, émission, libération ou production d'une instance

## providerNote
* label: note associée à l’instance
* description: Note associée à la publication, impression, distribution, émission, libération ou production d'une instance

# Event
* label: Événement
* description: Occurrence ou fait marquant

## who
* label: qui
* description: Personne ou chose liée à un événement

## what
* label: que
* description: Ressource liée à un événement

## where
* label: où
* description: Lieu associé à un événement

## when
* label: quand
* description: Date associée à un événement
* remark: Conseillé d'utiliser ISO 8601

## why
* label: pourquoi
* description: Concept associé à un événement

# Annotation
* label: Annotation
* description:  Lien ajoutée vers une métadonnée pour une ressource

## annotator
* label: annotateur
* description: Qui ajoute l'annotation

## body
* label: texte de l’annotation
* description: Information essential d'une annotation

## target
* label: prévu
* description: Métadonnée lié relatif aux données annotées

# Collection
* label: Compilation d’œuvres
* description: Agrégation ou le ramassage des œuvres

## primary
* label: œuvre principal
* description: Œuvre prédominante

## memberOf
* label: membre du
* description: Ensemble duquel c'est un élément

## isVersionOf
* label: version de
* description: Ressource duquel c'est un version
