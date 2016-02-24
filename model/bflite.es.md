<!--

Bibframe Lite es un punto de partida para vocabularios personalizados Bibframe
y perfiles. Es marco conformes a Bibframe y
link-compatible con la Biblioteca del Congreso de vocabulario Bibframe,
http://bibframe.org/

-->

# @docheader

* @iri:
    * @base: http://bibfra.me/vocab/lite/
    * @property: http://bibfra.me/purl/versa/support
* @language: es

# Resource

* label: Recurso
* description: La mayor entidad genérica Bibframe

## label

* label: etiqueta
* description: Cadena de texto que representa el nombre del recurso

## prefLabel

* label: etiqueta preferida
* description: Etiqueta preferida del recurso

## description

* label: descripción
* description: Descripción del recurso
* remark: Descripción del ejemplo de recursos bibliográficos puede incluir, pero no se limita a: un resumen, una tabla de contenidos, una representación gráfica, o una cuenta de texto libre del recurso.

## image

* label: imagen
* description: IRI que apunta a una imagen del recurso

## link

* label: vínculo
* description: IRI de un recurso

## rightsStatement

* label: declaración de derechos
* description: Declaración de los derechos asociados con el recurso de origen

## controlCode

* label: código de control
* description: Cadena alfanumérica o indicador usado para encontrar e identificar el recurso
* remark: Un identificador no basado en el IRI que refleja las prácticas de codificación locales o de la comunidad.

## related

* label: relacionado
* description: Recursos relacionados con el recurso de origen

## language

* label: idioma
* description: Idioma asociado con el recurso

# LanguageCategory

* label: Idioma Categoría
* description: Lista de idiomas
* remark: Un vocabulario controlado.

# Temporal

* label: Relación con Tiempo
* description: Se utiliza para indicar el contexto para el progreso continuo cronológico de la existencia y eventos en el pasado, presente y futuro.

## date

* label: fecha
* description: Fecha asociada con el recurso
* remark: Fecha recomendada ISO 8601

## dateStart

* label: fecha de inicio
* description: La fecha de inicio asociada con el recurso
* remark: Fecha recomendada ISO 8601

## dateEnd

* label: fecha del final
* description: Fecha de finalización asociada con el recurso
* remark: Fecha recomendada ISO 8601

## dateBirth

* label: fecha de nacimiento
* description: Fecha de nacimiento asociada con la persona
* remark: Fecha recomendada ISO 8601

## dateDeath

* label: fecha de la muerte
* description: Día de muerte asociado con la persona
* remark: Fecha recomendada ISO 8601

## audience

* label: audiencia
* description: Clase de usuario para el que el contenido de un recurso tiene por objeto, o en los que el contenido se considera adecuado

## note

* label: nota
* description: Información descriptiva adicional asociado con el recurso

# Authority

* label: Dominio
* description: Creíble, descripción curada de una persona, lugar o cosa

## name

* label: nombre
* description: Nombre de un vínculo de autoridad

## nameAlternative

* label: nombre alternativo
* description: Nombre alternativo de un dominio

## authorityLink

* label: enlazar de dominio
* description: Accionable IRI ligarse a un vocabulario controlado autorizada
* remark: Ejemplos incluyen identificadores VIAF, LCNAF, ISNI, ORCID, etc.

# Work

* label: Obra
* description: Creación intelectual o artística distinta

## title

* label: titulo
* description: Título del recurso

## titleAlternative

* label: título alternativo
* description: Título alternativo del recurso

## creator

* label: creador
* description: Entidad (o entidades) responsable de la creación del recurso origen

## contributor

* label: contribuyente
* description: Entidad (o entidades) que contribuyeron al origen de los recursos

## subject

* label: sujeto
* description: Índice plazo, sujeto plazo, encabezamientos de materia o descriptor, un término para la recuperación de información que captura la esencia del tema de un recurso
* remark: El 'ness-acerca' de una obra

## genre

* label: género
* description: Categoría de la composición artística que se caracteriza por las similitudes en la forma, el estilo, o el sujeto
* remark: The 'is-ness' of a work

# Agent

* label: Agente
* description: Entidad (por ejemplo persona, organización, etc.) asociado a un recurso

## email

* label: dirección de correo electrónico
* description: Dirección que identifica un buzón de correo electrónico a la que se entregan los mensajes de correo electrónico a un agente

# Person

* label: Persona
* description: Individual (vivo, muerto, muertos vivientes, o de ficción) en relación con un recurso

# Organization

* label: Organización
* description: Unidad de las personas, por ejemplo, una institución, una asociación o entidad corporativa

