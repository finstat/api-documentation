# API na účtovné výkazy firiem
Aktuálne finančné údaje slovenských firiem

---
## Požiadavka GetStatements
Požiadavka na získanie zoznamu všetkých závierok pre dané *{IČO}*

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatements```<br />
> **Hash parameter**: {ico}

### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatements?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Zoznam dostupných závierok `StatementItem`

[](../../../common/responses/statementitem-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede

[](../../../common/examples/statements.md ':include')

## Požiadavka GetStatementDetail
Požiadavka na detail účtovnej závierky

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementdetail```<br />
> **Hash parameter**: {ico}|{year}

[](../../../common/parameters/statement-detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementdetail?ico=47165367&year=2022&template=Template2011v2&apikey=YourAPIKey&hash=8725046bc5a88b4311a1dcb87511fa5935c13a9d7cd69e4cd757b66cbc351c90&StationId=YourStationID&StationName=Your+Station+Name```


### Popis odpovede

Podľa typu šablóny (template) api vráti odpoveď typu:

[](../../../common/responses/statementresult-sk.md ':include')

[](../../../common/responses/nonprofitstatementresult-sk.md ':include')

[](../../../common/responses/assetstatementvalue-sk.md ':include')

[](../../../common/responses/statementvalue-sk.md ':include')

[](../../../common/responses/financialstatementvalue-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
#### StatementResult
[](../../../common/examples/statements-statement.md ':include')
#### NonProfitStatementResult
[](../../../common/examples/statements-nonprofit.md ':include')

## Požiadavka GetStatementTemplateLegend
Požiadavka na stiahnutie legendy kľúčov účtovných závierok

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementtemplatelegend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/statement-legend-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementtemplatelegend?lang=sk&template=Template2011v2&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```


### Popis odpovede
Podľa typu šablóny (template) api vráti odpoveď typu:

[](../../../common/responses/statementlegendresult-sk.md ':include')

[](../../../common/responses/nonprofitstatementlegendresult-sk.md ':include')

[](../../../common/responses/statementlegendvalue-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
#### StatementLegendResult
[](../../../common/examples/statements-statement.md ':include')
#### NonProfitStatementLegendResult
[](../../../common/examples/statements-nonprofit.md ':include')