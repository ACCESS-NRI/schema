# General Software `spack.yaml` Schema Changelog

## 2-0-0

* Require reserved definitions for `_spack-version`, `_provenance`, `_injection`
* Require `spack.repos.access_spack_packages` section, with a constant `spack.repos.access_spack_packages.destination`
* Optional reserved definition for `_custom-scopes`

## 1-0-0

* Initial release
* Based on `au.org.access-nri/model/spack/environment/deployment/1-0-7.json`, except:
  * There is no restriction on `spack.specs` Versioning
  * There is no restriction on `spack.packages` Versioning
