# Bankruptcy and restructuring API for companies

## CompanyBankruptcyRestructuring request
Request for a list of company bankruptcy and restructuring proceedings [`BankruptcyRestructuring`](#BankruptcyRestructuring).
> **Dopytovaná URL**: ```https://www.finstat.sk/api/CompanyBankruptcyRestructuring```<br />
> **Hash parameter**: {ico} or {name} 

>**Warning**: only one of the parameters should be sent, not both.

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **ico**<br />*[mandatory]*|  TIN of company if *name* is not  filled in  |
| **name**<br />*[mandatory]*| name of company if *ICO* is not  filled in   |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/CompanyBankruptcyRestructuring?ico=36381250&apiKey=YourAPIKey&hash=3fa36ce129f7757f57a8104ef045f9bfaff7d1868c3609238948851dfe9b6497&StationId=YourStationID&StationName=Your+Station+Name```

> **Example call:** ```https://www.finstat.sk/api/CompanyBankruptcyRestructuring?name=talise&apiKey=YourAPIKey&hash=103915d0f482a6d1ea95848c52b2435f752cd8e4c8eed7cb9adadb9790136384&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/bankruptcyrestructuring-en.md ':include')

[](../../../common/responses/address-en.md ':include')

[](../../../common/responses/fulladdress-en.md ':include')

[](../../../common/responses/personaddress-en.md ':include')

> **Note:**  order of parameters can be different from list above

# Example XML response
[](../../../common/examples/bankruptcyrestructuring.md ':include')
