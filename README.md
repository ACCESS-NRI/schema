# ACCESS-NRI schema

## Overview

This repo contains first attempts to arrive at a common schema to describe various types of assets used/supported by ACCESS-NRI. The primary motivation for developing these schema at this stage is the development of the ACCESS-NRI Intake catalog.

## Versioning

We utilize [`SchemaVer`](https://docs.snowplow.io/docs/pipeline-components-and-applications/iglu/common-architecture/schemaver/) for schema versioning in this repository.

In a nutshell, `SchemaVer` is a `MODEL-REVISION-ADDITION` format, where:

* If adding changes that have no interoperability with the previous schema or historical data, the `MODEL` version should be incremented.
* If adding changes that may have interoperability with the previous schema and some historical data, increment the `REVISION` version.
* If adding changes that are interoperable with the previous schema and all historical data, increment the `ADDITION` version.
