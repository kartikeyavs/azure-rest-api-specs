## AzureResourceSchema

These settings apply only when `--azureresourceschema` is specified on the command line.

### AzureResourceSchema multi-api

``` yaml $(azureresourceschema) && $(multiapi)
# include the azure profile definitions from the standard location
require: ../../../profiles/readme.md

output-folder: $(azureresourceschema-folder)/schemas

# all the input files across all versions
input-file:
  - Microsoft.ResourceGraph/preview/2020-04-01-preview/resourcegraph.json
  - Microsoft.ResourceGraph/stable/2019-04-01/resourcegraph.json
  - Microsoft.ResourceGraph/preview/2018-09-01-preview/resourcegraph.json
  - Microsoft.ResourceGraph/preview/2018-09-01-preview/graphquery.json

```