# Deployment Special Packages Schema

This schema is used to mark certain packages as special in a model deployment repository.

Currently we have to special marks:

* `provenance`: That a package is recorded in the release provenance database. It is also automatically injected in the `spack.modules.tcl.default` section of the manifest.
* `injection`: That a package is injected into the `spack.modules.tcl.default` section of the manifest.

It is used in specific model deployment repositories `config` directories, such as [ACCESS-NRI/ACCESS-OM2](https://github.com/ACCESS-NRI/ACCESS-OM2/tree/main/config).

## Extending the schema

To modify the schema, a new version of the schema will need to be created.

1. Determine the new schema version: We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning. In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:
    * If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
    * If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
    * If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.

2. Create a new file for the new schema version, e.g. `1-0-1.json`
