# Daily diff file with extended company data
Monitor important changes in companies

## GetListOfDiffs request
The request for a list [`DailyDiffList`](#DailyDiffList) of all events

> **Requested URL**: ```https://www.finstat.sk/api/getlistofdiffs```<br />
> **Hash parameter**: empty

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getlistofdiffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## GetFile request
The request for downloading of a concrete file that contains changes of a concrete date.
Returns data of requested **.zip** file

> **Requested URL**: ```https://www.finstat.sk/api/getfile```<br />
> **Hash parameter**: *{filename}*

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| file name as given in [GetListOfDiffs](#getlistofdiffs-request) |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getfile?filename=diff-2024-02-08.zip&apikey=YourAPIKey&hash=314ced77d148eb8e515e733c6ed73571e146480eecb2e06c02f39c0e990fc29c&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/diff-en.md ':include')

[](../../../common/responses/dailydiff-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/diff-daily.md ':include')