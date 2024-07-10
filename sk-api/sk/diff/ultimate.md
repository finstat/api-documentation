# Denný zmenový súbor s podrobnými údajmi o firmách
Sledovanie podrobností, vrátane zmien štatutárov, stavu a priebehu konkurzných konaní a iných kritických udalostí

---
## Požiadavka GetListOfUltimateDiffs
ožiadavka na získanie zoznamu všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofultimatediffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofultimatediffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../../../common/responses/diff-sk.md ':include')

[](../../../common/responses/dailydiff-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/diff-ultimate.md ':include')

## Požiadavka GetUltimateFile
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getultimatefile```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfDiffs](#požiadavka-getlistofultimatediffs) |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getultimatefile?filename=ultimatediff-2024-02-08.zip&apikey=YourAPIKey&hash=50fce1c887049c20d0861d5173170e9d4d1a1db0bf4ba4c541bb4f19e5a154c2&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede

Dopyt vráti dáta požadovaného **.zip** súboru
#### Návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **404**| Požadovaný súbor neexistuje |

[](../../../common/http/errorcodes-sk.md ':include')