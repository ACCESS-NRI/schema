# ACCESS-NRI schema

## Overview

This repo contains first attempts to arrive at a common schema to describe various types of assets used/supported by ACCESS-NRI. The primary motivation for developing these schema at this stage is the development of the ACCESS-NRI Intake catalog.

## Schema Versioning

We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning in this repository.

In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:

* If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
* If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
* If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.

## Schema organisation

All ACCESS-NRI schema should be under the `au.org.access-nri` top-level directory. In this way this schema repository could contain copies of schema it does not "own" but that were used within the organisation.

Below the organisation top-level schema are organised by domain and purpose:
```
$ tree au.org.access-nri/
au.org.access-nri/
└── model
    ├── reproducibility
    │   └── checksums
    │       ├── 1-0-0.json
    │       ├── CHANGELOG.md
    │       └── README.md
    └── output
        ├── experiment-metadata
        │   ├── 1-0-0.json
        │   ├── 1-0-1.json
        │   ├── 1-0-2.json
        │   ├── 1-0-3.json
        │   ├── CHANGELOG.md
        │   └── README.md
        └── file-metadata
            ├── 1-0-0.json
            ├── 1-0-1.json
            ├── CHANGELOG.md
            └── README.md
```

## Updating schema

Note that new versions of schema are stored in different files named for the version. This can make it difficult to review a pull request which adds a new version as there is no useful `diff` information. The entire file is new.

When creating new versions of schema consider creating an initial commit that just copies the previous version into the new version, and then another separate commit that makes the required changes. This makes it easier to see what has changed, e.g. [GitHub has a feature to isolate changes to a single commit, or a specific range of commits](https://stackoverflow.com/a/50417336).

## Using schema

When downloading or referencing schema from this repo in other applications it is a good idea to use a specific commit of the schema. This will make your application more robust to future changes to this repo.

## CI in this Repository

Pull Requests and Pushes to this repository checks that the schema itself is valid according to a metaschema given in the `$schema` property. Please remember to add a `$schema` property to your schema, like so:

```json
{
    "$id": "https://raw.githubusercontent.com/ACCESS-NRI/schema/main/au.org.access-nri/path/to/schema/1-0-0.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "title": "A Cool Schema!"
}
```

## Custom Actions in this Repository

This repository has a `validate-with-schema` Github Actions action that should be used in conjunction with data that relies on a schema within this repository. See more in [the actions README.md](./.github/actions/validate-with-schema/README.md).
