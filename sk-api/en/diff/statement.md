#  Daily diff files for company financial statements
This API provides a way to access data without the need to query the API for changes every day. The API generates a change file for each day when a change occurred, containing the latest changes in the financial statements.

Companies that have not had any changes for a while have statements in files generated after the latest statement was published.

The API is an incremental export, so some statements may be found in multiple files, with the current value always in the export with the latest date

## GetListOfStatementDiffs request
The request to get a list [`DailyDiffList`](#DailyDiffList) of all change files

> **Requested URL**: ```https://www.finstat.sk/api/getlistofstatementdiffs```<br />
> **Hash parameter**: prázdny text

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getlistofstatementdiffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-sk.md ':include')

## GetStatementFile request
The request for downloading of a concrete file that contains changes of a concrete date.
Returns data of requested **.zip** file

> **Requested URL**: ```https://www.finstat.sk/api/getstatementfile```<br />
> **Hash parameter**: *{filename}*

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| file name as given in  [GetListOfStatementDiffs](#getlistofstatementdiffs-request) |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatementfile?filename=statementdiff-2024-02-08.zip&apikey=YourAPIKey&hash=fe0198c59c4df2e7016181b809aadbce48a5006935038c4500111209b3c48686&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

## GetStatementLegend request
Gets the legend [`KeyValue`](#KeyValue) in given language for keys of the statement files

> **Requested URL**: ```https://www.finstat.sk/api/getstatementlegend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/lang-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatementlegend?lang=sk&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/diff-en.md ':include')

[](../../../common/responses/dailydiff-en.md ':include')

[](../../../common/responses/keyvalue-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML responses
[](../../../common/examples/diff-statement.md ':include')

[](../../../common/examples/diff-statement-legend.md ':include')