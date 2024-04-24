# `spack.yaml` Schema Changelog

## 1-0-0

* Initial release
* Contains rules constraining the use of `spack.yaml` features:
  * `spack.specs`:
    * Disallowing `spack.specs.matrix`
    * Disallowing `spack.specs.*` == `null`
    * Having a single root SBD of the format `<model>@git.<version>`
  * `spack.packages`:
    * Disallowing `spack.packages.require` in it's non-`array` format
    * Package definitions in `spack.packages` having a version in the `spack.packages.require[0]` section - the others are fine
