# API for tracking important events (Company ID)

## MonitoringProceedings request
Request for a list of proceedings [`ProceedingResult`](#ProceedingResult) for the last 10 days

> **Requested URL**: ```https://www.finstat.sk/api/monitoringproceedings```<br />
> **Hash parameter**: proceedings

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringproceedings?apikey=YourAPIKey&hash=7e78a38b3f54bb2d10fae11aa2f15cdddc97744da85046423797d5fdbc1abf65&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/monitoring-proceedings-en.md ':include')

[](../../../common/responses/address-en.md ':include')

[](../../../common/responses/fulladdress-en.md ':include')

[](../../../common/responses/personaddress-en.md ':include')

[](../../../common/responses/administratoraddress-en.md ':include')

[](../../../common/responses/issuedperson-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/monitoring-proceeding.md ':include')