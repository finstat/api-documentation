# Autocomplete
Api for company name or company  identification number *IČO* serch according given text.

## Autocomplete request
Returns suggestions of companies stored on FinStat.sk according requested *query*.
Suggestions are returned as [`ApiAutoComplete`](#ApiAutoComplete) structure

> **Requested URL**: ```https://www.finstat.sk/api/autocomplete```<br />
> **Hash parameter**: {query}

### Parameters
[](../../../common/parameters/autocomplete-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/autocomplete?query=test&apikey=YourAPIKey&hash=63678854b4b02034b4127cd9188b3a514b67e054465e3b8d4dd5284c46f7c099&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
| Error Code | Description |
| ----------- | ----------- |
| **404**| requested query string is too short (minimum length is 3 characters) |

[](../../../common/http/errorcodes-en.md ':include')

# Response structure

[](../../../common/responses/autocomplete-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
Example XML response (for query `test`):

[](../../../common/examples/autocomplete.md ':include')