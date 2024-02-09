# API na účtovné výkazy firiem
Aktuálne finančné údaje slovenských firiem

---
## Požiadavka GetStatements
Požiadavka na získanie zoznamu všetkých závierok pre dané *{IČO}*

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatements```<br />
> **Hash parameter**: {ico}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **ico**<br />*[povinný]*| IČO subjektu, ktorého závierky žiadame |

[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatements?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede

| Parameter | Popis |
| ----------- | ----------- |
| **Year**| Rok závierky |
| **DateFrom**| Dátum obdobia závierky od |
| **DateTo**| Dátum obdobia závierky do |
| **DatePublished**| Dátum zverejnenia závierky od |
| **Templates**| Zoznam šablón, do ktorých je závierku možno konvertovať `TemplateTypeEnum` <ul><li>Template2011v2</li><li>Template2014</li><li>Template2014micro</li><li>TemplateFinancial</li><li>TemplateROPO</li><li>TemplateNujPU</li></ul>|

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede

[](../../examples/statements.md ':include')

## Požiadavka GetStatementDetail
Požiadavka na detail účtovnej závierky

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementdetail```<br />
> **Hash parameter**: {ico}|{year}

| Parameter | Popis |
| ----------- | ----------- |
| **template**<br />*[povinný]*| názov šablóny ako je uvedený vo výsledku požiadavky [GetStatements](sk/special/statement?id=požiadavka-getstatements) |
| **ico**<br />*[povinný]*| IČO subjektu, ktorého závierky žiadame |
| **year**<br />*[povinný]*| Rok závierky |

[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementdetail?ico=47165367&year=2022&template=Template2011v2&apikey=YourAPIKey&hash=8725046bc5a88b4311a1dcb87511fa5935c13a9d7cd69e4cd757b66cbc351c90&StationId=YourStationID&StationName=Your+Station+Name```


### Popis odpovede

Podľa typu šablóny (template) api vráti odpoveď typu:
#### StatementResult
štandardné firmy a organizácie 

| Parameter | Popis |
| ----------- | ----------- |
| **ICO** | identifikačné číslo organizácie (IČO) |
| **Name** | meno firmy |
| **Year** | rok závierky |
| **DateFrom** | dátum obdobia závierky od |
| **DateTo** | dátum obdobia závierky do |
| **DatePublished** | dátum zverejnenia |
| **Format** | šablóna exportovanej závierky |
| **OriginalFormat** | originálna šablóna závierky |
| **Source** | zdroj závierky |
| **Assets** | zoznam hodnôt aktív závierky `AssetStatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr><tr><td>**ActualBrutto**</td><td>brutto hodnota (môže byť null)</td></tr><tr><td>**ActualCorrection**</td><td>korekcia (môže byť null)</td></tr></table> |
| **LiabilitiesAndEquity** | zoznam hodnôt pasív závierky `StatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr></table>|
| **IncomeStatement** | zoznam hodnôt ziskov a strát závierky `StatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr></table> |
| **PreviousAccountingPeriodFrom** | dátum začiatku predošlého obdobia vo výkaze |
| **PreviousAccountingPeriodTo** | dátum konca predošlého obdobia vo výkaze |

#### NonProfitStatementResult
neziskové a rozpočtové organizácie

| Parameter | Popis |
| ----------- | ----------- |
| **ICO** | identifikačné číslo organizácie (IČO) |
| **Name** | meno firmy |
| **Year** | rok závierky |
| **DateFrom** | dátum obdobia závierky od |
| **DateTo** | dátum obdobia závierky do |
| **DatePublished** | dátum zverejnenia |
| **Format** | šablóna exportovanej závierky |
| **OriginalFormat** | originálna šablóna závierky |
| **Source** | zdroj závierky |
| **Assets** | zoznam hodnôt aktív závierky `AssetStatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr><tr><td>**ActualBrutto**</td><td>brutto hodnota (môže byť null)</td></tr><tr><td>**ActualCorrection**</td><td>korekcia (môže byť null)</td></tr></table> |
| **LiabilitiesAndEquity** | zoznam hodnôt pasív závierky `StatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr></table>|
| **Expenses** | zoznam hodnôt výdavkov závierky `FinancialStatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr><tr><td>**ActualMain**</td><td>hodnota z hlavnej činnosti (môže byť null)</td></tr><tr><td>**ActualCommercial**</td><td>hodnota z obchodnej činnosti (môže byť null)</td></tr></table> |
| **Revenues** | oznam hodnôt výnosov závierky `FinancialStatementValue` <table><tr><td>**ReportRow**</td><td>číslo riadku ukazovateľa v závierke</td></tr><tr><td>**ReportSection**</td><td>sekcia ukazovateľa v závierke</td></tr><tr><td>**Actual**</td><td>aktuálna hodnota (môže byť null)</td></tr><tr><td>**Previous**</td><td>predošlá hodnota (môže byť null)</td></tr><tr><td>**ActualMain**</td><td>hodnota z hlavnej činnosti (môže byť null)</td></tr><tr><td>**ActualCommercial**</td><td>hodnota z obchodnej činnosti (môže byť null)</td></tr></table> |
| **PreviousAccountingPeriodFrom** | dátum začiatku predošlého obdobia vo výkaze |
| **PreviousAccountingPeriodTo** | dátum konca predošlého obdobia vo výkaze |

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
#### StatementResult
[](../../examples/statements-statement.md ':include')
#### NonProfitStatementResult
[](../../examples/statements-nonprofit.md ':include')

## Požiadavka GetStatementTemplateLegend
Požiadavka na stiahnutie legendy kľúčov účtovných závierok

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementtemplatelegend```<br />
> **Hash parameter**: {lang}

| Parameter | Popis |
| ----------- | ----------- |
| **template**<br />*[povinný]*| názov šablóny ako je uvedený vo výsledku požiadavky [GetStatements](sk/special/statement?id=požiadavka-getstatements) |
| **lang**<br />*[povinný]*| jazyk legendy. Možné hodnoty: <ul><li>SK</li><li>EN</li></ul> |

[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementtemplatelegend?lang=sk&template=Template2011v2&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```


### Popis odpovede
Podľa typu šablóny (template) api vráti odpoveď typu:

Odpoveď `StatementLegendResult` pozostáva z 3 sekcií:

| Parameter | Popis |
| ----------- | ----------- |
| **Assets** | zoznam hodnôt aktív závierky |
| **LiabilitiesAndEquity** | zoznam hodnôt pasív závierky |
| **IncomeStatement** | zoznam hodnôt ziskov a strát závierky |

Odpoveď `NonProfitStatementLegendResult` pozostáva z 4 sekcií:

| Parameter | Popis |
| ----------- | ----------- |
| **Assets** | zoznam hodnôt aktív závierky |
| **LiabilitiesAndEquity** | zoznam hodnôt pasív závierky |
| **Expenses** | zoznam hodnôt výdajov |
| **Revenue** | zoznam hodnôt ziskov |

Každá sekcia je zoznam položiek `StatementLegendValue`

| Parameter | Popis |
| ----------- | ----------- |
| **ReportRow** | Číslo riadku v závierke  |
| **ReportSection** | Názov sekcie v závierke |
| **Name** |  Názov ukazovateľa v danom jazyku |

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
#### StatementLegendResult
[](../../examples/statements-statement.md ':include')
#### NonProfitStatementLegendResult
[](../../examples/statements-nonprofit.md ':include')