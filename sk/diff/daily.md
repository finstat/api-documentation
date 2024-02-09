# Denný zmenový súbor s rozšírenými údajmi o firmách
Sledovanie najdôležitejších zmien v celej databáze

---
## Požiadavka GetListOfDiffs
Požiadavka na získanie zoznamu všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofdiffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../parts/parameters.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofdiffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../parts/diff-daily.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/diff-daily.md ':include')

## Požiadavka GetFile
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getfile```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfDiffs](sk/diff/daily?id=požiadavka-getlistofdiffs) |

[](../parts/parameters.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

> **Príklad volania:** ```https://www.finstat.sk/api/getfile?filename=diff-2024-02-08.zip&apikey=YourAPIKey&hash=314ced77d148eb8e515e733c6ed73571e146480eecb2e06c02f39c0e990fc29c&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede

Dopyt vráti dáta požadovaného **.zip** súboru
#### Návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **404**| Požadovaný súbor neexistuje |

[](../parts/httperrorcodes.md ':include')