# ACCESS-OM2 Checksums

This schema is used for checksum files generated as part of ACCESS-OM2
reproducibility CI checks for model configurations in the
[ACCESS-NRI/access-om2-configs](https://github.com/ACCESS-NRI/access-om2-configs)
repository.

## Extending the schema

To modify the schema, a new version of the schema will need to be created.

1. Determine the new schema version: We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning. In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:
    * If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
    * If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
    * If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.

2. Create a new file for the new schema version, e.g. `access-om2-checksums_$VERSION.json`

3. Once this change has been merged into the `main` branch, push a
new tag with the format `access-om2-checksums_$VERSION`
