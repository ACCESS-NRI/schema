# Experiment asset

*A collection of one or more datasets that each may comprise one or more [file assets](https://github.com/ACCESS-NRI/schema/blob/main/file_asset.md).*

Examples: 
- an ACCESS-CM2 historical run comprising many netcdf files (file assets) that can be merged into distinct datasets (e.g. atmospheric daily data, ocean monthly data etc)
- a collection of CMIP6 data spanning multiple models, each comprising many netcdf files that can be merged into distinct datasets

| Property | Expected type | Description | Notes | Enforce entry in `metadata.yaml` |
| --- | --- | --- | --- | --- |
| **name** | string | Name of the experiment asset  | Enforcing combination of only lowercase + uppercase letters, digits and underscores adds functionality to Intake catalog | :heavy_check_mark: |
| **uuid** | string | Unique uuid for the experiment asset  |  | :heavy_check_mark: |
| **short_description** | string | Short description of the experiment asset (< 150 char)  |  | :heavy_check_mark: |
| **long_description** | string | Long description of the experiment asset (no char limit) |  | :heavy_check_mark: |
| **model** | string or list of strings | The name of the model used |  |  |
| **contact** | string | Contact name |  |  |
| **email** | string | Contact email address |  |  |
| **created** | string | Initial creation date of experiment asset | This is the earliest relevant date | |
| **reference** | string | Citation or reference information | Could be in the form a DOI or a request, e.g "please consider citing blah" |  |
| **parent_experiment** | string | uuid for parent experiment if appropriate |  |  |
| **related_experiments** | list of string | uuids for any related experiment assets | Maybe this is overkill? |  |
| **notes** | string | Additional notes |  |  |
| **keywords** | list of string | Keywords to associated with experiment asset |  |  |
