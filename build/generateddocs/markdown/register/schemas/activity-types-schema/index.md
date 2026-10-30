
# Activity Types Register Profile Schema (Schema)

`ogc.register.schemas.activity-types-schema` *v0.3*

This is a schema representation of the ogc.register.activity-types model

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### example Activity Type
A general activity type
#### json
```json
 {
    "id": "Activity",
    "title": "Example of a generic processing activity ",
    "description": "This activity is a general activity described with provenance information.",
    "version": "2.0.0",
    "type": "activity-type",
    "itemClass": "rim:RegisterItemClass",
    "objectIdentifier": "https://example.org/registers/activity/v1",
    "validityStatus": "invalid",
    "publicationStatus": "unpublished",
    "inRegister": "https://example.org/registers/activity-types",
    "realizes": "https://example.org/def/activity"
}
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/activity-type-register/build/annotated/register/schemas/activity-types-schema/context.jsonld",
  "id": "Activity",
  "title": "Example of a generic processing activity ",
  "description": "This activity is a general activity described with provenance information.",
  "version": "2.0.0",
  "type": "activity-type",
  "itemClass": "rim:RegisterItemClass",
  "objectIdentifier": "https://example.org/registers/activity/v1",
  "validityStatus": "invalid",
  "publicationStatus": "unpublished",
  "inRegister": "https://example.org/registers/activity-types",
  "realizes": "https://example.org/def/activity"
}
```

