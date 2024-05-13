# Model Configuration Checksums

This schema is used for checksum files used as part of model reproducibility CI checks for model configurations. For example, the checksums are saved to released ACCESS-OM2 model configurations in the [ACCESS-NRI/access-om2-configs](https://github.com/ACCESS-NRI/access-om2-configs) repository. The pytests that are run as part of these CI tests that generate and compare checksums are in the [ACCESS-NRI/model-config-tests](https://github.com/ACCESS-NRI/model-config-tests/) repository.



## Extending the schema

To modify the schema, a new version of the schema will need to be created.

1. Determine the new schema version: We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning. In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:
    * If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
    * If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
    * If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.

2. Create a new file for the new schema version, e.g. `1-0-1.json`
