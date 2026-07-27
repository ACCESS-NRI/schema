# Deployment Packages Location Schema

> [!IMPORTANT]
> This schema is deprecated for MDR/SDRs using `build-cd@v9` or later, as that information is now in the `spack.yaml`. This config information is now in the [MDR `spack.yaml` schema](./../../../spack/environment/deployment/) from `3-0-0` onwards, or the [SDR `spack.yaml` schema](./../../../../tools/spack/environment/deployment/) from `2-0-0` onwards.

This schema is used to specify versions of various repositories that are needed in the deployment of a specific model using `spack`.

It is used in specific model repositories `config` directories, such as [ACCESS-NRI/ACCESS-OM2](https://github.com/ACCESS-NRI/ACCESS-OM2/tree/main/config).

## Extending the schema

To modify the schema, a new version of the schema will need to be created.

1. Determine the new schema version: We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning. In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:
    * If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
    * If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
    * If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.

2. Create a new file for the new schema version, e.g. `1-0-1.json`
