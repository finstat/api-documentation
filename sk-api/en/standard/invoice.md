# Invoice API
Request to simple company data [`BasicResult`](#BasicResult)[`BasicResult`](#BasicResult)

## Basic request
Detail of company according company id *ico*
> **Requested URL**: ```https://www.finstat.sk/api/basic```<br />
> **Hash parameter**: {ico}

### Parameters
[](../../../common/parameters/detail-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/basic?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-detail.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

# Response structures
#### BasicResult
[](../../../common/responses/basic-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/invoice.md ':include')

[](../../../common/texts/anonymized-en.md ':include')

[](../../../common/examples/detail-an.md ':include')
