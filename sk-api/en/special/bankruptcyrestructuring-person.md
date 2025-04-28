# Bankruptcy and restructuring API for persons

## PersonBankruptcyProceedings request
Request for a list of persons bankruptcy and restructuring proceedings [`BankruptcyRestructuring`](#BankruptcyRestructuring).
> **Requested URL**: ```https://www.finstat.sk/api/PersonBankruptcyProceedings```<br />
> **Hash parameter**: {name}|{surname}|{dateofbirth}

> **Warning**: due to the need for clarity, the hash calculation must utilize the specified format for. *{dateofbirth}* `yyyy-mm-dd`

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **name**<br />*[mandatory]*| person name |
| **surname**<br />*[mandatory]*| person surname |
| **dateofbirth**<br />*[mandatory]*| date of birth of the person. Supported formats. `"dd.mm.yyyy", "d.m.yyyy", "dd.m.yyyy", "d.mm.yyyy", "yyyy-mm-dd", "mm/dd/yyyy"` 

[](../../../common/parameters/parameters-sk.md ':include')

> **Example call:** ```https://www.finstat.sk/api/PersonBankruptcyProceedings?name=peter&surname=toth&dateofbirth=1988-08-16&apiKey=YourAPIKey&hash=b1f071914dc48db219c7865a057e4a72d1dd6a60b919eeda3ac475a9ac7a45c4&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/bankruptcyrestructuring-en.md ':include')

[](../../../common/responses/personaddress-en.md ':include')

> **Note:**  order of parameters can be different from list above

# Example XML response
[](../../../common/examples/bankruptcyrestructuring.md ':include')
