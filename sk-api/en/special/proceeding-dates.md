# API for tracking important events (Dates of birth)

## MonitoringDateProceedings request
Request for a list of proceedings [`ProceedingResult`](#ProceedingResult) for the last 10 days

> **Requested URL**: ```https://www.finstat.sk/api/monitoringdateproceedings```<br />
> **Hash parameter**: dateproceedings

### Parameters
[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/monitoringdateproceedings?apikey=YourAPIKey&hash=7b0b6f41052ed12cb0438c75d335ac7e578ec8cb6a9ed428301e6d95f4896e94&StationId=YourStationID&StationName=Your+Station+Name```

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
