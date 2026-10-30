# Activity Type Register

A general-purpose, engine- and format-agnostic vocabulary of Generic Profiles, 
independent of any one project. 
A Generic Profile gives one or more related operations an abstract I/O signature (named roles and abstract types, no format, no size limit)


The profiles in this register are implemented as classes of the Registered Item Model, which lives in a separate [register](https://ogcincubator.github.io/registered-item-model/). 
The intent for this register is to be the genereric 'top level' register that federated registers can inherit from for specific activity profiles in the respective domains.


## Building Blocks

### `ogc.register.activity-types` — Activity Types Register Profile

**Type:** model

A profile of the Registered Item Model for governed activity type records in the acttype:ActivityType hierarchy, with related PROV object types and an optional plan.

### `ogc.register.geoprocessing-activity-types` — Geoprocessing Activity Types Profile

**Type:** model

A profile of the Activity Type Register Profile for geoprocessing activity types: registered sub-classes of geoproc:GeoprocessingActivityType, each required to use or generate at least one GeoSPARQL spatial data type.

### `ogc.register.st-ml-activity-types` — SpatioTemporal ML Activity Types Profile

**Type:** model

A profile of the SpatioTemporal Machine learning Activity Types Profile describing spatiotemporal machine learning training and inference runs, and registrable ML activity types, using the STAC MLM extension's task, framework/accelerator and input/output vocabulary.

### `ogc.register.schemas.activity-types-schema` — Activity Types Register Profile Schema

**Type:** schema

This is a schema representation of the ogc.register.activity-types model

### `ogc.register.schemas.geoprocessing-activity-types-schema` — Geoprocessing Activity Types Profile Schema

**Type:** schema

This is a schema representation of the ogc.register.geoprocessing-activity-types model

### `ogc.register.schemas.st-ml-activity-types-schema` — SpatioTemporal ML Activity Types Profile Schema

**Type:** schema

This is a schema representation of the ogc.register.st-ml-activity-types model

