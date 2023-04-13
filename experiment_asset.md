# Experiment asset

*A collection of one or more datasets that each may comprise one or more data assets.*

Example: an ACCESS-CM2 historical run comprising many netcdf files (data assets) that can be merged into distinct datasets (e.g. atmospheric daily data, ocean monthly data etc)

| Property | Expected type | Description | Entry required | Notes | in `metadata.yaml` |
| --- | --- | --- | --- | --- | --- |
| **name** | string | Name of the experiment asset | :heavy_check_mark: | Enforing combination of only lowercase + uppercase letters, digits and underscores adds functionality to Intake catalog | :heavy_check_mark: |
| **uuid** | string | Unique uuid for the experiment asset | :heavy_check_mark: |  | :heavy_check_mark: |
| **short_description** | string | Short description of the experiment asset (< 150 char) | :heavy_check_mark: |  | :heavy_check_mark: |
| **long_description** | string | Long description of the experiment asset (no char limit) | :heavy_check_mark: |  | :heavy_check_mark: |
| **model** | string | The name of the model used |  |  | :heavy_check_mark: |
| **contact** | string | Contact name |  |  | :heavy_check_mark: |
| **email** | string | Contact email address |  |  | :heavy_check_mark: |
| **created** | string | Initial creation date of experiment asset |  | This is the earliest relevant date | :heavy_check_mark: |
| **reference** | string | Citation or reference information |  | Could be in the form a DOI or a request, e.g "please consider citing blah" | :heavy_check_mark: |
| **related_experiments** | list of string | uuids for any related experiment assets |  | Maybe this is overkill? | :heavy_check_mark: |
| **notes** | string | Additional notes |  |  | :heavy_check_mark: |
| **keywords** | list of string | Keywords to associated with experiment asset |  |  | :heavy_check_mark: |
