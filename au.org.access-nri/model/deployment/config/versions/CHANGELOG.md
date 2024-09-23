# `Model Deployment Repo Versions` Schema Changelog

## 1-0-0

* Initial release

## 2-0-0

* Added required `spack` version. This hard requirement means this schema and historical data is not interoperable.

## 3-0-0

* Removed `spack-config` version as it is being incorporated into `build-cd` - see this [Pull Request](https://github.com/ACCESS-NRI/build-cd/pull/128). Since this was a `required` property in the schema, this schema is not interoperable with historical data.
