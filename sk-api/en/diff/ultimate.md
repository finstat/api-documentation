# Daily diff file with detailed company data
Monitoring of critical events and persons in companies

## GetListOfUltimateDiffs request
The request for a list [`DailyDiffList`](#DailyDiffList) of all events

> **Requested URL**: ```https://www.finstat.sk/api/getlistofultimatediffs```<br />
> **Hash parameter**: empty

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getlistofultimatediffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## GetUltimateFile request
The request for downloading of a concrete file that contains changes of a concrete date.
Returns data of requested **.zip** file

> **Requested URL**: ```https://www.finstat.sk/api/getultimatefile```<br />
> **Hash parameter**: *{filename}*

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| file name as given in [GetListOfUltimateDiffs](#getlistofultimatediffs-request) |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getultimatefile?filename=ultimatediff-2024-02-08.zip&apikey=YourAPIKey&hash=50fce1c887049c20d0861d5173170e9d4d1a1db0bf4ba4c541bb4f19e5a154c2&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/diff-en.md ':include')

[](../../../common/responses/dailydiff-en.md ':include')

[](../../../common/responses/extendeddiff-en.md ':include')

[](../../../common/responses/ultimatediff-en.md ':include')

[](../../../common/responses/extendeddiffother-en.md ':include')

[](../../../common/responses/ultimatediffother-en.md':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/diff-ultimate.md ':include')