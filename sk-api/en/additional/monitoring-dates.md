# Portfolio Sync API (Dates of birth)

[](monitoring-categories.md ':include')

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringcategories?apikey=YourAPIKey&hash=05e261e4d5a50ceecfc584ca85623595ceae8b1de2a40252ea1472f13361b564&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## AddDateToMonitoring request
Request for adding a date of birth to monitoring.
Returns `true` in successful or `false` in unsuccessful adding to the monitoring

> **Requested URL**: ```https://www.finstat.sk/api/adddatetomonitoring```<br />
> **Hash parameter**: {date}

### Parameters
[](../../../common/parameters/monitoring-addremove-date-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/adddatetomonitoring?date=9.2.2024&apikey=YourAPIKey&hash=b8c62bab2473673ae1c9a461cab2dd824d86da1d62745290dbb110140075b076&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## RemoveDateFromMonitoring request
Request for removing date of birth from monitoring.
Returns `true` in successful or `false` in unsuccessful adding to the monitoring

> **Requested URL**: ```https://www.finstat.sk/api/removedatefrommonitoring```<br />
> **Hash parameter**: {date}

### Parameters
[](../../../common/parameters/monitoring-addremove-date-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/removedatefrommonitoring?date=9.2.2024&apikey=YourAPIKey&hash=b8c62bab2473673ae1c9a461cab2dd824d86da1d62745290dbb110140075b076&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-sk.md ':include')

## MonitoringDateList request
Request for current list of dates in monitoring.

> **Requested URL**: ```https://www.finstat.sk/api/monitoringdatelist```<br />
> **Hash parameter**: datelist

### Parameters
[](../../../common/parameters/monitoring-category-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringdatelist?apikey=YourAPIKey&hash=3cb3d0526473367453ee5779e985a33194356df01551e45ebc2d2f873df79c0e&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## MonitoringDateReport request
Request for current list of monitoring  [`MonitoringDate`](#MonitoringDate) events that happened in the last 30 days

> **Requested URL**: ```https://www.finstat.sk/api/monitoringdatereport```<br />
> **Hash parameter**: datereport

### Parameters
[](../../../common/parameters/monitoring-category-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringdatereport?apikey=YourAPIKey&hash=a0c1760f69233637d6238dcac01fbb4226d69f461a4ca72bd1c8576dfd3f27d4&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures

[](../../../common/responses/monitoring-categories-en.md ':include')

[](../../../common/responses/monitoring-date-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML responses

[](../../../common/examples/monitoring-categories.md ':include')

[](../../../common/examples/monitoring-datelist.md ':include')

[](../../../common/examples/monitoring-datereport.md ':include')