# Portfolio Sync API (Company ID)

[](monitoring-categories.md ':include')

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringcategories?apikey=YourAPIKey&hash=05e261e4d5a50ceecfc584ca85623595ceae8b1de2a40252ea1472f13361b564&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## AddToMonitoring request
Request for adding a company ID *IČO* to monitoring.
Returns `true` in successful or `false` in unsuccessful adding to the monitoring

> **Requested URL**: ```https://www.finstat.sk/api/addtomonitoring```<br />
> **Hash parameter**: {ico}

### Parameters
[](../../../common/parameters/monitoring-addremove-ico-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/addtomonitoring?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-sk.md ':include')

## RemoveFromMonitoring request
Request for removing company ID *IČO* from monitoring.
Returns `true` in successful or `false` in unsuccessful removing from the monitoring

> **Requested URL**: ```https://www.finstat.sk/api/removefrommonitoring```<br />
> **Hash parameter**: {ico}

### Parameters
[](../../../common/parameters/monitoring-addremove-ico-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/removefrommonitoring?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## MonitoringList request
Request for current list of companies in monitoring

> **Requested URL**: ```https://www.finstat.sk/api/monitoringlist```<br />
> **Hash parameter**: list

### Parameters
[](../../../common/parameters/monitoring-category-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringlist?apikey=YourAPIKey&hash=da32661cb223d07c2e1bbc8390ab559503e7d937a21e9107445f82f02b73ad42&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## MonitoringReport request
Request for current list of monitoring events [`Monitoring`](#Monitoring) that happened in the last 30 days

> **Requested URL**: ```https://www.finstat.sk/api/monitoringreport```<br />
> **Hash parameter**: report

### Parameters
[](../../../common/parameters/monitoring-category-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringreport?apikey=YourAPIKey&hash=816fa3eb97d4acec7ab73f7264a79f5cbe7280f3b0f81dd7b93b8e2981933e0c&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures

[](../../../common/responses/monitoring-categories-en.md ':include')

[](../../../common/responses/monitoring-ico-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML responses

[](../../../common/examples/monitoring-categories.md ':include')

[](../../../common/examples/monitoring-list.md ':include')

[](../../../common/examples/monitoring-report.md ':include')