# Telemetry for Release Provenance DB Schema Changelog

## 1-0-0

* Initial release

## 2-0-0

We need to keep track of both `ACCESS-NRI/access-spack-packages` and `spack/spack-packages` when we deploy to `spack >= 1.0`. We update the schema to reflect this:

* Add `deployment-target.access_spack_packages_[version|git_hash]`
* Add `deployment-target.builtin_spack_packages_[version|git_hash]`
* Remove `deployment-target.spack_packages_[version|git_hash]`
