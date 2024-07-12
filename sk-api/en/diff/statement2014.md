# Daily diff files for company financial statements (template 2014)
This API provides a way to access data without the need to query the API for changes every day. The API generates a change file for each day when a change occurred, containing the latest changes in the financial statements.

The API includes information about all financial statements with the 2014 template. Companies that have not had any changes for a while have statements in files generated after the latest statement was published.

The API is an incremental export, so some statements may be found in multiple files, with the current value always in the export with the latest date

## GetListOfStatement2014Diffs request
The request to get a list [`DailyDiffList`](#DailyDiffList) of all change files

> **Requested URL**: ```https://www.finstat.sk/api/getlistofstatement2014diffs```<br />
> **Hash parameter**: prázdny text

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getlistofstatement2014diffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-sk.md ':include')

## GetStatement2014File request
The request for downloading of a concrete file that contains changes of a concrete date.
Returns data of requested **.zip** file

> **Requested URL**: ```https://www.finstat.sk/api/getstatement2014file```<br />
> **Hash parameter**: *{filename}*

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| file name as given in [GetListOfStatement2014Diffs](#getlistofstatement2014diffs-request) |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatement2014file?filename=statement2014diff-2024-02-08.zip&apikey=YourAPIKey&hash=994141238a0e7a68eabc8028f1f95d4483105b5f259fb7ea82414d8a595a05b1&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

## GetStatement2014Legend request

Gets the legend [`StatementLegendResult`](#StatementLegendResult) in given language for keys of the statement files

> **Requested URL**: ```https://www.finstat.sk/api/getstatement2014legend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/lang-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatement2014legend?lang=sk&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/diff-en.md ':include')

[](../../../common/responses/dailydiff-en.md ':include')

[](../../../common/responses/statementlegendresult-en.md ':include')

[](../../../common/responses/statementlegendvalue-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML responses
[](../../../common/examples/diff-statement.md ':include')

[](../../../common/examples/diff-statement2014-legend.md ':include')