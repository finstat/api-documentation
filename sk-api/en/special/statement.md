# API for financial statements of companies
Current financial data of Slovak companies

## GetStatements request
Requirement to obtain a list of all financial statements for a given company id *{IČO}* [`StatementItem`](#StatementItem)

> **Requested URL**: ```https://www.finstat.sk/api/getstatements```<br />
> **Hash parameter**: {ico}

### Parameters
[](../../../common/parameters/detail-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatements?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## GetStatementDetail request
Request for detail of financial statements.
According template returns [`StatementResult`](#StatementResult) or [`NonProfitStatementResult`](#NonProfitStatementResult)

> **Requested URL**: ```https://www.finstat.sk/api/getstatementdetail```<br />
> **Hash parameter**: {ico}|{year}

[](../../../common/parameters/statement-detail-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatementdetail?ico=47165367&year=2022&template=Template2011v2&apikey=YourAPIKey&hash=8725046bc5a88b4311a1dcb87511fa5935c13a9d7cd69e4cd757b66cbc351c90&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## GetStatementTemplateLegend request
Request for statement keys legend.
According template returns [`StatementLegendResult`](#StatementLegendResult) or [`NonProfitStatementLegendResult`](#NonProfitStatementLegendResult)

> **Requested URL**: ```https://www.finstat.sk/api/getstatementtemplatelegend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/statement-legend-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getstatementtemplatelegend?lang=sk&template=Template2011v2&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/statementitem-en.md ':include')

[](../../../common/responses/statementresult-en.md ':include')

[](../../../common/responses/nonprofitstatementresult-en.md ':include')

[](../../../common/responses/assetstatementvalue-en.md ':include')

[](../../../common/responses/statementvalue-en.md ':include')

[](../../../common/responses/financialstatementvalue-en.md ':include')

[](../../../common/responses/statementlegendresult-en.md ':include')

[](../../../common/responses/nonprofitstatementlegendresult-en.md ':include')

[](../../../common/responses/statementlegendvalue-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/statements.md ':include')

#### StatementResult
[](../../../common/examples/statements-statement.md ':include')

#### NonProfitStatementResult
[](../../../common/examples/statements-nonprofit.md ':include')

#### StatementLegendResult
[](../../../common/examples/statements-statement.md ':include')

#### NonProfitStatementLegendResult
[](../../../common/examples/statements-nonprofit.md ':include')