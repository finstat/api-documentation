# Denný zmenový súbor s rozšírenými údajmi o firmách
Sledovanie najdôležitejších zmien v celej databáze

## Požiadavka GetListOfDiffs
Požiadavka na získanie zoznamu [`DailyDiffList`](#DailyDiffList) všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofdiffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofdiffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```


#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka GetFile
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum.
Dopyt vráti dáta požadovaného **.zip** súboru

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getfile```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfDiffs](#požiadavka-getlistofdiffs) |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getfile?filename=diff-2024-02-08.zip&apikey=YourAPIKey&hash=314ced77d148eb8e515e733c6ed73571e146480eecb2e06c02f39c0e990fc29c&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-file.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovedí
[](../../../common/responses/diff-sk.md ':include')

[](../../../common/responses/dailydiff-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklady XML odpovedí
[](../../../common/examples/diff-daily.md ':include')