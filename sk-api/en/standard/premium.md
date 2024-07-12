# Premium API
Request to detailed company data [`DetailResult`](#DetailResult)

## Detail request
Detail of company according company id *ico*
> **Requested URL**: ```https://www.finstat.sk/api/detail```<br />
> **Hash parameter**: {ico}

### Parameters
[](../../../common/parameters/detail-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/detail?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-detail.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

# Response structures
#### DetailResult
[](../../../common/responses/basic-en.md ':include')

[](../../../common/responses/premium-common-en.md ':include')

[](../../../common/responses/premium-en.md ':include')

[](../../../common/responses/icdphadditional-en.md ':include')

[](../../../common/responses/judgementindicator-en.md ':include')

[](../../../common/responses/bankaccount-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response

[](../../../common/examples/premium.md ':include')

[](../../../common/texts/anonymized-en.md ':include')

[](../../../common/examples/detail-an.md ':include')