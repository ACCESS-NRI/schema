# Climate model experiment asset

*A collection of one or more climate model datasets that each may comprise one or more [climate model file assets](https://github.com/ACCESS-NRI/schema/blob/main/file_asset.md).*

Examples: 
- an ACCESS-CM2 historical run comprising many netcdf files (file assets) that can be merged into distinct datasets (e.g. atmospheric daily data, ocean monthly data etc)
- a collection of CMIP6 data spanning multiple models, each comprising many netcdf files that can be merged into distinct datasets

| Property | Expected type | Description | Notes | In `metadata.yaml` (double for enforced) | Column in metacatalog |
| --- | --- | --- | --- | --- | --- |
| **name** | string | Name of the experiment asset  | Enforcing combination of only lowercase + uppercase letters, digits and underscores adds functionality to Intake catalog | :heavy_check_mark: :heavy_check_mark: | :heavy_check_mark: |
| **experiment_uuid** | string | Unique uuid for the experiment asset  |  | :heavy_check_mark: :heavy_check_mark: |  |
| **short_description** | string | Short description of the experiment asset (< 150 char)  |  | :heavy_check_mark: :heavy_check_mark: | :heavy_check_mark: ("description") |
| **long_description** | string | Long description of the experiment asset (no char limit) |  | :heavy_check_mark: :heavy_check_mark: |  |
| **model** | string or list of strings | The name of the model(s) used in the experiment |  | :heavy_check_mark: | :heavy_check_mark: |
| **realm** | string or list of strings | The realms included in the experiment | Would be helpful to enforce a vocab, e.g. CMIP6 |  | :heavy_check_mark: |
| **frequency** | string or list of strings | The frequency(/ies) included in the experiment | Would be helpful to enforce a vocab e.g. "fx", "subhr", "\d+hr", "\d+day", "\d+mon", "\d+yr", "\d+dec" |  | :heavy_check_mark: |
| **variable** | string or list of strings | The variable(s) included in the experiment |  |  | :heavy_check_mark: |
| **nominal_resolution** | string or list of strings | The nominal resolution(s) of model(s) used in the experiment | Difficult to enforce a vocab | :heavy_check_mark: | |
| **version** | string | The version of the experiment | | :heavy_check_mark: | |
| **contact** | string | Contact name |  | :heavy_check_mark: |  |
| **email** | string | Contact email address |  | :heavy_check_mark: |  |
| **created** | string | Initial creation date of experiment asset | This is the earliest relevant date | :heavy_check_mark: |  |
| **reference** | string | Citation or reference information | Could be in the form a DOI or a request, e.g "please consider citing blah" | :heavy_check_mark: |  |
| **parent_experiment** | string | uuid for parent experiment if appropriate |  | :heavy_check_mark: |  |
| **related_experiments** | list of string | uuids for any related experiment assets | Maybe this is overkill? | :heavy_check_mark: |  |
| **notes** | string | Additional notes |  | :heavy_check_mark: |  |
| **keywords** | list of string | Keywords to associated with experiment asset |  | :heavy_check_mark: |  |
