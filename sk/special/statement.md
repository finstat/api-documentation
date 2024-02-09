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

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede

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
- `StatementResult` - štandardné firmy a organizácie 
- `NonProfitStatementResult` - neziskové a rozpočtové organizácie

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede

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
- `StatementResult` - štandardné firmy a organizácie 
- `NonProfitStatementResult` - neziskové a rozpočtové organizácie

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede