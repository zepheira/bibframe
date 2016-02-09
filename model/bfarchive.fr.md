<!---

Bibframe Lite + Archive

Archive Bibframe est un point de départ pour la description archivistique qui se fonde sur le vocabulaire 
Bibframe Lite. Il est conforme au cadre Bibframe et Archives Décrire: Une norme de contenu (DACS). 
Lorsque cela est possible, le vocabulaire est lien-compatible avec le vocabulaire BIBFRAME de la Bibliothèque du Congrès.

Actuellement, nous analysons les normes de codage y compris Encoded Archival Description et archivistique 
encodée organes Contexte-entreprise pour développer Bibframe Archive et outils prototypes pour transformer 
XML pour les données liées. Nous nous félicitons de la rétroaction des archives et de métadonnées professionnels. 
Pour fournir des commentaires ou demander plus d'informations sur Archive Bibframe, s'il vous plaît contacter 
Gloria Gonzalez au gloria (at) zepheira (dot) com.

Vous remarquerez que les termes Archives BIBFRAME utilisent un humpCase / convention HumpCase,
qui découle de l'héritage BIBFRAME.

-->

# @docheader

* @iri:
    * @base: http://bibfra.me/vocab/archive/
    * @property: http://bibfra.me/purl/versa/support
* @language: fr
* title: Bibframe Archive vocabulary
* @interpretations:
    * scope: @resource

# Archive
* label: Archive
* description: Placez d'accès, de curé, et de stocker des collections d'archives de documents historiques ou des documents fournissant des informations sur les lieux, les institutions, les groupes des peuples, des événements et l'activité créatrice.

# FindingAid
* label: Instrument de recherche
* description: Document utilisé pour donner le contrôle physique et intellectuel référentiel sur les matériaux, et d'aider les utilisateurs à accéder à et de comprendre les collections d'archives.

# Repository
* label: Dépôt
* description: Organisation qui stocke et gère des documents d'archives.
* remark: Équivalent à Nom du Référentiel Élément (2.2) dans la description Archives: une norme de contenu, 2e édition (2015).

# Box
* label: Box
* description: Box qui contient des documents d'archives.
* properties: contains

# Folder
* label: Dossier
* description: Dossier contenant des documents d'archives.
* properties: contains

# Item
* label: Item
* description: Item ou un objet d'archivage.
* properties: scopeContent referenceCode

# File
* label: Limer
* description: Objet numérique. Un fichier est une séquence de données binaires et est décrit par certaines métadonnées d'accompagnement. Les métadonnées comprend généralement au métadonnées techniques de base moins y compris la taille, le type de contenu, la date de modification, etc., ainsi que les propriétés liées à la préservation, processus de numérisation, la provenance, etc.
* remark: Équivalent à PCDM:Limer.

## contains
* label: contenir
* description: Une partie de la relation

## arranger
* label: arrangeur
* description: Personne qui travaille pour donner accès aux collections d'archives de documents historiques ou des documents fournissant des informations sur les lieux, les institutions, les groupes des peuples, des événements et l'activité créatrice.

## addressRepository 
* label: adresse référentiel
* description: Adresse de l'exploitation organisation ou référentiel.
* remark: Équivalent à Lieu de dépôt Element (2.2) dans les archives Décrire: une norme de contenu, 2e édition (2015).

## eadId
* label: identificateur de l'EAD
* description: Désigne un code unique pour un document d'aide à la constatation particulière EAD.
* remark: Équivalent à EAD ID <eadid>

## referenceCode
* label: code de référence
* description: Un identifiant local ou un référentiel pour la collecte d'archives, boîte, dossier ou un item.
* remark: Équivalent à Code de référence Element 2.1 dans les archives Décrire: une norme de contenu, 2e édition (2015). Au plus haut niveau de description, cela est souvent connu comme le numéro de collection, par exemple, pour UARS745 Archives de l'Université de la fiche de la série 745.

## extent
* label: ampleur
* description: Utilisée pour identifier et décrire l'étendue physique ou logique et le moyen de l'unité de description. Souvent mesurée dans l'espace d'étagère linéaire ou espace de stockage cube de l'unité de description, ou la quantité de fichiers numériques et de l'espace de stockage.
* remark: Équivalent à étendre Element 2.5 dans les archives Décrire: une norme de contenu, 2e édition (2015).

## scopeContent
* label: portée et le contenu
* description: Portée et contenu note. 
* remark: Équivalent à portée et le contenu Element 3.1 pour décrire les archives: une norme de contenu, 2e édition (2015).

## accessConditions
* label: conditions d'accès
* description: Note sur les conditions d'accès à un fonds d'archives.
* remark: Équivalent à la portée et les conditions d'accès Element 4.1 dans les archives Décrire: une norme de contenu, 2e édition (2015).
