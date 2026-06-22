# MDR `config/auto-configs-pr.json` Schema Changelog

## 1-0-1

* Allows a profile to be associated with a particular workflow manager - currently only payu or rose-cylc.

## 1-0-0

* Initial release
* Allows a set of different model configuration *profiles* which contain model configurations to open PRs for (and optionally run repro checks against) for a given model configurations repository.
* Requires a `default` profile to be specified
