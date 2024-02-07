# ACCESS-OM2 Checksums

This schema is used for checksum files generated as part of ACCESS-OM2 
reproducibility CI checks for model configurations in the 
[ACCESS-NRI/access-om2-configs](https://github.com/ACCESS-NRI/access-om2-configs)
repository.

## Extending the schema
To modify the schema, a new version of the schema will need to be created.
1. Determine the new schema version:
    If adding breaking changes, the major version should be incremented. 
    If adding non-breaking changes, e.g. adding a new field, or extending a type, increment the minor version.
1. Create a new file for the new schema version, e.g. `access-om2-checksums-$VERSION.json`
2. Once this change has been merged into the `main` branch, push a
new tag with the format `access-om2-checksums-$VERSION`