# Meeting

* label: Reunión
* description: Reunión formal de las personas para un fin determinado

# Family

* label: Familia
* description: Unidad social relacionadas por nacimiento, matrimonio, adopción, unión civil o relación similar

# Place

* label: Lugar
* description: Ubicación geográfica

# Category

* label: Categoría
* description: Lista de cosas considera que tiene determinadas características compartidas
* remark: Un vocabulario controlado.

# Topic

* label: Tema
* description: Asunto que describe un concepto, evento u objeto término general

# Form

* label: formar
* description: Categoría o género que describe lo que es el recurso

# Concept

* label: Concepto
* description: Término que describe el tema, aboutness, idea o concepto de un recurso

# Instance

* label: Instancia
* description: Realización individual de una obra

## instantiates

* label: ejemplariza
* description: Obra los crea instancias de recursos o los manifiestos
* remark: Para su uso para conectar las instancias a las obras en la estructura BIBFRAME.

## focus

* label: foco
* description: Entidad subyacente o focal asociada con un concepto
* remark: Muchas veces el foco es la principal entidad asociada a un concepto.

## subFocus

* label: foco sub
* description: Calificador o modificador usado para describir una entidad focal subyacente adicional asociado a un concepto.
* remark: Muchas veces las entidades de foco sub siguen el foco primario asociado a un concepto.

## provision

* label: provisión
* description: Proveedor asociado con el portador
* remark: La conexión a detalles como el lugar, el nombre y / o información actualizada referente a la publicación, impresión, distribución, emisión, liberación, o la producción de una instancia.

## copyright

* label: derechos de autor
* description: Caso de derechos de autor asociado a la instancia

## format

* label: formato
* description: Formato de archivo o medio físico de una instancia.

## medium

* label: medio
* description: Medio de la Instancia

## extent

* label: alcance
* description: Número de páginas físicas, volúmenes, casetes, tiempo total de reproducción, etc., de los de cada tipo de unidad

## dimensions

* label: dimensiones
* description: Medición de tamaño

# ProviderEvent

* label: Proveedor de Eventos
* description: Evento asociado con la publicación, impresión, distribución, emisión, la liberación o la producción de una Instancia

# CopyrightEvent

* label: Los Derechos de Autor de Eventos
* description: Caso de derechos de autor asociado a la propiedad intelectual de una Instancia.

## license

* label: licencia
* description: Licencia asociada con el evento de derechos asociada con una obra

## copyrightAgent

* label: agente de derechos de autor
* description: Agente asociado a los derechos de autor de una Instancia

## copyrightPlace

* label: lugar de derechos de autor
* description: Lugar asociado con el copyright de una Instancia

## copyrightDate

* label: fecha de derechos de autor
* description: Fecha asociada con los derechos de autor de una Instancia

## copyrightNote

* label: nota de derechos de autor
* description: Nota asociada a los derechos de autor de una Instancia

## providerAgent

* label: agente proveedor
* description: Agente asociado con la publicación, impresión, distribución, emisión, la liberación o la producción de una Instancia

## providerPlace

* label: lugar proveedor
* description: Lugar asociado con la publicación, impresión, distribución, emisión, la liberación o la producción de una Instancia

## providerDate

* label: fecha proveedor
* description: Fecha asociada con la publicación, impresión, distribución, emisión, la liberación o la producción de una Instancia

## providerNote

* label: nota proveedor
* description: Nota asociada con la publicación, impresión, distribución, emisión, la liberación o la producción de una instancia

# Event

* label: Evento
* description: Ocurrencia significativa o suceso

## who

* label: quien
* description: Persona o cosa relacionada con un evento

## what

* label: qué
* description: Recursos relacionados con un evento

## where

* label: dónde
* description: Lugar asociado con un evento

## when

* label: cuando
* description: Fecha asociada a un evento
* remark: Recomendada ISO 8601 fecha

## why

* label: por qué
* description: Concepto asociado con un evento

# Annotation

* label: Anotación
* description: Anotación, proporciona información pegada ligeramente sobre un recurso

## annotator

* label: anotador
* description: Agente asociado con la anotación

## body

* label: cuerpo
* description: Cuerpo de una anotación

## target

* label: objetivo
* description: Objetivo de una anotación

# Collection

* label: Colección
* description: La agregación o reunión de las obras

## primary

* label: trabajo principal
* description: El obro principal asociada a una colección

## memberOf

* label: miembro de
* description: Miembro de una colección

## isVersionOf

* label: es la versión de
* description: Obra de la que se trata de una versión
