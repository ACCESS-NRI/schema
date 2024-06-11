# Validate With Schema Action

This action validates a `json` or `yaml` file using a given schema. Essentially acts as a convenience wrapper over `GrantBirki/json-yaml-validate`.

## Inputs

| Name | Type | Description | Required | Default | Example |
| ---- | ---- | ----------- | -------- | ------- | ------- |
| `schema-version` | `string` | Version of the schema required in SchemaVer | `true` | N/A | `"1-0-0"` |
| `schema-location` | `string` | Directory within access-nri/schema that contains the schema | `true` | N/A | `"access-nri.org.au/deployment/config/versions"` |
| `data-location` | `string` | Path(s) to the json/yaml data file(s) in the callers repository. File is either `.json` or `.yml`/`.yaml` | `true` | N/A | `"./some/data.json"` or `"/path/to/some/data.yaml"` or ```./file1 \n ./file2``` if newline-separated |
| `meta-schema-location` | `string` | Meta schema version of the schema required | `false` | `"draft-07"` | `"draft-07"` or `"draft-2019-09"` or `"draft-2020-12"` |

## Outputs

No direct outputs but failure of this job indicates a failure of validation.

## Example

```yaml
# ...
steps:
  - name: Validate
    # This will validate some/data.json against this repositories deployment/config/versions/2-0-0.json
    uses: access-nri/schema/.github/actions/validate-with-schema@main
    with:
      schema-location: access-nri.org.au/deployment/config/versions
      schema-version: 2-0-0
      data-location: some/data.json
```
