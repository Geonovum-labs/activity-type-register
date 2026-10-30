# Activity Type Register

A general-purpose, engine- and format-agnostic vocabulary of Generic Profiles, 
independent of any one project. 
A Generic Profile gives one or more related operations an abstract I/O signature (named roles and abstract types, no format, no size limit)


The description can be longer. Both **the abstract** *and the description* support Markdown,
including [links](https://google.es).


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

A profile of the Registered Item Model for governed activity type records in the acttype:ActivityType hierarchy, with related PROV object types and an optional plan.

### `ogc.register.schemas.geoprocessing-activity-types-schema` — Geoprocessing Activity Types Profile Schema

**Type:** schema

A profile of the Activity Type Register Profile for geoprocessing activity types: registered sub-classes of geoproc:GeoprocessingActivityType, each required to use or generate at least one GeoSPARQL spatial data type.

### `ogc.register.schemas.st-ml-activity-types-schema` — SpatioTemporal ML Activity Types Profile Schema

**Type:** schema

A profile of the SpatioTemporal Machine learning Activity Types Profile describing spatiotemporal machine learning training and inference runs, and registrable ML activity types, using the STAC MLM extension's task, framework/accelerator and input/output vocabulary.

