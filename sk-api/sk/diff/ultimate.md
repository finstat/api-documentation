# Denný zmenový súbor s podrobnými údajmi o firmách
Sledovanie podrobností, vrátane zmien štatutárov, stavu a priebehu konkurzných konaní a iných kritických udalostí

## Požiadavka GetListOfUltimateDiffs
Požiadavka na získanie zoznamu [`DailyDiffList`](#DailyDiffList) všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofultimatediffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofultimatediffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka GetUltimateFile
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum
Dopyt vráti dáta požadovaného **.zip** súboru

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getultimatefile```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfUltimateDiffs](#požiadavka-getlistofultimatediffs) |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getultimatefile?filename=ultimatediff-2024-02-08.zip&apikey=YourAPIKey&hash=50fce1c887049c20d0861d5173170e9d4d1a1db0bf4ba4c541bb4f19e5a154c2&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-file.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovedí
[](../../../common/responses/diff-sk.md ':include')

[](../../../common/responses/dailydiff-sk.md ':include')

[](../../../common/responses/extendeddiff-sk.md ':include')

[](../../../common/responses/ultimatediff-sk.md ':include')

[](../../../common/responses/extendeddiffother-sk.md ':include')

[](../../../common/responses/ultimatediffother-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklady XML odpovedí
[](../../../common/examples/diff-ultimate.md ':include')