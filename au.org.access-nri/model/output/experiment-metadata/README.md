# Experiment metadata

This schema is used for metadata associated with a model experiment. A model experiment is loosely defined as a collection of one or more climate model datasets that each may comprise one a more files. Examples of a model experiment include:

- an ACCESS-CM2 historical run comprising many netcdf files that can be merged into distinct datasets (e.g. atmospheric daily data, ocean monthly data etc),
- a collection of CMIP6 data spanning multiple models, each comprising many netcdf files that can be merged into distinct datasets.

This schema describes the `metadata.yaml` files used by [Payu](https://github.com/payu-org/payu) and the [ACCESS-NRI Intake catalog](https://github.com/ACCESS-NRI/access-nri-intake-catalog).

## Extending the schema

To modify the schema, a [new version of the schema](https://github.com/ACCESS-NRI/schema?tab=readme-ov-file#versioning) will need to be created.

Note, this schema is related to the [`au.org.access-nri/model/output/file-metadata`](https://github.com/ACCESS-NRI/schema/tree/main/au.org.access-nri/model/output/file-metadata). Please consider whether edits are also needed there.
