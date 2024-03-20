# File metadata

This schema is used for metadata associated with a file containing or referencing climate model data. Examples of a file containing of referencing climate model data include:

- a single netcdf file output from an ACCESS-CM2 historical run,
- a [kerchunk](https://github.com/fsspec/kerchunk) reference file describing a climate dataset comprising many files.

This schema describes the file metadata in the [ACCESS-NRI Intake catalog](https://github.com/ACCESS-NRI/access-nri-intake-catalog).

## Extending the schema

To modify the schema, a [new version of the schema](https://github.com/ACCESS-NRI/schema?tab=readme-ov-file#versioning) will need to be created.

Note, this schema is related to the [`au.org.access-nri/model/output/experiment-metadata`](https://github.com/ACCESS-NRI/schema/tree/main/au.org.access-nri/model/output/experiment-metadata). Please consider whether edits are also needed there.
