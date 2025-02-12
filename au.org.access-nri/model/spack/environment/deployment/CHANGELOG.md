# `spack.yaml` Schema Changelog

## 1-0-5

* Updated `spack.specs` to allow > 1 specs allowed. The first spec is still used as a basis for deployment information.
* Updated `spack.specs` pattern to allow `=VERSION` after `@git.REF`

This has full interoperability with the earlier schema/data.

## 1-0-4

* Updated `spack.definitions` to require definitions for `ROOT_PACKAGE` and `ROOT_SPEC` iff `spack.specs` contains `"$ROOT_SPEC"`.
* Updated `spack.specs` to allow `"$ROOT_SPEC"` in speclist.

This has full interoperability with the earlier schema/data.

## 1-0-3

* Updated `spack.specs` pattern to allow variants following the `@git.VERSION`. This has full interoperability with the earlier schema.

## 1-0-2

* Updated `spack.packages.*.require[0]` syntax to allow for versions that have a `/` in them. For example, `spack.packages.mypackage.require[0] == @git.user/feature` allows the `mypackage` to use the branch `user/feature` as a version. This has full interoperability with the earlier schema.

## 1-0-1

* Modified regex of `spack.packages.*.require[0]` to include `=` as a symbol. This allows versions like `@git.2024.05.28=access-esm1.5`. See [issue](https://github.com/ACCESS-NRI/spack-packages/issues/111) and related [PR](https://github.com/ACCESS-NRI/build-cd/pull/87). This has full interoperability with the earlier schema.

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