#### ttl
```ttl
@prefix dct: <http://purl.org/dc/terms/> .
@prefix rim: <https://w3id.org/ogc/rim/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/Activity> a <file:///github/workspace/activity-type> ;
    dct:description "This activity is a general activity described with provenance information." ;
    dct:title "Example of a generic processing activity " ;
    rim:inRegister <https://example.org/registers/activity-types> ;
    rim:itemClass rim:RegisterItemClass ;
    rim:objectIdentifier "https://example.org/registers/activity/v1"^^xsd:anyURI ;
    rim:publicationStatus rim:unpublished ;
    rim:realizes <https://example.org/def/activity> ;
    rim:validityStatus rim:invalid ;
    rim:version "2.0.0" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
title: Activity Type
description: 'A registered activity type based on the Registered Item Model.

  '
allOf:
- $ref: https://geonovum-labs.github.io/registered-item-model/build/annotated/rim/schemas/register-item/schema.yaml
- type: object
  properties:
    usedEntityType:
      type: string
      format: uri
      description: "A type of prov:Entity that activities of this type use (prov:used)
        \u2014 for example a type of input dataset."
      x-jsonld-id: https://w3id.org/ogc/rim/activity-type/usedEntityType
      x-jsonld-type: '@id'
    generatedEntityType:
      type: string
      format: uri
      description: "A type of prov:Entity that activities of this type generate (prov:generated)
        \u2014 for example a type of output product."
      x-jsonld-id: https://w3id.org/ogc/rim/activity-type/generatedEntityType
      x-jsonld-type: '@id'
    associatedAgentType:
      type: string
      format: uri
      description: A type of prov:Agent (for example prov:Person, prov:SoftwareAgent,
        or a narrower role-bearing type) that activities of this type are associated
        with (prov:wasAssociatedWith).
      x-jsonld-id: https://w3id.org/ogc/rim/activity-type/associatedAgentType
      x-jsonld-type: '@id'
    informedByActivityType:
      type: string
      format: uri
      description: "A type of acttype:ActivityType whose instances typically inform
        activities of this type (prov:wasInformedBy) \u2014 for example an upstream
        preparation activity type."
      x-jsonld-id: https://w3id.org/ogc/rim/activity-type/informedByActivityType
      x-jsonld-type: '@id'
  unevaluatedProperties: true
x-jsonld-extra-terms:
  id: '@id'
  type: '@type'
  title: http://purl.org/dc/terms/title
  description: http://purl.org/dc/terms/description
  version: http://www.w3.org/2002/07/owl#versionInfo
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  owl: http://www.w3.org/2002/07/owl#
  acttype: https://w3id.org/ogc/rim/activity-type/
  rim: https://w3id.org/ogc/rim#
x-bblocks-metadata:
  itemIdentifier: ogc.register.schemas.activity-types-schema
  register: https://geonovum-labs.github.io/activity-type-register/build/register.json
  version: '0.3'
  dateOfLastChange: '2026-10-30'

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/activity-type-register/build/annotated/register/schemas/activity-types-schema/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/activity-type-register/build/annotated/register/schemas/activity-types-schema/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Register": "rim:Register",
    "RegisterSystem": "rim:RegisterSystem",
    "RegisterSpecification": "rim:RegisterSpecification",
    "RegisterItemClass": "rim:RegisterItemClass",
    "RegisterItem": "rim:RegisterItem",
    "RegisterAction": "rim:RegisterAction",
    "Concept": "rim:Concept",
    "ConceptVersion": "rim:ConceptVersion",
    "ConceptSystem": "rim:ConceptSystem",
    "Commitment": "rim:Commitment",
    "Agent": "prov:Agent",
    "Organization": "prov:Organization",
    "Person": "prov:Person",
    "label": "rdfs:label",
    "prefLabel": "skos:prefLabel",
    "definition": "skos:definition",
    "inScheme": {
      "@id": "skos:inScheme",
      "@type": "@id"
    },
    "runsOn": {
      "@id": "rim:runsOn",
      "@type": "@id"
    },
    "hasSpecification": {
      "@id": "rim:hasSpecification",
      "@type": "@id"
    },
    "definesSubstantiveChange": "rim:definesSubstantiveChange",
    "registerOwner": {
      "@id": "rim:registerOwner",
      "@type": "@id"
    },
    "registerManager": {
      "@id": "rim:registerManager",
      "@type": "@id"
    },
    "controlBody": {
      "@id": "rim:controlBody",
      "@type": "@id"
    },
    "registerSystemManager": {
      "@id": "rim:registerSystemManager",
      "@type": "@id"
    },
    "registerUser": {
      "@id": "rim:registerUser",
      "@type": "@id"
    },
    "hasCommitment": {
      "@id": "rim:hasCommitment",
      "@type": "@id"
    },
    "commitmentCategory": {
      "@id": "rim:commitmentCategory",
      "@type": "@vocab"
    },
    "access": "rim:accessCommitment",
    "persistence": "rim:persistenceCommitment",
    "transparency": "rim:transparencyCommitment",
    "definedIn": {
      "@id": "rim:definedIn",
      "@type": "@id"
    },
    "validatedBy": {
      "@id": "rim:validatedBy",
      "@type": "@id"
    },
    "versionOf": {
      "@id": "rim:versionOf",
      "@type": "@id"
    },
    "version": "rim:version",
    "valid": "rim:valid",
    "invalid": "rim:invalid",
    "published": "rim:published",
    "unpublished": "rim:unpublished",
    "appliesTo": {
      "@id": "rim:appliesTo",
      "@type": "@id"
    },
    "proposer": {
      "@id": "rim:proposer",
      "@type": "@id"
    },
    "actionType": {
      "@id": "rim:actionType",
      "@type": "@vocab"
    },
    "addition": "rim:additionAction",
    "publish": "rim:publishAction",
    "unpublish": "rim:unpublishAction",
    "invalidation": "rim:invalidationAction",
    "supersession": "rim:supersessionAction",
    "redaction": "rim:redactionAction",
    "deletion": "rim:deletionAction",
    "changeClassification": {
      "@id": "rim:changeClassification",
      "@type": "@vocab"
    },
    "substantive": "rim:substantiveChange",
    "clarifying": "rim:clarifyingChange",
    "correctional": "rim:correctionalChange",
    "startedAtTime": {
      "@id": "prov:startedAtTime",
      "@type": "xsd:dateTime"
    },
    "endedAtTime": {
      "@id": "prov:endedAtTime",
      "@type": "xsd:dateTime"
    },
    "wasAssociatedWith": {
      "@id": "prov:wasAssociatedWith",
      "@type": "@id"
    },
    "id": "@id",
    "type": "@type",
    "objectIdentifier": {
      "@id": "rim:objectIdentifier",
      "@type": "xsd:anyURI"
    },
    "functionalIdentifier": {
      "@id": "rim:functionalIdentifier",
      "@type": "xsd:anyURI"
    },
    "itemClass": {
      "@id": "rim:itemClass",
      "@type": "@id"
    },
    "inRegister": {
      "@id": "rim:inRegister",
      "@type": "@id"
    },
    "realizes": {
      "@id": "rim:realizes",
      "@type": "@id"
    },
    "validityStatus": {
      "@id": "rim:validityStatus",
      "@type": "@vocab"
    },
    "publicationStatus": {
      "@id": "rim:publicationStatus",
      "@type": "@vocab"
    },
    "isRedacted": {
      "@id": "rim:isRedacted",
      "@type": "xsd:boolean"
    },
    "isDeleted": {
      "@id": "rim:isDeleted",
      "@type": "xsd:boolean"
    },
    "title": "dct:title",
    "description": "dct:description",
    "relatedItem": {
      "@id": "rim:relatedItem",
      "@type": "@id"
    },
    "supersededBy": {
      "@id": "rim:supersededBy",
      "@type": "@id"
    },
    "supersedes": {
      "@id": "rim:supersedes",
      "@type": "@id"
    },
    "hasAction": {
      "@id": "rim:hasAction",
      "@type": "@id"
    },
    "usedEntityType": {
      "@id": "rim:activity-type/usedEntityType",
      "@type": "@id"
    },
    "generatedEntityType": {
      "@id": "rim:activity-type/generatedEntityType",
      "@type": "@id"
    },
    "associatedAgentType": {
      "@id": "rim:activity-type/associatedAgentType",
      "@type": "@id"
    },
    "informedByActivityType": {
      "@id": "rim:activity-type/informedByActivityType",
      "@type": "@id"
    },
    "rim": "https://w3id.org/ogc/rim/",
    "prov": "http://www.w3.org/ns/prov#",
    "dct": "http://purl.org/dc/terms/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "acttype": "rim:activity-type/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/activity-type-register/build/annotated/register/schemas/activity-types-schema/context.jsonld)

## Sources

* [W3C PROV-O](https://www.w3.org/TR/prov-o/)
* [P-Plan Ontology](https://www.opmw.org/model/p-plan/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/activity-type-register](https://github.com/Geonovum-labs/activity-type-register)
* Path: `_sources/schemas/activity-types-schema`

