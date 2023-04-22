# File asset

*A file containing or referencing climate data*

Many file assets may constitute an [experiment asset](https://github.com/ACCESS-NRI/schema/blob/main/experiment_asset.md)

Examples: 
- a single netcdf file output from an ACCESS-CM2 historical run

| Property | Expected type | Description | Notes | core column in new intake-esm catalog |
| --- | --- | --- | --- | --- |
| **path** | string | The path to the file asset | | :heavy_check_mark: |
| **realm** | string | The realm of the variables in the asset | | :heavy_check_mark: (allow "aerosol", "atmos", "ice", "land", "multi", "ocean") |
| **variable** | string, list of string | The variable(s) in the asset | | :heavy_check_mark: (enforce as list) |
| **variable_long_name** | string, list of string | The long name of the variable(s) in the asset | | :heavy_check_mark: (enforce as list) |
| **frequency** | string | The frequency of the variables in the asset | | :heavy_check_mark: (allow "fx", "subhr", "\d+hr", "\d+day", "\d+mon", "\d+yr", "\d+dec") |
| **start_date** | string | The start date of the file | | :heavy_check_mark: (allow "%Y-%m-%d, %H:%M:%S") |
| **end_date** | string | The end date of the file | | :heavy_check_mark: (allow "%Y-%m-%d, %H:%M:%S") |
| **units** | string, list of string | The units of the variable(s) in the asset | | |
| **variable_standard_name** | string, list of string | The standard name of the variable(s) in the asset | | |
| **nominal_resolution** | string | The nominal resolution | Perhaps restrict to "[\d.]+ km", "\dx\d degree" to overlap with CMIP6 | |
