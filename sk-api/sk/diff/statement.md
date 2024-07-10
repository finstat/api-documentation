# Denný zmenový súbor na finančné výkazy
Toto API poskytuje možnosť, ako získať prístup k dátam bez nutnosti každý deň dotazovať API na 
zmeny. API vygeneruje pre každý deň, kedy nastala zmena, zmenový súbor obsahujúci posledné 
zmeny v závierkach.
API obsahuje informácie o všetkých závierkach. Firmy, u ktorých sa dlho neudiala žiadna zmena, majú 
závierky v súboroch vygenerovaných po zverejnení poslednej závierky. 
API je inkrementálny export, a tak sa niektoré závierky môžu nachádzať vo viacerých súboroch, kde 
aktuálna hodnota je vždy v exporte s najnovším dátumom.
---

## Požiadavka GetListOfStatementDiffs
Požiadavka na získanie zoznamu všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofstatementdiffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofstatementdiffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../../../common/responses/diff-sk.md ':include')

[](../../../common/responses/dailydiff-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/diff-statement.md ':include')


## Požiadavka GetStatementFile
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementfile```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfDiffs](#požiadavka-getlistofstatementdiffs) |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementfile?filename=statementdiff-2024-02-08.zip&apikey=YourAPIKey&hash=fe0198c59c4df2e7016181b809aadbce48a5006935038c4500111209b3c48686&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede

Dopyt vráti dáta požadovaného **.zip** súboru
#### Návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **404**| Požadovaný súbor neexistuje |

[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka GetStatementLegend

Požiadavka na stiahnutie legendy kľúčov súboru závierok

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatementlegend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/lang-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatementlegend?lang=sk&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Zoznam položiek `KeyValue`, ktoré obsahujú legendu v danom jazyku.
[](../../../common/responses/keyvalue-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu


#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/diff-statement-legend.md ':include')
